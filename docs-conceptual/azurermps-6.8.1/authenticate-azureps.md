---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 137365e9c022d0ca88dcfd3987e856beb2432897
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300977"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="c01b7-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c01b7-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="c01b7-104">Azure PowerShell har stöd för flera autentiseringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="c01b7-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="c01b7-105">Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="c01b7-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="c01b7-106">Logga in interaktivt</span><span class="sxs-lookup"><span data-stu-id="c01b7-106">Sign in interactively</span></span>

<span data-ttu-id="c01b7-107">Använd cmdleten [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) för att logga in interaktivt.</span><span class="sxs-lookup"><span data-stu-id="c01b7-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="c01b7-108">Den här cmdleten visar en dialogruta där du anger den e-postadress och det lösenord som är associerade med ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="c01b7-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="c01b7-109">Den här autentiseringen varar under den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="c01b7-109">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c01b7-110">Från och med Azure PowerShell 6.3.0 delas dina autentiseringsuppgifter mellan flera PowerShell-sessioner så länge du förblir inloggad i Windows.</span><span class="sxs-lookup"><span data-stu-id="c01b7-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="c01b7-111">Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="c01b7-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="c01b7-112">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="c01b7-112">Sign in with a service principal</span></span>

<span data-ttu-id="c01b7-113">Tjänstens huvudnamn är icke-interaktiva Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="c01b7-113">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="c01b7-114">Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c01b7-114">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="c01b7-115">Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.</span><span class="sxs-lookup"><span data-stu-id="c01b7-115">By granting a service principle only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="c01b7-116">I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c01b7-116">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="c01b7-117">Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzureRmAccount` för att logga in med ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c01b7-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="c01b7-118">Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="c01b7-118">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="c01b7-119">Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="c01b7-119">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="c01b7-120">Den här cmdleten visar en dialogruta där du anger användar-ID för tjänstens huvudnamn och lösenord.</span><span class="sxs-lookup"><span data-stu-id="c01b7-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="c01b7-121">Logga in med en hanterad tjänstidentitet i Azure</span><span class="sxs-lookup"><span data-stu-id="c01b7-121">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="c01b7-122">Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c01b7-122">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="c01b7-123">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="c01b7-123">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="c01b7-124">Hanterade identiteter är endast tillgängliga på virtuella datorer som körs i ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="c01b7-124">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="c01b7-125">Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="c01b7-125">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="c01b7-126">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="c01b7-126">Sign in to another Cloud</span></span>

<span data-ttu-id="c01b7-127">Azure-molntjänster erbjuder miljöer som följer regionala föreskrifter för datahantering.</span><span class="sxs-lookup"><span data-stu-id="c01b7-127">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="c01b7-128">För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="c01b7-128">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="c01b7-129">Om ditt konto till exempel finns i Kina-molnet:</span><span class="sxs-lookup"><span data-stu-id="c01b7-129">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="c01b7-130">Följande kommando hämtar en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="c01b7-130">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="c01b7-131">Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure</span><span class="sxs-lookup"><span data-stu-id="c01b7-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="c01b7-132">Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="c01b7-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="c01b7-133">Azure PowerShell-cmdletar för rollhantering:</span><span class="sxs-lookup"><span data-stu-id="c01b7-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="c01b7-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c01b7-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="c01b7-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c01b7-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="c01b7-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c01b7-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="c01b7-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c01b7-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="c01b7-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c01b7-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="c01b7-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c01b7-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="c01b7-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c01b7-140">Set-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
