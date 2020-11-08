---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricApplication.md
ms.openlocfilehash: e438b4f22bbd3d574788efd93d29aad0b2586767
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091447"
---
# <span data-ttu-id="ee3ab-101">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ee3ab-101">Update-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ee3ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3ab-103">Uppdatera ett tjänst Fabric-program.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-103">Update a service fabric application.</span></span> <span data-ttu-id="ee3ab-104">Då kan du uppdatera program parametrarna och/eller uppgradera program typs versionen som utlöser en program uppgradering.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-104">This allows to update the application parameters and/or upgrade the application type version which will trigger an application upgrade.</span></span>

## <span data-ttu-id="ee3ab-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee3ab-105">SYNTAX</span></span>

### <span data-ttu-id="ee3ab-106">ByResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="ee3ab-106">ByResourceGroup (Default)</span></span>
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

### <span data-ttu-id="ee3ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee3ab-107">ByResourceId</span></span>
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

### <span data-ttu-id="ee3ab-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ee3ab-108">ByInputObject</span></span>
```
Update-AzServiceFabricApplication -InputObject <PSApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee3ab-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee3ab-109">DESCRIPTION</span></span>
<span data-ttu-id="ee3ab-110">Denna cmdlet kan användas för att uppdatera program parametrar och uppgradera program typs versionen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-110">This cmdlet can be used to update application parameters and upgrade the application type version.</span></span> <span data-ttu-id="ee3ab-111">Uppdatering av parametern ändrar bara modellen på ARM-sidan, bara när en ny typ version används, utlöses en program uppgradering.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-111">Updating the parameter will only change the model in ARM side, only when a new type version is used, the command will trigger an application upgrade.</span></span> <span data-ttu-id="ee3ab-112">Den angivna typen version ska redan vara skapad i klustret med **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-112">The type version specified should already be created in the cluster using **New-AzServiceFabricApplicationTypeVersion**.</span></span>

## <span data-ttu-id="ee3ab-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee3ab-113">EXAMPLES</span></span>

### <span data-ttu-id="ee3ab-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee3ab-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="ee3ab-115">I det här exemplet startas en program uppgradering för att uppdatera typ versionen till "v2" som skapades med **New-AzServiceFabricApplicationTypeVersion**.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-115">This example will start an application upgrade to update the type version to "v2" which was created with **New-AzServiceFabricApplicationTypeVersion**.</span></span> <span data-ttu-id="ee3ab-116">De program parametrar som används ska vara definierade i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-116">The application parameters used should be defined in the application manifest.</span></span>

### <span data-ttu-id="ee3ab-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ee3ab-117">Example 2</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -MinimumNodes 1 -MaximumNodes 4 -Verbose
```

<span data-ttu-id="ee3ab-118">I det här exemplet uppdateras begränsningen för lägsta och högsta antal noder för programmet.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-118">This example will update the minimum and maximum number of nodes restriction for the application.</span></span>

### <span data-ttu-id="ee3ab-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="ee3ab-119">Example 3</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $version = "v2"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testAppType_v2.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -Version $version -PackageUrl $packageUrl -Verbose
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationTypeVersion $version -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"} -HealthCheckStableDurationSec 0 -HealthCheckWaitDurationSec 0 -HealthCheckRetryTimeoutSec 0 -UpgradeDomainTimeoutSec 5000 -UpgradeTimeoutSec 7000 -FailureAction Rollback -UpgradeReplicaSetCheckTimeoutSec 300 -ForceRestart
```

<span data-ttu-id="ee3ab-120">I det här exemplet startas en program uppgradering för att uppdatera typ versionen till "v2" och dessutom anges vissa uppgraderings princip parametrar som kommer att gälla från den aktuella uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-120">This example will start an application upgrade to update the type version to "v2" and also sets some upgrade policy parameters that will take effect from the current upgrade.</span></span>

### <span data-ttu-id="ee3ab-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="ee3ab-121">Example 4</span></span>
```powershell
PS C:\> Update-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="ee3ab-122">I det här exemplet uppdateras program parametrarna men ändringarna börjar gälla tills nästa version uppgraderas till programmet.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-122">This example updates the application parameters but these changes will only take effect until the next version upgrade to the application.</span></span>

