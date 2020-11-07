---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlOpCluster.md
ms.openlocfilehash: 51c8beb396bb0795fa77431a256ddc38e4e8df38
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743695"
---
# <span data-ttu-id="cd48e-101">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="cd48e-101">New-AzMlOpCluster</span></span>

## <span data-ttu-id="cd48e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd48e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd48e-103">Skapar ett nytt operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="cd48e-103">Creates a new operationalization cluster.</span></span>

## <span data-ttu-id="cd48e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd48e-104">SYNTAX</span></span>

### <span data-ttu-id="cd48e-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="cd48e-105">CreateWithInputObject</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd48e-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="cd48e-106">CreateWithParameters</span></span>
```
New-AzMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd48e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd48e-107">DESCRIPTION</span></span>
<span data-ttu-id="cd48e-108">Skapar ett nytt operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="cd48e-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="cd48e-109">Detta skapar ett kluster objekt, en behållar tjänst om det behövs, Application Insights och ett Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="cd48e-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="cd48e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd48e-110">EXAMPLES</span></span>

### <span data-ttu-id="cd48e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd48e-111">Example 1</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="cd48e-112">Skapar ett nytt operationalization-kluster med Azure Container-tjänsten och Kubernetes som Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="cd48e-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="cd48e-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cd48e-113">Example 2</span></span>
```
PS C:\> New-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="cd48e-114">Skapar ett nytt operationalization-kluster lokalt.</span><span class="sxs-lookup"><span data-stu-id="cd48e-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="cd48e-115">Detta skapar ett Azure-behållarobjekt, Application Insights och Storage-konto, men skapar inte en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="cd48e-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="cd48e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd48e-116">PARAMETERS</span></span>

### <span data-ttu-id="cd48e-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="cd48e-117">-AgentCount</span></span>
<span data-ttu-id="cd48e-118">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd48e-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="cd48e-119">-AgentVmSize</span></span>
<span data-ttu-id="cd48e-120">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd48e-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cd48e-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="cd48e-122">Den URI till Azure-behållarobjektet som ska användas i stället för att skapa en.</span><span class="sxs-lookup"><span data-stu-id="cd48e-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="cd48e-123">-ClientId</span></span>
<span data-ttu-id="cd48e-124">Huvud-ID för ACS-klustrets tjänst.</span><span class="sxs-lookup"><span data-stu-id="cd48e-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="cd48e-125">-ClusterType</span></span>
<span data-ttu-id="cd48e-126">Kluster typen operationalization.</span><span class="sxs-lookup"><span data-stu-id="cd48e-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd48e-127">-DefaultProfile</span></span>
<span data-ttu-id="cd48e-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd48e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd48e-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="cd48e-129">-Description</span></span>
<span data-ttu-id="cd48e-130">Antalet huvudnoder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd48e-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="cd48e-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="cd48e-132">Ytterligare egenskaper för den globala tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="cd48e-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="cd48e-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="cd48e-134">Konfigurationens ETag för uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="cd48e-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd48e-135">-InputObject</span></span>
<span data-ttu-id="cd48e-136">Kluster egenskaperna för operationalization.</span><span class="sxs-lookup"><span data-stu-id="cd48e-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="cd48e-137">-Location</span></span>
<span data-ttu-id="cd48e-138">Operationalization-klustrets plats.</span><span class="sxs-lookup"><span data-stu-id="cd48e-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="cd48e-139">-MasterCount</span></span>
<span data-ttu-id="cd48e-140">Antalet huvudnoder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd48e-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd48e-141">-Name</span></span>
<span data-ttu-id="cd48e-142">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd48e-142">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="cd48e-143">-OrchestratorType</span></span>
<span data-ttu-id="cd48e-144">ACS-klustrets Orchestrator-typ.</span><span class="sxs-lookup"><span data-stu-id="cd48e-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd48e-145">-ResourceGroupName</span></span>
<span data-ttu-id="cd48e-146">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="cd48e-146">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="cd48e-147">-Secret</span></span>
<span data-ttu-id="cd48e-148">Huvud hemlighet för ACS-klustrets säkerhets tjänst.</span><span class="sxs-lookup"><span data-stu-id="cd48e-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="cd48e-149">-SslCertificate</span></span>
<span data-ttu-id="cd48e-150">SSL-certifikatets data i PEM-format kodat som base64-sträng.</span><span class="sxs-lookup"><span data-stu-id="cd48e-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="cd48e-151">-SslCName</span></span>
<span data-ttu-id="cd48e-152">CName för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="cd48e-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="cd48e-153">-SslKey</span></span>
<span data-ttu-id="cd48e-154">SSL-PEM kodas som base64-sträng.</span><span class="sxs-lookup"><span data-stu-id="cd48e-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="cd48e-155">-SslStatus</span></span>
<span data-ttu-id="cd48e-156">SSL-status.</span><span class="sxs-lookup"><span data-stu-id="cd48e-156">SSL status.</span></span>
<span data-ttu-id="cd48e-157">Möjliga värden är "Enabled" och "Disabled".</span><span class="sxs-lookup"><span data-stu-id="cd48e-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd48e-158">-StorageAccount</span></span>
<span data-ttu-id="cd48e-159">Den URI till lagrings kontot som ska användas i stället för att skapa ett.</span><span class="sxs-lookup"><span data-stu-id="cd48e-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd48e-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd48e-160">-Confirm</span></span>
<span data-ttu-id="cd48e-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd48e-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd48e-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd48e-162">-WhatIf</span></span>
<span data-ttu-id="cd48e-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd48e-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd48e-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd48e-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd48e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd48e-165">CommonParameters</span></span>
<span data-ttu-id="cd48e-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd48e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd48e-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd48e-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd48e-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd48e-168">INPUTS</span></span>

### <span data-ttu-id="cd48e-169">Ingen</span><span class="sxs-lookup"><span data-stu-id="cd48e-169">None</span></span>

## <span data-ttu-id="cd48e-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd48e-170">OUTPUTS</span></span>

### <span data-ttu-id="cd48e-171">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="cd48e-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="cd48e-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd48e-172">NOTES</span></span>

## <span data-ttu-id="cd48e-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd48e-173">RELATED LINKS</span></span>
