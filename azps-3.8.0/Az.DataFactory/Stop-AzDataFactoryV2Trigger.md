---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2Trigger.md
ms.openlocfilehash: 80e9ed345b9d1b80dd75be2036826559ac3bbb9a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927665"
---
# <span data-ttu-id="ed516-101">Stop-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed516-101">Stop-AzDataFactoryV2Trigger</span></span>

## <span data-ttu-id="ed516-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed516-102">SYNOPSIS</span></span>
<span data-ttu-id="ed516-103">Stoppar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ed516-103">Stops a trigger in a data factory.</span></span>

## <span data-ttu-id="ed516-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed516-104">SYNTAX</span></span>

### <span data-ttu-id="ed516-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ed516-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed516-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed516-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed516-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed516-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed516-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed516-108">DESCRIPTION</span></span>
<span data-ttu-id="ed516-109">Cmdleten **Stop-AzDataFactoryV2Trigger** stoppar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ed516-109">The **Stop-AzDataFactoryV2Trigger** cmdlet stops a trigger in a data factory.</span></span> <span data-ttu-id="ed516-110">Om utlösaren är i läget startat stoppar cmdleten utlösaren och är inte längre aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ed516-110">If the trigger is in the 'Started' state, the cmdlet stops the trigger and no longer invokes pipelines.</span></span> <span data-ttu-id="ed516-111">Om utlösaren redan är i tillståndet ' stoppad har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="ed516-111">If the trigger is already in the 'Stopped' state, this cmdlet has no effect.</span></span> <span data-ttu-id="ed516-112">Om parametern Force anges frågar inte cmdleten innan utlösaren stoppas.</span><span class="sxs-lookup"><span data-stu-id="ed516-112">If the Force parameter is specified, the cmdlet doesn't prompt before stopping the trigger.</span></span>

## <span data-ttu-id="ed516-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed516-113">EXAMPLES</span></span>

### <span data-ttu-id="ed516-114">Exempel 1: stoppa en utlösare</span><span class="sxs-lookup"><span data-stu-id="ed516-114">Example 1: Stop a trigger</span></span>
```
Stop-AzDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to stop trigger 'ScheduledTrigger' in data factory 'TestFactory'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ed516-115">Stoppar en utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="ed516-115">Stops a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="ed516-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed516-116">PARAMETERS</span></span>

### <span data-ttu-id="ed516-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ed516-117">-DataFactoryName</span></span>
<span data-ttu-id="ed516-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ed516-118">The data factory name.</span></span>

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

### <span data-ttu-id="ed516-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed516-119">-DefaultProfile</span></span>
<span data-ttu-id="ed516-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed516-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed516-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ed516-121">-Force</span></span>
<span data-ttu-id="ed516-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ed516-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ed516-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed516-123">-InputObject</span></span>
<span data-ttu-id="ed516-124">Utlös ande objekt att starta.</span><span class="sxs-lookup"><span data-stu-id="ed516-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="ed516-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed516-125">-Name</span></span>
<span data-ttu-id="ed516-126">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="ed516-126">The trigger name.</span></span>

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

### <span data-ttu-id="ed516-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed516-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed516-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ed516-128">The resource group name.</span></span>

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

### <span data-ttu-id="ed516-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed516-129">-ResourceId</span></span>
<span data-ttu-id="ed516-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="ed516-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ed516-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed516-131">-Confirm</span></span>
<span data-ttu-id="ed516-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed516-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed516-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed516-133">-WhatIf</span></span>
<span data-ttu-id="ed516-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed516-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ed516-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed516-135">CommonParameters</span></span>
<span data-ttu-id="ed516-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed516-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed516-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed516-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed516-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed516-138">INPUTS</span></span>

### <span data-ttu-id="ed516-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ed516-139">System.String</span></span>

### <span data-ttu-id="ed516-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="ed516-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ed516-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed516-141">OUTPUTS</span></span>

### <span data-ttu-id="ed516-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="ed516-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ed516-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed516-143">NOTES</span></span>

## <span data-ttu-id="ed516-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed516-144">RELATED LINKS</span></span>

[<span data-ttu-id="ed516-145">Get-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed516-145">Get-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ed516-146">Set-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed516-146">Set-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ed516-147">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed516-147">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ed516-148">Remove-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed516-148">Remove-AzDataFactoryV2Trigger</span></span>]()
