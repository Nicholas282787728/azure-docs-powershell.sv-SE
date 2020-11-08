---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258718"
---
# <span data-ttu-id="4f4ec-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="4f4ec-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="4f4ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f4ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4ec-103">Tar bort en flytt resurs från flytt samlingen.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="4f4ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f4ec-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4f4ec-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f4ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4f4ec-106">Tar bort en flytt resurs från flytt samlingen.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="4f4ec-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f4ec-107">EXAMPLES</span></span>

### <span data-ttu-id="4f4ec-108">Exempel 1: ta bort resursen från flytt samlingen</span><span class="sxs-lookup"><span data-stu-id="4f4ec-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="4f4ec-109">Ta bort resursen från flytt samlingen inom det angivna abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="4f4ec-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f4ec-110">PARAMETERS</span></span>

### <span data-ttu-id="4f4ec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f4ec-111">-AsJob</span></span>
<span data-ttu-id="4f4ec-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="4f4ec-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4f4ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4ec-113">-DefaultProfile</span></span>
<span data-ttu-id="4f4ec-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f4ec-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="4f4ec-115">-MoveCollectionName</span></span>
<span data-ttu-id="4f4ec-116">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4f4ec-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f4ec-117">-Name</span></span>
<span data-ttu-id="4f4ec-118">Namnet på den flyttade resursen.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f4ec-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4f4ec-119">-NoWait</span></span>
<span data-ttu-id="4f4ec-120">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="4f4ec-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4f4ec-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f4ec-121">-PassThru</span></span>
<span data-ttu-id="4f4ec-122">Returnerar true när kommandot lyckas</span><span class="sxs-lookup"><span data-stu-id="4f4ec-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4f4ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f4ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f4ec-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4f4ec-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f4ec-125">-SubscriptionId</span></span>
<span data-ttu-id="4f4ec-126">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="4f4ec-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f4ec-127">-Confirm</span></span>
<span data-ttu-id="4f4ec-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f4ec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f4ec-129">-WhatIf</span></span>
<span data-ttu-id="4f4ec-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f4ec-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f4ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4ec-132">CommonParameters</span></span>
<span data-ttu-id="4f4ec-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4ec-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f4ec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4ec-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f4ec-135">INPUTS</span></span>

## <span data-ttu-id="4f4ec-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f4ec-136">OUTPUTS</span></span>

### <span data-ttu-id="4f4ec-137">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="4f4ec-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="4f4ec-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f4ec-138">NOTES</span></span>

<span data-ttu-id="4f4ec-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4f4ec-139">ALIASES</span></span>

## <span data-ttu-id="4f4ec-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f4ec-140">RELATED LINKS</span></span>

