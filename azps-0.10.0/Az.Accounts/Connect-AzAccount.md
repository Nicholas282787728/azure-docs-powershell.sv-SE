---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/connect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Connect-AzAccount.md
ms.openlocfilehash: 87e8615e7862e8b3314c9dace4849621a8ed4c78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922010"
---
# <span data-ttu-id="90001-101">Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="90001-101">Connect-AzAccount</span></span>

## <span data-ttu-id="90001-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90001-102">SYNOPSIS</span></span>
<span data-ttu-id="90001-103">Anslut till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="90001-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="90001-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90001-104">SYNTAX</span></span>

### <span data-ttu-id="90001-105">UserWithSubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="90001-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-UseDeviceAuthentication] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90001-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90001-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90001-107">UserWithCredential</span><span class="sxs-lookup"><span data-stu-id="90001-107">UserWithCredential</span></span>
```
Connect-AzAccount [-Environment <String>] -Credential <PSCredential> [-Tenant <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90001-108">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90001-108">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -Tenant <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90001-109">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90001-109">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] -AccessToken <String> [-GraphAccessToken <String>]
 [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipValidation] [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90001-110">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="90001-110">ManagedServiceLogin</span></span>
```
Connect-AzAccount [-Environment <String>] [-Tenant <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90001-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90001-111">DESCRIPTION</span></span>
<span data-ttu-id="90001-112">Connect-AzAccount cmdlet ansluter till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="90001-112">The Connect-AzAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="90001-113">Du kan endast använda detta autentiserade konto med Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90001-113">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="90001-114">Använd Add-AzAccount eller Import-AzPublishSettingsFile cmdlet för att lägga till ett autentiserat konto för användning med tjänst hanterings cmdletar.</span><span class="sxs-lookup"><span data-stu-id="90001-114">To add an authenticated account for use with Service Management cmdlets, use the Add-AzAccount or the Import-AzPublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="90001-115">Om det inte finns någon kontext för den aktuella användaren kommer det här kommandot att fylla i användarens kontext lista med en kontext för var och en av sina (första 25) prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="90001-115">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="90001-116">Listan med kontexter som skapas för användaren kan hittas med "Get-AzContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="90001-116">The list of contexts created for the user can be found by running "Get-AzContext -ListAvailable".</span></span> <span data-ttu-id="90001-117">Om du vill hoppa över den här kontext populationen kan du köra det här kommandot med växeln "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="90001-117">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="90001-118">När du har kört denna cmdlet kan du koppla ner från ett Azure-konto med AzAccount.</span><span class="sxs-lookup"><span data-stu-id="90001-118">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzAccount.</span></span>

## <span data-ttu-id="90001-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90001-119">EXAMPLES</span></span>

### <span data-ttu-id="90001-120">Exempel 1: Använd en interaktiv inloggning för att ansluta till ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="90001-120">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-121">Det här kommandot ansluter till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="90001-121">This command connects to an Azure account.</span></span>
<span data-ttu-id="90001-122">Om du vill köra Azure Resource Manager-cmdlets med det här kontot måste du ange autentiseringsuppgifter för Microsoft-konto eller organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="90001-122">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="90001-123">Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.</span><span class="sxs-lookup"><span data-stu-id="90001-123">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="90001-124">Exempel 2: (endast Windows PowerShell 5,1) Anslut till ett Azure-konto med autentiseringsuppgifter för organisations-ID</span><span class="sxs-lookup"><span data-stu-id="90001-124">Example 2: (Windows PowerShell 5.1 only) Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-125">Det här scenariot fungerar bara i Windows PowerShell 5,1.</span><span class="sxs-lookup"><span data-stu-id="90001-125">This scenario works only in Windows PowerShell 5.1.</span></span> <span data-ttu-id="90001-126">Det första kommandot frågar efter användar uppgifter (användar namn och lösen ord) och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="90001-126">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="90001-127">Det andra kommandot ansluter till ett Azure-konto med autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="90001-127">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="90001-128">Det här kontot autentiseras med Azure Resource Manager med autentiseringsuppgifter för organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="90001-128">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="90001-129">Du kan inte använda multifaktorautentisering eller autentiseringsuppgifter för Microsoft-konto för att köra Azure Resource Manager-cmdletar med detta konto.</span><span class="sxs-lookup"><span data-stu-id="90001-129">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="90001-130">Exempel 3: ansluta till ett huvud konto för Azure-tjänsten</span><span class="sxs-lookup"><span data-stu-id="90001-130">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-131">Det första kommandot får tjänstens huvud referenser (program-ID och tjänste huvud hemlighet) och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="90001-131">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="90001-132">Det andra kommandot ansluter till Azure med hjälp av tjänstens huvud uppgifter som lagrats i $Credential för den angivna innehavaren.</span><span class="sxs-lookup"><span data-stu-id="90001-132">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="90001-133">Parametern ServicePrincipal anger att kontot autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="90001-133">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="90001-134">Exempel 4: använda en interaktiv inloggning för att ansluta till ett konto för en viss klient organisation och prenumeration</span><span class="sxs-lookup"><span data-stu-id="90001-134">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-135">Det här kommandot ansluter till ett Azure-konto och konfigurerat AzureRM PowerShell för att köra cmdletar för angiven klient organisation och prenumeration som standard.</span><span class="sxs-lookup"><span data-stu-id="90001-135">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="90001-136">Exempel 5: lägga till ett konto med inloggning med hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="90001-136">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzAccount -Identity

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-137">Det här kommandot ansluter med den hanterade tjänstens identitet för värd miljön (om du till exempel har körts på en VirtualMachine med en tilldelad hanterad tjänst identitet, tillåter detta att koden loggar in med den tilldelade identiteten)</span><span class="sxs-lookup"><span data-stu-id="90001-137">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="90001-138">Exempel 6: lägga till ett konto med inloggnings-och ClientId för hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="90001-138">Example 6: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.ClientId # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-139">Det här kommandot ansluter med den hanterade tjänst identiteten för "myUserAssignedIdentity" genom att lägga till användaren tilldelad identitet till den virtuella datorn och sedan ansluta med ClientId för den användare som tilldelats identiteten.</span><span class="sxs-lookup"><span data-stu-id="90001-139">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the ClientId of the User Assigned Identity.</span></span>
<span data-ttu-id="90001-140">Mer information om hur du konfigurerar hanterade identiteter finns här: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="90001-140">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="90001-141">Exempel 7: lägga till ett konto med inloggnings-och ClientId för hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="90001-141">Example 7: Add an Account Using Managed Service Identity Login and ClientId</span></span>
```powershell
PS C:\> $identity = Get-AzUserAssignedIdentity -ResourceGroupName "myResourceGroup" -Name "myUserAssignedIdentity"
PS C:\> Get-AzVM -ResourceGroupName contoso -Name testvm | Update-AzVM -IdentityType UserAssigned -IdentityId $identity.Id
PS C:\> Connect-AzAccount -Identity -AccountId $identity.Id # Run on the "testvm" virtual machine

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
yyyy-yyyy-yyyy-yyyy    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-142">Det här kommandot ansluter med den hanterade tjänst identiteten för "myUserAssignedIdentity" genom att lägga till användaren tilldelad identitet till den virtuella datorn och sedan ansluta med ID: t för den användare som tilldelats identiteten.</span><span class="sxs-lookup"><span data-stu-id="90001-142">This command connects using the managed service identity of "myUserAssignedIdentity" by adding the User Assigned Identity to the Virtual Machine, then connecting using the Id of the User Assigned Identity.</span></span>
<span data-ttu-id="90001-143">Mer information om hur du konfigurerar hanterade identiteter finns här: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm .</span><span class="sxs-lookup"><span data-stu-id="90001-143">More information about configuring Managed Identities can be found here: https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/qs-configure-powershell-windows-vm.</span></span>

### <span data-ttu-id="90001-144">Exempel 8: lägga till ett konto med certifikat</span><span class="sxs-lookup"><span data-stu-id="90001-144">Example 8: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="90001-145">Det här kommandot ansluter till ett Azure-konto med certifikatbaserad tjänstens huvud identifiering.</span><span class="sxs-lookup"><span data-stu-id="90001-145">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="90001-146">Tjänstens huvud namn som används för auktorisering bör ha skapats med det angivna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="90001-146">The service principal used for authentication should have been created with the given certificate.</span></span>

### <span data-ttu-id="90001-147">Exempel 9: lägga till ett konto med AccessToken-verifikation</span><span class="sxs-lookup"><span data-stu-id="90001-147">Example 9: Add an account using AccessToken authentication</span></span>
```powershell
PS C:\> $url = "https://login.windows.net/<TenantId>/oauth2/token"
PS C:\> $body = "grant_type=refresh_token&refresh_token=<refreshtoken>" # Refresh token obtained from ~/.azure/TokenCache.dat
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body
PS C:\> $AccessToken = $response.access_token
PS C:\> $body1 = $body + "&resource=https%3A%2F%2Fvault.azure.net"
PS C:\> $response = Invoke-RestMethod $url -Method POST -Body $body1
PS C:\> $body2 = $body + "&resource=https%3A%2F%2Fgraph.windows.net"
PS C:\> $GraphAccessToken = $response.access_token
PS C:\> Connect-AzAccount -AccountId "azureuser@contoso.com" -AccessToken $AccessToken -KeyVaultAccessToken $KeyVaultAccessToken -GraphAccessToken $GraphAccessToken -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="90001-148">Det här kommandot ansluter till ett Azure-konto som anges i "AccountId" med hjälp av AccessToken och KeyVaultAccessToken.</span><span class="sxs-lookup"><span data-stu-id="90001-148">This command connects to an Azure account specified in "AccountId" using the AccessToken and KeyVaultAccessToken provided.</span></span>

## <span data-ttu-id="90001-149">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90001-149">PARAMETERS</span></span>

### <span data-ttu-id="90001-150">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="90001-150">-AccessToken</span></span>
<span data-ttu-id="90001-151">Anger en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="90001-151">Specifies an access token.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-152">-AccountId</span><span class="sxs-lookup"><span data-stu-id="90001-152">-AccountId</span></span>
<span data-ttu-id="90001-153">Konto-ID för åtkomsttoken i AccessToken parameter set.</span><span class="sxs-lookup"><span data-stu-id="90001-153">Account Id for access token in AccessToken parameter set.</span></span> <span data-ttu-id="90001-154">Konto-ID för hanterad tjänst i ManagedService parameter uppsättning.</span><span class="sxs-lookup"><span data-stu-id="90001-154">Account Id for managed service in ManagedService parameter set.</span></span> <span data-ttu-id="90001-155">Kan vara ett hanterat tjänst resurs-ID eller associerat klient-ID. Lämna det här fältet tomt om du vill använda SystemAssigned-identiteten.</span><span class="sxs-lookup"><span data-stu-id="90001-155">Can be a managed service resource Id, or the associated client id. To use the SystemAssigned identity, leave this field blank.</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-156">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="90001-156">-ApplicationId</span></span>
<span data-ttu-id="90001-157">SPN</span><span class="sxs-lookup"><span data-stu-id="90001-157">SPN</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-158">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="90001-158">-CertificateThumbprint</span></span>
<span data-ttu-id="90001-159">Certifikat-hash (tumavtryck)</span><span class="sxs-lookup"><span data-stu-id="90001-159">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-160">-ContextName</span><span class="sxs-lookup"><span data-stu-id="90001-160">-ContextName</span></span>
<span data-ttu-id="90001-161">Namn på standard kontext från den här inloggningen.</span><span class="sxs-lookup"><span data-stu-id="90001-161">Name of the default context from this login.</span></span>  <span data-ttu-id="90001-162">Du kan välja den här kontexten efter inloggning.</span><span class="sxs-lookup"><span data-stu-id="90001-162">You will be able to select this context by this name after login.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-163">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="90001-163">-Credential</span></span>
<span data-ttu-id="90001-164">Anger ett PSCredential-objekt.</span><span class="sxs-lookup"><span data-stu-id="90001-164">Specifies a PSCredential object.</span></span>
<span data-ttu-id="90001-165">Om du vill ha mer information om PSCredential-objektet skriver du Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="90001-165">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="90001-166">PSCredential-objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="90001-166">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, UserWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-167">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90001-167">-DefaultProfile</span></span>
<span data-ttu-id="90001-168">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90001-168">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-169">-Miljö</span><span class="sxs-lookup"><span data-stu-id="90001-169">-Environment</span></span>
<span data-ttu-id="90001-170">Miljö som innehåller kontot att logga in på</span><span class="sxs-lookup"><span data-stu-id="90001-170">Environment containing the account to log into</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-171">-Force</span><span class="sxs-lookup"><span data-stu-id="90001-171">-Force</span></span>
<span data-ttu-id="90001-172">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="90001-172">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-173">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="90001-173">-GraphAccessToken</span></span>
<span data-ttu-id="90001-174">AccessToken för Graph-tjänsten</span><span class="sxs-lookup"><span data-stu-id="90001-174">AccessToken for Graph Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-175">-Identity</span><span class="sxs-lookup"><span data-stu-id="90001-175">-Identity</span></span>
<span data-ttu-id="90001-176">Logga in med hanterad tjänst identitet i den aktuella miljön.</span><span class="sxs-lookup"><span data-stu-id="90001-176">Login using managed service identity in the current environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-177">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="90001-177">-KeyVaultAccessToken</span></span>
<span data-ttu-id="90001-178">AccessToken för valv tjänsten</span><span class="sxs-lookup"><span data-stu-id="90001-178">AccessToken for KeyVault Service</span></span>

```yaml
Type: System.String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-179">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="90001-179">-ManagedServiceHostName</span></span>
<span data-ttu-id="90001-180">Värdnamn för hanterad tjänst inloggning</span><span class="sxs-lookup"><span data-stu-id="90001-180">Host name for managed service login</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-181">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="90001-181">-ManagedServicePort</span></span>
<span data-ttu-id="90001-182">Port nummer för hanterad tjänst inloggning</span><span class="sxs-lookup"><span data-stu-id="90001-182">Port number for managed service login</span></span>

```yaml
Type: System.Int32
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-183">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="90001-183">-ManagedServiceSecret</span></span>
<span data-ttu-id="90001-184">Hemlighet, används för vissa typer av hanterad tjänst inloggning.</span><span class="sxs-lookup"><span data-stu-id="90001-184">Secret, used for some kinds of managed service login.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ManagedServiceLogin
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-185">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="90001-185">-Scope</span></span>
<span data-ttu-id="90001-186">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="90001-186">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-187">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="90001-187">-ServicePrincipal</span></span>
<span data-ttu-id="90001-188">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="90001-188">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-189">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="90001-189">-SkipContextPopulation</span></span>
<span data-ttu-id="90001-190">Hoppar över kontext populationen om ingen kontext hittas.</span><span class="sxs-lookup"><span data-stu-id="90001-190">Skips context population if no contexts are found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-191">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="90001-191">-SkipValidation</span></span>
<span data-ttu-id="90001-192">Hoppa över verifiering för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="90001-192">Skip validation for access token</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-193">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="90001-193">-Subscription</span></span>
<span data-ttu-id="90001-194">Prenumerationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="90001-194">Subscription Name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90001-195">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="90001-195">-Tenant</span></span>
<span data-ttu-id="90001-196">Valfritt klient namn eller ID</span><span class="sxs-lookup"><span data-stu-id="90001-196">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, UserWithCredential, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-197">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="90001-197">-UseDeviceAuthentication</span></span>
<span data-ttu-id="90001-198">Använda enhets kod i stället för en webb läsar kontroll</span><span class="sxs-lookup"><span data-stu-id="90001-198">Use device code authentication instead of a browser control</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UserWithSubscriptionId
Aliases: DeviceCode, DeviceAuth, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-199">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90001-199">-Confirm</span></span>
<span data-ttu-id="90001-200">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90001-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90001-201">-WhatIf</span></span>
<span data-ttu-id="90001-202">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90001-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90001-203">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90001-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90001-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90001-204">CommonParameters</span></span>
<span data-ttu-id="90001-205">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90001-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90001-206">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90001-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90001-207">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90001-207">INPUTS</span></span>

### <span data-ttu-id="90001-208">System. String</span><span class="sxs-lookup"><span data-stu-id="90001-208">System.String</span></span>

## <span data-ttu-id="90001-209">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90001-209">OUTPUTS</span></span>

### <span data-ttu-id="90001-210">Microsoft. Azure. commands. Profile. Models. Core. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="90001-210">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureProfile</span></span>

## <span data-ttu-id="90001-211">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90001-211">NOTES</span></span>

## <span data-ttu-id="90001-212">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90001-212">RELATED LINKS</span></span>
