---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263474"
---
# <span data-ttu-id="9e4f6-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9e4f6-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="9e4f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4f6-103">Uppdaterar en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="9e4f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e4f6-104">SYNTAX</span></span>

### <span data-ttu-id="9e4f6-105">SetByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="9e4f6-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="9e4f6-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9e4f6-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4f6-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="9e4f6-107">SetByParentObject</span></span>
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

### <span data-ttu-id="9e4f6-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="9e4f6-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4f6-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e4f6-109">SetByResourceId</span></span>
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

### <span data-ttu-id="9e4f6-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="9e4f6-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e4f6-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9e4f6-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="9e4f6-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="9e4f6-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e4f6-113">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e4f6-113">DESCRIPTION</span></span>
<span data-ttu-id="9e4f6-114">Cmdleten **set-AzSynapseIntegrationRuntime** uppdaterar en integrations körning med specifika parametrar.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="9e4f6-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e4f6-115">EXAMPLES</span></span>

### <span data-ttu-id="9e4f6-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e4f6-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="9e4f6-117">Cmdleten uppdaterar beskrivningen av integrations körningen "test-selfhost-IR".</span><span class="sxs-lookup"><span data-stu-id="9e4f6-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="9e4f6-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9e4f6-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="9e4f6-119">Cmdleten lägger till arbets ytan för att använda den delade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="9e4f6-120">Om du använder en `-SharedIntegrationRuntimeResourceId` parameter `-Type` måste också inkluderas.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="9e4f6-121">Observera att arbets ytan måste ges tillstånd att använda integrerings programmet innan cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="9e4f6-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e4f6-122">PARAMETERS</span></span>

### <span data-ttu-id="9e4f6-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="9e4f6-123">-AuthKey</span></span>
<span data-ttu-id="9e4f6-124">En autentiseringsnyckel för den självvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="9e4f6-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="9e4f6-126">Katalog databasens administratörs behörighet för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="9e4f6-127">-CatalogPricingTier</span></span>
<span data-ttu-id="9e4f6-128">Pris nivån i katalog databasen för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e4f6-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="9e4f6-130">Katalog databas server slut punkten för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="9e4f6-131">-DataFlowComputeType</span></span>
<span data-ttu-id="9e4f6-132">Beräknings typ för data flödes klustret som kör data flödes jobb.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="9e4f6-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="9e4f6-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="9e4f6-134">Antal kärnor i data flödes klustret som kör data flödes jobb.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="9e4f6-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="9e4f6-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="9e4f6-136">TTL-värde (Time to Live) för data flödes klustret som kör data flödes jobb.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="9e4f6-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="9e4f6-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="9e4f6-138">Namnet på den Self-Hosted-integrering som används som proxy.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="9e4f6-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="9e4f6-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="9e4f6-140">Det länkade tjänst namn för Azure Blob Storage som refererar till det lagrings data lager som ska användas när data flyttas mellan Self-Hosted och Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="9e4f6-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="9e4f6-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="9e4f6-142">Sökvägen i mellanlagringsområdet för att användas när data flyttas mellan Self-Hosted och Azure-SSIS integrerings körningar används en standard behållare om ospecificerad.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="9e4f6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4f6-143">-DefaultProfile</span></span>
<span data-ttu-id="9e4f6-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4f6-145">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="9e4f6-145">-Description</span></span>
<span data-ttu-id="9e4f6-146">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="9e4f6-147">-Utgåva</span><span class="sxs-lookup"><span data-stu-id="9e4f6-147">-Edition</span></span>
<span data-ttu-id="9e4f6-148">Integrerings versionen för SSIS som kan vara standard eller Enterprise, standard är standard om den inte anges.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="9e4f6-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="9e4f6-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="9e4f6-150">Den snabba anpassade konfigurationen för SSIS integration runtime som kan användas för att konfigurera konfigurationer och komponenter från tredje part utan anpassade installations skript.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="9e4f6-151">-Force</span><span class="sxs-lookup"><span data-stu-id="9e4f6-151">-Force</span></span>
<span data-ttu-id="9e4f6-152">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9e4f6-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e4f6-153">-InputObject</span></span>
<span data-ttu-id="9e4f6-154">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="9e4f6-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9e4f6-155">-LicenseType</span></span>
<span data-ttu-id="9e4f6-156">Den licens typ som du vill välja för SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="9e4f6-157">Det finns två typer: LicenseIncluded eller BasePrice.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="9e4f6-158">Om du är berättigad till priser för Azure Hybrid användning (AHUB) väljer du BasePrice.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="9e4f6-159">Om inte, Välj LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="9e4f6-160">-Plats</span><span class="sxs-lookup"><span data-stu-id="9e4f6-160">-Location</span></span>
<span data-ttu-id="9e4f6-161">Integrations körens beskrivning.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="9e4f6-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="9e4f6-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="9e4f6-163">Maximalt antal parallell körningar per nod för en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-164">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e4f6-164">-Name</span></span>
<span data-ttu-id="9e4f6-165">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="9e4f6-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="9e4f6-166">-NodeCount</span></span>
<span data-ttu-id="9e4f6-167">Antal målnod för integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="9e4f6-168">-NodeSize</span></span>
<span data-ttu-id="9e4f6-169">Integreringens nodadress.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="9e4f6-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="9e4f6-170">-PublicIP</span></span>
<span data-ttu-id="9e4f6-171">De statiska offentliga IP-adresserna som integreringen använder.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="9e4f6-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e4f6-172">-ResourceGroupName</span></span>
<span data-ttu-id="9e4f6-173">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-173">Resource group name.</span></span>

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

