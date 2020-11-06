---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581408"
---
# <span data-ttu-id="68ea1-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="68ea1-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="68ea1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="68ea1-103">Skapar ett nytt operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="68ea1-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68ea1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68ea1-104">SYNTAX</span></span>

### <span data-ttu-id="68ea1-105">Skapa ett nytt operationalization-kluster från en OperationalizationCluster-instans.</span><span class="sxs-lookup"><span data-stu-id="68ea1-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="68ea1-106">Skapa ett nytt operationalization-kluster från indataparametrar för cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68ea1-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="68ea1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68ea1-107">DESCRIPTION</span></span>
<span data-ttu-id="68ea1-108">Skapar ett nytt operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="68ea1-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="68ea1-109">Detta skapar ett kluster objekt, en behållar tjänst om det behövs, Application Insights och ett Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="68ea1-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="68ea1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68ea1-110">EXAMPLES</span></span>

### <span data-ttu-id="68ea1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="68ea1-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="68ea1-112">Skapar ett nytt operationalization-kluster med Azure Container-tjänsten och Kubernetes som Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="68ea1-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="68ea1-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="68ea1-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="68ea1-114">Skapar ett nytt operationalization-kluster lokalt.</span><span class="sxs-lookup"><span data-stu-id="68ea1-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="68ea1-115">Detta skapar ett Azure-behållarobjekt, Application Insights och Storage-konto, men skapar inte en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="68ea1-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="68ea1-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68ea1-116">PARAMETERS</span></span>

### <span data-ttu-id="68ea1-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="68ea1-117">-AgentCount</span></span>
<span data-ttu-id="68ea1-118">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="68ea1-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="68ea1-119">-AgentVmSize</span></span>
<span data-ttu-id="68ea1-120">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="68ea1-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="68ea1-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="68ea1-122">Den URI till Azure-behållarobjektet som ska användas i stället för att skapa en.</span><span class="sxs-lookup"><span data-stu-id="68ea1-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68ea1-123">-InputObject</span></span>
<span data-ttu-id="68ea1-124">Kluster egenskaperna för operationalization.</span><span class="sxs-lookup"><span data-stu-id="68ea1-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="68ea1-125">-ClusterType</span></span>
<span data-ttu-id="68ea1-126">Kluster typen operationalization.</span><span class="sxs-lookup"><span data-stu-id="68ea1-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68ea1-127">-Confirm</span></span>
<span data-ttu-id="68ea1-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68ea1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ea1-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="68ea1-129">-Description</span></span>
<span data-ttu-id="68ea1-130">Antalet huvudnoder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="68ea1-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="68ea1-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="68ea1-132">Ytterligare egenskaper för den globala tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="68ea1-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="68ea1-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="68ea1-134">Konfigurationens ETag för uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="68ea1-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="68ea1-135">-Location</span></span>
<span data-ttu-id="68ea1-136">Operationalization-klustrets plats.</span><span class="sxs-lookup"><span data-stu-id="68ea1-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="68ea1-137">-MasterCount</span></span>
<span data-ttu-id="68ea1-138">Antalet huvudnoder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="68ea1-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="68ea1-139">-Name</span></span>
<span data-ttu-id="68ea1-140">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="68ea1-140">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-141">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="68ea1-141">-OrchestratorType</span></span>
<span data-ttu-id="68ea1-142">ACS-klustrets Orchestrator-typ.</span><span class="sxs-lookup"><span data-stu-id="68ea1-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ea1-143">-ResourceGroupName</span></span>
<span data-ttu-id="68ea1-144">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="68ea1-144">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="68ea1-145">-ClientId</span></span>
<span data-ttu-id="68ea1-146">Huvud-ID för ACS-klustrets tjänst.</span><span class="sxs-lookup"><span data-stu-id="68ea1-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="68ea1-147">-Secret</span></span>
<span data-ttu-id="68ea1-148">Huvud hemlighet för ACS-klustrets säkerhets tjänst.</span><span class="sxs-lookup"><span data-stu-id="68ea1-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="68ea1-149">-SslCName</span></span>
<span data-ttu-id="68ea1-150">CName för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="68ea1-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="68ea1-151">-SslCertificate</span></span>
<span data-ttu-id="68ea1-152">SSL-certifikatets data i PEM-format kodat som base64-sträng.</span><span class="sxs-lookup"><span data-stu-id="68ea1-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="68ea1-153">-SslKey</span></span>
<span data-ttu-id="68ea1-154">SSL-PEM kodas som base64-sträng.</span><span class="sxs-lookup"><span data-stu-id="68ea1-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="68ea1-155">-SslStatus</span></span>
<span data-ttu-id="68ea1-156">SSL-status.</span><span class="sxs-lookup"><span data-stu-id="68ea1-156">SSL status.</span></span>
<span data-ttu-id="68ea1-157">Möjliga värden är "Enabled" och "Disabled".</span><span class="sxs-lookup"><span data-stu-id="68ea1-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="68ea1-158">-StorageAccount</span></span>
<span data-ttu-id="68ea1-159">Den URI till lagrings kontot som ska användas i stället för att skapa ett.</span><span class="sxs-lookup"><span data-stu-id="68ea1-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ea1-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ea1-160">-WhatIf</span></span>
<span data-ttu-id="68ea1-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68ea1-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ea1-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68ea1-162">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="68ea1-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68ea1-163">INPUTS</span></span>

### <span data-ttu-id="68ea1-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="68ea1-164">None</span></span>


## <span data-ttu-id="68ea1-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68ea1-165">OUTPUTS</span></span>

### <span data-ttu-id="68ea1-166">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="68ea1-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="68ea1-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68ea1-167">NOTES</span></span>

## <span data-ttu-id="68ea1-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68ea1-168">RELATED LINKS</span></span>

