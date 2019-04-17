---
title: Bevara autentiseringsuppgifter för användare mellan PowerShell-sessioner
description: Lär dig hur du återanvänder Azure-autentiseringsuppgifter och annan information över flera PowerShell-sessioner.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363840"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>Bevara autentiseringsuppgifter för användare mellan PowerShell-sessioner

Azure PowerShell erbjuder en funktion som kallas **Azure Context Autosave**, som ger följande funktioner:

- Bevara inloggningsinformation för återanvändning i nya PowerShell-sessioner.
- Enklare användning av bakgrundsaktiviteter för att köra tidskrävande cmdletar.
- Växla mellan konton, prenumerationer och miljöer utan separat inloggning.
- Köra uppgifter med olika autentiseringsuppgifter och prenumerationer, samtidigt från samma PowerShell-session.

## <a name="azure-contexts-defined"></a>Definitioner av Azure-kontexter

En *Azure-kontext* är en informationsuppsättning som definierar målet för Azure PowerShell-cmdletar. Kontexten består av fem delar:

- Ett *konto* – användarnamnet eller tjänstens huvudnamn som används för att autentisera kommunikationen med Azure
- En *prenumeration* – Azure-prenumerationen med de resurser där åtgärder vidtas.
- En *klientorganisation* – Azure Active Directory-klienten som innehåller din prenumeration. Klienter är viktigare för ServicePrincipal-autentisering.
- En *miljö* – det specifika Azure-moln som är målet, vanligtvis det globala Azure-molnet.
  Med miljöinställningen kan du även ange nationella, offentliga och lokala moln (Azure Stack) som mål.
- *Autentiseringsuppgifter* – den information som används av Azure för att verifiera din identitet och bekräfta din behörighet att komma åt resurser i Azure

Med den senaste versionen av Azure PowerShell kan Azure-kontexter sparas automatiskt när du öppnar en ny PowerShell-session.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>Spara automatiskt kontexten för nästa inloggning

Azure PowerShell behåller automatiskt din kontextinformation från session till session. Om du vill ange att PowerShell ska glömma kontexten och autentiseringsuppgifterna ska du använda `Disable-AzContextAutoSave`. Om kontextsparande har inaktiverats måste du logga in på Azure varje gång du öppnar en PowerShell-session.

Om du vill tillåta Azure PowerShell att komma ihåg kontexten när PowerShell-sessionen avslutas ska du använda `Enable-AzContextAutosave`. Information om kontext och autentiseringsuppgifter sparas automatiskt i en särskild dold mapp i användarkatalogen (`$env:USERPROFILE\.Azure` i Windows och `$HOME/.Azure` på andra plattformar). I varje ny PowerShell-session används kontexten i den senaste sessionen som mål.

