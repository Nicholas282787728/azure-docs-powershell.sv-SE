---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricService.md
ms.openlocfilehash: 930d86e457bef446d282db95d4289913bdcf10b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399195"
---
# <span data-ttu-id="e259c-101">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="e259c-101">New-AzServiceFabricService</span></span>

## <span data-ttu-id="e259c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e259c-102">SYNOPSIS</span></span>
<span data-ttu-id="e259c-103">Skapa en ny tjänst infrastruktur tjänst under det angivna programmet och klustret.</span><span class="sxs-lookup"><span data-stu-id="e259c-103">Create new service fabric service under the specified application and cluster.</span></span>

## <span data-ttu-id="e259c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e259c-104">SYNTAX</span></span>

### <span data-ttu-id="e259c-105">Stateless-Singleton (standard)</span><span class="sxs-lookup"><span data-stu-id="e259c-105">Stateless-Singleton (Default)</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeSingleton] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e259c-106">Stateless-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="e259c-106">Stateless-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeUniformInt64] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e259c-107">Stateless-Named</span><span class="sxs-lookup"><span data-stu-id="e259c-107">Stateless-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateless] -InstanceCount <Int32> [-DefaultMoveCost <MoveCostEnum>]
 [-PartitionSchemeNamed] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e259c-108">Stateful-Singleton</span><span class="sxs-lookup"><span data-stu-id="e259c-108">Stateful-Singleton</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeSingleton]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e259c-109">Stateful-UniformInt64Range</span><span class="sxs-lookup"><span data-stu-id="e259c-109">Stateful-UniformInt64Range</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeUniformInt64]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e259c-110">Stateful-Named</span><span class="sxs-lookup"><span data-stu-id="e259c-110">Stateful-Named</span></span>
```
New-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> -Type <String> [-Stateful] -TargetReplicaSetSize <Int32> -MinReplicaSetSize <Int32>
 [-ReplicaRestartWaitDuration <TimeSpan>] [-QuorumLossWaitDuration <TimeSpan>]
 [-StandByReplicaKeepDuration <TimeSpan>] [-DefaultMoveCost <MoveCostEnum>] [-PartitionSchemeNamed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e259c-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e259c-111">DESCRIPTION</span></span>
<span data-ttu-id="e259c-112">Denna cmdlet tillåter att tillstånds lösa eller tillstånds lösa tjänster skapas under det angivna programmet.</span><span class="sxs-lookup"><span data-stu-id="e259c-112">This cmdlet allows to creating  stateless or stateful services under the specified application.</span></span> <span data-ttu-id="e259c-113">Tjänsten ska avslutas i program manifestet och typen ska vara samma som i manifestet.</span><span class="sxs-lookup"><span data-stu-id="e259c-113">The service should exit in the application manifest and the type should be the same as the one in the manifest.</span></span> <span data-ttu-id="e259c-114">Program namnet bör vara ett prefix för tjänstens namn.</span><span class="sxs-lookup"><span data-stu-id="e259c-114">The application name should be a prefix of the service name.</span></span>

## <span data-ttu-id="e259c-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e259c-115">EXAMPLES</span></span>

### <span data-ttu-id="e259c-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e259c-116">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> $serviceTypeName = "testStateless"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateless -InstanceCount -1 -PartitionSchemaSingleton -Verbose
```

<span data-ttu-id="e259c-117">I det här exemplet skapas en ny autonom tjänst "testApp ~ testService1" med instans antal-1 (på alla noder).</span><span class="sxs-lookup"><span data-stu-id="e259c-117">This example will create a new stateless service "testApp~testService1" with instance count -1 (on all the nodes).</span></span>

