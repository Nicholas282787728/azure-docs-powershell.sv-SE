---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/20/2019
ms.openlocfilehash: 897bc20721305c03a0545bc236fa91292861ef1e
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363824"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="93fa0-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="93fa0-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="93fa0-104">Azure PowerShell har stöd för flera autentiseringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="93fa0-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="93fa0-105">Det enklaste sättet att komma igång är med [Azure Cloud Shell](/azure/cloud-shell/overview), som automatiskt loggar in dig.</span><span class="sxs-lookup"><span data-stu-id="93fa0-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="93fa0-106">Med en lokal installation kan du logga in interaktivt via webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="93fa0-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="93fa0-107">När du skriver skript för automatisering är den rekommenderade metoden att använda ett [tjänsthuvudnamn](create-azure-service-principal-azureps.md) med de nödvändiga behörigheterna.</span><span class="sxs-lookup"><span data-stu-id="93fa0-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="93fa0-108">Du kan skydda dina Azure-resurser genom att begränsa behörigheterna för inloggning så mycket som möjligt.</span><span class="sxs-lookup"><span data-stu-id="93fa0-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="93fa0-109">När du har loggat in körs kommandon mot standardprenumerationen.</span><span class="sxs-lookup"><span data-stu-id="93fa0-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="93fa0-110">Använd cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) för att ändra din aktiva prenumeration för en session.</span><span class="sxs-lookup"><span data-stu-id="93fa0-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="93fa0-111">Använd [Set-AzDefault](/powershell/module/az.accounts/set-azdefault) för att ändra standardprenumerationen som används när du loggar in med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93fa0-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="93fa0-112">Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.</span><span class="sxs-lookup"><span data-stu-id="93fa0-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="93fa0-113">Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="93fa0-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="93fa0-114">Logga in interaktivt</span><span class="sxs-lookup"><span data-stu-id="93fa0-114">Sign in interactively</span></span>

