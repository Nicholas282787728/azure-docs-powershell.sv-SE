---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 5f5509da60351216a5ea004eae59e551a74e601a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409600"
---
# <span data-ttu-id="63cc5-101">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="63cc5-101">Remove-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="63cc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="63cc5-103">Ta bort nodtypen eller specifika noder inom nodtypen.</span><span class="sxs-lookup"><span data-stu-id="63cc5-103">Remove the node type or specific nodes within the node type.</span></span>

## <span data-ttu-id="63cc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63cc5-104">SYNTAX</span></span>

### <span data-ttu-id="63cc5-105">DeleteNodeTypeByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="63cc5-105">DeleteNodeTypeByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63cc5-106">DeleteNodeTypeByName</span><span class="sxs-lookup"><span data-stu-id="63cc5-106">DeleteNodeTypeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63cc5-107">DeleteNodeByName</span><span class="sxs-lookup"><span data-stu-id="63cc5-107">DeleteNodeByName</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63cc5-108">DeleteNodeByObj</span><span class="sxs-lookup"><span data-stu-id="63cc5-108">DeleteNodeByObj</span></span>
```
Remove-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]>
 [-ForceRemoveNode] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63cc5-109">DeleteNodeTypeById</span><span class="sxs-lookup"><span data-stu-id="63cc5-109">DeleteNodeTypeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63cc5-110">DeleteNodeById</span><span class="sxs-lookup"><span data-stu-id="63cc5-110">DeleteNodeById</span></span>
```
Remove-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-ForceRemoveNode]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63cc5-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63cc5-111">DESCRIPTION</span></span>
<span data-ttu-id="63cc5-112">Ta bort nodtypen eller specifika noder inom nodtypen.</span><span class="sxs-lookup"><span data-stu-id="63cc5-112">Remove the node type or specific nodes within the node type.</span></span> <span data-ttu-id="63cc5-113">Om paremter-nodnamn används kommer bara noder som är angivna att tas bort.</span><span class="sxs-lookup"><span data-stu-id="63cc5-113">If the paremter -NodeName is used then only nodes specified will be removed.</span></span>

## <span data-ttu-id="63cc5-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63cc5-114">EXAMPLES</span></span>

### <span data-ttu-id="63cc5-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="63cc5-115">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName
```

<span data-ttu-id="63cc5-116">Ta bort nodtyp.</span><span class="sxs-lookup"><span data-stu-id="63cc5-116">Remove node type.</span></span>

### <span data-ttu-id="63cc5-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="63cc5-117">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt2"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType
```

<span data-ttu-id="63cc5-118">Ta bort nodtyp med rör.</span><span class="sxs-lookup"><span data-stu-id="63cc5-118">Remove node type, with piping.</span></span>

### <span data-ttu-id="63cc5-119">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="63cc5-119">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="63cc5-120">Ta bort två noder från nodtypen.</span><span class="sxs-lookup"><span data-stu-id="63cc5-120">Remove 2 nodes from the node type.</span></span>

### <span data-ttu-id="63cc5-121">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="63cc5-121">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeType -NodeName nt1_0, nt1_3
```

<span data-ttu-id="63cc5-122">Ta bort två noder från nodtypen med rör dragningen.</span><span class="sxs-lookup"><span data-stu-id="63cc5-122">Remove 2 nodes from the node type, with piping.</span></span>

## <span data-ttu-id="63cc5-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63cc5-123">PARAMETERS</span></span>

### <span data-ttu-id="63cc5-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63cc5-124">-AsJob</span></span>
<span data-ttu-id="63cc5-125">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="63cc5-125">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="63cc5-126">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="63cc5-126">-ClusterName</span></span>
<span data-ttu-id="63cc5-127">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="63cc5-127">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cc5-128">-DefaultProfile</span></span>
<span data-ttu-id="63cc5-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63cc5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63cc5-130">-ForceRemoveNode</span><span class="sxs-lookup"><span data-stu-id="63cc5-130">-ForceRemoveNode</span></span>
<span data-ttu-id="63cc5-131">Om du använder den här flaggan tvingas borttagningen även om Service Fabric inte kan inaktivera noderna.</span><span class="sxs-lookup"><span data-stu-id="63cc5-131">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="63cc5-132">Använd med försiktighet eftersom det här kan leda till förlust av data om tillstånds känslig arbets belastning körs på noderna, eller kan ta bort klustret om det inte finns tillräckligt många dirigeringsroutrar efter opearion.</span><span class="sxs-lookup"><span data-stu-id="63cc5-132">Use with caution as this might cause data loss if stateful workloads are running on the nodes, or might bring the cluster down if there are not enough seed nodes after the opearion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63cc5-133">-InputObject</span></span>
<span data-ttu-id="63cc5-134">Resurs för nodtyp</span><span class="sxs-lookup"><span data-stu-id="63cc5-134">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: DeleteNodeTypeByObj, DeleteNodeByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="63cc5-135">-Name</span></span>
<span data-ttu-id="63cc5-136">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="63cc5-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-137">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="63cc5-137">-NodeName</span></span>
<span data-ttu-id="63cc5-138">Lista över nodnamn för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="63cc5-138">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: DeleteNodeByName, DeleteNodeByObj, DeleteNodeById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63cc5-139">-PassThru</span></span>
<span data-ttu-id="63cc5-140">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="63cc5-140">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="63cc5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cc5-141">-ResourceGroupName</span></span>
<span data-ttu-id="63cc5-142">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="63cc5-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeByName, DeleteNodeByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63cc5-143">-ResourceId</span></span>
<span data-ttu-id="63cc5-144">Resurs-ID för nodtyp</span><span class="sxs-lookup"><span data-stu-id="63cc5-144">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteNodeTypeById, DeleteNodeById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63cc5-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63cc5-145">-Confirm</span></span>
<span data-ttu-id="63cc5-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63cc5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63cc5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63cc5-147">-WhatIf</span></span>
<span data-ttu-id="63cc5-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63cc5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63cc5-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63cc5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63cc5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cc5-150">CommonParameters</span></span>
<span data-ttu-id="63cc5-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63cc5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cc5-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63cc5-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cc5-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63cc5-153">INPUTS</span></span>

### <span data-ttu-id="63cc5-154">System. String</span><span class="sxs-lookup"><span data-stu-id="63cc5-154">System.String</span></span>

## <span data-ttu-id="63cc5-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63cc5-155">OUTPUTS</span></span>

### <span data-ttu-id="63cc5-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63cc5-156">System.Boolean</span></span>

## <span data-ttu-id="63cc5-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63cc5-157">NOTES</span></span>

## <span data-ttu-id="63cc5-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63cc5-158">RELATED LINKS</span></span>