## <span data-ttu-id="ee3ab-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee3ab-123">PARAMETERS</span></span>

### <span data-ttu-id="ee3ab-124">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="ee3ab-124">-ApplicationParameter</span></span>
<span data-ttu-id="ee3ab-125">Ange program parametrar som nycklar/värde par.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-125">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="ee3ab-126">Dessa parametrar måste finnas i program manifestet.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-126">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="ee3ab-127">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ee3ab-127">-ApplicationTypeVersion</span></span>
<span data-ttu-id="ee3ab-128">Ange program typ version</span><span class="sxs-lookup"><span data-stu-id="ee3ab-128">Specify the application type version</span></span>

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

### <span data-ttu-id="ee3ab-129">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="ee3ab-129">-ClusterName</span></span>
<span data-ttu-id="ee3ab-130">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ee3ab-131">-ConsiderWarningAsError</span><span class="sxs-lookup"><span data-stu-id="ee3ab-131">-ConsiderWarningAsError</span></span>
<span data-ttu-id="ee3ab-132">Anger om en varnings händelse ska behandlas som en fel händelse under en hälso utvärdering.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-132">Indicates whether to treat a warning health event as an error event during health evaluation.</span></span>

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

### <span data-ttu-id="ee3ab-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3ab-133">-DefaultProfile</span></span>
<span data-ttu-id="ee3ab-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee3ab-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span><span class="sxs-lookup"><span data-stu-id="ee3ab-135">-DefaultServiceTypeMaxPercentUnhealthyPartitionsPerService</span></span>
<span data-ttu-id="ee3ab-136">Anger maximalt antal unhelthy-partitioner per tjänst som tillåts av hälso policyn för den standard tjänst typ som ska användas för den övervakade uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-136">Specifies the maximum percent of unhelthy partitions per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="ee3ab-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span><span class="sxs-lookup"><span data-stu-id="ee3ab-137">-DefaultServiceTypeMaxPercentUnhealthyReplicasPerPartition</span></span>
<span data-ttu-id="ee3ab-138">Anger det maximala antalet unhelthy-repliker per tjänst som tillåts av hälso policyn för den standard tjänst typ som ska användas för den övervakade uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-138">Specifies the maximum percent of unhelthy replicas per service allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="ee3ab-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span><span class="sxs-lookup"><span data-stu-id="ee3ab-139">-DefaultServiceTypeUnhealthyServicesMaxPercent</span></span>
<span data-ttu-id="ee3ab-140">Anger den maximala procent andelen unhelthy tjänster som tillåts av hälso policyn för den standard tjänst typ som ska användas för den övervakade uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-140">Specifies the maximum percent of unhelthy services allowed by the health policy for the default service type to use for the monitored upgrade.</span></span>

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

### <span data-ttu-id="ee3ab-141">-FailureAction</span><span class="sxs-lookup"><span data-stu-id="ee3ab-141">-FailureAction</span></span>
<span data-ttu-id="ee3ab-142">Anger vilken åtgärd som ska vidtas om den övervakade uppgraderingen Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-142">Specifies the action to take if the monitored upgrade fails.</span></span>
<span data-ttu-id="ee3ab-143">De acceptabla värdena för den här parametern är rollback eller manual.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-143">The acceptable values for this parameter are Rollback or Manual.</span></span>

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

### <span data-ttu-id="ee3ab-144">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="ee3ab-144">-ForceRestart</span></span>
<span data-ttu-id="ee3ab-145">Anger att tjänst värden startas om även om uppgraderingen är en konfigurations ändring.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-145">Indicates that the service host restarts even if the upgrade is a configuration-only change.</span></span>

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

