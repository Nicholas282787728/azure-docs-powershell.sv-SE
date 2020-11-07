---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744692"
---
# <span data-ttu-id="4d80b-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d80b-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4d80b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d80b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d80b-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="4d80b-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="4d80b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d80b-104">SYNTAX</span></span>

### <span data-ttu-id="4d80b-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="4d80b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d80b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d80b-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d80b-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="4d80b-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d80b-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4d80b-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d80b-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4d80b-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d80b-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4d80b-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d80b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d80b-111">DESCRIPTION</span></span>
<span data-ttu-id="4d80b-112">Set-AzDataFactoryV2IntegrationRuntime cmdlet uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="4d80b-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="4d80b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d80b-113">EXAMPLES</span></span>

### <span data-ttu-id="4d80b-114">Exempel 1: Uppdatera beskrivningen av integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="4d80b-115">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="4d80b-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="4d80b-116">Exempel 2: dela självvärdbaserade integrerings körningar.</span><span class="sxs-lookup"><span data-stu-id="4d80b-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="4d80b-117">Denna cmdlet lägger till ADF för att använda den delade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="4d80b-118">Om du använder en `-SharedIntegrationRuntimeResourceId` parameter `-Type` måste också inkluderas.</span><span class="sxs-lookup"><span data-stu-id="4d80b-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="4d80b-119">Observera att data fabriken måste ges tillstånd att använda integrations körningen innan cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d80b-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="4d80b-120">Exempel 3: Konfigurera Self-Hosted IR som en proxy för Azure-SSIS IR i ADF.</span><span class="sxs-lookup"><span data-stu-id="4d80b-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="4d80b-121">Cmdleten uppdaterar Azure-SSIS integration runtime för att använda integrerings programmet för självvärdering som dataproxy.</span><span class="sxs-lookup"><span data-stu-id="4d80b-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="4d80b-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d80b-122">PARAMETERS</span></span>

### <span data-ttu-id="4d80b-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="4d80b-123">-AuthKey</span></span>
<span data-ttu-id="4d80b-124">En autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="4d80b-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="4d80b-126">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="4d80b-127">-CatalogPricingTier</span></span>
<span data-ttu-id="4d80b-128">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d80b-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="4d80b-130">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4d80b-131">-DataFactoryName</span></span>
<span data-ttu-id="4d80b-132">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="4d80b-132">The data factory name.</span></span>

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

### <span data-ttu-id="4d80b-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4d80b-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="4d80b-134">Namn på Self-Hosted integrations körning som används som proxy</span><span class="sxs-lookup"><span data-stu-id="4d80b-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="4d80b-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="4d80b-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="4d80b-136">Det länkade tjänst namn för Azure Blob Storage som refererar till det lagrings data lager som ska användas när data flyttas mellan Self-Hosted och Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="4d80b-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="4d80b-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="4d80b-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="4d80b-138">Sökvägen i lagrings data lagret som ska användas när data flyttas mellan Self-Hosted och Azure-SSIS integrerings körningar används en standard behållare om ospecificerad</span><span class="sxs-lookup"><span data-stu-id="4d80b-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="4d80b-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d80b-139">-DefaultProfile</span></span>
<span data-ttu-id="4d80b-140">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d80b-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d80b-141">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="4d80b-141">-Description</span></span>
<span data-ttu-id="4d80b-142">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="4d80b-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="4d80b-143">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="4d80b-143">-Edition</span></span>
<span data-ttu-id="4d80b-144">Integrerings versionen för SSIS som kan vara standard eller Enterprise, standard är standard om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="4d80b-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="4d80b-145">-Force</span><span class="sxs-lookup"><span data-stu-id="4d80b-145">-Force</span></span>
<span data-ttu-id="4d80b-146">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4d80b-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4d80b-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d80b-147">-InputObject</span></span>
<span data-ttu-id="4d80b-148">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="4d80b-148">The integration runtime object.</span></span>

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

### <span data-ttu-id="4d80b-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4d80b-149">-LicenseType</span></span>
<span data-ttu-id="4d80b-150">Den licens typ som du vill välja för SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="4d80b-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="4d80b-151">Det finns två typer: LicenseIncluded eller BasePrice.</span><span class="sxs-lookup"><span data-stu-id="4d80b-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="4d80b-152">Om du är berättigad till priser för Azure Hybrid användning (AHUB) väljer du BasePrice.</span><span class="sxs-lookup"><span data-stu-id="4d80b-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="4d80b-153">Om inte, Välj LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="4d80b-153">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="4d80b-154">-Plats</span><span class="sxs-lookup"><span data-stu-id="4d80b-154">-Location</span></span>
<span data-ttu-id="4d80b-155">Integrations körens plats.</span><span class="sxs-lookup"><span data-stu-id="4d80b-155">The integration runtime location.</span></span>

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

### <span data-ttu-id="4d80b-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="4d80b-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="4d80b-157">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="4d80b-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-158">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d80b-158">-Name</span></span>
<span data-ttu-id="4d80b-159">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="4d80b-159">The integration runtime name.</span></span>

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

### <span data-ttu-id="4d80b-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="4d80b-160">-NodeCount</span></span>
<span data-ttu-id="4d80b-161">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-161">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="4d80b-162">-NodeSize</span></span>
<span data-ttu-id="4d80b-163">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="4d80b-163">The integration runtime node size.</span></span>

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

### <span data-ttu-id="4d80b-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d80b-164">-ResourceGroupName</span></span>
<span data-ttu-id="4d80b-165">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4d80b-165">The resource group name.</span></span>

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

### <span data-ttu-id="4d80b-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d80b-166">-ResourceId</span></span>
<span data-ttu-id="4d80b-167">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-167">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4d80b-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="4d80b-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="4d80b-169">SAS URI för Azure Blob-behållaren som innehåller det anpassade installations skriptet.</span><span class="sxs-lookup"><span data-stu-id="4d80b-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="4d80b-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="4d80b-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="4d80b-171">Resurs-ID för den delade högvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-171">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="4d80b-172">-Undernät</span><span class="sxs-lookup"><span data-stu-id="4d80b-172">-Subnet</span></span>
<span data-ttu-id="4d80b-173">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="4d80b-173">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="4d80b-174">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4d80b-174">-Type</span></span>
<span data-ttu-id="4d80b-175">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="4d80b-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="4d80b-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="4d80b-176">-VNetId</span></span>
<span data-ttu-id="4d80b-177">ID för det VNet som integrations körningen ansluter till.</span><span class="sxs-lookup"><span data-stu-id="4d80b-177">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="4d80b-178">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d80b-178">-Confirm</span></span>
<span data-ttu-id="4d80b-179">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d80b-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d80b-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d80b-180">-WhatIf</span></span>
<span data-ttu-id="4d80b-181">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d80b-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4d80b-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d80b-182">CommonParameters</span></span>
<span data-ttu-id="4d80b-183">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d80b-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d80b-184">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d80b-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d80b-185">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d80b-185">INPUTS</span></span>

### <span data-ttu-id="4d80b-186">System. String</span><span class="sxs-lookup"><span data-stu-id="4d80b-186">System.String</span></span>

### <span data-ttu-id="4d80b-187">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d80b-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4d80b-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d80b-188">OUTPUTS</span></span>

### <span data-ttu-id="4d80b-189">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d80b-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4d80b-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d80b-190">NOTES</span></span>

## <span data-ttu-id="4d80b-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d80b-191">RELATED LINKS</span></span>

[<span data-ttu-id="4d80b-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d80b-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
