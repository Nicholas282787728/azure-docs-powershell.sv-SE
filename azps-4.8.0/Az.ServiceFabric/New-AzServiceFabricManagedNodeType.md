---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 3e89e807acfb2507834686574931011bf398c76c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103502"
---
# <span data-ttu-id="08167-101">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="08167-101">New-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="08167-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08167-102">SYNOPSIS</span></span>
<span data-ttu-id="08167-103">Skapa en ny resurs för nodtyp.</span><span class="sxs-lookup"><span data-stu-id="08167-103">Create new node type resource.</span></span>

## <span data-ttu-id="08167-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08167-104">SYNTAX</span></span>

```
New-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -InstanceCount <Int32> [-Primary] [-DiskSize <Int32>] [-ApplicationStartPort <Int32>]
 [-ApplicationEndPort <Int32>] [-EphemeralStartPort <Int32>] [-EphemeralEndPort <Int32>] [-VmSize <String>]
 [-VmImagePublisher <String>] [-VmImageOffer <String>] [-VmImageSku <String>] [-VmImageVersion <String>]
 [-Capacity <Hashtable>] [-PlacementProperty <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08167-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08167-105">DESCRIPTION</span></span>
<span data-ttu-id="08167-106">Skapa en ny nodtyp för ett visst kluster.</span><span class="sxs-lookup"><span data-stu-id="08167-106">Create new node type resource for an specific cluster.</span></span>

## <span data-ttu-id="08167-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08167-107">EXAMPLES</span></span>

### <span data-ttu-id="08167-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08167-108">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -Primary -InstanceCount 3
```

<span data-ttu-id="08167-109">Skapa primär nodtyp med tre noder.</span><span class="sxs-lookup"><span data-stu-id="08167-109">Create primary node type with 3 nodes.</span></span>

