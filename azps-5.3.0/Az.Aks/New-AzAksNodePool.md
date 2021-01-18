---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAksNodePool.md
ms.openlocfilehash: 77125022002f09233154ba468f22a28228219e04
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523320"
---
# <span data-ttu-id="7fd73-101">New-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="7fd73-101">New-AzAksNodePool</span></span>

## <span data-ttu-id="7fd73-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fd73-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd73-103">Skapa en ny resurspool i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="7fd73-103">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="7fd73-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fd73-104">SYNTAX</span></span>

### <span data-ttu-id="7fd73-105">defaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd73-105">defaultParameterSet</span></span>
```
New-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-Count <Int32>]
 [-OsDiskSize <Int32>] [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd73-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd73-106">ParentObjectParameterSet</span></span>
```
New-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-Count <Int32>] [-OsDiskSize <Int32>]
 [-VmSize <String>] [-VnetSubnetID <String>] [-MaxPodCount <Int32>] [-OsType <String>]
 [-ScaleSetPriority <String>] [-ScaleSetEvictionPolicy <String>] [-VmSetType <String>] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd73-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fd73-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd73-108">Skapa en ny resurspool i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="7fd73-108">Create a new node pool in specified cluster.</span></span>

## <span data-ttu-id="7fd73-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fd73-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd73-110">Skapa en noduppsättning med standard parametrar</span><span class="sxs-lookup"><span data-stu-id="7fd73-110">Create node pool with default parameters</span></span>
```powershell
PS C:\> New-AzAksNodePool -ResourceGroupName myResouceGroup -ClusterName myCluster -Name mydefault
```

### <span data-ttu-id="7fd73-111">Skapa en Windows Server-behållare på en AKS</span><span class="sxs-lookup"><span data-stu-id="7fd73-111">Create Windows Server container on an AKS</span></span>
```powershell
PS C:\> $cred = ConvertTo-SecureString -AsPlainText "Password!!123" -Force
PS C:\> New-AzAks -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeVmSetType VirtualMachineScaleSets
PS C:\> New-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name win1 -OsType Windows -VmSetType VirtualMachineScaleSets
```

## <span data-ttu-id="7fd73-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fd73-112">PARAMETERS</span></span>

### <span data-ttu-id="7fd73-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="7fd73-113">-ClusterName</span></span>
<span data-ttu-id="7fd73-114">Namnet på den hanterade kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="7fd73-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="7fd73-115">-ClusterObject</span></span>
<span data-ttu-id="7fd73-116">Ange Cluster-objekt som du vill skapa en resurspool för.</span><span class="sxs-lookup"><span data-stu-id="7fd73-116">Specify cluster object in which to create node pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-117">-Antal</span><span class="sxs-lookup"><span data-stu-id="7fd73-117">-Count</span></span>
<span data-ttu-id="7fd73-118">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7fd73-118">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd73-119">-DefaultProfile</span></span>
<span data-ttu-id="7fd73-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd73-121">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="7fd73-121">-EnableAutoScaling</span></span>
<span data-ttu-id="7fd73-122">Om du vill aktivera automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="7fd73-122">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="7fd73-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7fd73-123">-Force</span></span>
<span data-ttu-id="7fd73-124">Skapa en noduppsättning även om den redan finns</span><span class="sxs-lookup"><span data-stu-id="7fd73-124">Create node pool even if it already exists</span></span>

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

### <span data-ttu-id="7fd73-125">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="7fd73-125">-KubernetesVersion</span></span>
<span data-ttu-id="7fd73-126">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="7fd73-126">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="7fd73-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7fd73-127">-MaxCount</span></span>
<span data-ttu-id="7fd73-128">Maximalt antal noder för automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="7fd73-128">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-129">-MaxPodCount</span><span class="sxs-lookup"><span data-stu-id="7fd73-129">-MaxPodCount</span></span>
<span data-ttu-id="7fd73-130">Maximalt antal Pods som kan köras på noden.</span><span class="sxs-lookup"><span data-stu-id="7fd73-130">Maximum number of pods that can run on node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-131">-MinCount</span><span class="sxs-lookup"><span data-stu-id="7fd73-131">-MinCount</span></span>
<span data-ttu-id="7fd73-132">Minsta antal noder för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="7fd73-132">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="7fd73-133">-Name</span></span>
<span data-ttu-id="7fd73-134">Namnet på Node-poolen.</span><span class="sxs-lookup"><span data-stu-id="7fd73-134">The name of the node pool.</span></span>

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

