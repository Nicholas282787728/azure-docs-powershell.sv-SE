---
title: Logga in med Azure PowerShell
description: Logga in med Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: edbf17141cac4ea6e41282c8e1dd07c5b738351c
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211612"
---
# <a name="log-in-with-azure-powershell"></a>Logga in med Azure PowerShell

Azure PowerShell har stöd för flera inloggningsmetoder. Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.

## <a name="interactive-log-in"></a>Interaktiv inloggning

1. Skriv `Login-AzureRmAccount`. En dialogruta som frågar efter dina Azure-autentiseringsuppgifter visas.

2. Ange e-postadressen och lösenordet som är kopplade till ditt konto. Azure autentiserar och sparar autentiseringsuppgifterna och stänger sedan fönstret.

## <a name="log-in-with-a-service-principal"></a>Logga in med ett huvudnamn för tjänsten

Tjänstens huvudnamn ger dig ett sätt att skapa icke-interaktiva konton som du sedan kan använda för att manipulera resurser. Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory. Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem den lägsta behörigheten som krävs för ett huvudnamn för tjänsten.

1. Om du inte redan har ett huvudnamn för tjänsten kan du [skapa ett](create-azure-service-principal-azureps.md).

2. Logga in med huvudnamnet för tjänsten.

    ```powershell-interactive
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    För att få ditt TenantId loggar du in interaktivt och hämtar sedan ditt TenantId från prenumerationen.

    ```powershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a>Logga in med hanterade identiteter för Azure-resurser

Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory. Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.

Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="log-in-to-another-cloud"></a>Logga in på ett annat moln

Azure-molntjänster erbjuder olika miljöer som följer olika myndigheters regler för datahantering. Om ditt Azure-konto finns i ett myndighetsmoln, behöver du specificera miljön när du loggar in. Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:

```powershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Använd följande kommando för att få en lista över tillgängliga miljöer:

```powershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure

Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).

Azure PowerShell-cmdletar för rollhantering

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
