---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586556"
---
# <span data-ttu-id="1083f-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1083f-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1083f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1083f-102">SYNOPSIS</span></span>
<span data-ttu-id="1083f-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="1083f-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1083f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1083f-104">SYNTAX</span></span>

### <span data-ttu-id="1083f-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="1083f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1083f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1083f-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1083f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1083f-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="1083f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1083f-108">DESCRIPTION</span></span>
<span data-ttu-id="1083f-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="1083f-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="1083f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1083f-110">EXAMPLES</span></span>

### <span data-ttu-id="1083f-111">Exempel 1: Uppdatera beskrivningen av integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1083f-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="1083f-112">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="1083f-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="1083f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1083f-113">PARAMETERS</span></span>

### <span data-ttu-id="1083f-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="1083f-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="1083f-115">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1083f-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="1083f-116">-CatalogPricingTier</span></span>
<span data-ttu-id="1083f-117">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1083f-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="1083f-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1083f-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="1083f-119">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1083f-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="1083f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1083f-120">-Confirm</span></span>
<span data-ttu-id="1083f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1083f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1083f-122">-DataFactoryName</span></span>
<span data-ttu-id="1083f-123">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1083f-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-124">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1083f-124">-Description</span></span>
<span data-ttu-id="1083f-125">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="1083f-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="1083f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1083f-126">-Force</span></span>
<span data-ttu-id="1083f-127">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1083f-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1083f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1083f-128">-InputObject</span></span>
<span data-ttu-id="1083f-129">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="1083f-129">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="1083f-130">-Location</span></span>
<span data-ttu-id="1083f-131">Integrations körens plats.</span><span class="sxs-lookup"><span data-stu-id="1083f-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="1083f-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="1083f-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="1083f-133">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="1083f-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="1083f-134">-Name</span></span>
<span data-ttu-id="1083f-135">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="1083f-135">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1083f-136">-NodeCount</span></span>
<span data-ttu-id="1083f-137">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1083f-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="1083f-138">-NodeSize</span></span>
<span data-ttu-id="1083f-139">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="1083f-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="1083f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1083f-140">-ResourceGroupName</span></span>
<span data-ttu-id="1083f-141">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1083f-141">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1083f-142">-ResourceId</span></span>
<span data-ttu-id="1083f-143">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="1083f-143">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-144">-Undernät</span><span class="sxs-lookup"><span data-stu-id="1083f-144">-Subnet</span></span>
<span data-ttu-id="1083f-145">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="1083f-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-146">– Skriv</span><span class="sxs-lookup"><span data-stu-id="1083f-146">-Type</span></span>
<span data-ttu-id="1083f-147">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="1083f-147">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1083f-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="1083f-148">-VNetId</span></span>
<span data-ttu-id="1083f-149">ID för det VNet som integrations körningen ansluter till.</span><span class="sxs-lookup"><span data-stu-id="1083f-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="1083f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1083f-150">-WhatIf</span></span>
<span data-ttu-id="1083f-151">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1083f-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1083f-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1083f-152">INPUTS</span></span>

### <span data-ttu-id="1083f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="1083f-153">System.String</span></span>
<span data-ttu-id="1083f-154">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1083f-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1083f-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1083f-155">OUTPUTS</span></span>

### <span data-ttu-id="1083f-156">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1083f-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1083f-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1083f-157">NOTES</span></span>

## <span data-ttu-id="1083f-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1083f-158">RELATED LINKS</span></span>
[<span data-ttu-id="1083f-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1083f-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
