---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523316"
---
# <span data-ttu-id="f1135-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="f1135-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="f1135-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f1135-102">SYNOPSIS</span></span>
<span data-ttu-id="f1135-103">Ta bort en resurspool från det hanterade klustret.</span><span class="sxs-lookup"><span data-stu-id="f1135-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="f1135-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f1135-104">SYNTAX</span></span>

### <span data-ttu-id="f1135-105">GroupNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f1135-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1135-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1135-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1135-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1135-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1135-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f1135-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1135-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f1135-109">DESCRIPTION</span></span>
<span data-ttu-id="f1135-110">Ta bort en resurspool från det hanterade klustret.</span><span class="sxs-lookup"><span data-stu-id="f1135-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="f1135-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f1135-111">EXAMPLES</span></span>

### <span data-ttu-id="f1135-112">Ta bort angiven noduppsättning</span><span class="sxs-lookup"><span data-stu-id="f1135-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="f1135-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f1135-113">PARAMETERS</span></span>

### <span data-ttu-id="f1135-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1135-114">-AsJob</span></span>
<span data-ttu-id="f1135-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f1135-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1135-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="f1135-116">-ClusterName</span></span>
<span data-ttu-id="f1135-117">Namn på ditt hanterade Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="f1135-117">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f1135-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="f1135-118">-ClusterObject</span></span>
<span data-ttu-id="f1135-119">Cluster-objekt.</span><span class="sxs-lookup"><span data-stu-id="f1135-119">The cluster object.</span></span>

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

### <span data-ttu-id="f1135-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1135-120">-DefaultProfile</span></span>
<span data-ttu-id="f1135-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f1135-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1135-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f1135-122">-Force</span></span>
<span data-ttu-id="f1135-123">Ta bort resurspool utan fråga</span><span class="sxs-lookup"><span data-stu-id="f1135-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="f1135-124">-ID</span><span class="sxs-lookup"><span data-stu-id="f1135-124">-Id</span></span>
<span data-ttu-id="f1135-125">ID för en noduppsättning i hanterat Kubernetes-kluster</span><span class="sxs-lookup"><span data-stu-id="f1135-125">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="f1135-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1135-126">-InputObject</span></span>
<span data-ttu-id="f1135-127">Ett PSAgentPool-objekt som normalt passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1135-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f1135-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f1135-128">-Name</span></span>
<span data-ttu-id="f1135-129">Namnet på din resurspool</span><span class="sxs-lookup"><span data-stu-id="f1135-129">Name of your node pool</span></span>

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

### <span data-ttu-id="f1135-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1135-130">-PassThru</span></span>
<span data-ttu-id="f1135-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f1135-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="f1135-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1135-132">-ResourceGroupName</span></span>
<span data-ttu-id="f1135-133">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f1135-133">Resource group name</span></span>

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

### <span data-ttu-id="f1135-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f1135-134">-Confirm</span></span>
<span data-ttu-id="f1135-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f1135-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1135-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1135-136">-WhatIf</span></span>
<span data-ttu-id="f1135-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f1135-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1135-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f1135-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1135-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1135-139">CommonParameters</span></span>
<span data-ttu-id="f1135-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1135-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1135-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1135-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1135-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f1135-142">INPUTS</span></span>

### <span data-ttu-id="f1135-143">Microsoft. Azure. commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="f1135-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="f1135-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f1135-144">System.String</span></span>

## <span data-ttu-id="f1135-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f1135-145">OUTPUTS</span></span>

### <span data-ttu-id="f1135-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f1135-146">System.Boolean</span></span>

## <span data-ttu-id="f1135-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f1135-147">NOTES</span></span>

## <span data-ttu-id="f1135-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f1135-148">RELATED LINKS</span></span>
