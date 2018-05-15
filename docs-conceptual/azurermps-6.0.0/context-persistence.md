---
title: Bevara användarinloggningar mellan PowerShell-sessioner
description: Den här artikeln beskriver nya funktioner i Azure PowerShell som gör att du kan återanvända autentiseringsuppgifter och annan användarinformation mellan flera olika PowerShell-sessioner.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: 15e1c9ca770c9fcd72513c4f53f7726edd9c2469
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a>Bevara användarinloggningar mellan PowerShell-sessioner

I versionen från september 2017 av Azure PowerShell introducerar Azure Resource Manager-cmdletar en ny funktion, **Azure Context Autosave**. Den här funktionen möjliggör flera nya användarscenarier, inklusive:

- Bevara inloggningsinformation för återanvändning nya PowerShell-sessioner.
- Enklare användning av bakgrundsaktiviteter för att köra tidskrävande cmdletar.
- Växla mellan konton, prenumerationer och miljöer utan separat inloggning.
- Köra uppgifter med olika autentiseringsuppgifter och prenumerationer, samtidigt från samma PowerShell-session.

## <a name="azure-contexts-defined"></a>Definitioner av Azure-kontexter

En *Azure-kontext* är en informationsuppsättning som definierar målet för Azure PowerShell-cmdletar. Kontexten består av fem delar:

- Ett *konto* – användarnamnet eller tjänstens huvudnamn som används för att autentisera kommunikationen med Azure
- En *prenumeration* – den Azure-prenumeration som innehåller de resurser där åtgärder vidtas.
- En *klientorganisation* – Azure Active Directory-klienten som innehåller din prenumeration. Klienter är viktigare för ServicePrincipal-autentisering.
- En *miljö* – det specifika Azure-moln som är målet, vanligtvis det globala Azure-molnet.
  Med miljöinställningen kan du även ange nationella, offentliga och lokala moln (Azure Stack) som mål.
- *Autentiseringsuppgifter* – den information som används av Azure för att verifiera din identitet och kontrollera din behörighet att komma åt resurser i Azure

I tidigare versioner måste Azure-kontexten skapas varje gång du öppnade en ny PowerShell-session. Från och med Azure PowerShell v4.4.0 kan du aktivera funktionen att spara automatiskt och återanvända Azure-kontexter varje gång du öppnar en ny PowerShell-session.

## <a name="automatically-saving-the-context-for-the-next-login"></a>Spara automatiskt kontexten för nästa inloggning

Som standard tar Azure PowerShell bort din kontextinformation när du stänger PowerShell-sessionen.

Om du vill tillåta Azure PowerShell att komma ihåg kontexten när PowerShell-sessionen avslutas ska du använda `Enable-AzureRmContextAutosave`. Information om kontext och autentiseringsuppgifter sparas automatiskt i en särskild dold mapp i användarkatalogen (`%AppData%\Roaming\Windows Azure PowerShell`).
I varje ny PowerShell-session därefter används kontexten i den senaste sessionen som mål.

Om du vill ange att PowerShell ska glömma kontexten och autentiseringsuppgifterna ska du använda `Disable-AzureRmContextAutoSave`. Du måste logga in på Azure varje gång du öppnar en PowerShell-session.

