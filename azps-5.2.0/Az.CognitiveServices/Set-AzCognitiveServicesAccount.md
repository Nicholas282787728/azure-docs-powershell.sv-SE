---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409816"
---
# <span data-ttu-id="adc70-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="adc70-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="adc70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adc70-102">SYNOPSIS</span></span>
<span data-ttu-id="adc70-103">Ändrar ett konto.</span><span class="sxs-lookup"><span data-stu-id="adc70-103">Modifies an account.</span></span>

## <span data-ttu-id="adc70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adc70-104">SYNTAX</span></span>

### <span data-ttu-id="adc70-105">CognitiveServicesEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="adc70-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adc70-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="adc70-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc70-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adc70-107">DESCRIPTION</span></span>
<span data-ttu-id="adc70-108">Cmdleten **set-AzCognitiveServicesAccount** ändrar SKU eller taggar för det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="adc70-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="adc70-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adc70-109">EXAMPLES</span></span>

### <span data-ttu-id="adc70-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="adc70-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="adc70-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adc70-111">PARAMETERS</span></span>

### <span data-ttu-id="adc70-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="adc70-112">-ApiProperty</span></span>
<span data-ttu-id="adc70-113">ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="adc70-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="adc70-114">Obligatoriskt enligt specifika konto typer.</span><span class="sxs-lookup"><span data-stu-id="adc70-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="adc70-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="adc70-115">-AssignIdentity</span></span>
<span data-ttu-id="adc70-116">Skapa och tilldela en ny profil för kognitiva tjänster för det här lagrings kontot för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="adc70-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="adc70-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="adc70-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="adc70-118">Om du vill ange ID-adress till Microsoft. CognitiveServices eller inte.</span><span class="sxs-lookup"><span data-stu-id="adc70-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="adc70-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="adc70-119">-CustomSubdomainName</span></span>
<span data-ttu-id="adc70-120">Namn på domän för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="adc70-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="adc70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc70-121">-DefaultProfile</span></span>
<span data-ttu-id="adc70-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="adc70-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adc70-123">-Force</span><span class="sxs-lookup"><span data-stu-id="adc70-123">-Force</span></span>
<span data-ttu-id="adc70-124">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="adc70-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adc70-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="adc70-125">-IdentityType</span></span>
<span data-ttu-id="adc70-126">Typ av hanterad tjänst identitet.</span><span class="sxs-lookup"><span data-stu-id="adc70-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc70-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="adc70-127">-KeyName</span></span>
<span data-ttu-id="adc70-128">Server konto kryptering-namn på nytt valv för nödsamtal</span><span class="sxs-lookup"><span data-stu-id="adc70-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="adc70-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="adc70-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="adc70-130">Om du vill ange ID-adress till Microsoft.-valv eller inte.</span><span class="sxs-lookup"><span data-stu-id="adc70-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="adc70-131">Om du anger namn, värde versions-och KeyVaultUri för en server till Microsoft. valv-väder den här parametern är inställd.</span><span class="sxs-lookup"><span data-stu-id="adc70-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="adc70-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="adc70-132">-KeyVaultUri</span></span>
<span data-ttu-id="adc70-133">ID för konto kryptering för en KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="adc70-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="adc70-134">-Version</span><span class="sxs-lookup"><span data-stu-id="adc70-134">-KeyVersion</span></span>
<span data-ttu-id="adc70-135">ID för en server för kognitiva tjänster-konto kryptering-version</span><span class="sxs-lookup"><span data-stu-id="adc70-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="adc70-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="adc70-136">-Name</span></span>
<span data-ttu-id="adc70-137">Anger namnet på kontot som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="adc70-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="adc70-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="adc70-138">-NetworkRuleSet</span></span>
<span data-ttu-id="adc70-139">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel hur du hanterar förfrågningar som inte matchar någon av de definierade reglerna</span><span class="sxs-lookup"><span data-stu-id="adc70-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="adc70-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="adc70-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="adc70-141">Nätverks åtkomst typen för kognitiv Services-konton.</span><span class="sxs-lookup"><span data-stu-id="adc70-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="adc70-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc70-142">-ResourceGroupName</span></span>
<span data-ttu-id="adc70-143">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="adc70-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="adc70-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="adc70-144">-SkuName</span></span>
<span data-ttu-id="adc70-145">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="adc70-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="adc70-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="adc70-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="adc70-147">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="adc70-147">F0 (free tier)</span></span>
- <span data-ttu-id="adc70-148">S0</span><span class="sxs-lookup"><span data-stu-id="adc70-148">S0</span></span>
- <span data-ttu-id="adc70-149">S</span><span class="sxs-lookup"><span data-stu-id="adc70-149">S1</span></span>
- <span data-ttu-id="adc70-150">S2</span><span class="sxs-lookup"><span data-stu-id="adc70-150">S2</span></span>
- <span data-ttu-id="adc70-151">S3</span><span class="sxs-lookup"><span data-stu-id="adc70-151">S3</span></span>
- <span data-ttu-id="adc70-152">S4</span><span class="sxs-lookup"><span data-stu-id="adc70-152">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc70-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="adc70-153">-StorageAccountId</span></span>
<span data-ttu-id="adc70-154">Lista över användardefinierade lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="adc70-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="adc70-155">-Tagg</span><span class="sxs-lookup"><span data-stu-id="adc70-155">-Tag</span></span>
<span data-ttu-id="adc70-156">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="adc70-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc70-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adc70-157">-Confirm</span></span>
<span data-ttu-id="adc70-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adc70-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc70-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc70-159">-WhatIf</span></span>
<span data-ttu-id="adc70-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adc70-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adc70-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adc70-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc70-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc70-162">CommonParameters</span></span>
<span data-ttu-id="adc70-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc70-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc70-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adc70-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc70-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adc70-165">INPUTS</span></span>

### <span data-ttu-id="adc70-166">System. String</span><span class="sxs-lookup"><span data-stu-id="adc70-166">System.String</span></span>

### <span data-ttu-id="adc70-167">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="adc70-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="adc70-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adc70-168">OUTPUTS</span></span>

### <span data-ttu-id="adc70-169">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="adc70-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="adc70-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adc70-170">NOTES</span></span>

## <span data-ttu-id="adc70-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adc70-171">RELATED LINKS</span></span>

[<span data-ttu-id="adc70-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="adc70-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="adc70-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="adc70-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="adc70-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="adc70-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
