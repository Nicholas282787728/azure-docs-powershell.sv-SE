---
title: Logga in med Azure PowerShell
description: Logga in med Azure PowerShell
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 1af5aeffb8e87e916df3e2440a84805935136c0f
ms.sourcegitcommit: 5fe9a579d2e0d1cb5a05aadaeba5db784f1b18fa
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/28/2018
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

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    För att få ditt TenantId loggar du in interaktivt och hämtar sedan ditt TenantId från prenumerationen.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Logga in med en hanterad tjänstidentitet för Azure VM

Hanterad tjänstidentitet är en funktion i förhandsversionen av Azure Active Directory. Du kan använda en hanterad tjänstidentitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.

Läs mer om [hur du använder en hanterad tjänstidentitet för Azure VM för att logga in och få en token](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="log-in-to-another-cloud"></a>Logga in på ett annat moln

Azure-molntjänster erbjuder olika miljöer som följer olika myndigheters regler för datahantering. Om ditt Azure-konto finns i ett myndighetsmoln, behöver du specificera miljön när du loggar in. Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Använd följande kommando för att få en lista över tillgängliga miljöer:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
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