### <span data-ttu-id="e259c-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e259c-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService2"
PS C:\> $serviceTypeName = "testStatefulType"
PS C:\> New-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName -Type $serviceTypeName -Stateful -TargetReplicaSetSize 3 MinReplicaSetSize 5
```

<span data-ttu-id="e259c-119">I det här exemplet skapas en ny tillstånds känslig tjänst "testApp ~ testService2" med ett mål på 5 noder.</span><span class="sxs-lookup"><span data-stu-id="e259c-119">This example will create a new stateful service "testApp~testService2" with a target of 5 nodes.</span></span>

## <span data-ttu-id="e259c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e259c-120">PARAMETERS</span></span>

### <span data-ttu-id="e259c-121">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="e259c-121">-ApplicationName</span></span>
<span data-ttu-id="e259c-122">Ange namnet på programmet.</span><span class="sxs-lookup"><span data-stu-id="e259c-122">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-123">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="e259c-123">-ClusterName</span></span>
<span data-ttu-id="e259c-124">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="e259c-124">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-125">-DefaultMoveCost</span><span class="sxs-lookup"><span data-stu-id="e259c-125">-DefaultMoveCost</span></span>
<span data-ttu-id="e259c-126">Ange standard kostnad för en flytt.</span><span class="sxs-lookup"><span data-stu-id="e259c-126">Specify the default cost for a move.</span></span>
<span data-ttu-id="e259c-127">Högre kostnader gör den mindre troligt att kluster resurs hanteraren flyttar repliken när de försöker utjämna klustret</span><span class="sxs-lookup"><span data-stu-id="e259c-127">Higher costs make it less likely that the Cluster Resource Manager will move the replica when trying to balance the cluster</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.MoveCostEnum
Parameter Sets: (All)
Aliases:
Accepted values: Zero, Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e259c-128">-DefaultProfile</span></span>
<span data-ttu-id="e259c-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e259c-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e259c-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="e259c-130">-InstanceCount</span></span>
<span data-ttu-id="e259c-131">Ange antal instanser för tjänsten</span><span class="sxs-lookup"><span data-stu-id="e259c-131">Specify the instance count for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-132">-MinReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="e259c-132">-MinReplicaSetSize</span></span>
<span data-ttu-id="e259c-133">Ange den minsta replik uppsättningens storlek för tjänsten</span><span class="sxs-lookup"><span data-stu-id="e259c-133">Specify the min replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="e259c-134">-Name</span></span>
<span data-ttu-id="e259c-135">Ange namnet på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e259c-135">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-136">-PartitionSchemeNamed</span><span class="sxs-lookup"><span data-stu-id="e259c-136">-PartitionSchemeNamed</span></span>
<span data-ttu-id="e259c-137">Anger att tjänsten använder det namngivna partitionsnamnet.</span><span class="sxs-lookup"><span data-stu-id="e259c-137">Indicates that the service uses the named partition scheme.</span></span>
<span data-ttu-id="e259c-138">Tjänster som använder den här modellen har vanligt vis data som kan buckets, inom en bunden mängd.</span><span class="sxs-lookup"><span data-stu-id="e259c-138">Services using this model usually have data that can be bucketed, within a bounded set.</span></span>
<span data-ttu-id="e259c-139">Vissa vanliga exempel på data fält som används som namngivna partitionstyper är regioner, post nummer, kund grupper eller andra affärs gränser.</span><span class="sxs-lookup"><span data-stu-id="e259c-139">Some common examples of data fields used as named partition keys would be regions, postal codes, customer groups, or other business boundaries.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Named, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-140">-PartitionSchemeSingleton</span><span class="sxs-lookup"><span data-stu-id="e259c-140">-PartitionSchemeSingleton</span></span>
<span data-ttu-id="e259c-141">Anger att tjänsten använder ett singleton-partitionsschema.</span><span class="sxs-lookup"><span data-stu-id="e259c-141">Indicates that the service uses the singleton partition scheme.</span></span>
<span data-ttu-id="e259c-142">Singleton-partitioner används vanligt vis när tjänsten inte kräver ytterligare routning.</span><span class="sxs-lookup"><span data-stu-id="e259c-142">Singleton partitions are typically used when the service does not require any additional routing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateful-Singleton
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-143">-PartitionSchemeUniformInt64</span><span class="sxs-lookup"><span data-stu-id="e259c-143">-PartitionSchemeUniformInt64</span></span>
<span data-ttu-id="e259c-144">Anger att tjänsten använder UniformInt64.</span><span class="sxs-lookup"><span data-stu-id="e259c-144">Indicates that the service uses the UniformInt64 partition scheme.</span></span>
<span data-ttu-id="e259c-145">Det innebär att varje partition äger ett utbud av Int64-nycklar.</span><span class="sxs-lookup"><span data-stu-id="e259c-145">This means that each partition owns a range of int64 keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-UniformInt64Range, Stateful-UniformInt64Range
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-146">-QuorumLossWaitDuration</span><span class="sxs-lookup"><span data-stu-id="e259c-146">-QuorumLossWaitDuration</span></span>
<span data-ttu-id="e259c-147">Ange tids längd för arbets förlusten för tjänsten</span><span class="sxs-lookup"><span data-stu-id="e259c-147">Specify the quorum loss wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-148">-ReplicaRestartWaitDuration</span><span class="sxs-lookup"><span data-stu-id="e259c-148">-ReplicaRestartWaitDuration</span></span>
<span data-ttu-id="e259c-149">Ange tids längd för replikeringens väntan</span><span class="sxs-lookup"><span data-stu-id="e259c-149">Specify the replica restart wait duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e259c-150">-ResourceGroupName</span></span>
<span data-ttu-id="e259c-151">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e259c-151">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-152">-StandByReplicaKeepDuration</span><span class="sxs-lookup"><span data-stu-id="e259c-152">-StandByReplicaKeepDuration</span></span>
<span data-ttu-id="e259c-153">Ange längden av replikernas varaktighet för tjänsten</span><span class="sxs-lookup"><span data-stu-id="e259c-153">Specify the stand by replica duration for the service</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-154">-Stateful</span><span class="sxs-lookup"><span data-stu-id="e259c-154">-Stateful</span></span>
<span data-ttu-id="e259c-155">Användning för tillstånds känslig tjänst</span><span class="sxs-lookup"><span data-stu-id="e259c-155">Use for stateful service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-156">-State-löst</span><span class="sxs-lookup"><span data-stu-id="e259c-156">-Stateless</span></span>
<span data-ttu-id="e259c-157">Användning för autonom tjänst</span><span class="sxs-lookup"><span data-stu-id="e259c-157">Use for stateless service</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Stateless-Singleton, Stateless-UniformInt64Range, Stateless-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-158">-TargetReplicaSetSize</span><span class="sxs-lookup"><span data-stu-id="e259c-158">-TargetReplicaSetSize</span></span>
<span data-ttu-id="e259c-159">Ange mål replik uppsättningens storlek för tjänsten</span><span class="sxs-lookup"><span data-stu-id="e259c-159">Specify the target replica set size for the service</span></span>

```yaml
Type: System.Int32
Parameter Sets: Stateful-Singleton, Stateful-UniformInt64Range, Stateful-Named
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-160">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e259c-160">-Type</span></span>
<span data-ttu-id="e259c-161">Ange namnet på tjänst typen för programmet, ska finnas i applikations manifestet.</span><span class="sxs-lookup"><span data-stu-id="e259c-161">Specify the service type name of the application, should exist in the application manifest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e259c-162">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e259c-162">-Confirm</span></span>
<span data-ttu-id="e259c-163">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e259c-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e259c-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e259c-164">-WhatIf</span></span>
<span data-ttu-id="e259c-165">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e259c-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e259c-166">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e259c-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e259c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e259c-167">CommonParameters</span></span>
<span data-ttu-id="e259c-168">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e259c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e259c-169">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e259c-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e259c-170">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e259c-170">INPUTS</span></span>

### <span data-ttu-id="e259c-171">System. String</span><span class="sxs-lookup"><span data-stu-id="e259c-171">System.String</span></span>

## <span data-ttu-id="e259c-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e259c-172">OUTPUTS</span></span>

### <span data-ttu-id="e259c-173">Microsoft. Azure. commands. ServiceFabric. Models. PSService</span><span class="sxs-lookup"><span data-stu-id="e259c-173">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="e259c-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e259c-174">NOTES</span></span>

## <span data-ttu-id="e259c-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e259c-175">RELATED LINKS</span></span>
