---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 533982757e4ea953c1f5d07ba67ac70af2161a10
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571620"
---
# <span data-ttu-id="19dd2-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="19dd2-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="19dd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19dd2-102">SYNOPSIS</span></span>
<span data-ttu-id="19dd2-103">Lägger till ett autentiserat konto som ska användas för Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="19dd2-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

## <span data-ttu-id="19dd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19dd2-104">SYNTAX</span></span>

### <span data-ttu-id="19dd2-105">UserWithSubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="19dd2-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-106">UserWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="19dd2-106">UserWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-107">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19dd2-107">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-108">ServicePrincipalWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="19dd2-108">ServicePrincipalWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-109">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19dd2-109">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-110">ServicePrincipalCertificateWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="19dd2-110">ServicePrincipalCertificateWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-111">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19dd2-111">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dd2-112">AccessTokenWithSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="19dd2-112">AccessTokenWithSubscriptionName</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String> -AccountId <String>
 -SubscriptionName <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19dd2-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19dd2-113">DESCRIPTION</span></span>
<span data-ttu-id="19dd2-114">Add-AzureRmAcccount cmdlet lägger till ett autentiserat Azure-konto som ska användas för Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="19dd2-114">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="19dd2-115">Du kan endast använda detta autentiserade konto med Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="19dd2-115">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="19dd2-116">Använd Add-AzureAccount eller Import-AzurePublishSettingsFile cmdlet för att lägga till ett autentiserat konto för användning med tjänst hanterings cmdletar.</span><span class="sxs-lookup"><span data-stu-id="19dd2-116">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="19dd2-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19dd2-117">EXAMPLES</span></span>

### <span data-ttu-id="19dd2-118">Exempel 1: lägga till ett konto som kräver interaktiv inloggning</span><span class="sxs-lookup"><span data-stu-id="19dd2-118">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="19dd2-119">Det här kommandot lägger till ett Azure Resource Manager-konto.</span><span class="sxs-lookup"><span data-stu-id="19dd2-119">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="19dd2-120">Om du vill köra Azure Resource Manager-cmdlets med det här kontot måste du ange autentiseringsuppgifter för Microsoft-konto eller organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="19dd2-120">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="19dd2-121">Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.</span><span class="sxs-lookup"><span data-stu-id="19dd2-121">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="19dd2-122">Exempel 2: lägga till ett konto som autentiserar med autentiseringsuppgifter för organisations-ID</span><span class="sxs-lookup"><span data-stu-id="19dd2-122">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="19dd2-123">Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="19dd2-123">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="19dd2-124">Det andra kommandot lägger till ett Azure Resource Manager-konto med autentiseringsuppgifterna i $Credential.</span><span class="sxs-lookup"><span data-stu-id="19dd2-124">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="19dd2-125">Det här kontot autentiseras med Azure Resource Manager med autentiseringsuppgifter för organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="19dd2-125">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="19dd2-126">Du kan inte använda multifaktorautentisering eller autentiseringsuppgifter för Microsoft-konto för att köra Azure Resource Manager-cmdletar med detta konto.</span><span class="sxs-lookup"><span data-stu-id="19dd2-126">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="19dd2-127">Exempel 3: lägga till ett konto som autentiserar med inloggnings uppgifter för tjänsten</span><span class="sxs-lookup"><span data-stu-id="19dd2-127">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="19dd2-128">Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="19dd2-128">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="19dd2-129">Det andra kommandot lägger till ett Azure Resource Manager-konto med autentiseringsuppgifterna som lagras i $Credential för den angivna innehavaren.</span><span class="sxs-lookup"><span data-stu-id="19dd2-129">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="19dd2-130">Parametern ServicePrincipal anger att kontot autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="19dd2-130">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="19dd2-131">Exempel 4: lägga till ett konto för en viss klient organisation och ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="19dd2-131">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="19dd2-132">Det här kommandot lägger till ett Azure Resource Manager-konto för att köra cmdletar för angiven klient organisation och prenumeration som standard.</span><span class="sxs-lookup"><span data-stu-id="19dd2-132">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="19dd2-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19dd2-133">PARAMETERS</span></span>

