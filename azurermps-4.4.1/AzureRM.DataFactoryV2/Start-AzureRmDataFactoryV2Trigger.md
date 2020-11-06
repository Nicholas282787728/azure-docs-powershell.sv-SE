---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 610aabd21fa1a3e7ae19430c4ce5d79d89f7ab3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586547"
---
# <span data-ttu-id="c11bd-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="c11bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c11bd-102">SYNOPSIS</span></span>

<span data-ttu-id="c11bd-103">Startar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="c11bd-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c11bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c11bd-104">SYNTAX</span></span>

### <span data-ttu-id="c11bd-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="c11bd-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c11bd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c11bd-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c11bd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c11bd-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="c11bd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c11bd-108">DESCRIPTION</span></span>

<span data-ttu-id="c11bd-109">Cmdleten **Start-AzureRmDataFactoryV2Trigger** startar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="c11bd-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="c11bd-110">Om utlösaren är i tillståndet "stoppad" startar cmdleten utlösaren och kommer slutligen till att ligga på grund val av dess definition.</span><span class="sxs-lookup"><span data-stu-id="c11bd-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="c11bd-111">Om utlösaren redan är i tillståndet start har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="c11bd-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="c11bd-112">Om parametern Force anges frågar inte cmdleten innan utlösaren startas.</span><span class="sxs-lookup"><span data-stu-id="c11bd-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>


## <span data-ttu-id="c11bd-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c11bd-113">EXAMPLES</span></span>

### <span data-ttu-id="c11bd-114">Exempel 1: starta en utlösare</span><span class="sxs-lookup"><span data-stu-id="c11bd-114">Example 1: Start a trigger</span></span>

```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="c11bd-115">Startar en utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="c11bd-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>


## <span data-ttu-id="c11bd-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c11bd-116">PARAMETERS</span></span>

### <span data-ttu-id="c11bd-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c11bd-117">-Confirm</span></span>
<span data-ttu-id="c11bd-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c11bd-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c11bd-119">-DataFactoryName</span></span>
<span data-ttu-id="c11bd-120">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="c11bd-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c11bd-121">-Force</span></span>
<span data-ttu-id="c11bd-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c11bd-122">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c11bd-123">-Name</span></span>
<span data-ttu-id="c11bd-124">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="c11bd-124">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c11bd-125">-ResourceGroupName</span></span>
<span data-ttu-id="c11bd-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c11bd-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c11bd-127">-ResourceId</span></span>
<span data-ttu-id="c11bd-128">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="c11bd-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c11bd-129">-InputObject</span></span>
<span data-ttu-id="c11bd-130">Utlös ande objekt att starta.</span><span class="sxs-lookup"><span data-stu-id="c11bd-130">Trigger object to start.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c11bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11bd-131">-WhatIf</span></span>
<span data-ttu-id="c11bd-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c11bd-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c11bd-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c11bd-133">INPUTS</span></span>

### <span data-ttu-id="c11bd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c11bd-134">System.String</span></span>
<span data-ttu-id="c11bd-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="c11bd-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c11bd-136">OUTPUTS</span></span>

### <span data-ttu-id="c11bd-137">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c11bd-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c11bd-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>


## <span data-ttu-id="c11bd-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c11bd-139">NOTES</span></span>

## <span data-ttu-id="c11bd-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c11bd-140">RELATED LINKS</span></span>
[<span data-ttu-id="c11bd-141">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-141">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c11bd-142">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-142">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c11bd-143">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-143">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c11bd-144">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c11bd-144">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
