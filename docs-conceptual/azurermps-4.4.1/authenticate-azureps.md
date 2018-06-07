---
title: Logga in med Azure PowerShell
description: Logga in med Azure PowerShell
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 52a2ccba1886c2761d66aee52b27d66e8da4d630
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819600"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="3b866-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b866-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="3b866-104">Azure PowerShell har stöd för flera inloggningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="3b866-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="3b866-105">Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="3b866-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="3b866-106">Interaktiv inloggning</span><span class="sxs-lookup"><span data-stu-id="3b866-106">Interactive log in</span></span>

1. <span data-ttu-id="3b866-107">Skriv `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="3b866-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="3b866-108">En dialogruta som frågar efter dina Azure-autentiseringsuppgifter visas.</span><span class="sxs-lookup"><span data-stu-id="3b866-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="3b866-109">Ange e-postadressen och lösenordet som är kopplade till ditt konto.</span><span class="sxs-lookup"><span data-stu-id="3b866-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="3b866-110">Azure autentiserar och sparar autentiseringsuppgifterna och stänger sedan fönstret.</span><span class="sxs-lookup"><span data-stu-id="3b866-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="3b866-111">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="3b866-111">Log in with a service principal</span></span>

<span data-ttu-id="3b866-112">Tjänstens huvudnamn ger dig ett sätt att skapa icke-interaktiva konton som du sedan kan använda för att manipulera resurser.</span><span class="sxs-lookup"><span data-stu-id="3b866-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="3b866-113">Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3b866-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="3b866-114">Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem den lägsta behörigheten som krävs för ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3b866-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="3b866-115">Om du inte redan har ett huvudnamn för tjänsten kan du [skapa ett](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="3b866-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="3b866-116">Logga in med huvudnamnet för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3b866-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="3b866-117">För att få ditt TenantId loggar du in interaktivt och hämtar sedan ditt TenantId från prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3b866-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

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

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="3b866-118">Logga in med en hanterad tjänstidentitet för Azure VM</span><span class="sxs-lookup"><span data-stu-id="3b866-118">Log in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="3b866-119">Hanterad tjänstidentitet är en funktion i förhandsversionen av Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3b866-119">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="3b866-120">Du kan använda en hanterad tjänstidentitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="3b866-120">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="3b866-121">Läs mer om [hur du använder en hanterad tjänstidentitet för Azure VM för att logga in och få en token](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="3b866-121">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="3b866-122">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="3b866-122">Log in to another Cloud</span></span>

<span data-ttu-id="3b866-123">Azure-molntjänster erbjuder olika miljöer som följer olika myndigheters regler för datahantering.</span><span class="sxs-lookup"><span data-stu-id="3b866-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="3b866-124">Om ditt Azure-konto finns i ett myndighetsmoln, behöver du specificera miljön när du loggar in.</span><span class="sxs-lookup"><span data-stu-id="3b866-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="3b866-125">Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="3b866-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="3b866-126">Använd följande kommando för att få en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="3b866-126">Use the following command to get a list of available environments:</span></span>

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

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="3b866-127">Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure</span><span class="sxs-lookup"><span data-stu-id="3b866-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="3b866-128">Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="3b866-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="3b866-129">Azure PowerShell-cmdletar för rollhantering</span><span class="sxs-lookup"><span data-stu-id="3b866-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="3b866-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3b866-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="3b866-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3b866-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="3b866-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3b866-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="3b866-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3b866-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="3b866-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3b866-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="3b866-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3b866-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="3b866-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3b866-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
