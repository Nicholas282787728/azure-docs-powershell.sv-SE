---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmAccount.md
ms.openlocfilehash: 11303438a50839bbe05139888cc665198ed09810
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584596"
---
# <span data-ttu-id="98769-101">Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="98769-101">Add-AzureRmAccount</span></span>

## <span data-ttu-id="98769-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98769-102">SYNOPSIS</span></span>
<span data-ttu-id="98769-103">Lägger till ett autentiserat konto som ska användas för Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="98769-103">Adds an authenticated account to use for Azure Resource Manager cmdlet requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98769-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98769-104">SYNTAX</span></span>

### <span data-ttu-id="98769-105">UserWithSubscriptionId (standard)</span><span class="sxs-lookup"><span data-stu-id="98769-105">UserWithSubscriptionId (Default)</span></span>
```
Add-AzureRmAccount [-Environment <String>] [[-Credential] <PSCredential>] [-TenantId <String>]
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98769-106">ServicePrincipalWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98769-106">ServicePrincipalWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-Credential] <PSCredential> [-ServicePrincipal] -TenantId <String>
 [-Subscription <String>] [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98769-107">ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98769-107">ServicePrincipalCertificateWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] -CertificateThumbprint <String> -ApplicationId <String>
 [-ServicePrincipal] -TenantId <String> [-Subscription <String>] [-ContextName <String>] [-Force]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98769-108">AccessTokenWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98769-108">AccessTokenWithSubscriptionId</span></span>
```
Add-AzureRmAccount [-Environment <String>] [-TenantId <String>] -AccessToken <String>
 [-GraphAccessToken <String>] [-KeyVaultAccessToken <String>] -AccountId <String> [-Subscription <String>]
 [-ContextName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98769-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98769-109">DESCRIPTION</span></span>
<span data-ttu-id="98769-110">Add-AzureRmAcccount cmdlet lägger till ett autentiserat Azure-konto som ska användas för Azure Resource Manager cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="98769-110">The Add-AzureRmAcccount cmdlet adds an authenticated Azure account to use for Azure Resource Manager cmdlet requests.</span></span>

<span data-ttu-id="98769-111">Du kan endast använda detta autentiserade konto med Azure Resource Manager-cmdletar.</span><span class="sxs-lookup"><span data-stu-id="98769-111">You can use this authenticated account only with Azure Resource Manager cmdlets.</span></span>
<span data-ttu-id="98769-112">Använd Add-AzureAccount eller Import-AzurePublishSettingsFile cmdlet för att lägga till ett autentiserat konto för användning med tjänst hanterings cmdletar.</span><span class="sxs-lookup"><span data-stu-id="98769-112">To add an authenticated account for use with Service Management cmdlets, use the Add-AzureAccount or the Import-AzurePublishSettingsFile cmdlet.</span></span>

## <span data-ttu-id="98769-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98769-113">EXAMPLES</span></span>

### <span data-ttu-id="98769-114">Exempel 1: lägga till ett konto som kräver interaktiv inloggning</span><span class="sxs-lookup"><span data-stu-id="98769-114">Example 1: Add an account that requires interactive login</span></span>
```
PS C:\>Add-AzureRmAccount
Account: azureuser@contoso.com
Environment: AzureCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="98769-115">Det här kommandot lägger till ett Azure Resource Manager-konto.</span><span class="sxs-lookup"><span data-stu-id="98769-115">This command adds an Azure Resource Manager account.</span></span>

<span data-ttu-id="98769-116">Om du vill köra Azure Resource Manager-cmdlets med det här kontot måste du ange autentiseringsuppgifter för Microsoft-konto eller organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="98769-116">To run Azure Resource Manager cmdlets with this account, you must provide Microsoft account or organizational ID credentials at the prompt.</span></span>

<span data-ttu-id="98769-117">Om multifaktorautentisering är aktiverat för dina autentiseringsuppgifter måste du logga in med det interaktiva alternativet eller använda tjänstens primära autentisering.</span><span class="sxs-lookup"><span data-stu-id="98769-117">If multi-factor authentication is enabled for your credentials, you must log in using the interactive option or use service principal authentication.</span></span>

### <span data-ttu-id="98769-118">Exempel 2: lägga till ett konto som autentiserar med autentiseringsuppgifter för organisations-ID</span><span class="sxs-lookup"><span data-stu-id="98769-118">Example 2: Add an account that authenticates with organizational ID credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential
Account: azureuser@contoso.com
Environment: AzureChinaCloud
Subscription: xxxx-xxxx-xxxx-xxxx
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="98769-119">Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="98769-119">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="98769-120">Det andra kommandot lägger till ett Azure Resource Manager-konto med autentiseringsuppgifterna i $Credential.</span><span class="sxs-lookup"><span data-stu-id="98769-120">The second command adds an Azure Resource Manager account with the credentials in $Credential.</span></span>

<span data-ttu-id="98769-121">Det här kontot autentiseras med Azure Resource Manager med autentiseringsuppgifter för organisations-ID.</span><span class="sxs-lookup"><span data-stu-id="98769-121">This account authenticates with Azure Resource Manager using organizational ID credentials.</span></span>
<span data-ttu-id="98769-122">Du kan inte använda multifaktorautentisering eller autentiseringsuppgifter för Microsoft-konto för att köra Azure Resource Manager-cmdletar med detta konto.</span><span class="sxs-lookup"><span data-stu-id="98769-122">You cannot use multi-factor authentication or Microsoft account credentials to run Azure Resource Manager cmdlets with this account.</span></span>

### <span data-ttu-id="98769-123">Exempel 3: lägga till ett konto som autentiserar med inloggnings uppgifter för tjänsten</span><span class="sxs-lookup"><span data-stu-id="98769-123">Example 3: Add an account that authenticates with service principal credentials</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> Add-AzureRmAccount -Credential $Credential -Tenant "xxxx-xxxx-xxxx-xxxx" -ServicePrincipal
Account: xxxx-xxxx-xxxx-xxxx
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="98769-124">Det första kommandot får användarautentiseringsuppgifter och lagrar dem sedan i $Credential variabel.</span><span class="sxs-lookup"><span data-stu-id="98769-124">The first command gets the user credentials, and then stores them in the $Credential variable.</span></span>

<span data-ttu-id="98769-125">Det andra kommandot lägger till ett Azure Resource Manager-konto med autentiseringsuppgifterna som lagras i $Credential för den angivna innehavaren.</span><span class="sxs-lookup"><span data-stu-id="98769-125">The second command adds an Azure Resource Manager account with the credentials stored in $Credential for the specified Tenant.</span></span>
<span data-ttu-id="98769-126">Parametern ServicePrincipal anger att kontot autentiseras som tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="98769-126">The ServicePrincipal switch parameter indicates that the account authenticates as a service principal.</span></span>

### <span data-ttu-id="98769-127">Exempel 4: lägga till ett konto för en viss klient organisation och ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="98769-127">Example 4: Add an account for a specific tenant and subscription</span></span>
```
PS C:\>Add-AzureRmAccount -Tenant "xxxx-xxxx-xxxx-xxxx" -SubscriptionId "yyyy-yyyy-yyyy-yyyy"
Account: pfuller@contoso.com
Environment: AzureCloud
Subscription: yyyy-yyyy-yyyy-yyyy
Tenant: xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="98769-128">Det här kommandot lägger till ett Azure Resource Manager-konto för att köra cmdletar för angiven klient organisation och prenumeration som standard.</span><span class="sxs-lookup"><span data-stu-id="98769-128">This command adds an Azure Resource Manager account to run cmdlets for the specified tenant and subscription by default.</span></span>

## <span data-ttu-id="98769-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98769-129">PARAMETERS</span></span>

### <span data-ttu-id="98769-130">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="98769-130">-AccessToken</span></span>
<span data-ttu-id="98769-131">Anger en åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="98769-131">Specifies an access token.</span></span>

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

### <span data-ttu-id="98769-132">-AccountId</span><span class="sxs-lookup"><span data-stu-id="98769-132">-AccountId</span></span>
<span data-ttu-id="98769-133">Konto-ID för åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="98769-133">Account Id for access token</span></span>

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

### <span data-ttu-id="98769-134">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="98769-134">-ApplicationId</span></span>
<span data-ttu-id="98769-135">SPN</span><span class="sxs-lookup"><span data-stu-id="98769-135">SPN</span></span>

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

### <span data-ttu-id="98769-136">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="98769-136">-CertificateThumbprint</span></span>
<span data-ttu-id="98769-137">Certifikat-hash (tumavtryck)</span><span class="sxs-lookup"><span data-stu-id="98769-137">Certificate Hash (Thumbprint)</span></span>

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

### <span data-ttu-id="98769-138">-ContextName</span><span class="sxs-lookup"><span data-stu-id="98769-138">-ContextName</span></span>
<span data-ttu-id="98769-139">Namn på standard kontext från den här inloggningen.</span><span class="sxs-lookup"><span data-stu-id="98769-139">Name of the default context from this login.</span></span>  <span data-ttu-id="98769-140">Du kan välja den här kontexten efter inloggning.</span><span class="sxs-lookup"><span data-stu-id="98769-140">You will be able to select this context by this name after login.</span></span>

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

### <span data-ttu-id="98769-141">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="98769-141">-Credential</span></span>
<span data-ttu-id="98769-142">Anger ett PSCredential-objekt.</span><span class="sxs-lookup"><span data-stu-id="98769-142">Specifies a PSCredential object.</span></span>
<span data-ttu-id="98769-143">Om du vill ha mer information om PSCredential-objektet skriver du Get-Help Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="98769-143">For more information about the PSCredential object, type Get-Help Get-Credential.</span></span>

<span data-ttu-id="98769-144">PSCredential-objektet innehåller användar-ID och lösen ord för autentiseringsuppgifter för organisations-ID, samt program-ID och hemlighet för autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="98769-144">The PSCredential object provides the user ID and password for organizational ID credentials, or the application ID and secret for service principal credentials.</span></span>

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

### <span data-ttu-id="98769-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98769-145">-DefaultProfile</span></span>
<span data-ttu-id="98769-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98769-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98769-147">-Miljö</span><span class="sxs-lookup"><span data-stu-id="98769-147">-Environment</span></span>
<span data-ttu-id="98769-148">Miljö som innehåller kontot att logga in på</span><span class="sxs-lookup"><span data-stu-id="98769-148">Environment containing the account to log into</span></span>

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

### <span data-ttu-id="98769-149">-Force</span><span class="sxs-lookup"><span data-stu-id="98769-149">-Force</span></span>
<span data-ttu-id="98769-150">Skriv över den befintliga kontexten med samma namn, om det finns någon.</span><span class="sxs-lookup"><span data-stu-id="98769-150">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="98769-151">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="98769-151">-GraphAccessToken</span></span>
<span data-ttu-id="98769-152">AccessToken för Graph-tjänsten</span><span class="sxs-lookup"><span data-stu-id="98769-152">AccessToken for Graph Service</span></span>

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

### <span data-ttu-id="98769-153">-KeyVaultAccessToken</span><span class="sxs-lookup"><span data-stu-id="98769-153">-KeyVaultAccessToken</span></span>
<span data-ttu-id="98769-154">AccessToken för valv tjänsten</span><span class="sxs-lookup"><span data-stu-id="98769-154">AccessToken for KeyVault Service</span></span>

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

### <span data-ttu-id="98769-155">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="98769-155">-Scope</span></span>
<span data-ttu-id="98769-156">Avgör omfattningen av kontext ändringar, till exempel wheher ändringar gäller endast för cusrrent-processen eller för alla sessioner som användaren startar.</span><span class="sxs-lookup"><span data-stu-id="98769-156">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="98769-157">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="98769-157">-ServicePrincipal</span></span>
<span data-ttu-id="98769-158">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="98769-158">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithSubscriptionId, ServicePrincipalCertificateWithSubscriptionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98769-159">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="98769-159">-Subscription</span></span>
<span data-ttu-id="98769-160">Prenumerationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="98769-160">Subscription Name or ID</span></span>

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

### <span data-ttu-id="98769-161">-TenantId</span><span class="sxs-lookup"><span data-stu-id="98769-161">-TenantId</span></span>
<span data-ttu-id="98769-162">Valfritt klient namn eller ID</span><span class="sxs-lookup"><span data-stu-id="98769-162">Optional tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: UserWithSubscriptionId, AccessTokenWithSubscriptionId
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

### <span data-ttu-id="98769-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="98769-163">-Confirm</span></span>
<span data-ttu-id="98769-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="98769-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98769-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98769-165">-WhatIf</span></span>
<span data-ttu-id="98769-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="98769-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98769-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="98769-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98769-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98769-168">CommonParameters</span></span>
<span data-ttu-id="98769-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98769-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98769-170">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98769-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98769-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98769-171">INPUTS</span></span>

### <span data-ttu-id="98769-172">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="98769-172">String</span></span>
<span data-ttu-id="98769-173">Parametern ' SubscriptionId ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="98769-173">Parameter 'SubscriptionId' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="98769-174">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="98769-174">String</span></span>
<span data-ttu-id="98769-175">Parametern ' SubscriptionName ' godkänner värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="98769-175">Parameter 'SubscriptionName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="98769-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98769-176">OUTPUTS</span></span>

### <span data-ttu-id="98769-177">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="98769-177">PSAzureProfile</span></span>
<span data-ttu-id="98769-178">Autentiseringsuppgifter, prenumeration, konto och information om klient organisationen för den inloggade användaren.</span><span class="sxs-lookup"><span data-stu-id="98769-178">Credentials, subscription, account, and tenant information for the logged in user.</span></span>

## <span data-ttu-id="98769-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98769-179">NOTES</span></span>

## <span data-ttu-id="98769-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98769-180">RELATED LINKS</span></span>