### <span data-ttu-id="19dd2-134">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="19dd2-134">-AccessToken</span></span>
<span data-ttu-id="19dd2-135">Anger en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="19dd2-135">Specifies an access token.</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-136">-AccountId</span><span class="sxs-lookup"><span data-stu-id="19dd2-136">-AccountId</span></span>
<span data-ttu-id="19dd2-137">Konto-ID för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="19dd2-137">Account Id for access token</span></span>

```yaml
Type: String
Parameter Sets: AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-138">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="19dd2-138">-ApplicationId</span></span>
<span data-ttu-id="19dd2-139">SPN</span><span class="sxs-lookup"><span data-stu-id="19dd2-139">SPN</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-140">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="19dd2-140">-CertificateThumbprint</span></span>
<span data-ttu-id="19dd2-141">Certifikat-hash (tumavtryck)</span><span class="sxs-lookup"><span data-stu-id="19dd2-141">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-142">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="19dd2-142">-Credential</span></span>
<span data-ttu-id="19dd2-143">Anger ett PSCredential-objekt.</span><span class="sxs-lookup"><span data-stu-id="19dd2-143">Specifies a PSCredential object.</span></span>
<span data-ttu-id="19dd2-144">Om du vill ha mer information om PSCredential-objektet skriver du Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="19dd2-144">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="19dd2-145">PSCredential-objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="19dd2-145">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-146">-Miljö</span><span class="sxs-lookup"><span data-stu-id="19dd2-146">-Environment</span></span>
<span data-ttu-id="19dd2-147">Miljö som innehåller kontot att logga in på</span><span class="sxs-lookup"><span data-stu-id="19dd2-147">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="19dd2-148">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="19dd2-148">-ServicePrincipal</span></span>
<span data-ttu-id="19dd2-149">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="19dd2-149">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19dd2-150">-SubscriptionId</span></span>
<span data-ttu-id="19dd2-151">Anger ID för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="19dd2-151">Specifies the ID of the subscription.</span></span>
<span data-ttu-id="19dd2-152">Om du inte anger den här parametern används den första prenumerationen från abonnemangs listan.</span><span class="sxs-lookup"><span data-stu-id="19dd2-152">If you do not specify this parameter, the first subscription from the subscription list is used.</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId, AccessTokenWithSubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-153">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="19dd2-153">-SubscriptionName</span></span>
<span data-ttu-id="19dd2-154">Prenumerationens namn</span><span class="sxs-lookup"><span data-stu-id="19dd2-154">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionName, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionName, AccessTokenWithSubscriptionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="19dd2-155">-TenantId</span></span>
<span data-ttu-id="19dd2-156">Valfritt klient namn eller ID</span><span class="sxs-lookup"><span data-stu-id="19dd2-156">Optional tenant name or ID</span></span>

```yaml
Type: String
Parameter Sets: UserWithSubscriptionId, UserWithSubscriptionName, AccessTokenWithSubscriptionId, AccessTokenWithSubscriptionName
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalWithSubscriptionName, ServicePrincipalCertificateWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionName
Aliases: Domain

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dd2-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19dd2-157">-Confirm</span></span>
<span data-ttu-id="19dd2-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19dd2-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19dd2-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19dd2-159">-WhatIf</span></span>
<span data-ttu-id="19dd2-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19dd2-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19dd2-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19dd2-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19dd2-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dd2-162">CommonParameters</span></span>
<span data-ttu-id="19dd2-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dd2-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dd2-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19dd2-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dd2-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19dd2-165">INPUTS</span></span>

## <span data-ttu-id="19dd2-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19dd2-166">OUTPUTS</span></span>

### <span data-ttu-id="19dd2-167">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="19dd2-167">PSAzureProfile</span></span>

## <span data-ttu-id="19dd2-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19dd2-168">NOTES</span></span>

## <span data-ttu-id="19dd2-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19dd2-169">RELATED LINKS</span></span>

