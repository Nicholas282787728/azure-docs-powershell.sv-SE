---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e53ed405c9a03e7a9ec7a7c3694a44d513a1a1ea
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525383"
---
# <span data-ttu-id="3d9ba-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="3d9ba-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="3d9ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3d9ba-103">Uppdatera ett tjänst Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-103">Update a service fabric application.</span></span> <span data-ttu-id="3d9ba-104">Då kan du uppdatera program parametrarna och/eller uppgradera program typs versionen som utlöser en program uppgradering.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span> <span data-ttu-id="3d9ba-105">Stöder endast program som distribueras av armar.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="3d9ba-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d9ba-106">SYNTAX</span></span>

### <span data-ttu-id="3d9ba-107">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="3d9ba-107">ByResourceGroup (Default)</span></span>
```
Update-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-ForceRestart] [-UpgradeReplicaSetCheckTimeoutSec <Int32>]
 [-FailureAction <FailureAction>] [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d9ba-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d9ba-108">ByResourceId</span></span>
```
Update-AzServiceFabricApplication [[-ApplicationTypeVersion] <String>] [-ApplicationParameter <Hashtable>]
 [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-ForceRestart]
 [-UpgradeReplicaSetCheckTimeoutSec <Int32>] [-FailureAction <FailureAction>]
 [-HealthCheckRetryTimeoutSec <Int32>] [-HealthCheckWaitDurationSec <Int32>]
 [-HealthCheckStableDurationSec <Int32>] [-UpgradeDomainTimeoutSec <Int32>] [-UpgradeTimeoutSec <Int32>]
 [-ConsiderWarningAsError] [-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService <Int32>]
 [-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition <Int32>]
 [-DefaultServiceTypeUnhealthyServicesMaxPercent <Int32>] [-UnhealthyDeployedApplicationsMaxPercent <Int32>]
 [-ServiceTypeHealthPolicyMap <Hashtable>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d9ba-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d9ba-109">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d9ba-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d9ba-110">DESCRIPTION</span></span>
<span data-ttu-id="3d9ba-111">Denna cmdlet kan användas för att uppdatera program parametrar och uppgradera program typs versionen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-111">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="3d9ba-112">Uppdatering av parametern ändrar bara modellen på ARM-sidan, bara när en ny typ version används, utlöses en program uppgradering.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-112">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="3d9ba-113">Den angivna typen version ska redan vara skapad i klustret med **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-113">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="3d9ba-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d9ba-114">EXAMPLES</span></span>

### <span data-ttu-id="3d9ba-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3d9ba-115">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="3d9ba-116">I det här exemplet startas en program uppgradering för att uppdatera typ versionen till "v2" som skapades med **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-116">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="3d9ba-117">De program parametrar som används ska vara definierade i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-117">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="3d9ba-118">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="3d9ba-118">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="3d9ba-119">I det här exemplet uppdateras begränsningen för lägsta och högsta antal noder för programmet.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-119">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="3d9ba-120">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="3d9ba-120">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="3d9ba-121">I det här exemplet startas en program uppgradering för att uppdatera typ versionen till "v2" och dessutom anges vissa uppgraderings princip parametrar som kommer att gälla från den aktuella uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-121">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="3d9ba-122">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="3d9ba-122">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="3d9ba-123">I det här exemplet uppdateras program parametrarna men ändringarna börjar gälla tills nästa version uppgraderas till programmet.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-123">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="3d9ba-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d9ba-124">PARAMETERS</span></span>

### <span data-ttu-id="3d9ba-125">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="3d9ba-125">-ApplicationParameter</span></span>
<span data-ttu-id="3d9ba-126">Ange program parametrar som nycklar/värde par.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-126">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="3d9ba-127">Dessa parametrar måste finnas i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-127">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-128">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="3d9ba-128">-ApplicationTypeVersion</span></span>
<span data-ttu-id="3d9ba-129">Ange program typ version</span><span class="sxs-lookup"><span data-stu-id="3d9ba-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-130">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="3d9ba-130">-ClusterName</span></span>
<span data-ttu-id="3d9ba-131">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-131">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-132">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="3d9ba-132">-ConsiderWarningAsError</span></span>
<span data-ttu-id="3d9ba-133">Anger om en varnings händelse ska behandlas som en fel händelse under en hälso utvärdering.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-133">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d9ba-134">-DefaultProfile</span></span>
<span data-ttu-id="3d9ba-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d9ba-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="3d9ba-136">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="3d9ba-137">Anger maximalt antal unhelthy-partitioner per tjänst som tillåts av hälso policyn för den standard tjänst typ som ska användas för den övervakade uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-137">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="3d9ba-138">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="3d9ba-139">Anger det maximala antalet unhelthy-repliker per tjänst som tillåts av hälso policyn för den standard tjänst typ som ska användas för den övervakade uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-139">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="3d9ba-140">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="3d9ba-141">Anger den maximala procent andelen unhelthy tjänster som tillåts av hälso policyn för den standard tjänst typ som ska användas för den övervakade uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-141">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-142">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="3d9ba-142">-FailureAction</span></span>
<span data-ttu-id="3d9ba-143">Anger vilken åtgärd som ska vidtas om den övervakade uppgraderingen Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-143">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="3d9ba-144">De acceptabla värdena för den här parametern är rollback eller manual.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-144">The acceptable values for this parameter are Rollback or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.FailureAction
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:
Accepted values: Rollback, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-145">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="3d9ba-145">-ForceRestart</span></span>
<span data-ttu-id="3d9ba-146">Anger att tjänst värden startas om även om uppgraderingen är en konfigurations ändring.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-146">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-147">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3d9ba-147">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="3d9ba-148">Anger hur länge (i sekunder) som tjänst Fabric försöker kontrol lera hälso kontrollen om den föregående hälso kontrollen Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-148">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-149">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="3d9ba-149">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="3d9ba-150">Anger hur länge tjänsten Fabric väntar för att kontrol lera att programmet är stabilt innan det flyttas till nästa uppgraderings domän eller att slutföra uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-150">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="3d9ba-151">Denna vänte tid hindrar obehöriga ändringar av hälso tillstånd direkt efter att hälso kontrollen har utförts.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-151">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-152">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="3d9ba-152">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="3d9ba-153">Anger hur länge tjänsten Fabric ska vänta innan den första hälso kontrollen utförs när uppgraderingen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-153">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d9ba-154">-InputObject</span></span>
<span data-ttu-id="3d9ba-155">Program resursen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-155">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-156">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="3d9ba-156">-MaximumNodeCount</span></span>
<span data-ttu-id="3d9ba-157">Anger det högsta antalet noder som ett program ska placeras på</span><span class="sxs-lookup"><span data-stu-id="3d9ba-157">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-158">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="3d9ba-158">-MinimumNodeCount</span></span>
<span data-ttu-id="3d9ba-159">Anger det minsta antalet noder där tjänste infrastruktur ska reservera kapacitet för det här programmet</span><span class="sxs-lookup"><span data-stu-id="3d9ba-159">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-160">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d9ba-160">-Name</span></span>
<span data-ttu-id="3d9ba-161">Ange namnet på programmet</span><span class="sxs-lookup"><span data-stu-id="3d9ba-161">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d9ba-162">-ResourceGroupName</span></span>
<span data-ttu-id="3d9ba-163">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d9ba-164">-ResourceId</span></span>
<span data-ttu-id="3d9ba-165">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-165">Arm ResourceId of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-166">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="3d9ba-166">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="3d9ba-167">Anger översikten över den hälso princip som ska användas för olika tjänst typer som en hash-tabell i följande format: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-167">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="3d9ba-168">Till exempel: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5; 5; 5"}</span><span class="sxs-lookup"><span data-stu-id="3d9ba-168">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-169">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="3d9ba-169">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="3d9ba-170">Anger den maximala procent andelen av program instanser som har distribuerats på de noder i klustret som har ett hälso fel som är felplacerat innan hälso tillståndet för klustret är fel.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-170">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-171">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3d9ba-171">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="3d9ba-172">Anger den maximala tiden i sekunder som Service Fabric tar uppgradera en enda uppgraderings domän.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-172">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="3d9ba-173">Efter den här perioden går uppgraderingen inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-173">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-174">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3d9ba-174">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="3d9ba-175">Anger den maximala tid som tjänstens Fabric väntar på att en tjänst ska omkonfigureras till ett säkert tillstånd, om den inte redan är i ett säkert tillstånd, innan Service Fabric fortsätter med uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-175">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-176">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="3d9ba-176">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="3d9ba-177">Anger den maximala tiden i sekunder som Service Fabric tar för hela uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-177">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="3d9ba-178">Efter den här perioden går uppgraderingen inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-178">After this period, the upgrade fails.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByResourceGroup, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d9ba-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d9ba-179">-Confirm</span></span>
<span data-ttu-id="3d9ba-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d9ba-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d9ba-181">-WhatIf</span></span>
<span data-ttu-id="3d9ba-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d9ba-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d9ba-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d9ba-184">CommonParameters</span></span>
<span data-ttu-id="3d9ba-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d9ba-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d9ba-186">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d9ba-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d9ba-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d9ba-187">INPUTS</span></span>

### <span data-ttu-id="3d9ba-188">System. String</span><span class="sxs-lookup"><span data-stu-id="3d9ba-188">System.String</span></span>

### <span data-ttu-id="3d9ba-189">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="3d9ba-189">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3d9ba-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d9ba-190">OUTPUTS</span></span>

### <span data-ttu-id="3d9ba-191">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="3d9ba-191">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="3d9ba-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d9ba-192">NOTES</span></span>

## <span data-ttu-id="3d9ba-193">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d9ba-193">RELATED LINKS</span></span>
