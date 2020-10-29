---
title: Azure-kontexter och autentiseringsuppgifter
description: Lär dig hur du återanvänder Azure-autentiseringsuppgifter och annan information över flera PowerShell-sessioner.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b6ac8b821f2d88431be67fd5fe1d50fc640d2b8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754045"
---
# <a name="azure-powershell-context-objects"></a>Azure PowerShell-kontextobjekt

Azure PowerShell använder _Azure PowerShell-kontextobjekt_ (Azure-kontexter) för att lagra information om prenumeration och autentisering. Om du har mer än en prenumeration kan du använda Azure-kontexter för att välja den prenumeration som du vill köra Azure PowerShell-cmdletar på. Azure-kontexter används också för att lagra inloggningsinformation över flera PowerShell-sessioner och köra bakgrundsaktiviteter.

Den här artikeln beskriver hur du hanterar Azure-kontexter, inte hantering av prenumerationer eller konton. Om du vill hantera användare, prenumerationer, klientorganisationer eller annan kontoinformation, se [Azure Active Directory](/azure/active-directory)-dokumentationen. När du har fått grepp om Azure-kontexter finns det information om hur du använder kontexter för att köra bakgrundsaktiviteter eller parallella uppgifter finns i [Använda Azure PowerShell-cmdletar i PowerShell-jobb](using-psjobs.md).

## <a name="overview-of-azure-context-objects"></a>Översikt över Azure-kontextobjekt

Azure-kontexter är PowerShell-objekt som representerar din aktiva prenumeration för att köra kommandon och den autentiseringsinformation som krävs för att ansluta till ett Azure-moln. Med Azure-kontexter behöver Azure PowerShell inte autentisera ditt konto varje gången du byter prenumerationer. En Azure-kontext består av följande:

* Det _konto_ som användes för att logga in på Azure med [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Azure-kontexter behandlar användare, program-ID:n och tjänsters huvudnamn från ett kontoperspektiv.
* Den aktiva _prenumerationen_ , ett serviceavtal med Microsoft om att skapa och köra Azure-resurser som är kopplade till en _klientorganisation_ . Klientorganisationer kallas ofta _organisationer_ i dokumentationen eller när du arbetar med Active Directory.
* En referens till en _tokencache_ , en lagrad autentiseringstoken för åtkomst till ett Azure-moln. Var denna token lagras och hur länge bestäms av [inställningen för att spara kontext automatiskt](#save-azure-contexts-across-powershell-sessions).

Mer information om de här villkoren finns i [Azure Active Directory-terminologi](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Autentiseringstokens som används av Azure-kontexter är samma som andra lagrade tokens som ingår i en beständig session. 

När du loggar in med `Connect-AzAccount` skapas minst en Azure-kontext för din standardprenumeration. Objektet som returneras av `Connect-AzAccount` är standardkontexten som används för resten av PowerShell-sessionen.

## <a name="get-azure-contexts"></a>Hämta Azure-kontexter

Tillgängliga Azure-kontexter hämtas med cmdleten [get-AzContext](/powershell/module/az.accounts/get-azcontext). Lista alla tillgängliga kontexter med `-ListAvailable`:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Eller hämta en kontext efter namn:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

Kontextnamn får vara ett annat än namnet på den associerade prenumerationen.

> [!IMPORTANT]
> De tillgängliga Azure-kontexterna __är inte__ alltid dina tillgängliga prenumerationer. Azure-kontexter representerar endast lokalt lagrad information. Du kan hämta dina prenumerationer med cmdleten [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription?view=azps-1.8.0).

## <a name="create-a-new-azure-context-from-subscription-information"></a>Skapa en ny Azure-kontext från prenumerationsinformation

Cmdleten [set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) används både för att skapa nya Azure-kontexter och ange dem som aktiv kontext.
Det enklaste sättet att skapa en ny Azure-kontext är att använda befintlig prenumerationsinformation. Cmdleten är utformad för att ta utdataobjektet från `Get-AzSubscription` som ett pipelinevärde och konfigurera en ny Azure-kontext:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

Eller ange prenumerationsnamnet eller -ID och klientorganisations-ID om det behövs:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Om argumentet `-Name` utelämnas används prenumerationens namn och ID som kontextnamn i formatet `Subscription Name (subscription-id)`.

## <a name="change-the-active-azure-context"></a>Ändra den aktiva Azure-kontexten

Både `Set-AzContext` och [Select-AzContext](/powershell/module/az.accounts/set-azcontext) kan användas för att ändra den aktiva Azure-kontexten. Som vi beskriver i [Skapa en ny Azure-kontext](#create-a-new-azure-context-from-subscription-information) skapar `Set-AzContext` en ny Azure-kontext för en prenumeration om den inte finns, och växlar sedan till att använda den kontexten som den aktiva.

`Select-AzContext` är avsedd att användas med befintliga Azure-kontexter och fungerar på liknande sätt som med `Set-AzContext -Context`, men är utformad för användning med pipeline:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Precis som många andra konto- och kontexthanteringskommandon i Azure PowerShell, har `Set-AzContext` och `Select-AzContext` stöd för argumentet `-Scope` så att du kan styra hur länge kontexten är aktiv. `-Scope` gör att du kan ändra en enskild sessions aktiva kontext utan att ändra standardvärdet:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

För att undvika att växla kontext för en hel PowerShell-session kan alla Azure PowerShell-kommandon köras mot en specifik kontext med argumentet `-AzContext`:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

Den andra huvudsakliga användningen av kontexter med Azure PowerShell-cmdletar är att köra bakgrundskommandon. Mer information om hur du kör PowerShell-jobb med Azure PowerShell finns i [Köra Azure PowerShell-cmdletar i PowerShell-jobb](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Spara Azure-kontexter mellan PowerShell-sessioner

Som standard sparas Azure-kontexter för användning mellan PowerShell-sessioner. Du kan ändra det här beteendet på följande sätt:

* Logga in med `-Scope Process` och `Connect-AzAccount`.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Azure-kontexten som returneras som en del av den här inloggningen är _endast_ giltig för den aktuella sessionen bara och sparas inte automatiskt, oavsett Azure PowerShell-inställningen för att spara kontext automatiskt.
* Inaktivera Azure Powershell-inställningen spara kontext automatiskt med cmdleten [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).
  Att du inaktivera inställningen spara kontext automatiskt rensar __inte__ alla lagrade tokens. Information om hur du rensar lagrad information om Azure-kontext finns i [Ta bort Azure-kontexter och autentiseringsuppgifter](#remove-azure-contexts-and-stored-credentials).
* Aktivera explicit inställningen spara Azure-kontext automatiskt kan aktiveras med cmdleten [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave). När spara automatiskt är aktiverat lagras alla användares kontexter lokalt för senare PowerShell-sessioner.
* Spara kontexter manuellt med [Save-AzContext](/powershell/module/az.accounts/save-azcontext) som ska användas i framtida PowerShell-sessioner, där de kan läsas in med [import-AzContext](/powershell/module/az.accounts/import-azcontext):

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> Om du inaktiverar spara kontext automatiskt rensas __inte__ eventuell lagrad kontextinformation som sparats. Om du vill ta bort lagrad information använder du cmdleten [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Mer information om hur du tar bort sparade kontexter finns i [Ta bort kontexter och autentiseringsuppgifter](#remove-azure-contexts-and-stored-credentials).

Vart och ett av dessa kommandon har stöd för parametern `-Scope`, som kan ta ett värde om `Process` för att endast appliceras på den processen som körs för närvarande. Om du till exempel vill se till att nyligen skapade kontexter inte sparas när du har avslutat en PowerShell-session:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Kontextinformation och tokens lagras i `$env:USERPROFILE\.Azure`-katalogen i Windows och på `$HOME/.Azure` på andra plattformar. Känslig information, till exempel prenumerations-ID och klientorganisations-ID kan fortfarande visas i lagrad information, via loggar eller sparade kontexter. Information om hur du rensar lagrad information finns i avsnittet [Ta bort kontexter och autentiseringsuppgifter](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Ta bort Azure-kontexter och lagrade autentiseringsuppgifter

Så här rensar du Azure-kontexter och autentiseringsuppgifter:

* Logga ut från ett konto med [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).
  Du kan logga ut från ett konto antingen via konto eller kontext:

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account 
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  Vid frånkoppling tas alltid lagrade autentiseringstokens bort och alla sparade kontexter som är kopplade till den frånkopplade användaren eller kontexten tas bort.
* Använd [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Den här cmdleten garanterar att lagrade kontexter och autentiseringstoken tas bort. Dessutom blir du utloggad.
* Ta bort en kontext med [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):
  
  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  Om du tar bort den aktiva kontexten kopplas du bort från Azure och måste autentiseras igen med `Connect-AzAccount`.

## <a name="see-also"></a>Se även

* [Köra Azure PowerShell-cmdletar i PowerShell-jobb](using-psjobs.md)
* [Azure Active Directory-terminologi](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Referens för Az.Accounts](/powershell/module/az.accounts)
