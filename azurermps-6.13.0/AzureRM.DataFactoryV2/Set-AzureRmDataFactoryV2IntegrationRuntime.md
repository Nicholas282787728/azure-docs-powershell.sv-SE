---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aae3b830a55b5a2a7683aa1608d15eb4a49a49fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585020"
---
# <span data-ttu-id="610d8-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="610d8-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="610d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="610d8-102">SYNOPSIS</span></span>
<span data-ttu-id="610d8-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="610d8-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="610d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="610d8-104">SYNTAX</span></span>

### <span data-ttu-id="610d8-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="610d8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610d8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="610d8-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610d8-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="610d8-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610d8-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="610d8-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610d8-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="610d8-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="610d8-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="610d8-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="610d8-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="610d8-111">DESCRIPTION</span></span>
<span data-ttu-id="610d8-112">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="610d8-112">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="610d8-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="610d8-113">EXAMPLES</span></span>

### <span data-ttu-id="610d8-114">Exempel 1: Uppdatera beskrivningen av integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="610d8-115">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="610d8-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="610d8-116">Exempel 2: dela självvärdbaserade integrerings körningar.</span><span class="sxs-lookup"><span data-stu-id="610d8-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="610d8-117">Denna cmdlet lägger till ADF för att använda den delade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="610d8-118">Om du använder en `-SharedIntegrationRuntimeResourceId` parameter `-Type` måste också inkluderas.</span><span class="sxs-lookup"><span data-stu-id="610d8-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="610d8-119">Observera att data fabriken måste ges tillstånd att använda integrations körningen innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="610d8-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="610d8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="610d8-120">PARAMETERS</span></span>

### <span data-ttu-id="610d8-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="610d8-121">-AuthKey</span></span>
<span data-ttu-id="610d8-122">En autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-122">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="610d8-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="610d8-124">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-124">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="610d8-125">-CatalogPricingTier</span></span>
<span data-ttu-id="610d8-126">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-126">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="610d8-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="610d8-128">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-128">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="610d8-129">-DataFactoryName</span></span>
<span data-ttu-id="610d8-130">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="610d8-130">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="610d8-131">-DefaultProfile</span></span>
<span data-ttu-id="610d8-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="610d8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="610d8-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="610d8-133">-Description</span></span>
<span data-ttu-id="610d8-134">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="610d8-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="610d8-135">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="610d8-135">-Edition</span></span>
<span data-ttu-id="610d8-136">Integrerings versionen för SSIS som kan vara standard eller Enterprise, standard är standard om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="610d8-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-137">-Force</span><span class="sxs-lookup"><span data-stu-id="610d8-137">-Force</span></span>
<span data-ttu-id="610d8-138">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="610d8-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="610d8-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="610d8-139">-InputObject</span></span>
<span data-ttu-id="610d8-140">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="610d8-140">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="610d8-141">-LicenseType</span></span>
<span data-ttu-id="610d8-142">Den licens typ som du vill välja för SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="610d8-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="610d8-143">Det finns två typer: LicenseIncluded eller BasePrice.</span><span class="sxs-lookup"><span data-stu-id="610d8-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="610d8-144">Om du är berättigad till priser för Azure Hybrid användning (AHUB) väljer du BasePrice.</span><span class="sxs-lookup"><span data-stu-id="610d8-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="610d8-145">Om inte, Välj LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="610d8-145">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="610d8-146">-Location</span></span>
<span data-ttu-id="610d8-147">Integrations körens plats.</span><span class="sxs-lookup"><span data-stu-id="610d8-147">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="610d8-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="610d8-149">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="610d8-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="610d8-150">-Name</span></span>
<span data-ttu-id="610d8-151">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="610d8-151">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="610d8-152">-NodeCount</span></span>
<span data-ttu-id="610d8-153">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-153">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="610d8-154">-NodeSize</span></span>
<span data-ttu-id="610d8-155">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="610d8-155">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="610d8-156">-ResourceGroupName</span></span>
<span data-ttu-id="610d8-157">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="610d8-157">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="610d8-158">-ResourceId</span></span>
<span data-ttu-id="610d8-159">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="610d8-159">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="610d8-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="610d8-161">SAS URI för Azure Blob-behållaren som innehåller det anpassade installations skriptet.</span><span class="sxs-lookup"><span data-stu-id="610d8-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="610d8-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="610d8-163">Resurs-ID för den delade högvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="610d8-163">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-164">-Undernät</span><span class="sxs-lookup"><span data-stu-id="610d8-164">-Subnet</span></span>
<span data-ttu-id="610d8-165">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="610d8-165">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-166">– Skriv</span><span class="sxs-lookup"><span data-stu-id="610d8-166">-Type</span></span>
<span data-ttu-id="610d8-167">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="610d8-167">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="610d8-168">-VNetId</span></span>
<span data-ttu-id="610d8-169">ID för det VNet som integrations körningen ansluter till.</span><span class="sxs-lookup"><span data-stu-id="610d8-169">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="610d8-170">-Confirm</span></span>
<span data-ttu-id="610d8-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="610d8-171">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="610d8-172">-WhatIf</span></span>
<span data-ttu-id="610d8-173">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="610d8-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="610d8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="610d8-174">CommonParameters</span></span>
<span data-ttu-id="610d8-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="610d8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="610d8-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="610d8-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="610d8-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="610d8-177">INPUTS</span></span>

### <span data-ttu-id="610d8-178">System. String</span><span class="sxs-lookup"><span data-stu-id="610d8-178">System.String</span></span>

### <span data-ttu-id="610d8-179">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="610d8-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="610d8-180">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="610d8-180">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="610d8-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="610d8-181">OUTPUTS</span></span>

### <span data-ttu-id="610d8-182">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="610d8-182">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="610d8-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="610d8-183">NOTES</span></span>

## <span data-ttu-id="610d8-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="610d8-184">RELATED LINKS</span></span>

[<span data-ttu-id="610d8-185">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="610d8-185">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
