---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: c4092d89f8b541db92737b71e534fcc1d4d917f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576933"
---
# <span data-ttu-id="d540c-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="d540c-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="d540c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d540c-102">SYNOPSIS</span></span>
<span data-ttu-id="d540c-103">Skapar ett nytt operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="d540c-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d540c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d540c-104">SYNTAX</span></span>

### <span data-ttu-id="d540c-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="d540c-105">CreateWithInputObject</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d540c-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="d540c-106">CreateWithParameters</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d540c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d540c-107">DESCRIPTION</span></span>
<span data-ttu-id="d540c-108">Skapar ett nytt operationalization-kluster.</span><span class="sxs-lookup"><span data-stu-id="d540c-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="d540c-109">Detta skapar ett kluster objekt, en behållar tjänst om det behövs, Application Insights och ett Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="d540c-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="d540c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d540c-110">EXAMPLES</span></span>

### <span data-ttu-id="d540c-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d540c-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="d540c-112">Skapar ett nytt operationalization-kluster med Azure Container-tjänsten och Kubernetes som Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="d540c-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="d540c-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d540c-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="d540c-114">Skapar ett nytt operationalization-kluster lokalt.</span><span class="sxs-lookup"><span data-stu-id="d540c-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="d540c-115">Detta skapar ett Azure-behållarobjekt, Application Insights och Storage-konto, men skapar inte en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="d540c-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="d540c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d540c-116">PARAMETERS</span></span>

### <span data-ttu-id="d540c-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="d540c-117">-AgentCount</span></span>
<span data-ttu-id="d540c-118">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="d540c-118">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="d540c-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="d540c-119">-AgentVmSize</span></span>
<span data-ttu-id="d540c-120">Antalet agent-noder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="d540c-120">The number of agent nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="d540c-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d540c-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="d540c-122">Den URI till Azure-behållarobjektet som ska användas i stället för att skapa en.</span><span class="sxs-lookup"><span data-stu-id="d540c-122">The URI to the azure container registry to use instead of creating one.</span></span>

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

### <span data-ttu-id="d540c-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="d540c-123">-ClientId</span></span>
<span data-ttu-id="d540c-124">Huvud-ID för ACS-klustrets tjänst.</span><span class="sxs-lookup"><span data-stu-id="d540c-124">The ACS cluster's orchestrator service principal id.</span></span>

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

### <span data-ttu-id="d540c-125">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d540c-125">-ClusterType</span></span>
<span data-ttu-id="d540c-126">Kluster typen operationalization.</span><span class="sxs-lookup"><span data-stu-id="d540c-126">The operationalization cluster type.</span></span>

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

### <span data-ttu-id="d540c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d540c-127">-DefaultProfile</span></span>
<span data-ttu-id="d540c-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d540c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d540c-129">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="d540c-129">-Description</span></span>
<span data-ttu-id="d540c-130">Antalet huvudnoder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="d540c-130">The number of master nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="d540c-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="d540c-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="d540c-132">Ytterligare egenskaper för den globala tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d540c-132">Additional properties for the global service configuration.</span></span>

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

### <span data-ttu-id="d540c-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="d540c-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="d540c-134">Konfigurationens ETag för uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="d540c-134">The configuration ETag for updates.</span></span>

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

### <span data-ttu-id="d540c-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d540c-135">-InputObject</span></span>
<span data-ttu-id="d540c-136">Kluster egenskaperna för operationalization.</span><span class="sxs-lookup"><span data-stu-id="d540c-136">The operationalization cluster properties.</span></span>

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

### <span data-ttu-id="d540c-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="d540c-137">-Location</span></span>
<span data-ttu-id="d540c-138">Operationalization-klustrets plats.</span><span class="sxs-lookup"><span data-stu-id="d540c-138">The operationalization cluster's location.</span></span>

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

### <span data-ttu-id="d540c-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d540c-139">-MasterCount</span></span>
<span data-ttu-id="d540c-140">Antalet huvudnoder i ACS-klustret.</span><span class="sxs-lookup"><span data-stu-id="d540c-140">The number of master nodes in the ACS cluster.</span></span>

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

### <span data-ttu-id="d540c-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="d540c-141">-Name</span></span>
<span data-ttu-id="d540c-142">Namnet på operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="d540c-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="d540c-143">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="d540c-143">-OrchestratorType</span></span>
<span data-ttu-id="d540c-144">ACS-klustrets Orchestrator-typ.</span><span class="sxs-lookup"><span data-stu-id="d540c-144">The ACS cluster's orchestrator type.</span></span>

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

### <span data-ttu-id="d540c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d540c-145">-ResourceGroupName</span></span>
<span data-ttu-id="d540c-146">Namnet på resurs gruppen för operationalization-klustret.</span><span class="sxs-lookup"><span data-stu-id="d540c-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="d540c-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="d540c-147">-Secret</span></span>
<span data-ttu-id="d540c-148">Huvud hemlighet för ACS-klustrets säkerhets tjänst.</span><span class="sxs-lookup"><span data-stu-id="d540c-148">The ACS cluster's orchestrator service principal secret.</span></span>

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

### <span data-ttu-id="d540c-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d540c-149">-SslCertificate</span></span>
<span data-ttu-id="d540c-150">SSL-certifikatets data i PEM-format kodat som base64-sträng.</span><span class="sxs-lookup"><span data-stu-id="d540c-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

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

### <span data-ttu-id="d540c-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="d540c-151">-SslCName</span></span>
<span data-ttu-id="d540c-152">CName för SSL-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="d540c-152">The CName for the SSL certificate.</span></span>

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

### <span data-ttu-id="d540c-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="d540c-153">-SslKey</span></span>
<span data-ttu-id="d540c-154">SSL-PEM kodas som base64-sträng.</span><span class="sxs-lookup"><span data-stu-id="d540c-154">The SSL key data in PEM format encoded as base64 string.</span></span>

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

### <span data-ttu-id="d540c-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="d540c-155">-SslStatus</span></span>
<span data-ttu-id="d540c-156">SSL-status.</span><span class="sxs-lookup"><span data-stu-id="d540c-156">SSL status.</span></span>
<span data-ttu-id="d540c-157">Möjliga värden är "Enabled" och "Disabled".</span><span class="sxs-lookup"><span data-stu-id="d540c-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

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

### <span data-ttu-id="d540c-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d540c-158">-StorageAccount</span></span>
<span data-ttu-id="d540c-159">Den URI till lagrings kontot som ska användas i stället för att skapa ett.</span><span class="sxs-lookup"><span data-stu-id="d540c-159">The URI to the storage account to use instead of creating one.</span></span>

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

### <span data-ttu-id="d540c-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d540c-160">-Confirm</span></span>
<span data-ttu-id="d540c-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d540c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d540c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d540c-162">-WhatIf</span></span>
<span data-ttu-id="d540c-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d540c-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d540c-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d540c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d540c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d540c-165">CommonParameters</span></span>
<span data-ttu-id="d540c-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d540c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d540c-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d540c-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d540c-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d540c-168">INPUTS</span></span>

### <span data-ttu-id="d540c-169">Ingen</span><span class="sxs-lookup"><span data-stu-id="d540c-169">None</span></span>

## <span data-ttu-id="d540c-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d540c-170">OUTPUTS</span></span>

### <span data-ttu-id="d540c-171">Microsoft. Azure. commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="d540c-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="d540c-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d540c-172">NOTES</span></span>

## <span data-ttu-id="d540c-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d540c-173">RELATED LINKS</span></span>
