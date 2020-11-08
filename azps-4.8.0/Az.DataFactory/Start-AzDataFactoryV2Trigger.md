---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 2a47676324f2955d02c2d50ff83d564ea150d818
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260560"
---
# <span data-ttu-id="9cbe3-101">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-101">Start-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="9cbe3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9cbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbe3-103">Startar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-103">Starts a trigger in a data factory.</span></span>

## <span data-ttu-id="9cbe3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9cbe3-104">SYNTAX</span></span>

### <span data-ttu-id="9cbe3-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9cbe3-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cbe3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9cbe3-106">ByInputObject</span></span>
```
Start-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cbe3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9cbe3-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cbe3-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9cbe3-108">DESCRIPTION</span></span>
<span data-ttu-id="9cbe3-109">Cmdleten **Start-AzDataFactoryV2Trigger** startar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-109">The **Start-AzDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="9cbe3-110">Om utlösaren är i tillståndet "stoppad" startar cmdleten utlösaren och kommer slutligen till att ligga på grund val av dess definition.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="9cbe3-111">Om utlösaren redan är i tillståndet start har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="9cbe3-112">Om parametern Force anges frågar inte cmdleten innan utlösaren startas.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="9cbe3-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9cbe3-113">EXAMPLES</span></span>

### <span data-ttu-id="9cbe3-114">Exempel 1: starta en utlösare</span><span class="sxs-lookup"><span data-stu-id="9cbe3-114">Example 1: Start a trigger</span></span>
```
Start-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="9cbe3-115">Startar en utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="9cbe3-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="9cbe3-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9cbe3-116">PARAMETERS</span></span>

### <span data-ttu-id="9cbe3-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9cbe3-117">-DataFactoryName</span></span>
<span data-ttu-id="9cbe3-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbe3-119">-DefaultProfile</span></span>
<span data-ttu-id="9cbe3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9cbe3-121">-Force</span></span>
<span data-ttu-id="9cbe3-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9cbe3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cbe3-123">-InputObject</span></span>
<span data-ttu-id="9cbe3-124">Utlös ande objekt att starta.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-124">Trigger object to start.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe3-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="9cbe3-125">-Name</span></span>
<span data-ttu-id="9cbe3-126">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-126">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbe3-127">-ResourceGroupName</span></span>
<span data-ttu-id="9cbe3-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cbe3-129">-ResourceId</span></span>
<span data-ttu-id="9cbe3-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-130">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cbe3-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9cbe3-131">-Confirm</span></span>
<span data-ttu-id="9cbe3-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cbe3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cbe3-133">-WhatIf</span></span>
<span data-ttu-id="9cbe3-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="9cbe3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbe3-135">CommonParameters</span></span>
<span data-ttu-id="9cbe3-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cbe3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbe3-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cbe3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbe3-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9cbe3-138">INPUTS</span></span>

### <span data-ttu-id="9cbe3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbe3-139">System.String</span></span>

### <span data-ttu-id="9cbe3-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9cbe3-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9cbe3-141">OUTPUTS</span></span>

### <span data-ttu-id="9cbe3-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9cbe3-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9cbe3-143">NOTES</span></span>

## <span data-ttu-id="9cbe3-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9cbe3-144">RELATED LINKS</span></span>

[<span data-ttu-id="9cbe3-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9cbe3-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9cbe3-147">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-147">Stop-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9cbe3-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9cbe3-148">Remove-AzDataFactoryV2Trigger</span></span>]()
