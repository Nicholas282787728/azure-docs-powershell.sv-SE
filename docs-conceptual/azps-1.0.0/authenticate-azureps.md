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
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="c8b63-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8b63-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="c8b63-104">Azure PowerShell har stöd för flera autentiseringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="c8b63-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="c8b63-105">Det är enklast att komma igång genom att logga in interaktivt via kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="c8b63-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="c8b63-106">Logga in interaktivt</span><span class="sxs-lookup"><span data-stu-id="c8b63-106">Sign in interactively</span></span>

<span data-ttu-id="c8b63-107">Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.</span><span class="sxs-lookup"><span data-stu-id="c8b63-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="c8b63-108">När du kör cmdleten visas en tokensträng.</span><span class="sxs-lookup"><span data-stu-id="c8b63-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="c8b63-109">Logga in genom att kopiera den här strängen och klistra in den i https://microsoft.com/devicelogin i en webbläsare.</span><span class="sxs-lookup"><span data-stu-id="c8b63-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="c8b63-110">PowerShell-sessionen autentiseras därefter för anslutning till Azure.</span><span class="sxs-lookup"><span data-stu-id="c8b63-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="c8b63-111">Den här autentiseringen varar under den aktuella PowerShell-sessionen.</span><span class="sxs-lookup"><span data-stu-id="c8b63-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="c8b63-112">Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.</span><span class="sxs-lookup"><span data-stu-id="c8b63-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="c8b63-113">Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="c8b63-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="c8b63-114">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="c8b63-114">Sign in with a service principal</span></span>

<span data-ttu-id="c8b63-115">Tjänstens huvudnamn är icke-interaktiva Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="c8b63-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="c8b63-116">Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8b63-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="c8b63-117">Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.</span><span class="sxs-lookup"><span data-stu-id="c8b63-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="c8b63-118">I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8b63-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="c8b63-119">Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c8b63-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="c8b63-120">Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="c8b63-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="c8b63-121">Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="c8b63-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="c8b63-122">Cmdleten visar en uppmaning om att ange användar-ID och lösenord för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="c8b63-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="c8b63-123">Logga in med en hanterad tjänstidentitet i Azure</span><span class="sxs-lookup"><span data-stu-id="c8b63-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="c8b63-124">Hanterade identiteter för Azure-resurser är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8b63-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="c8b63-125">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="c8b63-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="c8b63-126">Hanterade identiteter är endast tillgängliga på virtuella datorer som körs i ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="c8b63-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="c8b63-127">Mer information om hanterade identiteter för Azure-resurser finns i [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="c8b63-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="c8b63-128">Logga in som en leverantör av molnlösningar (CSP)</span><span class="sxs-lookup"><span data-stu-id="c8b63-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="c8b63-129">En inloggning för [leverantörer av molnlösningar (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) kräver `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="c8b63-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="c8b63-130">Den här parametern kan normalt sett anges som antingen ett klient-ID eller ett domännamn.</span><span class="sxs-lookup"><span data-stu-id="c8b63-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="c8b63-131">För CSP-inloggning måste den dock anges med ett **klient-ID**.</span><span class="sxs-lookup"><span data-stu-id="c8b63-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="c8b63-132">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="c8b63-132">Sign in to another Cloud</span></span>

<span data-ttu-id="c8b63-133">Azure-molntjänster erbjuder miljöer som följer regionala föreskrifter för datahantering.</span><span class="sxs-lookup"><span data-stu-id="c8b63-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="c8b63-134">För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="c8b63-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="c8b63-135">Om ditt konto till exempel finns i Kina-molnet:</span><span class="sxs-lookup"><span data-stu-id="c8b63-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="c8b63-136">Följande kommando hämtar en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="c8b63-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="c8b63-137">Lär dig mer om att hantera rollbaserad åtkomstkontroll i Azure</span><span class="sxs-lookup"><span data-stu-id="c8b63-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="c8b63-138">Mer information om hantering av autentisering och prenumerationer i Azure finns i [Hantera konton, prenumerationer och administrativa roller](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="c8b63-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="c8b63-139">Azure PowerShell-cmdletar för rollhantering:</span><span class="sxs-lookup"><span data-stu-id="c8b63-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="c8b63-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8b63-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="c8b63-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c8b63-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="c8b63-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8b63-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="c8b63-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c8b63-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="c8b63-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c8b63-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="c8b63-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c8b63-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="c8b63-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="c8b63-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