### <span data-ttu-id="ee3ab-146">-HealthCheckRetryTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ee3ab-146">-HealthCheckRetryTimeoutSec</span></span>
<span data-ttu-id="ee3ab-147">Anger hur länge (i sekunder) som tjänst Fabric försöker kontrol lera hälso kontrollen om den föregående hälso kontrollen Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-147">Specifies the duration, in seconds, after which Service Fabric retries the health check if the previous health check fails.</span></span>

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

### <span data-ttu-id="ee3ab-148">-HealthCheckStableDurationSec</span><span class="sxs-lookup"><span data-stu-id="ee3ab-148">-HealthCheckStableDurationSec</span></span>
<span data-ttu-id="ee3ab-149">Anger hur länge tjänsten Fabric väntar för att kontrol lera att programmet är stabilt innan det flyttas till nästa uppgraderings domän eller att slutföra uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-149">Specifies the duration, in seconds, that Service Fabric waits in order to verify that the application is stable before moving to the next upgrade domain or completing the upgrade.</span></span>
<span data-ttu-id="ee3ab-150">Denna vänte tid hindrar obehöriga ändringar av hälso tillstånd direkt efter att hälso kontrollen har utförts.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-150">This wait duration prevents undetected changes of health right after the health check is performed.</span></span>

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

### <span data-ttu-id="ee3ab-151">-HealthCheckWaitDurationSec</span><span class="sxs-lookup"><span data-stu-id="ee3ab-151">-HealthCheckWaitDurationSec</span></span>
<span data-ttu-id="ee3ab-152">Anger hur länge tjänsten Fabric ska vänta innan den första hälso kontrollen utförs när uppgraderingen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-152">Specifies the duration, in seconds, that Service Fabric waits before it performs the initial health check after it finishes the upgrade on the upgrade domain.</span></span>

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

### <span data-ttu-id="ee3ab-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee3ab-153">-InputObject</span></span>
<span data-ttu-id="ee3ab-154">Program resursen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-154">The application resource.</span></span>

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

### <span data-ttu-id="ee3ab-155">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="ee3ab-155">-MaximumNodeCount</span></span>
<span data-ttu-id="ee3ab-156">Anger det högsta antalet noder som ett program ska placeras på</span><span class="sxs-lookup"><span data-stu-id="ee3ab-156">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="ee3ab-157">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="ee3ab-157">-MinimumNodeCount</span></span>
<span data-ttu-id="ee3ab-158">Anger det minsta antalet noder där tjänste infrastruktur ska reservera kapacitet för det här programmet</span><span class="sxs-lookup"><span data-stu-id="ee3ab-158">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="ee3ab-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee3ab-159">-Name</span></span>
<span data-ttu-id="ee3ab-160">Ange namnet på programmet</span><span class="sxs-lookup"><span data-stu-id="ee3ab-160">Specify the name of the application</span></span>

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

### <span data-ttu-id="ee3ab-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee3ab-161">-ResourceGroupName</span></span>
<span data-ttu-id="ee3ab-162">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-162">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ee3ab-163">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee3ab-163">-ResourceId</span></span>
<span data-ttu-id="ee3ab-164">Programmets ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-164">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ee3ab-165">-ServiceTypeHealthPolicyMap</span><span class="sxs-lookup"><span data-stu-id="ee3ab-165">-ServiceTypeHealthPolicyMap</span></span>
<span data-ttu-id="ee3ab-166">Anger översikten över den hälso princip som ska användas för olika tjänst typer som en hash-tabell i följande format: @ {"ServiceTypeName": "MaxPercentUnhealthyPartitionsPerService, MaxPercentUnhealthyReplicasPerPartition, MaxPercentUnhealthyServices"}.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-166">Specifies the map of the health policy to use for different service types as a hash table in the following format: @ {"ServiceTypeName" : "MaxPercentUnhealthyPartitionsPerService,MaxPercentUnhealthyReplicasPerPartition,MaxPercentUnhealthyServices"}.</span></span>
<span data-ttu-id="ee3ab-167">Till exempel: @ {"ServiceTypeName01" = "5; 10; 5"; "ServiceTypeName02" = "5; 5; 5"}</span><span class="sxs-lookup"><span data-stu-id="ee3ab-167">For example: @{ "ServiceTypeName01" = "5,10,5"; "ServiceTypeName02" = "5,5,5" }</span></span>

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

