---
title: Logga in med Azure PowerShell
description: Så här loggar du in med Azure PowerShell som användare, med tjänstens huvudnamn eller med hanterade identiteter för Azure-resurser.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244559"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="9618a-103">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9618a-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="9618a-104">Azure PowerShell har stöd för flera autentiseringsmetoder.</span><span class="sxs-lookup"><span data-stu-id="9618a-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="9618a-105">Det enklaste sättet att komma igång är med [Azure Cloud Shell](/azure/cloud-shell/overview), som automatiskt loggar in dig.</span><span class="sxs-lookup"><span data-stu-id="9618a-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="9618a-106">Med en lokal installation kan du logga in interaktivt via webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="9618a-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="9618a-107">När du skriver skript för automatisering är den rekommenderade metoden att använda ett [tjänsthuvudnamn](create-azure-service-principal-azureps.md) med de nödvändiga behörigheterna.</span><span class="sxs-lookup"><span data-stu-id="9618a-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="9618a-108">Du kan skydda dina Azure-resurser genom att begränsa behörigheterna för inloggning så mycket som möjligt.</span><span class="sxs-lookup"><span data-stu-id="9618a-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="9618a-109">Inledningsvis är du inloggad på den första prenumerationen Azure returnerar om du har åtkomst till fler än en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9618a-109">Initially, you're signed into the first subscription Azure returns if you have access to more than one subscription.</span></span> <span data-ttu-id="9618a-110">Kommandon körs mot den här prenumerationen som standard.</span><span class="sxs-lookup"><span data-stu-id="9618a-110">Commands are run against this subscription by default.</span></span> <span data-ttu-id="9618a-111">Använd cmdleten [Set-AzContext](/powershell/module/az.accounts/set-azcontext) för att ändra din aktiva prenumeration för en session.</span><span class="sxs-lookup"><span data-stu-id="9618a-111">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="9618a-112">Använd [Select-AzContext](/powershell/module/az.accounts/select-azcontext)-cmdleten för att ändra din aktiva prenumeration och låta den vara permanent mellan sessioner på samma system.</span><span class="sxs-lookup"><span data-stu-id="9618a-112">To change your active subscription and have it persist between sessions on the same system, use the [Select-AzContext](/powershell/module/az.accounts/select-azcontext) cmdlet.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9618a-113">Dina autentiseringsuppgifter delas mellan flera PowerShell-sessioner så länge du är inloggad.</span><span class="sxs-lookup"><span data-stu-id="9618a-113">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="9618a-114">Mer information finns i artikeln om [Beständiga autentiseringsuppgifter](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9618a-114">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="9618a-115">Logga in interaktivt</span><span class="sxs-lookup"><span data-stu-id="9618a-115">Sign in interactively</span></span>

<span data-ttu-id="9618a-116">Använd cmdleten [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) för att logga in interaktivt.</span><span class="sxs-lookup"><span data-stu-id="9618a-116">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="9618a-117">När denna cmdlet körs från PowerShell version 6 och senare visar den en tokensträng.</span><span class="sxs-lookup"><span data-stu-id="9618a-117">When run from PowerShell version 6 and higher, this cmdlet presents a token string.</span></span> <span data-ttu-id="9618a-118">Logga in genom att kopiera den här strängen och klistra in den på [microsoft.com/devicelogin](https://microsoft.com/devicelogin) i en webbläsare.</span><span class="sxs-lookup"><span data-stu-id="9618a-118">To sign in, copy this string and paste it into [microsoft.com/devicelogin](https://microsoft.com/devicelogin) in a web browser.</span></span> <span data-ttu-id="9618a-119">PowerShell-sessionen autentiseras därefter för anslutning till Azure.</span><span class="sxs-lookup"><span data-stu-id="9618a-119">Your PowerShell session will be authenticated to connect to Azure.</span></span> <span data-ttu-id="9618a-120">Du kan ange att parametern `UseDeviceAuthentication` ska ta emot en tokensträng i Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9618a-120">You can specify the `UseDeviceAuthentication` parameter to receive a token string on Windows PowerShell.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9618a-121">Auktorisering med användarnamn/lösenord har tagits bort i Azure PowerShell på grund av ändringar i auktoriseringsimplementering och säkerhetsproblem i Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9618a-121">Username/password credential authorization has been removed in Azure PowerShell due to changes in Active Directory authorization implementations and security concerns.</span></span> <span data-ttu-id="9618a-122">Om du använder autentiseringsuppgifter för automation får du i stället [skapa ett huvudnamn för tjänsten](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9618a-122">If you use credential authorization for automation purposes, instead [create a service principal](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="9618a-123">Använd cmdleten [Get-AzContext](/powershell/module/az.accounts/get-azcontext) för att lagra din klientorganisations ID i en variabel som ska användas i de följande två avsnitten i den här artikeln.</span><span class="sxs-lookup"><span data-stu-id="9618a-123">Use the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet to store your tenant ID in a variable to be used in the next two sections of this article.</span></span>

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="9618a-124">Logga in med ett huvudnamn för tjänsten <a name="sp-signin"/></span><span class="sxs-lookup"><span data-stu-id="9618a-124">Sign in with a service principal <a name="sp-signin"/></span></span>

<span data-ttu-id="9618a-125">Tjänstens huvudnamn är icke-interaktiva Azure-konton.</span><span class="sxs-lookup"><span data-stu-id="9618a-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="9618a-126">Precis som med andra användarkonton hanteras deras behörigheter med Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9618a-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="9618a-127">Genom att endast bevilja de behörigheter som krävs för tjänstens huvudnamn skyddas dina automatiseringsskript.</span><span class="sxs-lookup"><span data-stu-id="9618a-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="9618a-128">I [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](create-azure-service-principal-azureps.md) finns information om hur du skapar ett huvudnamn för tjänsten som ska användas med Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9618a-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="9618a-129">Använd argumentet `-ServicePrincipal` med cmdleten `Connect-AzAccount` för att logga in med ett huvudnamn för tjänsten.</span><span class="sxs-lookup"><span data-stu-id="9618a-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="9618a-130">Du behöver även program-ID:t för tjänstens huvudnamn, inloggningsuppgifter och det klient-ID som är associerat med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="9618a-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="9618a-131">Hur du loggar in med ett huvudnamn för tjänsten beror på om det har konfigurerats för lösenordsbaserad eller certifikatbaserad autentisering.</span><span class="sxs-lookup"><span data-stu-id="9618a-131">How you sign in with a service principal depends on whether it's configured for password-based or certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="9618a-132">Lösenordsbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="9618a-132">Password-based authentication</span></span>

<span data-ttu-id="9618a-133">Skapa ett huvudnamn för tjänsten som ska användas i exemplen i det här avsnittet.</span><span class="sxs-lookup"><span data-stu-id="9618a-133">Create a service principal to be used in the examples in this section.</span></span> <span data-ttu-id="9618a-134">Läs mer om att skapa tjänsthuvudnamn i [Skapa tjänstens huvudnamn för Azure med Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span><span class="sxs-lookup"><span data-stu-id="9618a-134">For more information on creating service principals, see [Create an Azure service principal with Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="9618a-135">Använd cmdleten [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) för att hämta autentiseringsuppgifterna för tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="9618a-135">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="9618a-136">Cmdleten visar en uppmaning om att ange användarnamn och lösenord.</span><span class="sxs-lookup"><span data-stu-id="9618a-136">This cmdlet presents a prompt for a username and password.</span></span> <span data-ttu-id="9618a-137">Använd tjänsthuvudnamnets `applicationID` som användarnamn och konvertera `secret` till oformaterad text för lösenordet.</span><span class="sxs-lookup"><span data-stu-id="9618a-137">Use the service principal's `applicationID` for the username and convert its `secret` to plain text for the password.</span></span>

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="9618a-138">I automationsscenarier måste du skapa autentiseringsuppgifter från ett tjänsthuvudnamns `applicationId` och `secret`:</span><span class="sxs-lookup"><span data-stu-id="9618a-138">For automation scenarios, you need to create credentials from a service principal's `applicationId` and `secret`:</span></span>

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

<span data-ttu-id="9618a-139">Se till att du använder metoder för säker lagring av lösenord vid automatisering av anslutningar med tjänstens huvudnamn.</span><span class="sxs-lookup"><span data-stu-id="9618a-139">Make sure that you use good password storage practices when automating service principal connections.</span></span>

### <a name="certificate-based-authentication"></a><span data-ttu-id="9618a-140">Certifikatbaserad autentisering</span><span class="sxs-lookup"><span data-stu-id="9618a-140">Certificate-based authentication</span></span>

<span data-ttu-id="9618a-141">För certifikatbaserad autentisering måste Azure PowerShell kunna hämta information från ett lokalt certifikatarkiv baserat på ett tumavtryck för certifikat.</span><span class="sxs-lookup"><span data-stu-id="9618a-141">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="9618a-142">När du använder tjänstens huvudnamn i stället för ett registrerat program, lägger du till argumentet `-ServicePrincipal` och anger program-ID:t för tjänstens huvudnamn som `-ApplicationId`-parameterns värde.</span><span class="sxs-lookup"><span data-stu-id="9618a-142">When using a service principal instead of a registered application, add the `-ServicePrincipal` argument and provide the service principal's Application ID as the `-ApplicationId` parameter's value.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="9618a-143">I PowerShell 5.1 kan certifikatarkivet hanteras och kontrolleras med [PKI](/powershell/module/pkiclient)-modulen.</span><span class="sxs-lookup"><span data-stu-id="9618a-143">In PowerShell 5.1, the certificate store can be managed and inspected with the [PKI](/powershell/module/pkiclient) module.</span></span> <span data-ttu-id="9618a-144">I PowerShell Core 6.x och senare är processen mer komplicerad.</span><span class="sxs-lookup"><span data-stu-id="9618a-144">For PowerShell Core 6.x and later, the process is more complicated.</span></span> <span data-ttu-id="9618a-145">Följande skript visar hur du importerar ett befintligt certifikat till det certifikatarkiv som är tillgängligt för PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9618a-145">The following scripts show you how to import an existing certificate into the certificate store accessible by PowerShell.</span></span>

#### <a name="import-a-certificate-in-powershell-51"></a><span data-ttu-id="9618a-146">Importera ett certifikat i PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="9618a-146">Import a certificate in PowerShell 5.1</span></span>

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a><span data-ttu-id="9618a-147">Importera ett certifikat i PowerShell Core 6.x och senare</span><span class="sxs-lookup"><span data-stu-id="9618a-147">Import a certificate in PowerShell Core 6.x and later</span></span>

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

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="9618a-148">Logga in med en hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="9618a-148">Sign in using a managed identity</span></span>

<span data-ttu-id="9618a-149">Hanterade identiteter är en funktion i Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9618a-149">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="9618a-150">Hanterade identiteter är tjänsthuvudnamn som tilldelats till resurser som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="9618a-150">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="9618a-151">Du kan använda en hanterad identitet som tjänstens huvudnamn för att logga in och få en app-begränsad åtkomsttoken för att komma åt andra resurser.</span><span class="sxs-lookup"><span data-stu-id="9618a-151">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="9618a-152">Hanterade identiteter är endast tillgängliga på resurser som körs i ett Azure-moln.</span><span class="sxs-lookup"><span data-stu-id="9618a-152">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="9618a-153">Det här exemplet ansluts med hjälp av den hanterade identiteten för värdmiljön.</span><span class="sxs-lookup"><span data-stu-id="9618a-153">This example connects using the managed identity of the host environment.</span></span> <span data-ttu-id="9618a-154">Om kommandot till exempel körs på en virtuell dator med en tilldelad hanterad tjänstidentitet kan koden logga in med hjälp av den tilldelade identiteten.</span><span class="sxs-lookup"><span data-stu-id="9618a-154">For example, if executed on a VirtualMachine with an assigned Managed Service Identity, this allows the code to sign in using that assigned identity.</span></span>

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="9618a-155">Logga in med en klientorganisation som inte är standard eller som molnlösningsleverantör (CSP)</span><span class="sxs-lookup"><span data-stu-id="9618a-155">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="9618a-156">Om ditt konto är associerat med fler än en klientorganisation måste parametern `-Tenant` specificeras när du ansluter för att logga in.</span><span class="sxs-lookup"><span data-stu-id="9618a-156">If your account is associated with more than one tenant, sign-in requires the `-Tenant` parameter to be specified when connecting.</span></span> <span data-ttu-id="9618a-157">Den här parametern fungerar med alla inloggningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="9618a-157">This parameter works with any sign-in method.</span></span> <span data-ttu-id="9618a-158">När du loggar in kan det här parametervärdet antingen vara klientorganisationens objekt-ID för Azure (klient-ID) eller det fullständigt kvalificerade domännamnet för klientorganisationen.</span><span class="sxs-lookup"><span data-stu-id="9618a-158">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="9618a-159">Om du är [molnlösningsleverantör (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/)**måste** värdet `-Tenant` vara ett klient-ID.</span><span class="sxs-lookup"><span data-stu-id="9618a-159">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/), the `-Tenant` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="9618a-160">Logga in på ett annat moln</span><span class="sxs-lookup"><span data-stu-id="9618a-160">Sign in to another Cloud</span></span>

<span data-ttu-id="9618a-161">Azures molntjänster erbjuder miljöer som följer regionala lagar för datahantering.</span><span class="sxs-lookup"><span data-stu-id="9618a-161">Azure cloud services offer environments compliant with regional data-handling laws.</span></span> <span data-ttu-id="9618a-162">För konton i ett regionalt moln anger du miljön när du loggar in med argumentet `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="9618a-162">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span> <span data-ttu-id="9618a-163">Den här parametern fungerar med alla inloggningsmetoder.</span><span class="sxs-lookup"><span data-stu-id="9618a-163">This parameter works with any sign-in method.</span></span> <span data-ttu-id="9618a-164">Om ditt konto till exempel finns i Kina-molnet:</span><span class="sxs-lookup"><span data-stu-id="9618a-164">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="9618a-165">Följande kommando hämtar en lista över tillgängliga miljöer:</span><span class="sxs-lookup"><span data-stu-id="9618a-165">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
