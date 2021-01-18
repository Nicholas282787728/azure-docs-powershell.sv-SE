---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523907"
---
# <span data-ttu-id="d281c-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d281c-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="d281c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d281c-102">SYNOPSIS</span></span>
<span data-ttu-id="d281c-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="d281c-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="d281c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d281c-104">SYNTAX</span></span>

### <span data-ttu-id="d281c-105">SetByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="d281c-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d281c-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="d281c-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="d281c-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d281c-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="d281c-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d281c-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d281c-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d281c-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d281c-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d281c-113">DESCRIPTION</span></span>
<span data-ttu-id="d281c-114">Cmdleten **set-AzSynapseIntegrationRuntime** uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="d281c-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="d281c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d281c-115">EXAMPLES</span></span>

### <span data-ttu-id="d281c-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d281c-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="d281c-117">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="d281c-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="d281c-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d281c-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="d281c-119">Cmdleten lägger till arbets ytan för att använda den delade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="d281c-120">Om du använder en `-SharedIntegrationRuntimeResourceId` parameter `-Type` måste också inkluderas.</span><span class="sxs-lookup"><span data-stu-id="d281c-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="d281c-121">Observera att arbets ytan måste ges tillstånd att använda integrerings programmet innan cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="d281c-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="d281c-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d281c-122">PARAMETERS</span></span>

### <span data-ttu-id="d281c-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="d281c-123">-AuthKey</span></span>
<span data-ttu-id="d281c-124">En autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="d281c-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="d281c-126">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="d281c-127">-CatalogPricingTier</span></span>
<span data-ttu-id="d281c-128">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d281c-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="d281c-130">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="d281c-131">-DataFlowComputeType</span></span>
<span data-ttu-id="d281c-132">Beräknings typ för data flödes klustret som kör data flödes jobb.</span><span class="sxs-lookup"><span data-stu-id="d281c-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="d281c-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="d281c-134">Antal kärnor i data flödes klustret som kör data flödes jobb.</span><span class="sxs-lookup"><span data-stu-id="d281c-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d281c-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="d281c-136">TTL-värde (Time to Live) för data flödes klustret som kör data flödes jobb.</span><span class="sxs-lookup"><span data-stu-id="d281c-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d281c-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="d281c-138">Namnet på den Self-Hosted-integrering som används som proxy.</span><span class="sxs-lookup"><span data-stu-id="d281c-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="d281c-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="d281c-140">Det länkade tjänst namn för Azure Blob Storage som refererar till det lagrings data lager som ska användas när data flyttas mellan Self-Hosted och Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="d281c-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="d281c-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="d281c-142">Sökvägen i mellanlagringsområdet för att användas när data flyttas mellan Self-Hosted och Azure-SSIS integrerings körningar används en standard behållare om ospecificerad.</span><span class="sxs-lookup"><span data-stu-id="d281c-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d281c-143">-DefaultProfile</span></span>
<span data-ttu-id="d281c-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d281c-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d281c-145">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d281c-145">-Description</span></span>
<span data-ttu-id="d281c-146">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="d281c-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="d281c-147">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="d281c-147">-Edition</span></span>
<span data-ttu-id="d281c-148">Integrerings versionen för SSIS som kan vara standard eller Enterprise, standard är standard om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="d281c-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="d281c-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="d281c-150">Den snabba anpassade konfigurationen för SSIS integration runtime som kan användas för att konfigurera konfigurationer och komponenter från tredje part utan anpassade installations skript.</span><span class="sxs-lookup"><span data-stu-id="d281c-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-151">-Force</span><span class="sxs-lookup"><span data-stu-id="d281c-151">-Force</span></span>
<span data-ttu-id="d281c-152">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d281c-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d281c-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d281c-153">-InputObject</span></span>
<span data-ttu-id="d281c-154">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="d281c-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d281c-155">-LicenseType</span></span>
<span data-ttu-id="d281c-156">Den licens typ som du vill välja för SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="d281c-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="d281c-157">Det finns två typer: LicenseIncluded eller BasePrice.</span><span class="sxs-lookup"><span data-stu-id="d281c-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="d281c-158">Om du är berättigad till priser för Azure Hybrid användning (AHUB) väljer du BasePrice.</span><span class="sxs-lookup"><span data-stu-id="d281c-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="d281c-159">Om inte, Välj LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="d281c-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-160">-Plats</span><span class="sxs-lookup"><span data-stu-id="d281c-160">-Location</span></span>
<span data-ttu-id="d281c-161">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="d281c-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="d281c-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="d281c-163">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="d281c-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-164">-Namn</span><span class="sxs-lookup"><span data-stu-id="d281c-164">-Name</span></span>
<span data-ttu-id="d281c-165">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="d281c-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d281c-166">-NodeCount</span></span>
<span data-ttu-id="d281c-167">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="d281c-168">-NodeSize</span></span>
<span data-ttu-id="d281c-169">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="d281c-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="d281c-170">-PublicIP</span></span>
<span data-ttu-id="d281c-171">De statiska offentliga IP-adresserna som integreringen använder.</span><span class="sxs-lookup"><span data-stu-id="d281c-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d281c-172">-ResourceGroupName</span></span>
<span data-ttu-id="d281c-173">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d281c-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d281c-174">-ResourceId</span></span>
<span data-ttu-id="d281c-175">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="d281c-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="d281c-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="d281c-177">SAS URI för Azure Blob-behållaren som innehåller det anpassade installations skriptet.</span><span class="sxs-lookup"><span data-stu-id="d281c-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="d281c-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="d281c-179">Resurs-ID för den delade högvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="d281c-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-180">-Undernät</span><span class="sxs-lookup"><span data-stu-id="d281c-180">-Subnet</span></span>
<span data-ttu-id="d281c-181">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="d281c-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-182">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d281c-182">-Type</span></span>
<span data-ttu-id="d281c-183">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="d281c-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="d281c-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="d281c-184">-VNetId</span></span>
<span data-ttu-id="d281c-185">ID för det VNet som integrerings körningen ska anslutas till.</span><span class="sxs-lookup"><span data-stu-id="d281c-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d281c-186">-WorkspaceName</span></span>
<span data-ttu-id="d281c-187">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="d281c-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d281c-188">-WorkspaceObject</span></span>
<span data-ttu-id="d281c-189">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="d281c-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d281c-190">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d281c-190">-Confirm</span></span>
<span data-ttu-id="d281c-191">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d281c-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d281c-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d281c-192">-WhatIf</span></span>
<span data-ttu-id="d281c-193">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d281c-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d281c-194">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d281c-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d281c-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d281c-195">CommonParameters</span></span>
<span data-ttu-id="d281c-196">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d281c-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d281c-197">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d281c-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d281c-198">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d281c-198">INPUTS</span></span>

### <span data-ttu-id="d281c-199">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d281c-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d281c-200">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d281c-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d281c-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d281c-201">OUTPUTS</span></span>

### <span data-ttu-id="d281c-202">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d281c-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d281c-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d281c-203">NOTES</span></span>

## <span data-ttu-id="d281c-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d281c-204">RELATED LINKS</span></span>