### <span data-ttu-id="7fd73-135">-OsDiskSize</span><span class="sxs-lookup"><span data-stu-id="7fd73-135">-OsDiskSize</span></span>
<span data-ttu-id="7fd73-136">Standardvärdet för noder för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="7fd73-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="7fd73-137">-OsType</span></span>
<span data-ttu-id="7fd73-138">OsType som ska användas för att ange OS-typ.</span><span class="sxs-lookup"><span data-stu-id="7fd73-138">OsType to be used to specify os type.</span></span>
<span data-ttu-id="7fd73-139">Välj från Linux och Windows.</span><span class="sxs-lookup"><span data-stu-id="7fd73-139">Choose from Linux and Windows.</span></span>
<span data-ttu-id="7fd73-140">Standard för Linux.</span><span class="sxs-lookup"><span data-stu-id="7fd73-140">Default to Linux.</span></span>

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

### <span data-ttu-id="7fd73-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd73-141">-ResourceGroupName</span></span>
<span data-ttu-id="7fd73-142">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7fd73-142">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd73-143">-ScaleSetEvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fd73-143">-ScaleSetEvictionPolicy</span></span>
<span data-ttu-id="7fd73-144">ScaleSetEvictionPolicy ska användas för att ange borttagnings princip för skalnings uppsättning för den virtuella datorns Pro.</span><span class="sxs-lookup"><span data-stu-id="7fd73-144">ScaleSetEvictionPolicy to be used to specify eviction policy for low priority virtual machine scale set.</span></span>
<span data-ttu-id="7fd73-145">Standard för att ta bort.</span><span class="sxs-lookup"><span data-stu-id="7fd73-145">Default to Delete.</span></span>

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

### <span data-ttu-id="7fd73-146">-ScaleSetPriority</span><span class="sxs-lookup"><span data-stu-id="7fd73-146">-ScaleSetPriority</span></span>
<span data-ttu-id="7fd73-147">ScaleSetPriority används för att ange prioritet för den virtuella datorns skalnings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="7fd73-147">ScaleSetPriority to be used to specify virtual machine scale set priority.</span></span>
<span data-ttu-id="7fd73-148">Standard är normal.</span><span class="sxs-lookup"><span data-stu-id="7fd73-148">Default to regular.</span></span>

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

### <span data-ttu-id="7fd73-149">-VmSetType</span><span class="sxs-lookup"><span data-stu-id="7fd73-149">-VmSetType</span></span>
<span data-ttu-id="7fd73-150">Representerar typer av en noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="7fd73-150">Represents types of an node pool.</span></span>
<span data-ttu-id="7fd73-151">Möjliga värden är: ' VirtualMachineScaleSets ', ' AvailabilitySet '</span><span class="sxs-lookup"><span data-stu-id="7fd73-151">Possible values include: 'VirtualMachineScaleSets', 'AvailabilitySet'</span></span>

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

### <span data-ttu-id="7fd73-152">-VmSize</span><span class="sxs-lookup"><span data-stu-id="7fd73-152">-VmSize</span></span>
<span data-ttu-id="7fd73-153">Den virtuella datorns storlek.</span><span class="sxs-lookup"><span data-stu-id="7fd73-153">The size of the Virtual Machine.</span></span> <span data-ttu-id="7fd73-154">Standardvärdet är Standard_D2_v2.</span><span class="sxs-lookup"><span data-stu-id="7fd73-154">Default value is Standard_D2_v2.</span></span>

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

### <span data-ttu-id="7fd73-155">-VnetSubnetID</span><span class="sxs-lookup"><span data-stu-id="7fd73-155">-VnetSubnetID</span></span>
<span data-ttu-id="7fd73-156">VNet-SubnetID anger VNet-nätmask.</span><span class="sxs-lookup"><span data-stu-id="7fd73-156">VNet SubnetID specifies the VNet's subnet identifier.</span></span>

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

### <span data-ttu-id="7fd73-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fd73-157">-Confirm</span></span>
<span data-ttu-id="7fd73-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fd73-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd73-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd73-159">-WhatIf</span></span>
<span data-ttu-id="7fd73-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fd73-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd73-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fd73-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd73-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd73-162">CommonParameters</span></span>
<span data-ttu-id="7fd73-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd73-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd73-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fd73-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd73-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fd73-165">INPUTS</span></span>

### <span data-ttu-id="7fd73-166">Microsoft. Azure. commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7fd73-166">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7fd73-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fd73-167">OUTPUTS</span></span>

### <span data-ttu-id="7fd73-168">Microsoft. Azure. commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="7fd73-168">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="7fd73-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fd73-169">NOTES</span></span>

## <span data-ttu-id="7fd73-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fd73-170">RELATED LINKS</span></span>
