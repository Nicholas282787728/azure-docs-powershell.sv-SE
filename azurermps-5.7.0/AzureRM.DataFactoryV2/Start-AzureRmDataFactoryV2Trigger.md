---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: ed4769c26363c60aace191d439d4a450a894eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755772"
---
# <span data-ttu-id="80a68-101">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80a68-101">Start-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="80a68-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80a68-102">SYNOPSIS</span></span>
<span data-ttu-id="80a68-103">Startar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="80a68-103">Starts a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80a68-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80a68-104">SYNTAX</span></span>

### <span data-ttu-id="80a68-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="80a68-105">ByFactoryName (Default)</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a68-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="80a68-106">ByInputObject</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-InputObject] <PSTrigger> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80a68-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="80a68-107">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2Trigger [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80a68-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80a68-108">DESCRIPTION</span></span>
<span data-ttu-id="80a68-109">Cmdleten **Start-AzureRmDataFactoryV2Trigger** startar en utlösare i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="80a68-109">The **Start-AzureRmDataFactoryV2Trigger** cmdlet starts a trigger in a data factory.</span></span> <span data-ttu-id="80a68-110">Om utlösaren är i tillståndet "stoppad" startar cmdleten utlösaren och kommer slutligen till att ligga på grund val av dess definition.</span><span class="sxs-lookup"><span data-stu-id="80a68-110">If the trigger is in the 'Stopped' state, the cmdlet starts the trigger and it eventually invokes pipelines based on its definition.</span></span> <span data-ttu-id="80a68-111">Om utlösaren redan är i tillståndet start har denna cmdlet ingen effekt.</span><span class="sxs-lookup"><span data-stu-id="80a68-111">If the trigger is already in the 'Started' state, this cmdlet has no effect.</span></span> <span data-ttu-id="80a68-112">Om parametern Force anges frågar inte cmdleten innan utlösaren startas.</span><span class="sxs-lookup"><span data-stu-id="80a68-112">If the Force parameter is specified, the cmdlet doesn't prompt before starting the trigger.</span></span>

## <span data-ttu-id="80a68-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80a68-113">EXAMPLES</span></span>

### <span data-ttu-id="80a68-114">Exempel 1: starta en utlösare</span><span class="sxs-lookup"><span data-stu-id="80a68-114">Example 1: Start a trigger</span></span>
```
Start-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "ScheduledTrigger"

Confirm
Are you sure you want to start trigger 'ScheduledTrigger' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="80a68-115">Startar en utlösare som heter "ScheduledTrigger" i data fabriken "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="80a68-115">Starts a trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span>

## <span data-ttu-id="80a68-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80a68-116">PARAMETERS</span></span>

### <span data-ttu-id="80a68-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="80a68-117">-DataFactoryName</span></span>
<span data-ttu-id="80a68-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="80a68-118">The data factory name.</span></span>

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

### <span data-ttu-id="80a68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a68-119">-DefaultProfile</span></span>
<span data-ttu-id="80a68-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="80a68-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a68-121">-Force</span><span class="sxs-lookup"><span data-stu-id="80a68-121">-Force</span></span>
<span data-ttu-id="80a68-122">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="80a68-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="80a68-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80a68-123">-InputObject</span></span>
<span data-ttu-id="80a68-124">Utlös ande objekt att starta.</span><span class="sxs-lookup"><span data-stu-id="80a68-124">Trigger object to start.</span></span>

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

### <span data-ttu-id="80a68-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="80a68-125">-Name</span></span>
<span data-ttu-id="80a68-126">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="80a68-126">The trigger name.</span></span>

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

### <span data-ttu-id="80a68-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80a68-127">-ResourceGroupName</span></span>
<span data-ttu-id="80a68-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="80a68-128">The resource group name.</span></span>

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

### <span data-ttu-id="80a68-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80a68-129">-ResourceId</span></span>
<span data-ttu-id="80a68-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="80a68-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="80a68-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="80a68-131">-Confirm</span></span>
<span data-ttu-id="80a68-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80a68-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80a68-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80a68-133">-WhatIf</span></span>
<span data-ttu-id="80a68-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="80a68-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="80a68-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a68-135">CommonParameters</span></span>
<span data-ttu-id="80a68-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80a68-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a68-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a68-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a68-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80a68-138">INPUTS</span></span>

### <span data-ttu-id="80a68-139">System. String</span><span class="sxs-lookup"><span data-stu-id="80a68-139">System.String</span></span>
<span data-ttu-id="80a68-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="80a68-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="80a68-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80a68-141">OUTPUTS</span></span>

### <span data-ttu-id="80a68-142">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="80a68-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="80a68-143">Microsoft. Azure. commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="80a68-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="80a68-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80a68-144">NOTES</span></span>

## <span data-ttu-id="80a68-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80a68-145">RELATED LINKS</span></span>

[<span data-ttu-id="80a68-146">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80a68-146">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="80a68-147">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80a68-147">Set-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="80a68-148">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80a68-148">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="80a68-149">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="80a68-149">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