Med de cmdletar du kan använda för att hantera Azure-kontexter kan du också göra mer detaljerade inställningar. Om du vill att ändringarna ska tillämpas endast på den aktuella PowerShell-sessionen (omfånget `Process`) eller alla PowerShell-sessioner (omfånget `CurrentUser`). Dessa alternativ beskrivs mer detaljerat i [Använda kontextomfång](#Using-Context-Scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Köra Azure PowerShell-cmdletar som bakgrundsjobb

Med funktionen **Azure Context Autosave** kan du också dela din kontext med PowerShell-bakgrundsjobb. I PowerShell kan du starta och övervaka tidskrävande uppgifter som bakgrundsjobb utan att behöva vänta tills uppgifterna har slutförts. Du kan dela autentiseringsuppgifter med bakgrundsjobb på två olika sätt:

- Skicka kontexten som ett argument

  Med de flesta AzureRM-cmdletar kan du skicka kontexten som en parameter till cmdleten. Du kan skicka en kontext till ett bakgrundsjobb enligt följande exempel:

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- Med hjälp av standardkontexten med spara automatiskt aktiverat

  Om du har aktiverat **Context Autosave** (Spara automatiskt kontext) använder bakgrundsjobben automatiskt den sparade standardkontexten.

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

När du behöver veta resultatet av en bakgrundsaktivitet kan du använda `Get-Job` för att kontrollera jobbstatus och `Wait-Job` för att vänta tills jobbet är slutfört. Använd `Receive-Job` för att registrera eller visa resultatet av bakgrundsjobbet. Mer information finns i artikeln [om jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Skapa, välja, byta namn på och ta bort kontexter

Om du vill skapa en kontext måste du vara inloggad i Azure. Med cmdleten `Connect-AzureRmAccount` (eller dess alias `Login-AzureRmAccount`) anger du standardkontexten som används av efterföljande Azure PowerShell-cmdletar och kan komma åt alla klienter eller prenumerationer som tillåts med dina inloggningsuppgifter.

Om du vill lägga till en ny kontext efter inloggningen ska du använda `Set-AzureRmContext` (eller dess alias `Select-AzureRmSubscription`).

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

I exemplet ovan läggs en ny kontext till med målet ”Contoso Subscription 1” med hjälp av dina aktuella autentiseringsuppgifter. Den nya kontexten har namnet ”Contoso1”. Om du inte anger ett namn för kontexten används ett standardnamn med konto-ID och prenumerations-ID.

Byt namn på en befintlig kontext genom att använda cmdlet `Rename-AzureRmContext`. Till exempel:

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

Det här exemplet byter namn på kontexten med det automatiska namnet `[user1@contoso.org; 123456-7890-1234-564321]` till ”Contoso2”. Cmdletar som hanterar kontexter använder också tabbifyllning, så att du snabbt kan välja kontexten.

Slutligen, för att ta bort en kontext använder du cmdlet `Remove-AzureRmContext`.  Till exempel:

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

Glömmer kontexten med namnet ”Contoso2”. Du kan återskapa den här kontexten senare med hjälp av `Set-AzureRmContext`

## <a name="removing-credentials"></a>Ta bort autentiseringsuppgifter

Du kan ta bort alla autentiseringsuppgifter och associerade kontexter för en användare eller en tjänsts huvudnamn med hjälp av `Disconnect-AzureRmAccount` (kallas även `Logout-AzureRmAccount`). När den körs utan parametrar tar cmdleten `Disconnect-AzureRmAccount` bort alla autentiseringsuppgifter och kontexter som är associerade med användaren eller tjänstens huvudnamn i den aktuella kontexten. Du kan skicka användarnamn, tjänstens huvudnamn eller kontext med ett visst huvudkonto som mål.

```powershell
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Använda kontextomfång

Ibland kan vilja du markera, ändra eller ta bort en kontext i en PowerShell-session utan att påverka andra sessioner. Om du vill ändra standardbeteendet för kontext-cmdletar ska du använda parametern `Scope`. Omfånget `Process` åsidosätter standardbeteendet genom att tillämpa det endast i den aktuella sessionen. Däremot ändrar omfånget `CurrentUser` kontexten i alla sessioner, inte bara i den aktuella sessionen.

Om du till exempel vill ändra standardkontexten i den aktuella PowerShell-sessionen utan att påverka andra fönster eller den kontext som används nästa gång en session öppnas, ska du använda:

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Hur inställningen spara automatiskt kontext bevaras

Inställningen för att spara kontext automatiskt sparas i användarens Azure PowerShell-katalog (`%AppData%\Roaming\Windows Azure PowerShell`). Vissa typer av datorkonton kanske inte har åtkomst till den här katalogen. I sådana scenarier kan du använda miljövariabeln

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

Om värdet är true sparas kontexten automatiskt. Om värdet är false sparas inte kontexten.

## <a name="changes-to-the-azurermprofile-module"></a>Ändringar i modulen AzureRM.Profile

Nya cmdletar för att hantera kontext

- [Enable-AzureRmContextAutosave][enable] – Tillåt att kontexten sparas mellan PowerShell-sessioner.
  Eventuella ändringar ändrar den globala kontexten.
- [Disable-AzureRmContextAutosave][disable] – Inaktivera automatiskt sparande av kontexten. Inloggning krävs för varje ny PowerShell-session.
- [Select-AzureRmContext][select] – Välj en kontext som standard. Alla efterföljande cmdletar använder autentiseringsuppgifterna i den här kontexten för autentisering.
- [Disconnect-AzureRmAccount][remove-cred] – Ta bort alla autentiseringsuppgifter och kontexter som är kopplade till ett konto.
- [Remove-AzureRmContext][remove-context] – Ta bort en namngiven kontext.
- [Rename-AzureRmContext][rename] – Byt namn på en befintlig kontext.

Ändringar av befintliga profil-cmdletar

- [Add-AzureRmAccount][login] – Gör det möjligt att ange omfång för inloggningen till processen eller till den aktuella användaren.
  Gör det möjligt att ge standardkontexten ett namn efter inloggning.
- [Import-AzureRmContext][import] – Gör det möjligt att ange omfång för inloggningen till processen eller till den aktuella användaren.
- [Set-AzureRmContext][set-context] – Gör det möjligt att välja befintliga, namngivna kontexter och ändra omfång till processen eller till den aktuella användaren.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
