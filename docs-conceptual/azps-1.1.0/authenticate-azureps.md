---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342205"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="cbc3d-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbc3d-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="cbc3d-104">Azure PowerShell har stöd för flera autentiseringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="cbc3d-105">Det enklaste sättet att komma igång är med [Azure Cloud Shell](/azure/cloud-shell/overview), som automatiskt loggar in dig.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="cbc3d-106">Med en lokal installation kan du logga in interaktivt via webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="cbc3d-107">När du skriver skript för automatisering är den rekommenderade metoden att använda ett [tjänsthuvudnamn](create-azure-service-principal-azureps.md) med de nödvändiga behörigheterna.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="cbc3d-108">Du kan skydda dina Azure-resurser genom att begränsa behörigheterna för inloggning så mycket som möjligt.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="cbc3d-109">När du har loggat in körs kommandon mot standardprenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="cbc3d-110">Använd cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) för att ändra din aktiva prenumeration för en session.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="cbc3d-111">Använd [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) för att ändra standardprenumerationen som används när du loggar in med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="cbc3d-112">Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="cbc3d-113">Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="cbc3d-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="cbc3d-114">Logga in interaktivt</span><span class="sxs-lookup"><span data-stu-id="cbc3d-114">Sign in interactively</span></span>

<span data-ttu-id="cbc3d-115">Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="cbc3d-116">När du kör cmdleten visas en tokensträng.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="cbc3d-117">Kopiera den här strängen och klistra in den i https://microsoft.com/devicelogin i en webbläsare för att logga in.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="cbc3d-118">PowerShell-sessionen autentiseras därefter för anslutning till Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="cbc3d-119">Logga in med autentiseringsuppgifter</span><span class="sxs-lookup"><span data-stu-id="cbc3d-119">Sign in with credentials</span></span>

<span data-ttu-id="cbc3d-120">Du kan även logga in med ett `PSCredential`-objekt som har behörighet för att ansluta till Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="cbc3d-121">Det enklaste sättet att hämta ett autentiseringsuppgiftsobjekt är med en [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential)-cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="cbc3d-122">När den körs uppmanas du att ange ett användarnamn och ett lösenord.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="cbc3d-123">Den här metoden fungerar inte med Microsoft-konton eller konton som har tvåfaktorsautentisering aktiverad.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="cbc3d-124">Logga in med ett huvudnamn för tjänsten</span><span class="sxs-lookup"><span data-stu-id="cbc3d-124">Sign in with a service principal</span></span>

<span data-ttu-id="cbc3d-125">Tjänstens huvudnamn är icke-interaktiva Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="cbc3d-126">Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="cbc3d-127">Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="cbc3d-128">I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="cbc3d-129">Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="cbc3d-130">Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="cbc3d-131">Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="cbc3d-132">Cmdleten visar en uppmaning om att ange användar-ID och lösenord för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="cbc3d-133">Logga in med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="cbc3d-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="cbc3d-134">Hanterade identiteter är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="cbc3d-135">Hanterade identiteter är tjänsthuvudnamn som tilldelats till resurser som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="cbc3d-136">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="cbc3d-137">Hanterade identiteter är endast tillgängliga på resurser som körs i ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="cbc3d-138">Om du vill lära dig mer om hanterade identiteter för Azure-resurser kan du läsa [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="cbc3d-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="cbc3d-139">Logga in med en klientorganisation som inte är standard eller som molnlösningsleverantör (CSP)</span><span class="sxs-lookup"><span data-stu-id="cbc3d-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="cbc3d-140">Om ditt konto är associerat med fler än en klientorganisation måste du använda parametern `-TenantId` när du ansluter för att logga in.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="cbc3d-141">Den här parametern fungerar med alla andra inloggningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="cbc3d-142">När du loggar in kan det här parametervärdet antingen vara klientorganisationens objekt-ID för Azure (klient-ID) eller det fullständigt kvalificerade domännamnet för klientorganisationen.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="cbc3d-143">Om du är [molnlösningsleverantör (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) **måste** värdet `-TenantId` vara ett klient-ID.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="cbc3d-144">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="cbc3d-144">Sign in to another Cloud</span></span>

<span data-ttu-id="cbc3d-145">Azures molntjänster erbjuder miljöer som följer regionala lagar för datahantering.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="cbc3d-146">För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="cbc3d-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="cbc3d-147">Om ditt konto till exempel finns i Kina-molnet:</span><span class="sxs-lookup"><span data-stu-id="cbc3d-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="cbc3d-148">Följande kommando hämtar en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="cbc3d-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```