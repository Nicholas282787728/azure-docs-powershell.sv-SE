---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576579"
---
# <span data-ttu-id="45d4a-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="45d4a-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="45d4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="45d4a-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="45d4a-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45d4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45d4a-104">SYNTAX</span></span>

### <span data-ttu-id="45d4a-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="45d4a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="45d4a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="45d4a-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d4a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="45d4a-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d4a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45d4a-108">DESCRIPTION</span></span>
<span data-ttu-id="45d4a-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="45d4a-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="45d4a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45d4a-110">EXAMPLES</span></span>

### <span data-ttu-id="45d4a-111">Exempel 1: Uppdatera beskrivningen av integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="45d4a-112">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="45d4a-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="45d4a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45d4a-113">PARAMETERS</span></span>

### <span data-ttu-id="45d4a-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="45d4a-114">-AuthKey</span></span>
<span data-ttu-id="45d4a-115">En autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d4a-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="45d4a-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="45d4a-117">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-117">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="45d4a-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="45d4a-118">-CatalogPricingTier</span></span>
<span data-ttu-id="45d4a-119">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-119">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="45d4a-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="45d4a-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="45d4a-121">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-121">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="45d4a-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="45d4a-122">-DataFactoryName</span></span>
<span data-ttu-id="45d4a-123">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="45d4a-123">The data factory name.</span></span>

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

### <span data-ttu-id="45d4a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d4a-124">-DefaultProfile</span></span>
<span data-ttu-id="45d4a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45d4a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d4a-126">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="45d4a-126">-Description</span></span>
<span data-ttu-id="45d4a-127">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="45d4a-127">The integration runtime description.</span></span>

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

### <span data-ttu-id="45d4a-128">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="45d4a-128">-Edition</span></span>
<span data-ttu-id="45d4a-129">Integrerings versionen för SSIS som kan vara standard eller Enterprise, standard är standard om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="45d4a-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d4a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="45d4a-130">-Force</span></span>
<span data-ttu-id="45d4a-131">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="45d4a-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="45d4a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45d4a-132">-InputObject</span></span>
<span data-ttu-id="45d4a-133">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="45d4a-133">The integration runtime object.</span></span>

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

### <span data-ttu-id="45d4a-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="45d4a-134">-LicenseType</span></span>
<span data-ttu-id="45d4a-135">Den licens typ som du vill välja för SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="45d4a-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="45d4a-136">Det finns två typer: LicenseIncluded eller BasePrice.</span><span class="sxs-lookup"><span data-stu-id="45d4a-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="45d4a-137">Om du är berättigad till priser för Azure Hybrid användning (AHUB) väljer du BasePrice.</span><span class="sxs-lookup"><span data-stu-id="45d4a-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="45d4a-138">Om inte, Välj LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="45d4a-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d4a-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="45d4a-139">-Location</span></span>
<span data-ttu-id="45d4a-140">Integrations körens plats.</span><span class="sxs-lookup"><span data-stu-id="45d4a-140">The integration runtime location.</span></span>

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

### <span data-ttu-id="45d4a-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="45d4a-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="45d4a-142">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="45d4a-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="45d4a-143">-Namn</span><span class="sxs-lookup"><span data-stu-id="45d4a-143">-Name</span></span>
<span data-ttu-id="45d4a-144">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="45d4a-144">The integration runtime name.</span></span>

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

### <span data-ttu-id="45d4a-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="45d4a-145">-NodeCount</span></span>
<span data-ttu-id="45d4a-146">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-146">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="45d4a-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="45d4a-147">-NodeSize</span></span>
<span data-ttu-id="45d4a-148">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="45d4a-148">The integration runtime node size.</span></span>

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

### <span data-ttu-id="45d4a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45d4a-149">-ResourceGroupName</span></span>
<span data-ttu-id="45d4a-150">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="45d4a-150">The resource group name.</span></span>

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

### <span data-ttu-id="45d4a-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45d4a-151">-ResourceId</span></span>
<span data-ttu-id="45d4a-152">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-152">The Azure resource ID.</span></span>

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

### <span data-ttu-id="45d4a-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="45d4a-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="45d4a-154">SAS URI för Azure Blob-behållaren som innehåller det anpassade installations skriptet.</span><span class="sxs-lookup"><span data-stu-id="45d4a-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="45d4a-155">-Undernät</span><span class="sxs-lookup"><span data-stu-id="45d4a-155">-Subnet</span></span>
<span data-ttu-id="45d4a-156">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="45d4a-156">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="45d4a-157">– Skriv</span><span class="sxs-lookup"><span data-stu-id="45d4a-157">-Type</span></span>
<span data-ttu-id="45d4a-158">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="45d4a-158">The integration runtime type.</span></span>

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

### <span data-ttu-id="45d4a-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="45d4a-159">-VNetId</span></span>
<span data-ttu-id="45d4a-160">ID för det VNet som integrations körningen ansluter till.</span><span class="sxs-lookup"><span data-stu-id="45d4a-160">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="45d4a-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45d4a-161">-Confirm</span></span>
<span data-ttu-id="45d4a-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45d4a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d4a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d4a-163">-WhatIf</span></span>
<span data-ttu-id="45d4a-164">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45d4a-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="45d4a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d4a-165">CommonParameters</span></span>
<span data-ttu-id="45d4a-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d4a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d4a-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d4a-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d4a-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45d4a-168">INPUTS</span></span>

### <span data-ttu-id="45d4a-169">System. String</span><span class="sxs-lookup"><span data-stu-id="45d4a-169">System.String</span></span>
<span data-ttu-id="45d4a-170">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="45d4a-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="45d4a-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45d4a-171">OUTPUTS</span></span>

### <span data-ttu-id="45d4a-172">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="45d4a-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="45d4a-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45d4a-173">NOTES</span></span>

## <span data-ttu-id="45d4a-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45d4a-174">RELATED LINKS</span></span>

[<span data-ttu-id="45d4a-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="45d4a-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