### <span data-ttu-id="9e4f6-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e4f6-174">-ResourceId</span></span>
<span data-ttu-id="9e4f6-175">Resurs-ID för Synapse.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="9e4f6-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="9e4f6-177">SAS URI för Azure Blob-behållaren som innehåller det anpassade installations skriptet.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="9e4f6-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="9e4f6-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="9e4f6-179">Resurs-ID för den delade högvärdbaserade integrerings körningen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="9e4f6-180">-Undernät</span><span class="sxs-lookup"><span data-stu-id="9e4f6-180">-Subnet</span></span>
<span data-ttu-id="9e4f6-181">Namnet på under nätet i VNet.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="9e4f6-182">– Skriv</span><span class="sxs-lookup"><span data-stu-id="9e4f6-182">-Type</span></span>
<span data-ttu-id="9e4f6-183">Integrations körnings typen.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="9e4f6-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="9e4f6-184">-VNetId</span></span>
<span data-ttu-id="9e4f6-185">ID för det VNet som integrerings körningen ska anslutas till.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="9e4f6-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9e4f6-186">-WorkspaceName</span></span>
<span data-ttu-id="9e4f6-187">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9e4f6-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9e4f6-188">-WorkspaceObject</span></span>
<span data-ttu-id="9e4f6-189">objekt för arbets yta, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9e4f6-190">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e4f6-190">-Confirm</span></span>
<span data-ttu-id="9e4f6-191">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4f6-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4f6-192">-WhatIf</span></span>
<span data-ttu-id="9e4f6-193">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e4f6-194">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4f6-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4f6-195">CommonParameters</span></span>
<span data-ttu-id="9e4f6-196">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4f6-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4f6-197">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e4f6-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4f6-198">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e4f6-198">INPUTS</span></span>

### <span data-ttu-id="9e4f6-199">Microsoft. Azure. commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9e4f6-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="9e4f6-200">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9e4f6-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9e4f6-201">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e4f6-201">OUTPUTS</span></span>

### <span data-ttu-id="9e4f6-202">Microsoft. Azure. commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="9e4f6-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="9e4f6-203">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e4f6-203">NOTES</span></span>

## <span data-ttu-id="9e4f6-204">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e4f6-204">RELATED LINKS</span></span>
