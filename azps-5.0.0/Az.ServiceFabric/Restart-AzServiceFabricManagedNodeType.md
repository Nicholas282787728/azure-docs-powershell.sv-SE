---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269083"
---
# <span data-ttu-id="68eaf-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="68eaf-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="68eaf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="68eaf-103">Starta om specifika noder från nodtypen.</span><span class="sxs-lookup"><span data-stu-id="68eaf-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="68eaf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68eaf-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68eaf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="68eaf-106">Starta om specifika noder från nodtypen.</span><span class="sxs-lookup"><span data-stu-id="68eaf-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="68eaf-107">Den inaktive ras av tjänstens Fabric-noder innan de startas om och du aktiverade dem igen när de kommer tillbaka.</span><span class="sxs-lookup"><span data-stu-id="68eaf-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="68eaf-108">Om det sker på primära nodtyper kan det ta en stund eftersom det inte går att starta om alla noder samtidigt.</span><span class="sxs-lookup"><span data-stu-id="68eaf-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="68eaf-109">Use-ForceRestart tvinga åtgärden även om Service Fabric inte kan inaktivera noderna men använda försiktighet eftersom det kan orsaka data förlust om tillstånds krävande arbets belastningar körs på noden.</span><span class="sxs-lookup"><span data-stu-id="68eaf-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="68eaf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68eaf-110">EXAMPLES</span></span>

### <span data-ttu-id="68eaf-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="68eaf-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="68eaf-112">Starta om nod 0 och 3 på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="68eaf-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="68eaf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68eaf-113">PARAMETERS</span></span>

### <span data-ttu-id="68eaf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68eaf-114">-AsJob</span></span>
<span data-ttu-id="68eaf-115">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="68eaf-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="68eaf-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="68eaf-116">-ClusterName</span></span>
<span data-ttu-id="68eaf-117">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="68eaf-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="68eaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68eaf-118">-DefaultProfile</span></span>
<span data-ttu-id="68eaf-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="68eaf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68eaf-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="68eaf-120">-ForceRestart</span></span>
<span data-ttu-id="68eaf-121">Om du använder den här flaggan måste du starta om noden även om Service Fabric inte kan inaktivera noderna.</span><span class="sxs-lookup"><span data-stu-id="68eaf-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="68eaf-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="68eaf-122">-Name</span></span>
<span data-ttu-id="68eaf-123">Ange namnet på nodtypen.</span><span class="sxs-lookup"><span data-stu-id="68eaf-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68eaf-124">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="68eaf-124">-NodeName</span></span>
<span data-ttu-id="68eaf-125">Lista över nodnamn för åtgärden.</span><span class="sxs-lookup"><span data-stu-id="68eaf-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68eaf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68eaf-126">-PassThru</span></span>
<span data-ttu-id="68eaf-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="68eaf-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="68eaf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68eaf-128">-ResourceGroupName</span></span>
<span data-ttu-id="68eaf-129">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="68eaf-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="68eaf-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="68eaf-130">-Confirm</span></span>
<span data-ttu-id="68eaf-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="68eaf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68eaf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68eaf-132">-WhatIf</span></span>
<span data-ttu-id="68eaf-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="68eaf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68eaf-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="68eaf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68eaf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68eaf-135">CommonParameters</span></span>
<span data-ttu-id="68eaf-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68eaf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68eaf-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68eaf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68eaf-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68eaf-138">INPUTS</span></span>

### <span data-ttu-id="68eaf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="68eaf-139">System.String</span></span>

## <span data-ttu-id="68eaf-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68eaf-140">OUTPUTS</span></span>

### <span data-ttu-id="68eaf-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68eaf-141">System.Boolean</span></span>

## <span data-ttu-id="68eaf-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68eaf-142">NOTES</span></span>

## <span data-ttu-id="68eaf-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68eaf-143">RELATED LINKS</span></span>
