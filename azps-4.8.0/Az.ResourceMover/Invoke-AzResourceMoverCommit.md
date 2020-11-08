---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259164"
---
# <span data-ttu-id="662c6-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="662c6-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="662c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="662c6-102">SYNOPSIS</span></span>
<span data-ttu-id="662c6-103">Aktiverar den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="662c6-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="662c6-104">Commit-åtgärden utlöses på moveResources i moveState "CommitPending" eller "CommitFailed" efter en lyckad slut för ande är moveResource moveState en över gång till bekräftat.</span><span class="sxs-lookup"><span data-stu-id="662c6-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="662c6-105">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="662c6-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="662c6-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="662c6-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="662c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="662c6-107">DESCRIPTION</span></span>
<span data-ttu-id="662c6-108">Aktiverar den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="662c6-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="662c6-109">Commit-åtgärden utlöses på moveResources i moveState "CommitPending" eller "CommitFailed" efter en lyckad slut för ande är moveResource moveState en över gång till bekräftat.</span><span class="sxs-lookup"><span data-stu-id="662c6-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="662c6-110">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="662c6-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="662c6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="662c6-111">EXAMPLES</span></span>

### <span data-ttu-id="662c6-112">Exempel 1: verifiera dependecies innan du genomför resurserna</span><span class="sxs-lookup"><span data-stu-id="662c6-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="662c6-113">Verifiera dependecies innan du genomför resurserna.</span><span class="sxs-lookup"><span data-stu-id="662c6-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="662c6-114">Exempel 2: bekräfta uppsättningen med resurser i flytt samlingen med "MoveResource Name" som indata</span><span class="sxs-lookup"><span data-stu-id="662c6-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="662c6-115">Bekräfta uppsättningen av resurser i flytt samlingen med "MoveResource Name" som indata</span><span class="sxs-lookup"><span data-stu-id="662c6-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="662c6-116">Exempel 3: genomföra en uppsättning resurser i flytt mängden med "SourceARMID" som indata</span><span class="sxs-lookup"><span data-stu-id="662c6-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="662c6-117">Bekräfta uppsättningen av resurser i flytt samlingen med "SourceARMID" som indata</span><span class="sxs-lookup"><span data-stu-id="662c6-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="662c6-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="662c6-118">PARAMETERS</span></span>

### <span data-ttu-id="662c6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="662c6-119">-AsJob</span></span>
<span data-ttu-id="662c6-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="662c6-120">Run the command as a job</span></span>

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

### <span data-ttu-id="662c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="662c6-121">-DefaultProfile</span></span>
<span data-ttu-id="662c6-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="662c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="662c6-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="662c6-123">-MoveCollectionName</span></span>
<span data-ttu-id="662c6-124">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="662c6-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="662c6-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="662c6-125">-MoveResource</span></span>
<span data-ttu-id="662c6-126">Hämtar eller anger listan med resurs-ID: n som standard accepteras flytta resurs-ID om inte inmatnings typen är växlad via egenskapen moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="662c6-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="662c6-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="662c6-127">-MoveResourceInputType</span></span>
<span data-ttu-id="662c6-128">Definierar inmatnings typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="662c6-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="662c6-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="662c6-129">-NoWait</span></span>
<span data-ttu-id="662c6-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="662c6-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="662c6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="662c6-131">-ResourceGroupName</span></span>
<span data-ttu-id="662c6-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="662c6-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="662c6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="662c6-133">-SubscriptionId</span></span>
<span data-ttu-id="662c6-134">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="662c6-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="662c6-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="662c6-135">-ValidateOnly</span></span>
<span data-ttu-id="662c6-136">Hämtar eller anger ett värde som anger om åtgärden bara behöver köra för hands förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="662c6-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="662c6-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="662c6-137">-Confirm</span></span>
<span data-ttu-id="662c6-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="662c6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="662c6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="662c6-139">-WhatIf</span></span>
<span data-ttu-id="662c6-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="662c6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="662c6-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="662c6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="662c6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="662c6-142">CommonParameters</span></span>
<span data-ttu-id="662c6-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="662c6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="662c6-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="662c6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="662c6-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="662c6-145">INPUTS</span></span>

## <span data-ttu-id="662c6-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="662c6-146">OUTPUTS</span></span>

### <span data-ttu-id="662c6-147">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="662c6-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="662c6-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="662c6-148">NOTES</span></span>

<span data-ttu-id="662c6-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="662c6-149">ALIASES</span></span>

## <span data-ttu-id="662c6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="662c6-150">RELATED LINKS</span></span>

