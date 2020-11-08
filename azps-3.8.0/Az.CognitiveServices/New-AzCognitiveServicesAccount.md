---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088039"
---
# <span data-ttu-id="e3a5e-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3a5e-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="e3a5e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a5e-103">Skapar ett konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="e3a5e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3a5e-104">SYNTAX</span></span>

### <span data-ttu-id="e3a5e-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="e3a5e-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3a5e-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="e3a5e-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a5e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3a5e-107">DESCRIPTION</span></span>
<span data-ttu-id="e3a5e-108">Cmdleten **New-AzCognitiveServicesAccount** skapar ett konto för kognitiva tjänster med den angivna typen och SKU.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="e3a5e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3a5e-109">EXAMPLES</span></span>

### <span data-ttu-id="e3a5e-110">9.1</span><span class="sxs-lookup"><span data-stu-id="e3a5e-110">1:</span></span>
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

## <span data-ttu-id="e3a5e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3a5e-111">PARAMETERS</span></span>

### <span data-ttu-id="e3a5e-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e3a5e-112">-AssignIdentity</span></span>
<span data-ttu-id="e3a5e-113">Skapa och tilldela en ny profil för kognitiva tjänster för det här lagrings kontot för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="e3a5e-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="e3a5e-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="e3a5e-115">Om du vill ange ID-adress till Microsoft. CognitiveServices eller inte.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="e3a5e-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="e3a5e-116">-CustomSubdomainName</span></span>
<span data-ttu-id="e3a5e-117">Namn på domän för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="e3a5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a5e-118">-DefaultProfile</span></span>
<span data-ttu-id="e3a5e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e3a5e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3a5e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e3a5e-120">-Force</span></span>
<span data-ttu-id="e3a5e-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3a5e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3a5e-122">-KeyName</span></span>
<span data-ttu-id="e3a5e-123">Server konto kryptering-namn på nytt valv för nödsamtal</span><span class="sxs-lookup"><span data-stu-id="e3a5e-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="e3a5e-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="e3a5e-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="e3a5e-125">Om du vill ange ID-adress till Microsoft.-valv eller inte.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="e3a5e-126">Om du anger namn, värde versions-och KeyVaultUri för en server till Microsoft. valv-väder den här parametern är inställd.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="e3a5e-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e3a5e-127">-KeyVaultUri</span></span>
<span data-ttu-id="e3a5e-128">ID för konto kryptering för en KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e3a5e-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="e3a5e-129">-Version</span><span class="sxs-lookup"><span data-stu-id="e3a5e-129">-KeyVersion</span></span>
<span data-ttu-id="e3a5e-130">ID för en server för kognitiva tjänster-konto kryptering-version</span><span class="sxs-lookup"><span data-stu-id="e3a5e-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="e3a5e-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="e3a5e-131">-Location</span></span>
<span data-ttu-id="e3a5e-132">Anger den plats där kontot ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="e3a5e-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3a5e-133">-Name</span></span>
<span data-ttu-id="e3a5e-134">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="e3a5e-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="e3a5e-135">-NetworkRuleSet</span></span>
<span data-ttu-id="e3a5e-136">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel hur du hanterar förfrågningar som inte matchar någon av de definierade reglerna</span><span class="sxs-lookup"><span data-stu-id="e3a5e-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="e3a5e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a5e-137">-ResourceGroupName</span></span>
<span data-ttu-id="e3a5e-138">Anger namnet på den resurs grupp som kontot ska tilldelas till.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="e3a5e-139">Resurs gruppen måste redan finnas.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="e3a5e-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e3a5e-140">-SkuName</span></span>
<span data-ttu-id="e3a5e-141">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="e3a5e-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e3a5e-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3a5e-143">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="e3a5e-143">F0 (free tier)</span></span>
- <span data-ttu-id="e3a5e-144">S0</span><span class="sxs-lookup"><span data-stu-id="e3a5e-144">S0</span></span>
- <span data-ttu-id="e3a5e-145">S</span><span class="sxs-lookup"><span data-stu-id="e3a5e-145">S1</span></span>
- <span data-ttu-id="e3a5e-146">S2</span><span class="sxs-lookup"><span data-stu-id="e3a5e-146">S2</span></span>
- <span data-ttu-id="e3a5e-147">S3</span><span class="sxs-lookup"><span data-stu-id="e3a5e-147">S3</span></span>
- <span data-ttu-id="e3a5e-148">S4 mer information finns i [API för kognitiva tjänster](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="e3a5e-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="e3a5e-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="e3a5e-149">-StorageAccountId</span></span>
<span data-ttu-id="e3a5e-150">Lista över användardefinierade lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="e3a5e-151">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e3a5e-151">-Tag</span></span>
<span data-ttu-id="e3a5e-152">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="e3a5e-153">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e3a5e-153">-Type</span></span>
<span data-ttu-id="e3a5e-154">Anger vilken typ av konto som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-154">Specifies the type of account to create.</span></span> <span data-ttu-id="e3a5e-155">Använd `Get-AzCognitiveServicesAccountType` cmdlet för att få aktuella acceptabla värden.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="e3a5e-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3a5e-156">-Confirm</span></span>
<span data-ttu-id="e3a5e-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a5e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a5e-158">-WhatIf</span></span>
<span data-ttu-id="e3a5e-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a5e-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a5e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a5e-161">CommonParameters</span></span>
<span data-ttu-id="e3a5e-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a5e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a5e-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3a5e-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a5e-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3a5e-164">INPUTS</span></span>

### <span data-ttu-id="e3a5e-165">System. String</span><span class="sxs-lookup"><span data-stu-id="e3a5e-165">System.String</span></span>

## <span data-ttu-id="e3a5e-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3a5e-166">OUTPUTS</span></span>

### <span data-ttu-id="e3a5e-167">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3a5e-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="e3a5e-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3a5e-168">NOTES</span></span>

## <span data-ttu-id="e3a5e-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3a5e-169">RELATED LINKS</span></span>

[<span data-ttu-id="e3a5e-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3a5e-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="e3a5e-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3a5e-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="e3a5e-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3a5e-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
