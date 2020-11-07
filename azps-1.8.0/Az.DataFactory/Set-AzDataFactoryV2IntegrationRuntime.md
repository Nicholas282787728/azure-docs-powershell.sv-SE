---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917030"
---
# <span data-ttu-id="1c9b4-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c9b4-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1c9b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1c9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9b4-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="1c9b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1c9b4-104">SYNTAX</span></span>

### <span data-ttu-id="1c9b4-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="1c9b4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c9b4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9b4-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c9b4-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9b4-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c9b4-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1c9b4-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c9b4-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1c9b4-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c9b4-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1c9b4-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9b4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1c9b4-111">DESCRIPTION</span></span>
<span data-ttu-id="1c9b4-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="1c9b4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1c9b4-113">EXAMPLES</span></span>

### <span data-ttu-id="1c9b4-114">Exempel 1: Uppdatera beskrivningen av integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="1c9b4-115">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="1c9b4-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="1c9b4-116">Exempel 2: dela självvärdbaserade integrerings körningar.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="1c9b4-117">Denna cmdlet lägger till ADF för att använda den delade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="1c9b4-118">Om du använder en `-SharedIntegrationRuntimeResourceId` parameter `-Type` måste också inkluderas.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="1c9b4-119">Observera att data fabriken måste ges tillstånd att använda integrations körningen innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="1c9b4-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1c9b4-120">PARAMETERS</span></span>

### <span data-ttu-id="1c9b4-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="1c9b4-121">-AuthKey</span></span>
<span data-ttu-id="1c9b4-122">En autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="1c9b4-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="1c9b4-124">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="1c9b4-125">-CatalogPricingTier</span></span>
<span data-ttu-id="1c9b4-126">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1c9b4-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="1c9b4-128">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1c9b4-129">-DataFactoryName</span></span>
<span data-ttu-id="1c9b4-130">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-130">The data factory name.</span></span>

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

### <span data-ttu-id="1c9b4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9b4-131">-DefaultProfile</span></span>
<span data-ttu-id="1c9b4-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c9b4-133">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1c9b4-133">-Description</span></span>
<span data-ttu-id="1c9b4-134">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="1c9b4-135">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="1c9b4-135">-Edition</span></span>
<span data-ttu-id="1c9b4-136">Integrerings versionen för SSIS som kan vara standard eller Enterprise, standard är standard om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="1c9b4-137">-Force</span><span class="sxs-lookup"><span data-stu-id="1c9b4-137">-Force</span></span>
<span data-ttu-id="1c9b4-138">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1c9b4-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c9b4-139">-InputObject</span></span>
<span data-ttu-id="1c9b4-140">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="1c9b4-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1c9b4-141">-LicenseType</span></span>
<span data-ttu-id="1c9b4-142">Den licens typ som du vill välja för SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="1c9b4-143">Det finns två typer: LicenseIncluded eller BasePrice.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="1c9b4-144">Om du är berättigad till priser för Azure Hybrid användning (AHUB) väljer du BasePrice.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="1c9b4-145">Om inte, Välj LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="1c9b4-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="1c9b4-146">-Location</span></span>
<span data-ttu-id="1c9b4-147">Integrations körens plats.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="1c9b4-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="1c9b4-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="1c9b4-149">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="1c9b4-150">-Name</span></span>
<span data-ttu-id="1c9b4-151">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="1c9b4-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="1c9b4-152">-NodeCount</span></span>
<span data-ttu-id="1c9b4-153">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="1c9b4-154">-NodeSize</span></span>
<span data-ttu-id="1c9b4-155">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="1c9b4-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9b4-156">-ResourceGroupName</span></span>
<span data-ttu-id="1c9b4-157">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-157">The resource group name.</span></span>

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

### <span data-ttu-id="1c9b4-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9b4-158">-ResourceId</span></span>
<span data-ttu-id="1c9b4-159">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1c9b4-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="1c9b4-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="1c9b4-161">SAS URI för Azure Blob-behållaren som innehåller det anpassade installations skriptet.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="1c9b4-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="1c9b4-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="1c9b4-163">Resurs-ID för den delade högvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="1c9b4-164">-Undernät</span><span class="sxs-lookup"><span data-stu-id="1c9b4-164">-Subnet</span></span>
<span data-ttu-id="1c9b4-165">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="1c9b4-166">– Skriv</span><span class="sxs-lookup"><span data-stu-id="1c9b4-166">-Type</span></span>
<span data-ttu-id="1c9b4-167">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="1c9b4-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="1c9b4-168">-VNetId</span></span>
<span data-ttu-id="1c9b4-169">ID för det VNet som integrations körningen ansluter till.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="1c9b4-170">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1c9b4-170">-Confirm</span></span>
<span data-ttu-id="1c9b4-171">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9b4-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9b4-172">-WhatIf</span></span>
<span data-ttu-id="1c9b4-173">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1c9b4-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9b4-174">CommonParameters</span></span>
<span data-ttu-id="1c9b4-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c9b4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9b4-176">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c9b4-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9b4-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1c9b4-177">INPUTS</span></span>

### <span data-ttu-id="1c9b4-178">System. String</span><span class="sxs-lookup"><span data-stu-id="1c9b4-178">System.String</span></span>

### <span data-ttu-id="1c9b4-179">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c9b4-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1c9b4-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1c9b4-180">OUTPUTS</span></span>

### <span data-ttu-id="1c9b4-181">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c9b4-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1c9b4-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1c9b4-182">NOTES</span></span>

## <span data-ttu-id="1c9b4-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1c9b4-183">RELATED LINKS</span></span>

[<span data-ttu-id="1c9b4-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1c9b4-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
