---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269092"
---
# <span data-ttu-id="cd9f3-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cd9f3-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="cd9f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9f3-103">Ta bort en kluster resurs.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-103">Remove cluster resource.</span></span>

## <span data-ttu-id="cd9f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd9f3-104">SYNTAX</span></span>

### <span data-ttu-id="cd9f3-105">ByObj (standard)</span><span class="sxs-lookup"><span data-stu-id="cd9f3-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9f3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cd9f3-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd9f3-107">ById</span><span class="sxs-lookup"><span data-stu-id="cd9f3-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9f3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd9f3-108">DESCRIPTION</span></span>
<span data-ttu-id="cd9f3-109">Ta bort kluster det här tar bort nodtyper under klustret också.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="cd9f3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd9f3-110">EXAMPLES</span></span>

### <span data-ttu-id="cd9f3-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd9f3-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="cd9f3-112">Ta bort kluster.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-112">Remove cluster.</span></span>

### <span data-ttu-id="cd9f3-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="cd9f3-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="cd9f3-114">Ta bort kluster med rör.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="cd9f3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd9f3-115">PARAMETERS</span></span>

### <span data-ttu-id="cd9f3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd9f3-116">-AsJob</span></span>
<span data-ttu-id="cd9f3-117">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cd9f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9f3-118">-DefaultProfile</span></span>
<span data-ttu-id="cd9f3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9f3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd9f3-120">-InputObject</span></span>
<span data-ttu-id="cd9f3-121">Hanterad kluster resurs</span><span class="sxs-lookup"><span data-stu-id="cd9f3-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f3-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd9f3-122">-Name</span></span>
<span data-ttu-id="cd9f3-123">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd9f3-124">-PassThru</span></span>
<span data-ttu-id="cd9f3-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cd9f3-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="cd9f3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9f3-126">-ResourceGroupName</span></span>
<span data-ttu-id="cd9f3-127">Ange namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd9f3-128">-ResourceId</span></span>
<span data-ttu-id="cd9f3-129">Hanterat kluster resurs-ID</span><span class="sxs-lookup"><span data-stu-id="cd9f3-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9f3-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd9f3-130">-Confirm</span></span>
<span data-ttu-id="cd9f3-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9f3-132">-WhatIf</span></span>
<span data-ttu-id="cd9f3-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9f3-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9f3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9f3-135">CommonParameters</span></span>
<span data-ttu-id="cd9f3-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9f3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9f3-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd9f3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9f3-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd9f3-138">INPUTS</span></span>

### <span data-ttu-id="cd9f3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cd9f3-139">System.String</span></span>

## <span data-ttu-id="cd9f3-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd9f3-140">OUTPUTS</span></span>

### <span data-ttu-id="cd9f3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd9f3-141">System.Boolean</span></span>

## <span data-ttu-id="cd9f3-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd9f3-142">NOTES</span></span>

## <span data-ttu-id="cd9f3-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd9f3-143">RELATED LINKS</span></span>
