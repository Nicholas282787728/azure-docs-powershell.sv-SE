---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321779"
---
# <span data-ttu-id="dcf08-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dcf08-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="dcf08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dcf08-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf08-103">Skapar ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="dcf08-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="dcf08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dcf08-104">SYNTAX</span></span>

### <span data-ttu-id="dcf08-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="dcf08-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf08-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="dcf08-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf08-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dcf08-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf08-108">Cmdleten **New-AzCognitiveServicesAccount** skapar ett konto för kognitiva tjänster med den angivna typen och SKU.</span><span class="sxs-lookup"><span data-stu-id="dcf08-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="dcf08-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dcf08-109">EXAMPLES</span></span>

### <span data-ttu-id="dcf08-110">9.1</span><span class="sxs-lookup"><span data-stu-id="dcf08-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="dcf08-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dcf08-111">PARAMETERS</span></span>

### <span data-ttu-id="dcf08-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="dcf08-112">-ApiProperty</span></span>
<span data-ttu-id="dcf08-113">ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="dcf08-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="dcf08-114">Obligatoriskt enligt specifika konto typer.</span><span class="sxs-lookup"><span data-stu-id="dcf08-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dcf08-115">-AssignIdentity</span></span>
<span data-ttu-id="dcf08-116">Skapa och tilldela en ny profil för kognitiva tjänster för det här lagrings kontot för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="dcf08-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="dcf08-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="dcf08-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="dcf08-118">Om du vill ange ID-adress till Microsoft. CognitiveServices eller inte.</span><span class="sxs-lookup"><span data-stu-id="dcf08-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="dcf08-119">-CustomSubdomainName</span></span>
<span data-ttu-id="dcf08-120">Namn på domän för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="dcf08-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="dcf08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf08-121">-DefaultProfile</span></span>
<span data-ttu-id="dcf08-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dcf08-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf08-123">-Force</span><span class="sxs-lookup"><span data-stu-id="dcf08-123">-Force</span></span>
<span data-ttu-id="dcf08-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dcf08-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dcf08-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcf08-125">-KeyName</span></span>
<span data-ttu-id="dcf08-126">Server konto kryptering-namn på nytt valv för nödsamtal</span><span class="sxs-lookup"><span data-stu-id="dcf08-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="dcf08-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="dcf08-128">Om du vill ange ID-adress till Microsoft.-valv eller inte.</span><span class="sxs-lookup"><span data-stu-id="dcf08-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="dcf08-129">Om du anger namn, värde versions-och KeyVaultUri för en server till Microsoft. valv-väder den här parametern är inställd.</span><span class="sxs-lookup"><span data-stu-id="dcf08-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="dcf08-130">-KeyVaultUri</span></span>
<span data-ttu-id="dcf08-131">ID för konto kryptering för en KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="dcf08-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-132">-Version</span><span class="sxs-lookup"><span data-stu-id="dcf08-132">-KeyVersion</span></span>
<span data-ttu-id="dcf08-133">ID för en server för kognitiva tjänster-konto kryptering-version</span><span class="sxs-lookup"><span data-stu-id="dcf08-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="dcf08-134">-Location</span></span>
<span data-ttu-id="dcf08-135">Anger den plats där kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="dcf08-135">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="dcf08-136">-Name</span></span>
<span data-ttu-id="dcf08-137">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="dcf08-137">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="dcf08-138">-NetworkRuleSet</span></span>
<span data-ttu-id="dcf08-139">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel hur du hanterar förfrågningar som inte matchar någon av de definierade reglerna</span><span class="sxs-lookup"><span data-stu-id="dcf08-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="dcf08-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="dcf08-141">Nätverks åtkomst typen för kognitiv Services-konton.</span><span class="sxs-lookup"><span data-stu-id="dcf08-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf08-142">-ResourceGroupName</span></span>
<span data-ttu-id="dcf08-143">Anger namnet på den resurs grupp som kontot ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="dcf08-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="dcf08-144">Resurs gruppen måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="dcf08-144">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dcf08-145">-SkuName</span></span>
<span data-ttu-id="dcf08-146">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="dcf08-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="dcf08-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dcf08-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dcf08-148">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="dcf08-148">F0 (free tier)</span></span>
- <span data-ttu-id="dcf08-149">S0</span><span class="sxs-lookup"><span data-stu-id="dcf08-149">S0</span></span>
- <span data-ttu-id="dcf08-150">S</span><span class="sxs-lookup"><span data-stu-id="dcf08-150">S1</span></span>
- <span data-ttu-id="dcf08-151">S2</span><span class="sxs-lookup"><span data-stu-id="dcf08-151">S2</span></span>
- <span data-ttu-id="dcf08-152">S3</span><span class="sxs-lookup"><span data-stu-id="dcf08-152">S3</span></span>
- <span data-ttu-id="dcf08-153">S4 mer information finns i [API för kognitiva tjänster](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="dcf08-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dcf08-154">-StorageAccountId</span></span>
<span data-ttu-id="dcf08-155">Lista över användardefinierade lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="dcf08-155">List of User Owned Storage Accounts.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-156">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dcf08-156">-Tag</span></span>
<span data-ttu-id="dcf08-157">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="dcf08-157">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-158">– Skriv</span><span class="sxs-lookup"><span data-stu-id="dcf08-158">-Type</span></span>
<span data-ttu-id="dcf08-159">Anger vilken typ av konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="dcf08-159">Specifies the type of account to create.</span></span> <span data-ttu-id="dcf08-160">Använd `Get-AzCognitiveServicesAccountType` cmdlet för att få aktuella acceptabla värden.</span><span class="sxs-lookup"><span data-stu-id="dcf08-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf08-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dcf08-161">-Confirm</span></span>
<span data-ttu-id="dcf08-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dcf08-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf08-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf08-163">-WhatIf</span></span>
<span data-ttu-id="dcf08-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dcf08-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf08-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dcf08-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf08-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf08-166">CommonParameters</span></span>
<span data-ttu-id="dcf08-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf08-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf08-168">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dcf08-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf08-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dcf08-169">INPUTS</span></span>

### <span data-ttu-id="dcf08-170">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf08-170">System.String</span></span>

## <span data-ttu-id="dcf08-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dcf08-171">OUTPUTS</span></span>

### <span data-ttu-id="dcf08-172">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dcf08-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="dcf08-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dcf08-173">NOTES</span></span>

## <span data-ttu-id="dcf08-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dcf08-174">RELATED LINKS</span></span>

[<span data-ttu-id="dcf08-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dcf08-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="dcf08-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dcf08-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="dcf08-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dcf08-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
