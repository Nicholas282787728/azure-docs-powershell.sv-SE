---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: a0f29e666a289faddbfce848b97cb0272ce67d0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757831"
---
# <span data-ttu-id="3a45a-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="3a45a-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="3a45a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3a45a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a45a-103">Anslut till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="3a45a-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a45a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3a45a-104">SYNTAX</span></span>

### <span data-ttu-id="3a45a-105">UserWithSubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="3a45a-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a45a-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a45a-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a45a-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a45a-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>]
 [-SkipContextPopulation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a45a-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a45a-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a45a-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="3a45a-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-ManagedServiceSecret <SecureString>]
 [-Subscription <String>] [-ContextName <String>] [-SkipContextPopulation] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a45a-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3a45a-110">DESCRIPTION</span></span>
<span data-ttu-id="3a45a-111">Connect-AzureRmAccount cmdlet ansluter till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="3a45a-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>
<span data-ttu-id="3a45a-112">Du kan endast använda detta autentiserade konto med Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="3a45a-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="3a45a-113">Använd Add-AzureAccount eller Import-AzurePublishSettingsFile cmdlet för att lägga till ett autentiserat konto för användning med tjänst hanterings cmdletar.</span><span class="sxs-lookup"><span data-stu-id="3a45a-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>
<span data-ttu-id="3a45a-114">Om det inte finns någon kontext för den aktuella användaren kommer det här kommandot att fylla i användarens kontext lista med en kontext för var och en av sina (första 25) prenumerationer.</span><span class="sxs-lookup"><span data-stu-id="3a45a-114">If no context is found for the current user, this command will populate the user's context list with a context for each of their (first 25) subscriptions.</span></span> <span data-ttu-id="3a45a-115">Listan med kontexter som skapas för användaren kan hittas med "Get-AzureRmContext-ListAvailable".</span><span class="sxs-lookup"><span data-stu-id="3a45a-115">The list of contexts created for the user can be found by running "Get-AzureRmContext -ListAvailable".</span></span> <span data-ttu-id="3a45a-116">Om du vill hoppa över den här kontext populationen kan du köra det här kommandot med växeln "-SkipContextPopulation".</span><span class="sxs-lookup"><span data-stu-id="3a45a-116">To skip this context population, you can run this command with the "-SkipContextPopulation" switch parameter.</span></span>
<span data-ttu-id="3a45a-117">När du har kört denna cmdlet kan du koppla ner från ett Azure-konto med AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="3a45a-117">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="3a45a-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3a45a-118">EXAMPLES</span></span>

### <span data-ttu-id="3a45a-119">Exempel 1: Använd en interaktiv inloggning för att ansluta till ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="3a45a-119">Example 1: Use an interactive login to connect to an Azure account</span></span>
```powershell
PS C:\> Connect-AzureRmAccount

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3a45a-120">Det här kommandot ansluter till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="3a45a-120">This command connects to an Azure account.</span></span>
<span data-ttu-id="3a45a-121">Om du vill köra Azure Resource Manager-cmdlets med det här kontot måste du ange autentiseringsuppgifter för Microsoft-konto eller organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="3a45a-121">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>
<span data-ttu-id="3a45a-122">Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.</span><span class="sxs-lookup"><span data-stu-id="3a45a-122">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="3a45a-123">Exempel 2: ansluta till ett Azure-konto med autentiseringsuppgifter för organisations-ID</span><span class="sxs-lookup"><span data-stu-id="3a45a-123">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```powershell
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3a45a-124">Det första kommandot frågar efter användar uppgifter (användar namn och lösen ord) och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="3a45a-124">The first command will prompt for user credentials (username and password), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="3a45a-125">Det andra kommandot ansluter till ett Azure-konto med autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="3a45a-125">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>
<span data-ttu-id="3a45a-126">Det här kontot autentiseras med Azure Resource Manager med autentiseringsuppgifter för organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="3a45a-126">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="3a45a-127">Du kan inte använda multifaktorautentisering eller autentiseringsuppgifter för Microsoft-konto för att köra Azure Resource Manager-cmdletar med detta konto.</span><span class="sxs-lookup"><span data-stu-id="3a45a-127">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="3a45a-128">Exempel 3: ansluta till ett huvud konto för Azure-tjänsten</span><span class="sxs-lookup"><span data-stu-id="3a45a-128">Example 3: Connect to an Azure service principal account</span></span>
```powershell
PS C:\> $Credential = Get-Credential

PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
xxxx-xxxx-xxxx-xxxx    Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3a45a-129">Det första kommandot får tjänstens huvud referenser (program-ID och tjänste huvud hemlighet) och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="3a45a-129">The first command gets the service principal credentials (application id and service principal secret), and then stores them in the $Credential variable.</span></span>
<span data-ttu-id="3a45a-130">Det andra kommandot ansluter till Azure med hjälp av tjänstens huvud uppgifter som lagrats i $Credential för den angivna innehavaren.</span><span class="sxs-lookup"><span data-stu-id="3a45a-130">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="3a45a-131">Parametern ServicePrincipal anger att kontot autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="3a45a-131">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="3a45a-132">Exempel 4: använda en interaktiv inloggning för att ansluta till ett konto för en viss klient organisation och prenumeration</span><span class="sxs-lookup"><span data-stu-id="3a45a-132">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
azureuser@contoso.com  Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3a45a-133">Det här kommandot ansluter till ett Azure-konto och konfigurerat AzureRM PowerShell för att köra cmdletar för angiven klient organisation och prenumeration som standard.</span><span class="sxs-lookup"><span data-stu-id="3a45a-133">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="3a45a-134">Exempel 5: lägga till ett konto med inloggning med hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="3a45a-134">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```powershell
PS C:\> Connect-AzureRmAccount -MSI

Account                SubscriptionName TenantId                Environment
-------                ---------------- --------                -----------
MSI@50342              Subscription1    xxxx-xxxx-xxxx-xxxx     AzureCloud
```

<span data-ttu-id="3a45a-135">Det här kommandot ansluter med den hanterade tjänstens identitet för värd miljön (om du till exempel har körts på en VirtualMachine med en tilldelad hanterad tjänst identitet, tillåter detta att koden loggar in med den tilldelade identiteten)</span><span class="sxs-lookup"><span data-stu-id="3a45a-135">This command connects using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

### <span data-ttu-id="3a45a-136">Exempel 6: lägga till ett konto med certifikat</span><span class="sxs-lookup"><span data-stu-id="3a45a-136">Example 6: Add an account using certificates</span></span>
```powershell
# For more information on creating a self-signed certificate
# and giving it proper permissions, please see the following:
# https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-authenticate-service-principal-powershell
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> Connect-AzureRmAccount -CertificateThumbprint $Thumbprint -ApplicationId $ApplicationId -Tenant $TenantId -ServicePrincipal

Account             SubscriptionName TenantId            Environment
-------             ---------------- --------            -----------
xxxx-xxxx-xxxx-xxxx Subscription1    xxxx-xxxx-xxxx-xxxx AzureCloud

Account          : 3794a65a-e4e4-493d-ac1d-f04308d712dd
SubscriptionName : MyTestSubscription
SubscriptionId   : 85f0f653-1f86-4d2c-a9f1-042efc00085c
TenantId         : 4cd76576-b611-43d0-8f2b-adcb139531bf
Environment      : AzureCloud
```

<span data-ttu-id="3a45a-137">Det här kommandot ansluter till ett Azure-konto med certifikatbaserad tjänstens huvud identifiering.</span><span class="sxs-lookup"><span data-stu-id="3a45a-137">This command connects to an Azure account using certificate-based service principal authentication.</span></span> <span data-ttu-id="3a45a-138">Service huvud namn som används för auktorisering bör ha skapats med det angivna certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3a45a-138">Theservice principal used for authentication should have been created with the given certificate.</span></span>

## <span data-ttu-id="3a45a-139">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3a45a-139">PARAMETERS</span></span>

### <span data-ttu-id="3a45a-140">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="3a45a-140">-AccessToken</span></span>
<span data-ttu-id="3a45a-141">Anger en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="3a45a-141">Specifies an access token.</span></span>

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

### <span data-ttu-id="3a45a-142">-AccountId</span><span class="sxs-lookup"><span data-stu-id="3a45a-142">-AccountId</span></span>
<span data-ttu-id="3a45a-143">Konto-ID för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="3a45a-143">Account Id for access token</span></span>

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

### <span data-ttu-id="3a45a-144">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3a45a-144">-ApplicationId</span></span>
<span data-ttu-id="3a45a-145">SPN</span><span class="sxs-lookup"><span data-stu-id="3a45a-145">SPN</span></span>

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

### <span data-ttu-id="3a45a-146">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="3a45a-146">-CertificateThumbprint</span></span>
<span data-ttu-id="3a45a-147">Certifikat-hash (tumavtryck)</span><span class="sxs-lookup"><span data-stu-id="3a45a-147">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="3a45a-148">-ContextName</span><span class="sxs-lookup"><span data-stu-id="3a45a-148">-ContextName</span></span>
<span data-ttu-id="3a45a-149">Namn på standard kontext från den här inloggningen.</span><span class="sxs-lookup"><span data-stu-id="3a45a-149">Name of the default context from this login.</span></span>  <span data-ttu-id="3a45a-150">Du kan välja den här kontexten efter inloggning.</span><span class="sxs-lookup"><span data-stu-id="3a45a-150">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="3a45a-151">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="3a45a-151">-Credential</span></span>
<span data-ttu-id="3a45a-152">Anger ett PSCredential-objekt.</span><span class="sxs-lookup"><span data-stu-id="3a45a-152">Specifies a PSCredential object.</span></span>
<span data-ttu-id="3a45a-153">Om du vill ha mer information om PSCredential-objektet skriver du Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="3a45a-153">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>
<span data-ttu-id="3a45a-154">PSCredential-objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="3a45a-154">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a45a-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a45a-155">-DefaultProfile</span></span>
<span data-ttu-id="3a45a-156">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3a45a-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a45a-157">-Miljö</span><span class="sxs-lookup"><span data-stu-id="3a45a-157">-Environment</span></span>
<span data-ttu-id="3a45a-158">Miljö som innehåller kontot att logga in på</span><span class="sxs-lookup"><span data-stu-id="3a45a-158">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="3a45a-159">-Force</span><span class="sxs-lookup"><span data-stu-id="3a45a-159">-Force</span></span>
<span data-ttu-id="3a45a-160">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="3a45a-160">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="3a45a-161">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="3a45a-161">-GraphAccessToken</span></span>
<span data-ttu-id="3a45a-162">AccessToken för Graph-tjänsten</span><span class="sxs-lookup"><span data-stu-id="3a45a-162">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="3a45a-163">-Identity</span><span class="sxs-lookup"><span data-stu-id="3a45a-163">-Identity</span></span>
<span data-ttu-id="3a45a-164">Logga in med hanterad tjänst identitet i den aktuella miljön.</span><span class="sxs-lookup"><span data-stu-id="3a45a-164">Login using managed service identity in the current environment.</span></span>

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

### <span data-ttu-id="3a45a-165">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="3a45a-165">-KeyVaultAccessToken</span></span>
<span data-ttu-id="3a45a-166">AccessToken för valv tjänsten</span><span class="sxs-lookup"><span data-stu-id="3a45a-166">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="3a45a-167">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="3a45a-167">-ManagedServiceHostName</span></span>
<span data-ttu-id="3a45a-168">Värdnamn för hanterad tjänst inloggning</span><span class="sxs-lookup"><span data-stu-id="3a45a-168">Host name for managed service login</span></span>

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

### <span data-ttu-id="3a45a-169">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="3a45a-169">-ManagedServicePort</span></span>
<span data-ttu-id="3a45a-170">Port nummer för hanterad tjänst inloggning</span><span class="sxs-lookup"><span data-stu-id="3a45a-170">Port number for managed service login</span></span>

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

### <span data-ttu-id="3a45a-171">-ManagedServiceSecret</span><span class="sxs-lookup"><span data-stu-id="3a45a-171">-ManagedServiceSecret</span></span>
<span data-ttu-id="3a45a-172">Hemlighet, används för vissa typer av hanterad tjänst inloggning.</span><span class="sxs-lookup"><span data-stu-id="3a45a-172">Secret, used for some kinds of managed service login.</span></span>

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

### <span data-ttu-id="3a45a-173">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="3a45a-173">-Scope</span></span>
<span data-ttu-id="3a45a-174">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="3a45a-174">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3a45a-175">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3a45a-175">-ServicePrincipal</span></span>
<span data-ttu-id="3a45a-176">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="3a45a-176">Indicates that this account authenticates by providing service principal credentials.</span></span>

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

### <span data-ttu-id="3a45a-177">-SkipContextPopulation</span><span class="sxs-lookup"><span data-stu-id="3a45a-177">-SkipContextPopulation</span></span>
<span data-ttu-id="3a45a-178">Hoppar över kontext populationen om ingen kontext hittas.</span><span class="sxs-lookup"><span data-stu-id="3a45a-178">Skips context population if no contexts are found.</span></span>

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

### <span data-ttu-id="3a45a-179">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="3a45a-179">-SkipValidation</span></span>
<span data-ttu-id="3a45a-180">Hoppa över verifiering för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="3a45a-180">Skip validation for access token</span></span>

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

### <span data-ttu-id="3a45a-181">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="3a45a-181">-Subscription</span></span>
<span data-ttu-id="3a45a-182">Prenumerationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="3a45a-182">Subscription Name or ID</span></span>

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

### <span data-ttu-id="3a45a-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="3a45a-183">-TenantId</span></span>
<span data-ttu-id="3a45a-184">Valfritt domän namn eller klient-ID.</span><span class="sxs-lookup"><span data-stu-id="3a45a-184">Optional domain name or tenant ID.</span></span> <span data-ttu-id="3a45a-185">Domän namnet fungerar inte i alla inloggnings situationer.</span><span class="sxs-lookup"><span data-stu-id="3a45a-185">Domain name will not work in all sign-in situations.</span></span> <span data-ttu-id="3a45a-186">För inloggning med moln lösnings tjänsten (CSP) krävs klient-ID.</span><span class="sxs-lookup"><span data-stu-id="3a45a-186">For Cloud Solution Provider (CSP) sign-in, tenant ID is required.</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a45a-187">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3a45a-187">-Confirm</span></span>
<span data-ttu-id="3a45a-188">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3a45a-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a45a-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a45a-189">-WhatIf</span></span>
<span data-ttu-id="3a45a-190">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3a45a-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a45a-191">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3a45a-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a45a-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a45a-192">CommonParameters</span></span>
<span data-ttu-id="3a45a-193">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a45a-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a45a-194">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a45a-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a45a-195">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3a45a-195">INPUTS</span></span>

### <span data-ttu-id="3a45a-196">System. String</span><span class="sxs-lookup"><span data-stu-id="3a45a-196">System.String</span></span>
<span data-ttu-id="3a45a-197">Parametrar: abonnemang (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a45a-197">Parameters: Subscription (ByValue)</span></span>

## <span data-ttu-id="3a45a-198">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3a45a-198">OUTPUTS</span></span>

### <span data-ttu-id="3a45a-199">Microsoft. Azure. commands. Profile. Models. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="3a45a-199">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>

## <span data-ttu-id="3a45a-200">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3a45a-200">NOTES</span></span>

## <span data-ttu-id="3a45a-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3a45a-201">RELATED LINKS</span></span>
