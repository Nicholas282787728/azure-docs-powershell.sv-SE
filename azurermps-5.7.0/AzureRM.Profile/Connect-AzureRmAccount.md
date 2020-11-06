---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/add-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Connect-AzureRmAccount.md
ms.openlocfilehash: 01cc9210e57edbb19caa8406e9015b36942b99d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573384"
---
# <span data-ttu-id="f5f82-101">Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f5f82-101">Connect-AzureRmAccount</span></span>

## <span data-ttu-id="f5f82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5f82-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f82-103">Anslut till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="f5f82-103">Connect to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5f82-104">SYNTAX</span></span>

### <span data-ttu-id="f5f82-105">UserWithSubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="f5f82-105">UserWithSubscriptionId (Default)</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f82-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5f82-106">ServicePrincipalWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f82-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5f82-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5f82-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5f82-108">AccessTokenWithSubscriptionId</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-SkipValidation] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5f82-109">ManagedServiceLogin</span><span class="sxs-lookup"><span data-stu-id="f5f82-109">ManagedServiceLogin</span></span>
```
Connect-AzureRmAccount [-Environment <String>] [-TenantId <String>] [-AccountId <String>] [-Identity]
 [-ManagedServicePort <Int32>] [-ManagedServiceHostName <String>] [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f82-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5f82-110">DESCRIPTION</span></span>
<span data-ttu-id="f5f82-111">Connect-AzureRmAccount cmdlet ansluter till Azure med ett autentiserat konto för användning med Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="f5f82-111">The Connect-AzureRmAccount cmdlet connects to Azure with an authenticated account for use with Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="f5f82-112">Du kan endast använda detta autentiserade konto med Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f5f82-112">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>

<span data-ttu-id="f5f82-113">Använd Add-AzureAccount eller Import-AzurePublishSettingsFile cmdlet för att lägga till ett autentiserat konto för användning med tjänst hanterings cmdletar.</span><span class="sxs-lookup"><span data-stu-id="f5f82-113">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

<span data-ttu-id="f5f82-114">När du har kört denna cmdlet kan du koppla ner från ett Azure-konto med AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="f5f82-114">After executing this cmdlet, you can disconnect from an Azure account using Disconnect-AzureRmAccount.</span></span>

## <span data-ttu-id="f5f82-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5f82-115">EXAMPLES</span></span>

### <span data-ttu-id="f5f82-116">Exempel 1: Använd en interaktiv inloggning för att ansluta till ett Azure-konto</span><span class="sxs-lookup"><span data-stu-id="f5f82-116">Example 1: Use an interactive login to connect to an Azure account</span></span>
```
PS C:\> Connect-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="f5f82-117">Det här kommandot ansluter till ett Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="f5f82-117">This command connects to an Azure account.</span></span>

<span data-ttu-id="f5f82-118">Om du vill köra Azure Resource Manager-cmdlets med det här kontot måste du ange autentiseringsuppgifter för Microsoft-konto eller organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="f5f82-118">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="f5f82-119">Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.</span><span class="sxs-lookup"><span data-stu-id="f5f82-119">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="f5f82-120">Exempel 2: ansluta till ett Azure-konto med autentiseringsuppgifter för organisations-ID</span><span class="sxs-lookup"><span data-stu-id="f5f82-120">Example 2: Connect to an Azure account using organizational ID credentials</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="f5f82-121">Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="f5f82-121">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="f5f82-122">Det andra kommandot ansluter till ett Azure-konto med autentiseringsuppgifterna som lagras i $Credential.</span><span class="sxs-lookup"><span data-stu-id="f5f82-122">The second command connects to an Azure account using the credentials stored in $Credential.</span></span>

<span data-ttu-id="f5f82-123">Det här kontot autentiseras med Azure Resource Manager med autentiseringsuppgifter för organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="f5f82-123">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>