<span data-ttu-id="93fa0-115">Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.</span><span class="sxs-lookup"><span data-stu-id="93fa0-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="93fa0-116">När du kör cmdleten visas en tokensträng.</span><span class="sxs-lookup"><span data-stu-id="93fa0-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="93fa0-117">Kopiera den här strängen och klistra in den i https://microsoft.com/devicelogin i en webbläsare för att logga in.</span><span class="sxs-lookup"><span data-stu-id="93fa0-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="93fa0-118">PowerShell-sessionen autentiseras därefter för anslutning till Azure.</span><span class="sxs-lookup"><span data-stu-id="93fa0-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="93fa0-119">Auktorisering med användarnamn/lösenord har tagits bort i Azure PowerShell på grund av ändringar i auktoriseringsimplementering och säkerhetsproblem i Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93fa0-119">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span>
> <span data-ttu-id="93fa0-120">Om du använder autentiseringsuppgifter för automation får du i stället [skapa ett huvudnamn för tjänsten](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="93fa0-120">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

## <a name="sign-in-with-a-service-principal-a-namesp-signin"></a><span data-ttu-id="93fa0-121">Logga in med ett huvudnamn för tjänsten <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="93fa0-121">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="93fa0-122">Tjänstens huvudnamn är icke-interaktiva Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="93fa0-122">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="93fa0-123">Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93fa0-123">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="93fa0-124">Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.</span><span class="sxs-lookup"><span data-stu-id="93fa0-124">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="93fa0-125">I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93fa0-125">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="93fa0-126">Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="93fa0-126">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="93fa0-127">Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="93fa0-127">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="93fa0-128">Hur du loggar in med ett huvudnamn för tjänsten beror på om det har konfigurerats för lösenordsbaserad eller certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="93fa0-128">How you sign in with a service principal will depend on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="93fa0-129">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="93fa0-129">Password-based authentication</span></span>

<span data-ttu-id="93fa0-130">Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="93fa0-130">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="93fa0-131">Cmdleten presenterar en uppmaning om att ange användarnamn och lösenord.</span><span class="sxs-lookup"><span data-stu-id="93fa0-131">This cmdlet will present a prompt for a username and password.</span></span> <span data-ttu-id="93fa0-132">Använd ID för tjänstens huvudnamn som användarnamn.</span><span class="sxs-lookup"><span data-stu-id="93fa0-132">Use the service principal ID for the username.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="93fa0-133">I automationsscenarier måste du skapa autentiseringsuppgifter från ett användarnamn och en säker sträng:</span><span class="sxs-lookup"><span data-stu-id="93fa0-133">For automation scenarios, you need to create credentials from a user name and secure string:</span></span>

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantId
```

<span data-ttu-id="93fa0-134">Se till att du använder metoder för säker lagring av lösenord vid automatisering av anslutningar med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="93fa0-134">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="93fa0-135">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="93fa0-135">Certificate-based authentication</span></span>

<span data-ttu-id="93fa0-136">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="93fa0-136">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>
```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="93fa0-137">I PowerShell 5 kan certifikatarkivet hanteras och kontrolleras med [PKI](/powershell/module/pkiclient)-modulen.</span><span class="sxs-lookup"><span data-stu-id="93fa0-137">In PowerShell 5, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="93fa0-138">I PowerShell 6 är processen mer komplicerad.</span><span class="sxs-lookup"><span data-stu-id="93fa0-138">For PowerShell 6, the process is more complicated.</span></span> <span data-ttu-id="93fa0-139">Följande skript visar hur du importerar ett befintligt certifikat till det certifikatarkiv som är tillgängligt för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="93fa0-139">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-5"></a><span data-ttu-id="93fa0-140">Importera ett certifikat i PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="93fa0-140">Import a certificate in PowerShell 5</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-6"></a><span data-ttu-id="93fa0-141">Importera ett certifikat i PowerShell 6</span><span class="sxs-lookup"><span data-stu-id="93fa0-141">Import a certificate in PowerShell 6</span></span>

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="93fa0-142">Logga in med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="93fa0-142">Sign in using a managed identity</span></span> 

<span data-ttu-id="93fa0-143">Hanterade identiteter är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93fa0-143">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="93fa0-144">Hanterade identiteter är tjänsthuvudnamn som tilldelats till resurser som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="93fa0-144">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="93fa0-145">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="93fa0-145">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="93fa0-146">Hanterade identiteter är endast tillgängliga på resurser som körs i ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="93fa0-146">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="93fa0-147">Om du vill lära dig mer om hanterade identiteter för Azure-resurser kan du läsa [Använda hanterade identiteter för Azure-resurser på en virtuell Azure-dator för att hämta en åtkomsttoken](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="93fa0-147">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="93fa0-148">Logga in med en klientorganisation som inte är standard eller som molnlösningsleverantör (CSP)</span><span class="sxs-lookup"><span data-stu-id="93fa0-148">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="93fa0-149">Om ditt konto är associerat med fler än en klientorganisation måste du använda parametern `-TenantId` när du ansluter för att logga in.</span><span class="sxs-lookup"><span data-stu-id="93fa0-149">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="93fa0-150">Den här parametern fungerar med alla andra inloggningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="93fa0-150">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="93fa0-151">När du loggar in kan det här parametervärdet antingen vara klientorganisationens objekt-ID för Azure (klient-ID) eller det fullständigt kvalificerade domännamnet för klientorganisationen.</span><span class="sxs-lookup"><span data-stu-id="93fa0-151">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="93fa0-152">Om du är [molnlösningsleverantör (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) **måste** värdet `-TenantId` vara ett klient-ID.</span><span class="sxs-lookup"><span data-stu-id="93fa0-152">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="93fa0-153">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="93fa0-153">Sign in to another Cloud</span></span>

<span data-ttu-id="93fa0-154">Azures molntjänster erbjuder miljöer som följer regionala lagar för datahantering.</span><span class="sxs-lookup"><span data-stu-id="93fa0-154">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="93fa0-155">För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="93fa0-155">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="93fa0-156">Om ditt konto till exempel finns i Kina-molnet:</span><span class="sxs-lookup"><span data-stu-id="93fa0-156">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="93fa0-157">Följande kommando hämtar en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="93fa0-157">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
