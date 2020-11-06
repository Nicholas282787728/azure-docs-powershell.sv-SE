---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Trigger.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 3a10820bb0e4ed8c2a9ddb95bc716753a4a96ca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586564"
---
# <span data-ttu-id="24906-101">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24906-101">Remove-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="24906-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24906-102">SYNOPSIS</span></span>
<span data-ttu-id="24906-103">Tar bort en utlösare från en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="24906-103">Removes a trigger from a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24906-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24906-104">SYNTAX</span></span>

### <span data-ttu-id="24906-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="24906-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="24906-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24906-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="24906-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24906-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="24906-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24906-108">DESCRIPTION</span></span>
<span data-ttu-id="24906-109">Cmdleten **Remove-AzureRmDataFactoryV2Trigger** tar bort en utlösare från en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="24906-109">The **Remove-AzureRmDataFactoryV2Trigger** cmdlet removes a trigger from a data factory.</span></span> <span data-ttu-id="24906-110">Om parametern _Force_ anges frågar inte cmdleten innan utlösaren tas bort.</span><span class="sxs-lookup"><span data-stu-id="24906-110">If the _Force_ parameter is specified, the cmdlet doesn't prompt before removing the trigger.</span></span>

## <span data-ttu-id="24906-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24906-111">EXAMPLES</span></span>

### <span data-ttu-id="24906-112">Exempel 1: ta bort en utlösare</span><span class="sxs-lookup"><span data-stu-id="24906-112">Example 1: Remove a trigger</span></span>
```
Remove-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger"

Confirm
Are you sure you want to remove trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="24906-113">Ta bort en utlösare som heter "ScheduledTrigger" från data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="24906-113">Remove a trigger called "ScheduledTrigger" from the data factory "WikiADF".</span></span>

## <span data-ttu-id="24906-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24906-114">PARAMETERS</span></span>

### <span data-ttu-id="24906-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24906-115">-Confirm</span></span>
<span data-ttu-id="24906-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24906-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24906-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="24906-117">-DataFactoryName</span></span>
<span data-ttu-id="24906-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="24906-118">The data factory name.</span></span>

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

### <span data-ttu-id="24906-119">-Force</span><span class="sxs-lookup"><span data-stu-id="24906-119">-Force</span></span>
<span data-ttu-id="24906-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="24906-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="24906-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="24906-121">-Name</span></span>
<span data-ttu-id="24906-122">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="24906-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24906-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24906-123">-ResourceGroupName</span></span>
<span data-ttu-id="24906-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="24906-124">The resource group name.</span></span>

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

### <span data-ttu-id="24906-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24906-125">-ResourceId</span></span>
<span data-ttu-id="24906-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="24906-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24906-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24906-127">-InputObject</span></span>
<span data-ttu-id="24906-128">Det Utlös ande objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="24906-128">The Trigger object to remove.</span></span>

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

### <span data-ttu-id="24906-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24906-129">-WhatIf</span></span>
<span data-ttu-id="24906-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24906-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="24906-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24906-131">INPUTS</span></span>

### <span data-ttu-id="24906-132">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="24906-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>
<span data-ttu-id="24906-133">System. String</span><span class="sxs-lookup"><span data-stu-id="24906-133">System.String</span></span>


## <span data-ttu-id="24906-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24906-134">OUTPUTS</span></span>

### <span data-ttu-id="24906-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="24906-135">System.Object</span></span>

## <span data-ttu-id="24906-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24906-136">NOTES</span></span>

## <span data-ttu-id="24906-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24906-137">RELATED LINKS</span></span>
[<span data-ttu-id="24906-138">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24906-138">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24906-139">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24906-139">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24906-140">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24906-140">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="24906-141">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="24906-141">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

