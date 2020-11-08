---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261733"
---
# <span data-ttu-id="ae826-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="ae826-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="ae826-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae826-102">SYNOPSIS</span></span>
<span data-ttu-id="ae826-103">Tar bort en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="ae826-103">Deletes a move collection.</span></span>

## <span data-ttu-id="ae826-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae826-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae826-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae826-105">DESCRIPTION</span></span>
<span data-ttu-id="ae826-106">Tar bort en flytt mängd.</span><span class="sxs-lookup"><span data-stu-id="ae826-106">Deletes a move collection.</span></span>

## <span data-ttu-id="ae826-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae826-107">EXAMPLES</span></span>

### <span data-ttu-id="ae826-108">Exempel 1: ta bort flytt samlingen från det angivna abonnemanget</span><span class="sxs-lookup"><span data-stu-id="ae826-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="ae826-109">Ta bort flytt samlingen från det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="ae826-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="ae826-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae826-110">PARAMETERS</span></span>

### <span data-ttu-id="ae826-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae826-111">-AsJob</span></span>
<span data-ttu-id="ae826-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ae826-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ae826-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae826-113">-DefaultProfile</span></span>
<span data-ttu-id="ae826-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae826-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae826-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae826-115">-Name</span></span>
<span data-ttu-id="ae826-116">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="ae826-116">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae826-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ae826-117">-NoWait</span></span>
<span data-ttu-id="ae826-118">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ae826-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae826-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae826-119">-PassThru</span></span>
<span data-ttu-id="ae826-120">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="ae826-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ae826-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae826-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae826-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ae826-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ae826-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae826-123">-SubscriptionId</span></span>
<span data-ttu-id="ae826-124">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="ae826-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="ae826-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ae826-125">-Confirm</span></span>
<span data-ttu-id="ae826-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae826-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae826-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae826-127">-WhatIf</span></span>
<span data-ttu-id="ae826-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ae826-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae826-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ae826-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae826-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae826-130">CommonParameters</span></span>
<span data-ttu-id="ae826-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae826-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae826-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae826-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae826-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae826-133">INPUTS</span></span>

## <span data-ttu-id="ae826-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae826-134">OUTPUTS</span></span>

### <span data-ttu-id="ae826-135">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ae826-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="ae826-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae826-136">NOTES</span></span>

<span data-ttu-id="ae826-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ae826-137">ALIASES</span></span>

## <span data-ttu-id="ae826-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae826-138">RELATED LINKS</span></span>

