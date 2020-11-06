---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: e359a99d1d420d9494b16719e61bec4d7ed670a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576571"
---
# <span data-ttu-id="5af74-101">Stop-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5af74-101">Stop-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5af74-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5af74-102">SYNOPSIS</span></span>
<span data-ttu-id="5af74-103">Stoppar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5af74-103">Stops a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5af74-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5af74-104">SYNTAX</span></span>

### <span data-ttu-id="5af74-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="5af74-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af74-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5af74-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af74-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5af74-107">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af74-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5af74-108">DESCRIPTION</span></span>
<span data-ttu-id="5af74-109">Cmdleten **Stop-AzureRmDataFactoryV2Trigger** stoppar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5af74-109">The **Stop-AzureRmDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="5af74-110">Om utlösaren är i läget startat stoppar cmdleten utlösaren och är inte längre aktive rad.</span><span class="sxs-lookup"><span data-stu-id="5af74-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="5af74-111">Om utlösaren redan är i tillståndet ' stoppad har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="5af74-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="5af74-112">Om parametern Force anges frågar inte cmdleten innan utlösaren stoppas.</span><span class="sxs-lookup"><span data-stu-id="5af74-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="5af74-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5af74-113">EXAMPLES</span></span>

### <span data-ttu-id="5af74-114">Exempel 1: stoppa en utlösare</span><span class="sxs-lookup"><span data-stu-id="5af74-114">Example 1: Stop a trigger</span></span>
```
Stop-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="5af74-115">Stoppar en utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5af74-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="5af74-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5af74-116">PARAMETERS</span></span>

### <span data-ttu-id="5af74-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5af74-117">-DataFactoryName</span></span>
<span data-ttu-id="5af74-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5af74-118">The data factory name.</span></span>

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

### <span data-ttu-id="5af74-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af74-119">-DefaultProfile</span></span>
<span data-ttu-id="5af74-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5af74-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af74-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5af74-121">-Force</span></span>
<span data-ttu-id="5af74-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5af74-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5af74-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5af74-123">-InputObject</span></span>
<span data-ttu-id="5af74-124">Utlös ande objekt att starta.</span><span class="sxs-lookup"><span data-stu-id="5af74-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="5af74-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5af74-125">-Name</span></span>
<span data-ttu-id="5af74-126">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="5af74-126">The trigger name.</span></span>

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

### <span data-ttu-id="5af74-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af74-127">-ResourceGroupName</span></span>
<span data-ttu-id="5af74-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5af74-128">The resource group name.</span></span>

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

### <span data-ttu-id="5af74-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af74-129">-ResourceId</span></span>
<span data-ttu-id="5af74-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="5af74-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5af74-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5af74-131">-Confirm</span></span>
<span data-ttu-id="5af74-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5af74-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af74-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af74-133">-WhatIf</span></span>
<span data-ttu-id="5af74-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5af74-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5af74-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af74-135">CommonParameters</span></span>
<span data-ttu-id="5af74-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af74-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af74-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af74-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af74-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5af74-138">INPUTS</span></span>

### <span data-ttu-id="5af74-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5af74-139">System.String</span></span>
<span data-ttu-id="5af74-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5af74-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5af74-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5af74-141">OUTPUTS</span></span>

### <span data-ttu-id="5af74-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5af74-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5af74-143">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5af74-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5af74-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5af74-144">NOTES</span></span>

## <span data-ttu-id="5af74-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5af74-145">RELATED LINKS</span></span>

[<span data-ttu-id="5af74-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5af74-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5af74-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5af74-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5af74-148">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5af74-148">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5af74-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5af74-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