### <span data-ttu-id="ee3ab-168">-UnhealthyDeployedApplicationsMaxPercent</span><span class="sxs-lookup"><span data-stu-id="ee3ab-168">-UnhealthyDeployedApplicationsMaxPercent</span></span>
<span data-ttu-id="ee3ab-169">Anger den maximala procent andelen av program instanser som har distribuerats på de noder i klustret som har ett hälso fel som är felplacerat innan hälso tillståndet för klustret är fel.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-169">Specifies the maximum percentage of the application instances deployed on the nodes in the cluster that have a health state of error before the application health state for the cluster is error.</span></span>

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

### <span data-ttu-id="ee3ab-170">-UpgradeDomainTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ee3ab-170">-UpgradeDomainTimeoutSec</span></span>
<span data-ttu-id="ee3ab-171">Anger den maximala tiden i sekunder som Service Fabric tar uppgradera en enda uppgraderings domän.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-171">Specifies the maximum time, in seconds, that Service Fabric takes to upgrade a single upgrade domain.</span></span>
<span data-ttu-id="ee3ab-172">Efter den här perioden går uppgraderingen inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-172">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="ee3ab-173">-UpgradeReplicaSetCheckTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ee3ab-173">-UpgradeReplicaSetCheckTimeoutSec</span></span>
<span data-ttu-id="ee3ab-174">Anger den maximala tid som tjänstens Fabric väntar på att en tjänst ska omkonfigureras till ett säkert tillstånd, om den inte redan är i ett säkert tillstånd, innan Service Fabric fortsätter med uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-174">Specifies the maximum time that Service Fabric waits for a service to reconfigure into a safe state, if not already in a safe state, before Service Fabric proceeds with the upgrade.</span></span>

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

### <span data-ttu-id="ee3ab-175">-UpgradeTimeoutSec</span><span class="sxs-lookup"><span data-stu-id="ee3ab-175">-UpgradeTimeoutSec</span></span>
<span data-ttu-id="ee3ab-176">Anger den maximala tiden i sekunder som Service Fabric tar för hela uppgraderingen.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-176">Specifies the maximum time, in seconds, that Service Fabric takes for the entire upgrade.</span></span>
<span data-ttu-id="ee3ab-177">Efter den här perioden går uppgraderingen inte att fungera.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-177">After this period, the upgrade fails.</span></span>

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

### <span data-ttu-id="ee3ab-178">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee3ab-178">-Confirm</span></span>
<span data-ttu-id="ee3ab-179">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3ab-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3ab-180">-WhatIf</span></span>
<span data-ttu-id="ee3ab-181">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee3ab-182">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-182">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3ab-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3ab-183">CommonParameters</span></span>
<span data-ttu-id="ee3ab-184">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee3ab-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3ab-185">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee3ab-185">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3ab-186">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee3ab-186">INPUTS</span></span>

### <span data-ttu-id="ee3ab-187">System. String</span><span class="sxs-lookup"><span data-stu-id="ee3ab-187">System.String</span></span>

### <span data-ttu-id="ee3ab-188">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="ee3ab-188">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ee3ab-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee3ab-189">OUTPUTS</span></span>

### <span data-ttu-id="ee3ab-190">Microsoft. Azure. commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="ee3ab-190">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ee3ab-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee3ab-191">NOTES</span></span>

## <span data-ttu-id="ee3ab-192">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee3ab-192">RELATED LINKS</span></span>
