---
title: Logga in med Azure PowerShell
description: Logga in med Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 71a2554052f5a25ea86fe44b6dcf5d9343c81f3e
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399203"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="b2b93-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2b93-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="b2b93-104">Azure PowerShell har stöd för flera inloggningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="b2b93-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="b2b93-105">Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="b2b93-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="b2b93-106">Interaktiv inloggning</span><span class="sxs-lookup"><span data-stu-id="b2b93-106">Interactive log in</span></span>

1. <span data-ttu-id="b2b93-107">Skriv `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="b2b93-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="b2b93-108">En dialogruta som frågar efter dina Azure-autentiseringsuppgifter visas.</span><span class="sxs-lookup"><span data-stu-id="b2b93-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="b2b93-109">Ange e-postadressen och lösenordet som är kopplade till ditt konto.</span><span class="sxs-lookup"><span data-stu-id="b2b93-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="b2b93-110">Azure autentiserar och sparar autentiseringsuppgifterna och stänger sedan fönstret.</span><span class="sxs-lookup"><span data-stu-id="b2b93-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="b2b93-111">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="b2b93-111">Log in with a service principal</span></span>

<span data-ttu-id="b2b93-112">Tjänstens huvudnamn ger dig ett sätt att skapa icke-interaktiva konton som du sedan kan använda för att manipulera resurser.</span><span class="sxs-lookup"><span data-stu-id="b2b93-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="b2b93-113">Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b2b93-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="b2b93-114">Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem den lägsta behörigheten som krävs för ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b2b93-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="b2b93-115">Om du inte redan har ett huvudnamn för tjänsten kan du [skapa ett](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="b2b93-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="b2b93-116">Logga in med huvudnamnet för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b2b93-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="b2b93-117">För att få ditt TenantId loggar du in interaktivt och hämtar sedan ditt TenantId från prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b2b93-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
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

### <a name="log-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="b2b93-118">Logga in med hanterade identiteter för Azure-resurser</span><span class="sxs-lookup"><span data-stu-id="b2b93-118">Log in using managed identities for Azure resources</span></span>

<span data-ttu-id="b2b93-119">Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b2b93-119">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="b2b93-120">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="b2b93-120">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="b2b93-121">Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="b2b93-121">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="b2b93-122">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="b2b93-122">Log in to another Cloud</span></span>

<span data-ttu-id="b2b93-123">Azure-molntjänster erbjuder olika miljöer som följer olika myndigheters regler för datahantering.</span><span class="sxs-lookup"><span data-stu-id="b2b93-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="b2b93-124">Om ditt Azure-konto finns i ett myndighetsmoln, behöver du specificera miljön när du loggar in.</span><span class="sxs-lookup"><span data-stu-id="b2b93-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="b2b93-125">Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="b2b93-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="b2b93-126">Använd följande kommando för att få en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="b2b93-126">Use the following command to get a list of available environments:</span></span>

```powershell
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

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="b2b93-127">Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure</span><span class="sxs-lookup"><span data-stu-id="b2b93-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="b2b93-128">Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="b2b93-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="b2b93-129">Azure PowerShell-cmdletar för rollhantering</span><span class="sxs-lookup"><span data-stu-id="b2b93-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="b2b93-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2b93-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="b2b93-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b2b93-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="b2b93-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2b93-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="b2b93-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b2b93-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="b2b93-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b2b93-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="b2b93-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b2b93-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="b2b93-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b2b93-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
