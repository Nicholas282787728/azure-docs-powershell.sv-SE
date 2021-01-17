---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406096"
---
# <span data-ttu-id="df95a-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="df95a-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="df95a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df95a-102">SYNOPSIS</span></span>
<span data-ttu-id="df95a-103">Initierar förberedelse för den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="df95a-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="df95a-104">Förberedelse åtgärden är på moveResources som finns i moveState "PreparePending" eller "PrepareFailed", efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.</span><span class="sxs-lookup"><span data-stu-id="df95a-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="df95a-105">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="df95a-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="df95a-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df95a-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df95a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df95a-107">DESCRIPTION</span></span>
<span data-ttu-id="df95a-108">Initierar förberedelse för den uppsättning resurser som ingår i förfrågnings texten.</span><span class="sxs-lookup"><span data-stu-id="df95a-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="df95a-109">Förberedelse åtgärden är på moveResources som finns i moveState "PreparePending" eller "PrepareFailed", efter en lyckad slut för ande är moveResource moveState en över gång till MovePending.</span><span class="sxs-lookup"><span data-stu-id="df95a-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="df95a-110">För att hjälpa användaren att vara förutsättning för att klienten kan anropa åtgärden med egenskapen validateOnly inställd på True.</span><span class="sxs-lookup"><span data-stu-id="df95a-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="df95a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df95a-111">EXAMPLES</span></span>

### <span data-ttu-id="df95a-112">Exempel 1: verifiera dependecies innan du förbereder dem</span><span class="sxs-lookup"><span data-stu-id="df95a-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="df95a-113">Verifiera dependecies innan du förbereder resursen.</span><span class="sxs-lookup"><span data-stu-id="df95a-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="df95a-114">Exempel 2: initiera förbereda för uppsättningen med resurser i flytt samlingen med "MoveResource Name" som indata</span><span class="sxs-lookup"><span data-stu-id="df95a-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="df95a-115">Börja förbereda en uppsättning resurser i flytt samlingen med "MoveResource Name" som indata.</span><span class="sxs-lookup"><span data-stu-id="df95a-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="df95a-116">Exempel 3: initiera förbereda för uppsättningen med resurser i flytt samlingen med "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="df95a-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="df95a-117">Börja förbereda en uppsättning resurser i flytt samlingen med "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="df95a-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="df95a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df95a-118">PARAMETERS</span></span>

### <span data-ttu-id="df95a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df95a-119">-AsJob</span></span>
<span data-ttu-id="df95a-120">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="df95a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="df95a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df95a-121">-DefaultProfile</span></span>
<span data-ttu-id="df95a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df95a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df95a-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="df95a-123">-MoveCollectionName</span></span>
<span data-ttu-id="df95a-124">Namn på flytta-samlingen.</span><span class="sxs-lookup"><span data-stu-id="df95a-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="df95a-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="df95a-125">-MoveResource</span></span>
<span data-ttu-id="df95a-126">Hämtar eller anger listan med resurs-ID: n som standard accepteras flytta resurs-ID om inte inmatnings typen är växlad via egenskapen moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="df95a-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="df95a-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="df95a-127">-MoveResourceInputType</span></span>
<span data-ttu-id="df95a-128">Definierar inmatnings typen för resursen.</span><span class="sxs-lookup"><span data-stu-id="df95a-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="df95a-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="df95a-129">-NoWait</span></span>
<span data-ttu-id="df95a-130">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="df95a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df95a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df95a-131">-ResourceGroupName</span></span>
<span data-ttu-id="df95a-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="df95a-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="df95a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="df95a-133">-SubscriptionId</span></span>
<span data-ttu-id="df95a-134">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="df95a-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="df95a-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="df95a-135">-ValidateOnly</span></span>
<span data-ttu-id="df95a-136">Hämtar eller anger ett värde som anger om åtgärden bara behöver köra för hands förutsättningar.</span><span class="sxs-lookup"><span data-stu-id="df95a-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="df95a-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df95a-137">-Confirm</span></span>
<span data-ttu-id="df95a-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df95a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df95a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df95a-139">-WhatIf</span></span>
<span data-ttu-id="df95a-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df95a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df95a-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df95a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df95a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df95a-142">CommonParameters</span></span>
<span data-ttu-id="df95a-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df95a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df95a-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df95a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df95a-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df95a-145">INPUTS</span></span>

## <span data-ttu-id="df95a-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df95a-146">OUTPUTS</span></span>

### <span data-ttu-id="df95a-147">Microsoft. Azure. PowerShell. cmdletar. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="df95a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="df95a-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df95a-148">NOTES</span></span>

<span data-ttu-id="df95a-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="df95a-149">ALIASES</span></span>

## <span data-ttu-id="df95a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df95a-150">RELATED LINKS</span></span>

