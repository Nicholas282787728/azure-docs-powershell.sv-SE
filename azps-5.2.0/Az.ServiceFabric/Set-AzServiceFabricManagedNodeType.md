---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: b0d22b0cb017c40dc0d1b0328f540b7774ca991b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408803"
---
# <span data-ttu-id="232dd-101">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="232dd-101">Set-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="232dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="232dd-102">SYNOPSIS</span></span>
<span data-ttu-id="232dd-103">Anger resurs egenskaper för nodtyp eller kör återavbildnings åtgärder för specifika NDES för noden nodtyp med-Rebild.</span><span class="sxs-lookup"><span data-stu-id="232dd-103">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span>

## <span data-ttu-id="232dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="232dd-104">SYNTAX</span></span>

### <span data-ttu-id="232dd-105">ByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="232dd-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232dd-106">WithParamsByName</span><span class="sxs-lookup"><span data-stu-id="232dd-106">WithParamsByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-AsJob] [-InstanceCount <Int32>] [-ApplicationStartPort <Int32>] [-ApplicationEndPort <Int32>]
 [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-Capacity <Hashtable>]
 [-PlacementProperty <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="232dd-107">ReimageByName</span><span class="sxs-lookup"><span data-stu-id="232dd-107">ReimageByName</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-Reimage] [-ForceReimage] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232dd-108">WithParamsById</span><span class="sxs-lookup"><span data-stu-id="232dd-108">WithParamsById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232dd-109">ReimageById</span><span class="sxs-lookup"><span data-stu-id="232dd-109">ReimageById</span></span>
```
Set-AzServiceFabricManagedNodeType [-ResourceId] <String> -NodeName <String[]> [-Reimage] [-ForceReimage]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="232dd-110">ReimageByObj</span><span class="sxs-lookup"><span data-stu-id="232dd-110">ReimageByObj</span></span>
```
Set-AzServiceFabricManagedNodeType [-InputObject] <PSManagedNodeType> -NodeName <String[]> [-Reimage]
 [-ForceReimage] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="232dd-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="232dd-111">DESCRIPTION</span></span>
<span data-ttu-id="232dd-112">Anger resurs egenskaper för nodtyp eller kör återavbildnings åtgärder för specifika NDES för noden nodtyp med-Rebild.</span><span class="sxs-lookup"><span data-stu-id="232dd-112">Sets node type resource properties or run reimage actions on specific ndes of the node type with -Reimage parameter.</span></span> <span data-ttu-id="232dd-113">På reimgae-åtgärden kommer tjänsten Service Fabric att inaktive ras innan de installeras om och aktive ras på nytt när de kommer tillbaka.</span><span class="sxs-lookup"><span data-stu-id="232dd-113">On reimgae operation the service fabric nodes will be disabled before reimaging the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="232dd-114">Om det sker på primära nodtyper kan det ta en stund eftersom det kanske inte går att återställa alla noder samtidigt.</span><span class="sxs-lookup"><span data-stu-id="232dd-114">If this is done on primary node types it might take a while as it might not reimage all the nodes at the same time.</span></span> <span data-ttu-id="232dd-115">Use-ForceReimage tvinga åtgärden även om Service Fabric inte kan inaktivera noderna men använda försiktighet eftersom det kan orsaka data förlust om tillstånds krävande arbets belastningar körs på noden.</span><span class="sxs-lookup"><span data-stu-id="232dd-115">Use -ForceReimage force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="232dd-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="232dd-116">EXAMPLES</span></span>

### <span data-ttu-id="232dd-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="232dd-117">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -InstanceCount 6 -Verbose
```

<span data-ttu-id="232dd-118">Uppdatera instans antalet av nodtypen.</span><span class="sxs-lookup"><span data-stu-id="232dd-118">Update the instance count of the node type.</span></span>

### <span data-ttu-id="232dd-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="232dd-119">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -name $NodeTypeName -PlacementProperty @{NodeColor="Red";SomeProperty="6";} -Verbose
```

<span data-ttu-id="232dd-120">Uppdatera placerings Properites för nodtypen.</span><span class="sxs-lookup"><span data-stu-id="232dd-120">Update placement properites of the node type.</span></span> <span data-ttu-id="232dd-121">Då skrivs äldre placerings Properites över.</span><span class="sxs-lookup"><span data-stu-id="232dd-121">This will overwrite older placement properites if any.</span></span>

### <span data-ttu-id="232dd-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="232dd-122">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Set-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -Reimage -NodeName nt1_0, nt1_3
```

<span data-ttu-id="232dd-123">Ange nod 0 och 3 på noden för nodtyp.</span><span class="sxs-lookup"><span data-stu-id="232dd-123">Reimage node 0 and 3 on the node type.</span></span>

### <span data-ttu-id="232dd-124">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="232dd-124">Example 4</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType.VmInstanceCount = 6
$nodeType | Set-AzServiceFabricManagedNodeType
```

<span data-ttu-id="232dd-125">Uppdatera instans antalet av nodtypen med rör dragningen.</span><span class="sxs-lookup"><span data-stu-id="232dd-125">Update the instance count of the node type, with piping.</span></span>

## <span data-ttu-id="232dd-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="232dd-126">PARAMETERS</span></span>

