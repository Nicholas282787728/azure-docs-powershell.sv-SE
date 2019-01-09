---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786687"
---
# <a name="sign-in-with-azure-powershell"></a>Logga in med Azure PowerShell

Azure PowerShell har stöd för flera autentiseringsmetoder. Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.

## <a name="sign-in-interactively"></a>Logga in interaktivt

Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.

```azurepowershell-interactive
Connect-AzAccount
```

När du kör cmdleten visas en tokensträng. Logga in genom att kopiera den här strängen och klistra in den i https://microsoft.com/devicelogin i en webbläsare. PowerShell-sessionen autentiseras därefter för anslutning till Azure. Den här autentiseringen varar under den aktuella PowerShell-sessionen.

> [!IMPORTANT]
>
> Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.
> Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Tjänstens huvudnamn är icke-interaktiva Azure-konton. Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory. Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.

I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.

Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten. Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn. Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn. Cmdleten visar en uppmaning om att ange användar-ID och lösenord för tjänstens huvudnamn.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Logga in med en hanterad tjänstidentitet i Azure

Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory. Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser. Hanterade identiteter är endast tillgängliga på virtuella datorer som körs i ett Azure-moln.

Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Logga in som en leverantör av molnlösningar (CSP)

En inloggning för [leverantörer av molnlösningar (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) kräver `-TenantId`. Den här parametern kan normalt sett anges som antingen ett klient-ID eller ett domännamn. För CSP-inloggning måste den dock anges med ett **klient-ID**.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Logga in på ett annat moln

Azure-molntjänster erbjuder miljöer som följer regionala föreskrifter för datahantering.
För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.
Om ditt konto till exempel finns i Kina-molnet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Följande kommando hämtar en lista över tillgängliga miljöer:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure

Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).

Azure PowerShell-cmdletar för rollhantering:

* [Get-AzRoleAssignment](/powershell/module/az.Resources/Get-azRoleAssignment)
* [Get-AzRoleDefinition](/powershell/module/az.Resources/Get-azRoleDefinition)
* [New-AzRoleAssignment](/powershell/module/az.Resources/New-azRoleAssignment)
* [New-AzRoleDefinition](/powershell/module/az.Resources/New-azRoleDefinition)
* [Remove-AzRoleAssignment](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [Remove-AzRoleDefinition](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.Resources/Set-azRoleDefinition)
