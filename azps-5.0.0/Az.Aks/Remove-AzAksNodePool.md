---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270336"
---
# <span data-ttu-id="a1472-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="a1472-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="a1472-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1472-102">SYNOPSIS</span></span>
<span data-ttu-id="a1472-103">Ta bort en resurspool från det hanterade klustret.</span><span class="sxs-lookup"><span data-stu-id="a1472-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="a1472-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1472-104">SYNTAX</span></span>

### <span data-ttu-id="a1472-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a1472-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1472-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1472-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1472-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1472-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1472-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1472-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1472-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1472-109">DESCRIPTION</span></span>
<span data-ttu-id="a1472-110">Ta bort en resurspool från det hanterade klustret.</span><span class="sxs-lookup"><span data-stu-id="a1472-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="a1472-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1472-111">EXAMPLES</span></span>

### <span data-ttu-id="a1472-112">Ta bort angiven noduppsättning</span><span class="sxs-lookup"><span data-stu-id="a1472-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="a1472-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1472-113">PARAMETERS</span></span>

### <span data-ttu-id="a1472-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1472-114">-AsJob</span></span>
<span data-ttu-id="a1472-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a1472-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1472-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a1472-116">-ClusterName</span></span>
<span data-ttu-id="a1472-117">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a1472-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1472-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="a1472-118">-ClusterObject</span></span>
<span data-ttu-id="a1472-119">Cluster-objekt.</span><span class="sxs-lookup"><span data-stu-id="a1472-119">The cluster object.</span></span>

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

### <span data-ttu-id="a1472-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1472-120">-DefaultProfile</span></span>
<span data-ttu-id="a1472-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1472-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1472-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a1472-122">-Force</span></span>
<span data-ttu-id="a1472-123">Ta bort resurspool utan fråga</span><span class="sxs-lookup"><span data-stu-id="a1472-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="a1472-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a1472-124">-Id</span></span>
<span data-ttu-id="a1472-125">ID för en noduppsättning i hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="a1472-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1472-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1472-126">-InputObject</span></span>
<span data-ttu-id="a1472-127">Ett PSAgentPool-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1472-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a1472-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1472-128">-Name</span></span>
<span data-ttu-id="a1472-129">Namnet på din resurspool</span><span class="sxs-lookup"><span data-stu-id="a1472-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1472-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1472-130">-PassThru</span></span>
<span data-ttu-id="a1472-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a1472-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a1472-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1472-132">-ResourceGroupName</span></span>
<span data-ttu-id="a1472-133">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a1472-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1472-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1472-134">-Confirm</span></span>
<span data-ttu-id="a1472-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1472-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1472-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1472-136">-WhatIf</span></span>
<span data-ttu-id="a1472-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1472-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1472-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1472-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1472-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1472-139">CommonParameters</span></span>
<span data-ttu-id="a1472-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1472-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1472-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1472-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1472-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1472-142">INPUTS</span></span>

### <span data-ttu-id="a1472-143">Microsoft. Azure. commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="a1472-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="a1472-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a1472-144">System.String</span></span>

## <span data-ttu-id="a1472-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1472-145">OUTPUTS</span></span>

### <span data-ttu-id="a1472-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1472-146">System.Boolean</span></span>

## <span data-ttu-id="a1472-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1472-147">NOTES</span></span>

## <span data-ttu-id="a1472-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1472-148">RELATED LINKS</span></span>