### <span data-ttu-id="232dd-127">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="232dd-127">-ApplicationEndPort</span></span>
<span data-ttu-id="232dd-128">Program slut port för en serie portar.</span><span class="sxs-lookup"><span data-stu-id="232dd-128">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-129">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="232dd-129">-ApplicationStartPort</span></span>
<span data-ttu-id="232dd-130">Start port för en serie portar.</span><span class="sxs-lookup"><span data-stu-id="232dd-130">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="232dd-131">-AsJob</span></span>
<span data-ttu-id="232dd-132">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="232dd-132">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="232dd-133">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="232dd-133">-Capacity</span></span>
<span data-ttu-id="232dd-134">Kapacitets flaggor som används för noderna i nodtypen som nycklar/värde-par använder kluster resurs hanteraren de här taggarna för att förstå hur mycket resurs en nod har.</span><span class="sxs-lookup"><span data-stu-id="232dd-134">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span> <span data-ttu-id="232dd-135">Om du uppdaterar det här åsidosätts de aktuella värdena.</span><span class="sxs-lookup"><span data-stu-id="232dd-135">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-136">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="232dd-136">-ClusterName</span></span>
<span data-ttu-id="232dd-137">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="232dd-137">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="232dd-138">-DefaultProfile</span></span>
<span data-ttu-id="232dd-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="232dd-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="232dd-140">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="232dd-140">-EphemeralEndPort</span></span>
<span data-ttu-id="232dd-141">Tillfällig slut port för en serie portar.</span><span class="sxs-lookup"><span data-stu-id="232dd-141">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-142">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="232dd-142">-EphemeralStartPort</span></span>
<span data-ttu-id="232dd-143">Tillfällig start port för ett utbud av portar.</span><span class="sxs-lookup"><span data-stu-id="232dd-143">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-144">-ForceReimage</span><span class="sxs-lookup"><span data-stu-id="232dd-144">-ForceReimage</span></span>
<span data-ttu-id="232dd-145">Om du använder den här flaggan tvingas borttagningen även om Service Fabric inte kan inaktivera noderna.</span><span class="sxs-lookup"><span data-stu-id="232dd-145">Using this flag will force the removal even if service fabric is unable to disable the nodes.</span></span>
<span data-ttu-id="232dd-146">Använd med försiktighet eftersom det kan leda till förlust av data om tillstånds krävande arbets belastningar körs på noden.</span><span class="sxs-lookup"><span data-stu-id="232dd-146">Use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="232dd-147">-InputObject</span></span>
<span data-ttu-id="232dd-148">Resurs för nodtyp</span><span class="sxs-lookup"><span data-stu-id="232dd-148">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj, ReimageByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-149">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="232dd-149">-InstanceCount</span></span>
<span data-ttu-id="232dd-150">Antalet noder i nodtypen.</span><span class="sxs-lookup"><span data-stu-id="232dd-150">The number of nodes in the node type.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="232dd-151">-Name</span></span>
<span data-ttu-id="232dd-152">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="232dd-152">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-153">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="232dd-153">-NodeName</span></span>
<span data-ttu-id="232dd-154">Lista över nodnamn för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="232dd-154">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="232dd-155">-PassThru</span></span>
<span data-ttu-id="232dd-156">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="232dd-156">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-157">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="232dd-157">-PlacementProperty</span></span>
<span data-ttu-id="232dd-158">Placerings flaggor som används på noder i nodtypen som nycklar/värde-par, som kan användas för att ange var vissa tjänster ska köras.</span><span class="sxs-lookup"><span data-stu-id="232dd-158">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span> <span data-ttu-id="232dd-159">Om du uppdaterar det här åsidosätts de aktuella värdena.</span><span class="sxs-lookup"><span data-stu-id="232dd-159">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: WithParamsByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-160">-Ombild</span><span class="sxs-lookup"><span data-stu-id="232dd-160">-Reimage</span></span>
<span data-ttu-id="232dd-161">Ange om du vill att bilder ska ombildas.</span><span class="sxs-lookup"><span data-stu-id="232dd-161">Specify to reimage nodes on the node type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReimageByName, ReimageById, ReimageByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="232dd-162">-ResourceGroupName</span></span>
<span data-ttu-id="232dd-163">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="232dd-163">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsByName, ReimageByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-164">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="232dd-164">-ResourceId</span></span>
<span data-ttu-id="232dd-165">Resurs-ID för nodtyp</span><span class="sxs-lookup"><span data-stu-id="232dd-165">Node type resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithParamsById, ReimageById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232dd-166">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="232dd-166">-Confirm</span></span>
<span data-ttu-id="232dd-167">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="232dd-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="232dd-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="232dd-168">-WhatIf</span></span>
<span data-ttu-id="232dd-169">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="232dd-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="232dd-170">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="232dd-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="232dd-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232dd-171">CommonParameters</span></span>
<span data-ttu-id="232dd-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232dd-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232dd-173">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="232dd-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232dd-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="232dd-174">INPUTS</span></span>

### <span data-ttu-id="232dd-175">System. String</span><span class="sxs-lookup"><span data-stu-id="232dd-175">System.String</span></span>

## <span data-ttu-id="232dd-176">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="232dd-176">OUTPUTS</span></span>

### <span data-ttu-id="232dd-177">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="232dd-177">System.Boolean</span></span>

## <span data-ttu-id="232dd-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="232dd-178">NOTES</span></span>

## <span data-ttu-id="232dd-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="232dd-179">RELATED LINKS</span></span>