Med de cmdletar du kan använda för att hantera Azure-kontexter kan du också göra mer detaljerade inställningar. Om du vill att ändringarna ska tillämpas endast på den aktuella PowerShell-sessionen (omfånget `Process`) eller alla PowerShell-sessioner (omfånget `CurrentUser`). Dessa alternativ beskrivs mer detaljerat i [Använda kontextomfång](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Köra Azure PowerShell-cmdletar som bakgrundsjobb

Med funktionen **Azure Context Autosave** kan du också dela din kontext med PowerShell-bakgrundsjobb. I PowerShell kan du starta och övervaka tidskrävande uppgifter som bakgrundsjobb utan att behöva vänta tills uppgifterna har slutförts. Du kan dela autentiseringsuppgifter med bakgrundsjobb på två olika sätt:

- Skicka kontexten som ett argument

  Med de flesta AzureRM-cmdletar kan du skicka kontexten som en parameter till cmdleten. Du kan skicka en kontext till ett bakgrundsjobb enligt följande exempel:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- Med hjälp av standardkontexten med spara automatiskt aktiverat

  Om du har aktiverat **Context Autosave** (Spara automatiskt kontext) använder bakgrundsjobben automatiskt den sparade standardkontexten.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

När du behöver veta resultatet av en bakgrundsaktivitet kan du använda `Get-Job` för att kontrollera jobbstatus och `Wait-Job` för att vänta tills jobbet är slutfört. Använd `Receive-Job` för att registrera eller visa resultatet av bakgrundsjobbet. Mer information finns i artikeln [om jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Skapa, välja, byta namn på och ta bort kontexter

Om du vill skapa en kontext måste du vara inloggad i Azure. Med cmdleten `Connect-AzAccount` (eller dess alias `Login-AzAccount`) anger du standardkontexten som används av Azure PowerShell-cmdletar och kan komma åt alla klienter eller prenumerationer som tillåts med dina autentiseringsuppgifter.

Om du vill lägga till en ny kontext efter inloggningen använder du `Set-AzContext` (eller dess alias `Select-AzSubscription`).

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

I exemplet ovan läggs en ny kontext till med målet ”Contoso Subscription 1” med hjälp av dina aktuella autentiseringsuppgifter. Den nya kontexten har namnet ”Contoso1”. Om du inte anger ett namn för kontexten används ett standardnamn med konto-ID och prenumerations-ID.

Byt namn på en befintlig kontext genom att använda cmdlet `Rename-AzContext`. Exempel:

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Det här exemplet byter namn på kontexten med det automatiska namnet `[user1@contoso.org; 123456-7890-1234-564321]` till ”Contoso2”. Cmdletar som hanterar kontexter använder också tabbifyllning, så att du snabbt kan välja kontexten.

Slutligen, för att ta bort en kontext använder du cmdlet `Remove-AzContext`.  Exempel:

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

Glömmer kontexten med namnet ”Contoso2”. Du kan återskapa den här kontexten med hjälp av
`Set-AzContext`

## <a name="removing-credentials"></a>Ta bort autentiseringsuppgifter

Du kan ta bort alla autentiseringsuppgifter och associerade kontexter för en användare eller en tjänsts huvudnamn med hjälp av `Disconnect-AzAccount` (kallas även `Logout-AzAccount`). När den körs utan parametrar tar cmdleten `Disconnect-AzAccount` bort alla autentiseringsuppgifter och kontexter som är associerade med användaren eller tjänstens huvudnamn i den aktuella kontexten. Du kan skicka användarnamn, tjänstens huvudnamn eller kontext med ett visst huvudkonto som mål.

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Använda kontextomfång

Ibland kan vilja du markera, ändra eller ta bort en kontext i en PowerShell-session utan att påverka andra sessioner. Om du vill ändra standardbeteendet för kontext-cmdletar ska du använda parametern `Scope`. Omfånget `Process` åsidosätter standardbeteendet genom att tillämpa det endast i den aktuella sessionen. Däremot ändrar omfånget `CurrentUser` kontexten i alla sessioner, inte bara i den aktuella sessionen.

Om du till exempel vill ändra standardkontexten i den aktuella PowerShell-sessionen utan att påverka andra fönster eller den kontext som används nästa gång en session öppnas, ska du använda:

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Hur inställningen spara automatiskt kontext bevaras

Inställningen för att spara kontext automatiskt sparas i användarens Azure PowerShell-katalog (`$env:USERPROFILE\.Azure` i Windows och `$HOME/.Azure` på andra plattformar). Vissa typer av datorkonton kanske inte har åtkomst till den här katalogen. I sådana scenarier kan du använda miljövariabeln

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

När värdet är true sparas kontexten automatiskt. Om värdet är false sparas inte kontexten.

## <a name="context-management-cmdlets"></a>Cmdletar för kontexthantering

- [Enable-AzContextAutosave][enable] – Tillåt att kontexten sparas mellan PowerShell-sessioner.
  Eventuella ändringar ändrar den globala kontexten.
- [Disable-AzContextAutosave][disable] – Inaktivera automatiskt sparande av kontexten. Inloggning krävs för varje ny PowerShell-session.
- [Select-AzContext][select] – Välj en kontext som standard. Alla cmdletar använder autentiseringsuppgifterna i den här kontexten för autentisering.
- [Disconnect-AzAccount][remove-cred] – Ta bort alla autentiseringsuppgifter och kontexter som är kopplade till ett konto.
- [Remove-AzContext][remove-context] – Ta bort en namngiven kontext.
- [Rename-AzContext][rename] – Byt namn på en befintlig kontext.
- [Add-AzAccount][login] – Gör det möjligt att ange omfång för inloggningen till processen eller till den aktuella användaren.
  Gör det möjligt att ge standardkontexten ett namn efter autentisering.
- [Import-AzContext][import] – Gör det möjligt att ange omfång för inloggningen till processen eller till den aktuella användaren.
- [Set-AzContext][set-context] – Gör det möjligt att välja befintliga, namngivna kontexter och ändra omfång till processen eller till den aktuella användaren.

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
