---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260416"
---
# <span data-ttu-id="cc383-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="cc383-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="cc383-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc383-102">SYNOPSIS</span></span>
<span data-ttu-id="cc383-103">Tar bort den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="cc383-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="cc383-104">Åtgärden ta bort utlöses på moveResources i moveState "CommitPending" eller "DiscardFailed" efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.</span><span class="sxs-lookup"><span data-stu-id="cc383-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="cc383-105">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="cc383-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="cc383-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc383-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc383-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc383-107">DESCRIPTION</span></span>
<span data-ttu-id="cc383-108">Tar bort den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="cc383-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="cc383-109">Åtgärden ta bort utlöses på moveResources i moveState "CommitPending" eller "DiscardFailed" efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.</span><span class="sxs-lookup"><span data-stu-id="cc383-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="cc383-110">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="cc383-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="cc383-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc383-111">EXAMPLES</span></span>

### <span data-ttu-id="cc383-112">Exempel 1: verifiera dependecies innan du tar bort resurserna.</span><span class="sxs-lookup"><span data-stu-id="cc383-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="cc383-113">Verifiera dependecies innan du tar bort resurserna.</span><span class="sxs-lookup"><span data-stu-id="cc383-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="cc383-114">Exempel 2: tar bort resursernas förflyttning med "MoveResource Name" som indata</span><span class="sxs-lookup"><span data-stu-id="cc383-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="cc383-115">Tar bort resursernas förflyttning med "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="cc383-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="cc383-116">Exempel 3: tar bort flytten av resurserna med "SourceARMID" som indata</span><span class="sxs-lookup"><span data-stu-id="cc383-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="cc383-117">Ignorerar flytten av resurserna med "SourceARMID" som indata.</span><span class="sxs-lookup"><span data-stu-id="cc383-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="cc383-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc383-118">PARAMETERS</span></span>

### <span data-ttu-id="cc383-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc383-119">-AsJob</span></span>
<span data-ttu-id="cc383-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="cc383-120">Run the command as a job</span></span>

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

### <span data-ttu-id="cc383-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc383-121">-DefaultProfile</span></span>
<span data-ttu-id="cc383-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cc383-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc383-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="cc383-123">-MoveResource</span></span>
<span data-ttu-id="cc383-124">Hämtar eller anger listan med resurs-ID: n som standard accepteras flytta resurs-ID om inte inmatnings typen är växlad via egenskapen moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="cc383-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="cc383-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="cc383-125">-MoveResourceInputType</span></span>
<span data-ttu-id="cc383-126">Definierar inmatnings typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="cc383-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="cc383-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="cc383-127">-Name</span></span>
<span data-ttu-id="cc383-128">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="cc383-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="cc383-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="cc383-129">-NoWait</span></span>
<span data-ttu-id="cc383-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="cc383-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc383-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc383-131">-ResourceGroupName</span></span>
<span data-ttu-id="cc383-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cc383-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="cc383-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc383-133">-SubscriptionId</span></span>
<span data-ttu-id="cc383-134">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="cc383-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="cc383-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="cc383-135">-ValidateOnly</span></span>
<span data-ttu-id="cc383-136">Hämtar eller anger ett värde som anger om åtgärden bara behöver köra för hands förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="cc383-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="cc383-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc383-137">-Confirm</span></span>
<span data-ttu-id="cc383-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc383-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc383-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc383-139">-WhatIf</span></span>
<span data-ttu-id="cc383-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc383-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc383-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc383-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc383-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc383-142">CommonParameters</span></span>
<span data-ttu-id="cc383-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc383-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc383-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc383-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc383-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc383-145">INPUTS</span></span>

## <span data-ttu-id="cc383-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc383-146">OUTPUTS</span></span>

### <span data-ttu-id="cc383-147">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="cc383-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="cc383-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc383-148">NOTES</span></span>

<span data-ttu-id="cc383-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cc383-149">ALIASES</span></span>

## <span data-ttu-id="cc383-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc383-150">RELATED LINKS</span></span>