<span data-ttu-id="f5f82-124">Du kan inte använda multifaktorautentisering eller autentiseringsuppgifter för Microsoft-konto för att köra Azure Resource Manager-cmdletar med detta konto.</span><span class="sxs-lookup"><span data-stu-id="f5f82-124">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="f5f82-125">Exempel 3: ansluta till ett huvud konto för Azure-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f5f82-125">Example 3: Connect to an Azure service principal account</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> Connect-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="f5f82-126">Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="f5f82-126">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="f5f82-127">Det andra kommandot ansluter till Azure med hjälp av tjänstens huvud uppgifter som lagrats i $Credential för den angivna innehavaren.</span><span class="sxs-lookup"><span data-stu-id="f5f82-127">The second command connect to Azure using the service principal credentials stored in $Credential for the specified Tenant.</span></span>

<span data-ttu-id="f5f82-128">Parametern ServicePrincipal anger att kontot autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="f5f82-128">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="f5f82-129">Exempel 4: använda en interaktiv inloggning för att ansluta till ett konto för en viss klient organisation och prenumeration</span><span class="sxs-lookup"><span data-stu-id="f5f82-129">Example 4: Use an interactive login to connect to an account for a specific tenant and subscription</span></span>
```
PS C:\> Connect-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="f5f82-130">Det här kommandot ansluter till ett Azure-konto och konfigurerat AzureRM PowerShell för att köra cmdletar för angiven klient organisation och prenumeration som standard.</span><span class="sxs-lookup"><span data-stu-id="f5f82-130">This command connects to an Azure account and configured AzureRM PowerShell to run cmdlets for the specified tenant and subscription by default.</span></span>

### <span data-ttu-id="f5f82-131">Exempel 5: lägga till ett konto med inloggning med hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="f5f82-131">Example 5: Add an Account Using Managed Service Identity Login</span></span>
```
PS C:\>Add-AzureRmAccount -MSI
Account: MSI@50342
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="f5f82-132">Det här kommandot loggar in med den hanterade tjänst identiteten för värd miljön (om du till exempel körde det på en VirtualMachine med en tilldelad hanterad tjänst identitet, tillåter detta att koden loggar in med den tilldelade identiteten)</span><span class="sxs-lookup"><span data-stu-id="f5f82-132">This command logs in using the managed service identity of the host environment (for example, if executed on a VirtualMachine with an assigned Managed Service Identity, this will allow the code to login using that assigned identity)</span></span>

## <span data-ttu-id="f5f82-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5f82-133">PARAMETERS</span></span>

### <span data-ttu-id="f5f82-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="f5f82-134">-AccessToken</span></span>
<span data-ttu-id="f5f82-135">Anger en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="f5f82-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="f5f82-136">-AccountId</span></span>
<span data-ttu-id="f5f82-137">Konto-ID för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="f5f82-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f5f82-138">-ApplicationId</span></span>
<span data-ttu-id="f5f82-139">SPN</span><span class="sxs-lookup"><span data-stu-id="f5f82-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f5f82-140">-CertificateThumbprint</span></span>
<span data-ttu-id="f5f82-141">Certifikat-hash (tumavtryck)</span><span class="sxs-lookup"><span data-stu-id="f5f82-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-142">-ContextName</span><span class="sxs-lookup"><span data-stu-id="f5f82-142">-ContextName</span></span>
<span data-ttu-id="f5f82-143">Namn på standard kontext från den här inloggningen.</span><span class="sxs-lookup"><span data-stu-id="f5f82-143">Name of the default context from this login.</span></span>  <span data-ttu-id="f5f82-144">Du kan välja den här kontexten efter inloggning.</span><span class="sxs-lookup"><span data-stu-id="f5f82-144">You will be able to select this context by this name after login.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-145">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="f5f82-145">-Credential</span></span>
<span data-ttu-id="f5f82-146">Anger ett PSCredential-objekt.</span><span class="sxs-lookup"><span data-stu-id="f5f82-146">Specifies a PSCredential object.</span></span>
<span data-ttu-id="f5f82-147">Om du vill ha mer information om PSCredential-objektet skriver du Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="f5f82-147">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="f5f82-148">PSCredential-objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="f5f82-148">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f82-149">-DefaultProfile</span></span>
<span data-ttu-id="f5f82-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f82-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-151">-Miljö</span><span class="sxs-lookup"><span data-stu-id="f5f82-151">-Environment</span></span>
<span data-ttu-id="f5f82-152">Miljö som innehåller kontot att logga in på</span><span class="sxs-lookup"><span data-stu-id="f5f82-152">Environment containing the account to log into</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-153">-Force</span><span class="sxs-lookup"><span data-stu-id="f5f82-153">-Force</span></span>
<span data-ttu-id="f5f82-154">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="f5f82-154">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-155">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="f5f82-155">-GraphAccessToken</span></span>
<span data-ttu-id="f5f82-156">AccessToken för Graph-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f5f82-156">AccessToken for Graph Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-157">-Identity</span><span class="sxs-lookup"><span data-stu-id="f5f82-157">-Identity</span></span>
<span data-ttu-id="f5f82-158">Logga in med hanterad tjänst identitet i den aktuella miljön.</span><span class="sxs-lookup"><span data-stu-id="f5f82-158">Login using managed service identity in the current environment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedServiceLogin
Aliases: MSI, ManagedService

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-159">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="f5f82-159">-KeyVaultAccessToken</span></span>
<span data-ttu-id="f5f82-160">AccessToken för valv tjänsten</span><span class="sxs-lookup"><span data-stu-id="f5f82-160">AccessToken for KeyVault Service</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-161">-ManagedServiceHostName</span><span class="sxs-lookup"><span data-stu-id="f5f82-161">-ManagedServiceHostName</span></span>
<span data-ttu-id="f5f82-162">Värdnamn för hanterad tjänst inloggning</span><span class="sxs-lookup"><span data-stu-id="f5f82-162">Host name for managed service login</span></span>

