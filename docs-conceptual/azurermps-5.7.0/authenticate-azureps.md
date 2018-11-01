---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 530eafcd0d14dbfd790a22d80c5922f304f4e0b2
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/01/2018
ms.locfileid: "50737568"
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
> Den här inloggningen är _endast_ för den aktuella PowerShell-sessionen. Om du vill bevara autentisering över flera sessioner kan du läsa artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Tjänstens huvudnamn ger dig ett sätt att skapa icke-interaktiva konton som du sedan kan använda för att manipulera resurser. Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory. Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem den lägsta behörigheten som krävs för ett huvudnamn för tjänsten.

Läs informationen i [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) om du behöver skapa ett huvudnamn för tjänsten som ska användas med Azure PowerShell.

Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzureRmAccount` för att logga in med ett huvudnamn för tjänsten. Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn. Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn. Den här cmdleten visar en dialogruta där du anger användar-ID för tjänstens huvudnamn och lösenord.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>Logga in med hanterade identiteter för Azure-resurser

Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory. Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser. Hanterade identiteter är endast tillgängliga på virtuella datorer som körs i ett Azure-moln.

Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-to-another-cloud"></a>Logga in på ett annat moln

Azure-molntjänster erbjuder olika miljöer som följer olika regioners regler för datahantering. Om ditt Azure-konto finns i ett moln som är associerat med en av de här regionerna behöver du specificera miljön när du loggar in. Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
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
