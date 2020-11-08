---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088026"
---
# <span data-ttu-id="76c2d-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76c2d-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="76c2d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76c2d-102">SYNOPSIS</span></span>
<span data-ttu-id="76c2d-103">Ändrar ett konto.</span><span class="sxs-lookup"><span data-stu-id="76c2d-103">Modifies an account.</span></span>

## <span data-ttu-id="76c2d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76c2d-104">SYNTAX</span></span>

### <span data-ttu-id="76c2d-105">CognitiveServicesEncryption (standard)</span><span class="sxs-lookup"><span data-stu-id="76c2d-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76c2d-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="76c2d-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76c2d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76c2d-107">DESCRIPTION</span></span>
<span data-ttu-id="76c2d-108">Cmdleten **set-AzCognitiveServicesAccount** ändrar SKU eller taggar för det angivna kontot för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="76c2d-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="76c2d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76c2d-109">EXAMPLES</span></span>

### <span data-ttu-id="76c2d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76c2d-110">Example 1</span></span>
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

## <span data-ttu-id="76c2d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76c2d-111">PARAMETERS</span></span>

### <span data-ttu-id="76c2d-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="76c2d-112">-AssignIdentity</span></span>
<span data-ttu-id="76c2d-113">Skapa och tilldela en ny profil för kognitiva tjänster för det här lagrings kontot för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="76c2d-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="76c2d-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="76c2d-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="76c2d-115">Om du vill ange ID-adress till Microsoft. CognitiveServices eller inte.</span><span class="sxs-lookup"><span data-stu-id="76c2d-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="76c2d-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="76c2d-116">-CustomSubdomainName</span></span>
<span data-ttu-id="76c2d-117">Namn på domän för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="76c2d-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="76c2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76c2d-118">-DefaultProfile</span></span>
<span data-ttu-id="76c2d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="76c2d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76c2d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="76c2d-120">-Force</span></span>
<span data-ttu-id="76c2d-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="76c2d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76c2d-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="76c2d-122">-IdentityType</span></span>
<span data-ttu-id="76c2d-123">Typ av hanterad tjänst identitet.</span><span class="sxs-lookup"><span data-stu-id="76c2d-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="76c2d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="76c2d-124">-KeyName</span></span>
<span data-ttu-id="76c2d-125">Server konto kryptering-namn på nytt valv för nödsamtal</span><span class="sxs-lookup"><span data-stu-id="76c2d-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="76c2d-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="76c2d-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="76c2d-127">Om du vill ange ID-adress till Microsoft.-valv eller inte.</span><span class="sxs-lookup"><span data-stu-id="76c2d-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="76c2d-128">Om du anger namn, värde versions-och KeyVaultUri för en server till Microsoft. valv-väder den här parametern är inställd.</span><span class="sxs-lookup"><span data-stu-id="76c2d-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="76c2d-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="76c2d-129">-KeyVaultUri</span></span>
<span data-ttu-id="76c2d-130">ID för konto kryptering för en KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="76c2d-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="76c2d-131">-Version</span><span class="sxs-lookup"><span data-stu-id="76c2d-131">-KeyVersion</span></span>
<span data-ttu-id="76c2d-132">ID för en server för kognitiva tjänster-konto kryptering-version</span><span class="sxs-lookup"><span data-stu-id="76c2d-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="76c2d-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="76c2d-133">-Name</span></span>
<span data-ttu-id="76c2d-134">Anger namnet på kontot som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="76c2d-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="76c2d-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="76c2d-135">-NetworkRuleSet</span></span>
<span data-ttu-id="76c2d-136">NetworkRuleSet används för att definiera en uppsättning konfigurations regler för brand väggar och virtuella nätverk, samt för att ange värden för nätverks egenskaper, till exempel hur du hanterar förfrågningar som inte matchar någon av de definierade reglerna</span><span class="sxs-lookup"><span data-stu-id="76c2d-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="76c2d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76c2d-137">-ResourceGroupName</span></span>
<span data-ttu-id="76c2d-138">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="76c2d-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="76c2d-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76c2d-139">-SkuName</span></span>
<span data-ttu-id="76c2d-140">Anger SKU för kontot.</span><span class="sxs-lookup"><span data-stu-id="76c2d-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="76c2d-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="76c2d-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76c2d-142">F0 (kostnads fri nivå)</span><span class="sxs-lookup"><span data-stu-id="76c2d-142">F0 (free tier)</span></span>
- <span data-ttu-id="76c2d-143">S0</span><span class="sxs-lookup"><span data-stu-id="76c2d-143">S0</span></span>
- <span data-ttu-id="76c2d-144">S</span><span class="sxs-lookup"><span data-stu-id="76c2d-144">S1</span></span>
- <span data-ttu-id="76c2d-145">S2</span><span class="sxs-lookup"><span data-stu-id="76c2d-145">S2</span></span>
- <span data-ttu-id="76c2d-146">S3</span><span class="sxs-lookup"><span data-stu-id="76c2d-146">S3</span></span>
- <span data-ttu-id="76c2d-147">S4</span><span class="sxs-lookup"><span data-stu-id="76c2d-147">S4</span></span>

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

### <span data-ttu-id="76c2d-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="76c2d-148">-StorageAccountId</span></span>
<span data-ttu-id="76c2d-149">Lista över användardefinierade lagrings konton.</span><span class="sxs-lookup"><span data-stu-id="76c2d-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="76c2d-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="76c2d-150">-Tag</span></span>
<span data-ttu-id="76c2d-151">Anger en tagg som ett namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="76c2d-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="76c2d-152">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="76c2d-152">-Confirm</span></span>
<span data-ttu-id="76c2d-153">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="76c2d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76c2d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76c2d-154">-WhatIf</span></span>
<span data-ttu-id="76c2d-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="76c2d-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76c2d-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="76c2d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76c2d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76c2d-157">CommonParameters</span></span>
<span data-ttu-id="76c2d-158">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76c2d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76c2d-159">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76c2d-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76c2d-160">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76c2d-160">INPUTS</span></span>

### <span data-ttu-id="76c2d-161">System. String</span><span class="sxs-lookup"><span data-stu-id="76c2d-161">System.String</span></span>

### <span data-ttu-id="76c2d-162">System. Collections. hash-program []</span><span class="sxs-lookup"><span data-stu-id="76c2d-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="76c2d-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76c2d-163">OUTPUTS</span></span>

### <span data-ttu-id="76c2d-164">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76c2d-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="76c2d-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76c2d-165">NOTES</span></span>

## <span data-ttu-id="76c2d-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76c2d-166">RELATED LINKS</span></span>

[<span data-ttu-id="76c2d-167">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76c2d-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="76c2d-168">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76c2d-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="76c2d-169">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="76c2d-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
