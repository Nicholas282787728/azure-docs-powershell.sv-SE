---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258406"
---
# <span data-ttu-id="b0907-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="b0907-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="b0907-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0907-102">SYNOPSIS</span></span>
<span data-ttu-id="b0907-103">Uppdatera noduppsättningen i ett hanterat kluster.</span><span class="sxs-lookup"><span data-stu-id="b0907-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="b0907-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0907-104">SYNTAX</span></span>

### <span data-ttu-id="b0907-105">defaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b0907-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0907-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0907-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0907-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0907-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0907-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0907-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b0907-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0907-109">DESCRIPTION</span></span>
<span data-ttu-id="b0907-110">Uppdatera noduppsättningen i ett hanterat kluster.</span><span class="sxs-lookup"><span data-stu-id="b0907-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="b0907-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0907-111">EXAMPLES</span></span>

### <span data-ttu-id="b0907-112">Ändra antal minimun till 5 för angiven noduppsättning</span><span class="sxs-lookup"><span data-stu-id="b0907-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="b0907-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0907-113">PARAMETERS</span></span>

### <span data-ttu-id="b0907-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0907-114">-AsJob</span></span>
<span data-ttu-id="b0907-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0907-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0907-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="b0907-116">-ClusterName</span></span>
<span data-ttu-id="b0907-117">Namnet på den hanterade kluster resursen.</span><span class="sxs-lookup"><span data-stu-id="b0907-117">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="b0907-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b0907-118">-ClusterObject</span></span>
<span data-ttu-id="b0907-119">Cluster-objekt</span><span class="sxs-lookup"><span data-stu-id="b0907-119">The cluster object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0907-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0907-120">-DefaultProfile</span></span>
<span data-ttu-id="b0907-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0907-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0907-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="b0907-122">-EnableAutoScaling</span></span>
<span data-ttu-id="b0907-123">Om du vill aktivera automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="b0907-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="b0907-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b0907-124">-Force</span></span>
<span data-ttu-id="b0907-125">Uppdatera resurspool utan fråga</span><span class="sxs-lookup"><span data-stu-id="b0907-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="b0907-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b0907-126">-Id</span></span>
<span data-ttu-id="b0907-127">ID för en noduppsättning i hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="b0907-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0907-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0907-128">-InputObject</span></span>
<span data-ttu-id="b0907-129">Ett PSAgentPool-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0907-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0907-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="b0907-130">-KubernetesVersion</span></span>
<span data-ttu-id="b0907-131">Den version av Kubernetes som ska användas för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="b0907-131">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="b0907-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b0907-132">-MaxCount</span></span>
<span data-ttu-id="b0907-133">Maximalt antal noder för automatisk skalning</span><span class="sxs-lookup"><span data-stu-id="b0907-133">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="b0907-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="b0907-134">-MinCount</span></span>
<span data-ttu-id="b0907-135">Minsta antal noder för automatisk skalning.</span><span class="sxs-lookup"><span data-stu-id="b0907-135">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="b0907-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="b0907-136">-Name</span></span>
<span data-ttu-id="b0907-137">Namnet på Node-poolen.</span><span class="sxs-lookup"><span data-stu-id="b0907-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0907-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0907-138">-ResourceGroupName</span></span>
<span data-ttu-id="b0907-139">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b0907-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="b0907-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0907-140">-Confirm</span></span>
<span data-ttu-id="b0907-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0907-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0907-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0907-142">-WhatIf</span></span>
<span data-ttu-id="b0907-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0907-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0907-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0907-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0907-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0907-145">CommonParameters</span></span>
<span data-ttu-id="b0907-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0907-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0907-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0907-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0907-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0907-148">INPUTS</span></span>

### <span data-ttu-id="b0907-149">Microsoft. Azure. commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="b0907-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="b0907-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b0907-150">System.String</span></span>

## <span data-ttu-id="b0907-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0907-151">OUTPUTS</span></span>

### <span data-ttu-id="b0907-152">Microsoft. Azure. commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="b0907-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="b0907-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0907-153">NOTES</span></span>

## <span data-ttu-id="b0907-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0907-154">RELATED LINKS</span></span>