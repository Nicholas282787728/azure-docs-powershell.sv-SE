---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259902"
---
# <span data-ttu-id="746a2-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="746a2-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="746a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="746a2-102">SYNOPSIS</span></span>
<span data-ttu-id="746a2-103">Flyttar den uppsättning resurser som ingår i bröd texten.</span><span class="sxs-lookup"><span data-stu-id="746a2-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="746a2-104">Flytt åtgärden utlöses efter att moveResources finns i moveState "MovePending" eller "MoveFailed" efter en lyckad slut för ande är moveResource moveState en över gång till CommitPending.</span><span class="sxs-lookup"><span data-stu-id="746a2-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="746a2-105">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="746a2-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="746a2-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="746a2-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="746a2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="746a2-107">DESCRIPTION</span></span>
<span data-ttu-id="746a2-108">Flyttar den uppsättning resurser som ingår i bröd texten.</span><span class="sxs-lookup"><span data-stu-id="746a2-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="746a2-109">Flytt åtgärden utlöses efter att moveResources finns i moveState "MovePending" eller "MoveFailed" efter en lyckad slut för ande är moveResource moveState en över gång till CommitPending.</span><span class="sxs-lookup"><span data-stu-id="746a2-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="746a2-110">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="746a2-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="746a2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="746a2-111">EXAMPLES</span></span>

### <span data-ttu-id="746a2-112">Exempel 1: verifiera dependecies innan du börjar flytta till resurserna.</span><span class="sxs-lookup"><span data-stu-id="746a2-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="746a2-113">Verifiera dependecies innan du börjar flytta till resurserna.</span><span class="sxs-lookup"><span data-stu-id="746a2-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="746a2-114">Exempel 2: initiera flytt för uppsättningen med resurser i flytt samlingen med "MoveResource Name" som indata</span><span class="sxs-lookup"><span data-stu-id="746a2-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="746a2-115">Initiera flytten för uppsättningen med resurser i flytt mängden med "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="746a2-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="746a2-116">Exempel 3: initiera flytt för uppsättningen med resurser i flytt mängden med "SourceARMID" som indata</span><span class="sxs-lookup"><span data-stu-id="746a2-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="746a2-117">Initiera flytten för uppsättningen med resurser i flytt mängden med "SourceARMID" som indata.</span><span class="sxs-lookup"><span data-stu-id="746a2-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="746a2-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="746a2-118">PARAMETERS</span></span>

### <span data-ttu-id="746a2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="746a2-119">-AsJob</span></span>
<span data-ttu-id="746a2-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="746a2-120">Run the command as a job</span></span>

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

### <span data-ttu-id="746a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746a2-121">-DefaultProfile</span></span>
<span data-ttu-id="746a2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="746a2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="746a2-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="746a2-123">-MoveCollectionName</span></span>
<span data-ttu-id="746a2-124">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="746a2-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="746a2-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="746a2-125">-MoveResource</span></span>
<span data-ttu-id="746a2-126">Hämtar eller anger listan med resurs-ID: n som standard accepteras flytta resurs-ID om inte inmatnings typen är växlad via egenskapen moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="746a2-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="746a2-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="746a2-127">-MoveResourceInputType</span></span>
<span data-ttu-id="746a2-128">Definierar inmatnings typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="746a2-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="746a2-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="746a2-129">-NoWait</span></span>
<span data-ttu-id="746a2-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="746a2-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="746a2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="746a2-131">-ResourceGroupName</span></span>
<span data-ttu-id="746a2-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="746a2-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="746a2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="746a2-133">-SubscriptionId</span></span>
<span data-ttu-id="746a2-134">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="746a2-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="746a2-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="746a2-135">-ValidateOnly</span></span>
<span data-ttu-id="746a2-136">Hämtar eller anger ett värde som anger om åtgärden bara behöver köra för hands förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="746a2-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="746a2-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="746a2-137">-Confirm</span></span>
<span data-ttu-id="746a2-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="746a2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746a2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746a2-139">-WhatIf</span></span>
<span data-ttu-id="746a2-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="746a2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746a2-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="746a2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746a2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746a2-142">CommonParameters</span></span>
<span data-ttu-id="746a2-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746a2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746a2-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="746a2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746a2-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="746a2-145">INPUTS</span></span>

## <span data-ttu-id="746a2-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="746a2-146">OUTPUTS</span></span>

### <span data-ttu-id="746a2-147">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="746a2-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="746a2-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="746a2-148">NOTES</span></span>

<span data-ttu-id="746a2-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="746a2-149">ALIASES</span></span>

## <span data-ttu-id="746a2-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="746a2-150">RELATED LINKS</span></span>