### <span data-ttu-id="08167-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="08167-110">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
New-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName -InstanceCount 5 -Primary -PlacementProperty @{NodeColor="Green";SomeProperty="5";} -Capacity @{ClientConnections="65536";} -ApplicationStartPort 20575 -ApplicationEndPort 20605 -EphemeralStartPort 20606 -EphemeralEndPort 20861
```

<span data-ttu-id="08167-111">Skapa primär nodtyp med 5 noder och ange placerings egenskaper, kapaciteter, program och tillfälliga portar.</span><span class="sxs-lookup"><span data-stu-id="08167-111">Create primary node type with 5 nodes and specifying placement properties, capacities, application and ephemeral ports.</span></span>

## <span data-ttu-id="08167-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08167-112">PARAMETERS</span></span>

### <span data-ttu-id="08167-113">-ApplicationEndPort</span><span class="sxs-lookup"><span data-stu-id="08167-113">-ApplicationEndPort</span></span>
<span data-ttu-id="08167-114">Program slut port för en serie portar.</span><span class="sxs-lookup"><span data-stu-id="08167-114">Application End port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-115">-ApplicationStartPort</span><span class="sxs-lookup"><span data-stu-id="08167-115">-ApplicationStartPort</span></span>
<span data-ttu-id="08167-116">Start port för en serie portar.</span><span class="sxs-lookup"><span data-stu-id="08167-116">Application start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08167-117">-AsJob</span></span>
<span data-ttu-id="08167-118">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="08167-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="08167-119">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="08167-119">-Capacity</span></span>
<span data-ttu-id="08167-120">Kapacitets flaggor som används för noderna i nodtypen som nycklar/värde-par använder kluster resurs hanteraren de här taggarna för att förstå hur mycket resurs en nod har.</span><span class="sxs-lookup"><span data-stu-id="08167-120">Capacity tags applied to the nodes in the node type as key/value pairs, the cluster resource manager uses these tags to understand how much resource a node has.</span></span>
<span data-ttu-id="08167-121">Om du uppdaterar det här åsidosätts de aktuella värdena.</span><span class="sxs-lookup"><span data-stu-id="08167-121">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-122">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="08167-122">-ClusterName</span></span>
<span data-ttu-id="08167-123">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="08167-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="08167-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08167-124">-DefaultProfile</span></span>
<span data-ttu-id="08167-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08167-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08167-126">-DiskSize</span><span class="sxs-lookup"><span data-stu-id="08167-126">-DiskSize</span></span>
<span data-ttu-id="08167-127">Disk storlek för varje VM i nodtypen i GBs.</span><span class="sxs-lookup"><span data-stu-id="08167-127">Disk size for each vm in the node type in GBs.</span></span>
<span data-ttu-id="08167-128">Standard 100.</span><span class="sxs-lookup"><span data-stu-id="08167-128">Default 100.</span></span>

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

### <span data-ttu-id="08167-129">-EphemeralEndPort</span><span class="sxs-lookup"><span data-stu-id="08167-129">-EphemeralEndPort</span></span>
<span data-ttu-id="08167-130">Tillfällig slut port för en serie portar.</span><span class="sxs-lookup"><span data-stu-id="08167-130">Ephemeral end port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-131">-EphemeralStartPort</span><span class="sxs-lookup"><span data-stu-id="08167-131">-EphemeralStartPort</span></span>
<span data-ttu-id="08167-132">Tillfällig start port för ett utbud av portar.</span><span class="sxs-lookup"><span data-stu-id="08167-132">Ephemeral start port of a range of ports.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-133">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="08167-133">-InstanceCount</span></span>
<span data-ttu-id="08167-134">Antalet noder i nodtypen.</span><span class="sxs-lookup"><span data-stu-id="08167-134">The number of nodes in the node type.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="08167-135">-Name</span></span>
<span data-ttu-id="08167-136">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="08167-136">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08167-137">-PlacementProperty</span><span class="sxs-lookup"><span data-stu-id="08167-137">-PlacementProperty</span></span>
<span data-ttu-id="08167-138">Placerings flaggor som används på noder i nodtypen som nycklar/värde-par, som kan användas för att ange var vissa tjänster ska köras.</span><span class="sxs-lookup"><span data-stu-id="08167-138">Placement tags applied to nodes in the node type as key/value pairs, which can be used to indicate where certain services (workload) should run.</span></span>
<span data-ttu-id="08167-139">Om du uppdaterar det här åsidosätts de aktuella värdena.</span><span class="sxs-lookup"><span data-stu-id="08167-139">Updating this will override the current values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-140">-Primär</span><span class="sxs-lookup"><span data-stu-id="08167-140">-Primary</span></span>
<span data-ttu-id="08167-141">Ange om nodtypen är primär.</span><span class="sxs-lookup"><span data-stu-id="08167-141">Specify if the node type is primary.</span></span>
<span data-ttu-id="08167-142">På den här nodtypen körs system tjänster.</span><span class="sxs-lookup"><span data-stu-id="08167-142">On this node type will run system services.</span></span>
<span data-ttu-id="08167-143">Endast en nodtyp ska vara markerad som primär.</span><span class="sxs-lookup"><span data-stu-id="08167-143">Only one node type should be marked as primary.</span></span>
<span data-ttu-id="08167-144">Det går inte att ta bort eller ändra primär nodtyp för befintliga kluster.</span><span class="sxs-lookup"><span data-stu-id="08167-144">Primary node type cannot be deleted or changed for existing clusters.</span></span>

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

### <span data-ttu-id="08167-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08167-145">-ResourceGroupName</span></span>
<span data-ttu-id="08167-146">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="08167-146">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="08167-147">-VmImageOffer</span><span class="sxs-lookup"><span data-stu-id="08167-147">-VmImageOffer</span></span>
<span data-ttu-id="08167-148">Utbuds typen för Marketplace för Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="08167-148">The offer type of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="08167-149">Standard: WindowsServer.</span><span class="sxs-lookup"><span data-stu-id="08167-149">Default: WindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "WindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-150">-VmImagePublisher</span><span class="sxs-lookup"><span data-stu-id="08167-150">-VmImagePublisher</span></span>
<span data-ttu-id="08167-151">Utgivaren av Marketplace för Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="08167-151">The publisher of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="08167-152">Standard: MicrosoftWindowsServer.</span><span class="sxs-lookup"><span data-stu-id="08167-152">Default: MicrosoftWindowsServer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "MicrosoftWindowsServer"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-153">-VmImageSku</span><span class="sxs-lookup"><span data-stu-id="08167-153">-VmImageSku</span></span>
<span data-ttu-id="08167-154">SKU för Marketplace-avbildningsfilen för Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="08167-154">The SKU of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="08167-155">Standard: 2019-datacenter.</span><span class="sxs-lookup"><span data-stu-id="08167-155">Default: 2019-Datacenter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "2019-Datacenter"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-156">-VmImageVersion</span><span class="sxs-lookup"><span data-stu-id="08167-156">-VmImageVersion</span></span>
<span data-ttu-id="08167-157">Versionen av Marketplace för Azure Virtual Machines.</span><span class="sxs-lookup"><span data-stu-id="08167-157">The version of the Azure Virtual Machines Marketplace image.</span></span>
<span data-ttu-id="08167-158">Standard: senaste.</span><span class="sxs-lookup"><span data-stu-id="08167-158">Default: latest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "latest"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-159">-VmSize</span><span class="sxs-lookup"><span data-stu-id="08167-159">-VmSize</span></span>
<span data-ttu-id="08167-160">Storleken på virtuella datorer i poolen.</span><span class="sxs-lookup"><span data-stu-id="08167-160">The size of virtual machines in the pool.</span></span>
<span data-ttu-id="08167-161">Alla virtuella datorer i en pool har samma storlek.</span><span class="sxs-lookup"><span data-stu-id="08167-161">All virtual machines in a pool are the same size.</span></span>
<span data-ttu-id="08167-162">Standard: Standard_D2.</span><span class="sxs-lookup"><span data-stu-id="08167-162">Default: Standard_D2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "Standard_D2"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08167-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08167-163">-Confirm</span></span>
<span data-ttu-id="08167-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08167-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08167-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08167-165">-WhatIf</span></span>
<span data-ttu-id="08167-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08167-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08167-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08167-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08167-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08167-168">CommonParameters</span></span>
<span data-ttu-id="08167-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08167-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08167-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08167-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08167-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08167-171">INPUTS</span></span>

### <span data-ttu-id="08167-172">System. String</span><span class="sxs-lookup"><span data-stu-id="08167-172">System.String</span></span>

## <span data-ttu-id="08167-173">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08167-173">OUTPUTS</span></span>

### <span data-ttu-id="08167-174">Microsoft. Azure. commands. ServiceFabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="08167-174">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="08167-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08167-175">NOTES</span></span>

## <span data-ttu-id="08167-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08167-176">RELATED LINKS</span></span>
