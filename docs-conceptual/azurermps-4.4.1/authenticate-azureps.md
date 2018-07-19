---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med en hanterad tjänstidentitet.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 6525e41be54c3f6b97812504c436e0ff3f5edf8e
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100094"
---
# <a name="sign-in-with-azure-powershell"></a>Logga in med Azure PowerShell

Azure PowerShell har stöd för flera autentiseringsmetoder. Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.

## <a name="sign-in-interactively"></a>Logga in interaktivt

Använd cmdleten [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) för att logga in interaktivt.

```azurepowershell
Connect-AzureRmAccount
```

Den här cmdleten visar en dialogruta där du anger den e-postadress och det lösenord som är associerade med ditt Azure-konto. När du autentiserar sparas informationen för den aktuella PowerShell-sessionen, dialogrutan stängs och du får åtkomst till alla Azure PowerShell-cmdletar.

> [!IMPORTANT]
> Från och med Azure PowerShell 6.3.0 delas dina autentiseringsuppgifter mellan flera PowerShell-sessioner så länge du förblir inloggad i Windows. Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Tjänstens huvudnamn ger dig ett sätt att skapa icke-interaktiva konton som du sedan kan använda för att manipulera resurser. Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory. Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem den lägsta behörigheten som krävs för ett huvudnamn för tjänsten.

Läs informationen i [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) om du behöver skapa ett huvudnamn för tjänsten som ska användas med Azure PowerShell.

Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzureRmAccount` för att logga in med ett huvudnamn för tjänsten. Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn. Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn. Den här cmdleten visar en dialogruta där du anger användar-ID för tjänstens huvudnamn och lösenord.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Logga in med en hanterad tjänstidentitet för en virtuell Azure-dator

Hanterad tjänstidentitet är en funktion i förhandsversionen av Azure Active Directory. Du kan använda en hanterad tjänstidentitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser. Hanterad tjänstidentitet är endast tillgänglig på virtuella datorer som körs i ett Azure-moln.

Läs mer om [hur du använder en hanterad tjänstidentitet för Azure VM för att logga in och få en token](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="sign-in-to-another-cloud"></a>Logga in på ett annat moln

Azure-molntjänster erbjuder olika miljöer som följer olika regioners regler för datahantering. Om ditt Azure-konto finns i ett moln som är associerat med en av de här regionerna behöver du specificera miljön när du loggar in. Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:

```azurepowershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Använd följande kommando för att få en lista över tillgängliga miljöer:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure

Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).

Azure PowerShell-cmdletar för rollhantering:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
