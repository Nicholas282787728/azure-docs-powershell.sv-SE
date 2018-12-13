---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: d3e467714b1a9e4840f2a34b57eabfa5a2c6eaec
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/13/2018
ms.locfileid: "53218195"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="ebed3-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ebed3-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="ebed3-104">Azure PowerShell har stöd för flera autentiseringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="ebed3-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="ebed3-105">Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="ebed3-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="ebed3-106">Logga in interaktivt</span><span class="sxs-lookup"><span data-stu-id="ebed3-106">Sign in interactively</span></span>

<span data-ttu-id="ebed3-107">Använd cmdleten [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) för att logga in interaktivt.</span><span class="sxs-lookup"><span data-stu-id="ebed3-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount
```

<span data-ttu-id="ebed3-108">Den här cmdleten visar en dialogruta där du anger den e-postadress och det lösenord som är associerade med ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="ebed3-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="ebed3-109">När du autentiserar sparas informationen för den aktuella PowerShell-sessionen, dialogrutan stängs och du får åtkomst till alla Azure PowerShell-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="ebed3-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ebed3-110">Från och med Azure PowerShell 6.3.0 delas dina autentiseringsuppgifter mellan flera PowerShell-sessioner så länge du förblir inloggad i Windows.</span><span class="sxs-lookup"><span data-stu-id="ebed3-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="ebed3-111">Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ebed3-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="ebed3-112">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="ebed3-112">Sign in with a service principal</span></span>

<span data-ttu-id="ebed3-113">Tjänstens huvudnamn ger dig ett sätt att skapa icke-interaktiva konton som du sedan kan använda för att manipulera resurser.</span><span class="sxs-lookup"><span data-stu-id="ebed3-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="ebed3-114">Huvudnamn för tjänsten liknar användarkonton som du kan tillämpa regler på med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ebed3-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="ebed3-115">Du kan säkerställa att dina automatiseringsskript är ännu säkrare genom att tilldela dem den lägsta behörigheten som krävs för ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ebed3-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="ebed3-116">Läs informationen i [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) om du behöver skapa ett huvudnamn för tjänsten som ska användas med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebed3-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="ebed3-117">Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzureRmAccount` för att logga in med ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ebed3-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="ebed3-118">Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="ebed3-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="ebed3-119">Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="ebed3-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="ebed3-120">Den här cmdleten visar en dialogruta där du anger användar-ID för tjänstens huvudnamn och lösenord.</span><span class="sxs-lookup"><span data-stu-id="ebed3-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="ebed3-121">Logga in med hanterade identiteter för Azure-resurser</span><span class="sxs-lookup"><span data-stu-id="ebed3-121">Sign in using managed identities for Azure resources</span></span>

<span data-ttu-id="ebed3-122">Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ebed3-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="ebed3-123">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="ebed3-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="ebed3-124">Hanterade identiteter är endast tillgängliga på virtuella datorer som körs i ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="ebed3-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="ebed3-125">Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="ebed3-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="ebed3-126">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="ebed3-126">Sign in to another Cloud</span></span>

<span data-ttu-id="ebed3-127">Azure-molntjänster erbjuder olika miljöer som följer olika regioners regler för datahantering.</span><span class="sxs-lookup"><span data-stu-id="ebed3-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="ebed3-128">Om ditt Azure-konto finns i ett moln som är associerat med en av de här regionerna behöver du specificera miljön när du loggar in.</span><span class="sxs-lookup"><span data-stu-id="ebed3-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="ebed3-129">Om ditt konto till exempel befinner sig i Kina-molnet, loggar du in med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="ebed3-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="ebed3-130">Använd följande kommando för att få en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="ebed3-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="ebed3-131">Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure</span><span class="sxs-lookup"><span data-stu-id="ebed3-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="ebed3-132">Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="ebed3-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="ebed3-133">Azure PowerShell-cmdletar för rollhantering:</span><span class="sxs-lookup"><span data-stu-id="ebed3-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="ebed3-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ebed3-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="ebed3-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ebed3-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="ebed3-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ebed3-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="ebed3-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ebed3-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="ebed3-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ebed3-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="ebed3-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ebed3-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="ebed3-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="ebed3-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
