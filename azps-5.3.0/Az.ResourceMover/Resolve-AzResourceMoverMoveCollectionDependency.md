---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521640"
---
# <span data-ttu-id="1842e-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="1842e-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="1842e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1842e-102">SYNOPSIS</span></span>
<span data-ttu-id="1842e-103">Beräknar, löser och validerar beroendena för moveResources i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="1842e-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="1842e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1842e-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1842e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1842e-105">DESCRIPTION</span></span>
<span data-ttu-id="1842e-106">Beräknar, löser och validerar beroendena för moveResources i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="1842e-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="1842e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1842e-107">EXAMPLES</span></span>

### <span data-ttu-id="1842e-108">Exempel 1: beräknar, matchar och validerar beroenden på moveresources i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="1842e-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="1842e-109">Beräknar, löser och validerar beroendena för moveresources i flytt mängden.</span><span class="sxs-lookup"><span data-stu-id="1842e-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="1842e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1842e-110">PARAMETERS</span></span>

### <span data-ttu-id="1842e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1842e-111">-AsJob</span></span>
<span data-ttu-id="1842e-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1842e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1842e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1842e-113">-DefaultProfile</span></span>
<span data-ttu-id="1842e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1842e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1842e-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1842e-115">-MoveCollectionName</span></span>
<span data-ttu-id="1842e-116">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="1842e-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1842e-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1842e-117">-NoWait</span></span>
<span data-ttu-id="1842e-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1842e-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1842e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1842e-119">-ResourceGroupName</span></span>
<span data-ttu-id="1842e-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1842e-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1842e-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1842e-121">-SubscriptionId</span></span>
<span data-ttu-id="1842e-122">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="1842e-122">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1842e-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1842e-123">-Confirm</span></span>
<span data-ttu-id="1842e-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1842e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1842e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1842e-125">-WhatIf</span></span>
<span data-ttu-id="1842e-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1842e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1842e-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1842e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1842e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1842e-128">CommonParameters</span></span>
<span data-ttu-id="1842e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1842e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1842e-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1842e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1842e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1842e-131">INPUTS</span></span>

## <span data-ttu-id="1842e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1842e-132">OUTPUTS</span></span>

### <span data-ttu-id="1842e-133">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="1842e-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="1842e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1842e-134">NOTES</span></span>

<span data-ttu-id="1842e-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1842e-135">ALIASES</span></span>

## <span data-ttu-id="1842e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1842e-136">RELATED LINKS</span></span>