```yaml
Type: String
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-163">-ManagedServicePort</span><span class="sxs-lookup"><span data-stu-id="f5f82-163">-ManagedServicePort</span></span>
<span data-ttu-id="f5f82-164">Port nummer för hanterad tjänst inloggning</span><span class="sxs-lookup"><span data-stu-id="f5f82-164">Port number for managed service login</span></span>

```yaml
Type: Int32
Parameter Sets: ManagedServiceLogin
Aliases: 

Required: False
Position: Named
Default value: 50342
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-165">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="f5f82-165">-Scope</span></span>
<span data-ttu-id="f5f82-166">Avgör omfattningen av kontext ändringar, till exempel om ändringar endast gäller för den aktuella processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="f5f82-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-167">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f5f82-167">-ServicePrincipal</span></span>
<span data-ttu-id="f5f82-168">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="f5f82-168">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-169">-SkipValidation</span><span class="sxs-lookup"><span data-stu-id="f5f82-169">-SkipValidation</span></span>
<span data-ttu-id="f5f82-170">Hoppa över verifiering för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="f5f82-170">Skip validation for access token</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-171">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="f5f82-171">-Subscription</span></span>
<span data-ttu-id="f5f82-172">Prenumerationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="f5f82-172">Subscription Name or ID</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-173">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f5f82-173">-TenantId</span></span>
<span data-ttu-id="f5f82-174">Valfritt klient namn eller ID</span><span class="sxs-lookup"><span data-stu-id="f5f82-174">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId, ManagedServiceLogin
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5f82-175">-Confirm</span></span>
<span data-ttu-id="f5f82-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5f82-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f82-177">-WhatIf</span></span>
<span data-ttu-id="f5f82-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5f82-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5f82-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5f82-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f82-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f82-180">CommonParameters</span></span>
<span data-ttu-id="f5f82-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f82-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f82-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f82-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f82-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5f82-183">INPUTS</span></span>

### <span data-ttu-id="f5f82-184">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="f5f82-184">String</span></span>
<span data-ttu-id="f5f82-185">Parametern ' SubscriptionId ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="f5f82-185">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="f5f82-186">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="f5f82-186">String</span></span>
<span data-ttu-id="f5f82-187">Parametern ' SubscriptionName ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="f5f82-187">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f5f82-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5f82-188">OUTPUTS</span></span>

### <span data-ttu-id="f5f82-189">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="f5f82-189">PSAzureProfile</span></span>
<span data-ttu-id="f5f82-190">Autentiseringsuppgifter, prenumeration, konto och information om klient organisationen för den inloggade användaren.</span><span class="sxs-lookup"><span data-stu-id="f5f82-190">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="f5f82-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5f82-191">NOTES</span></span>

## <span data-ttu-id="f5f82-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5f82-192">RELATED LINKS</span></span>

