---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: d5ea2dee1f6023b9505c38a58d364b7aa92591db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757305"
---
# <span data-ttu-id="c52a4-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="c52a4-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="c52a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c52a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c52a4-103">Returnerar information om trigger körs.</span><span class="sxs-lookup"><span data-stu-id="c52a4-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c52a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c52a4-104">SYNTAX</span></span>

### <span data-ttu-id="c52a4-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="c52a4-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="c52a4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c52a4-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="c52a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c52a4-107">DESCRIPTION</span></span>
<span data-ttu-id="c52a4-108">Kommandot **Get-AzureRmDataFactoryV2TriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="c52a4-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="c52a4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c52a4-109">EXAMPLES</span></span>

### <span data-ttu-id="c52a4-110">Exempel 1: få information om trigger-körning</span><span class="sxs-lookup"><span data-stu-id="c52a4-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded

```

<span data-ttu-id="c52a4-111">Det här kommandot visar information om hur du kör "WikiTrigger" i fabriken "WikiADF" som startade med "2017-09-01" och "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="c52a4-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="c52a4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c52a4-112">PARAMETERS</span></span>

### <span data-ttu-id="c52a4-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c52a4-113">-DataFactory</span></span>
<span data-ttu-id="c52a4-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="c52a4-114">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c52a4-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c52a4-115">-DataFactoryName</span></span>
<span data-ttu-id="c52a4-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="c52a4-116">The data factory name.</span></span>

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

### <span data-ttu-id="c52a4-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c52a4-117">-Name</span></span>
<span data-ttu-id="c52a4-118">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="c52a4-118">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c52a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="c52a4-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c52a4-120">The resource group name.</span></span>

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

### <span data-ttu-id="c52a4-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="c52a4-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="c52a4-122">Den tid eller det klock slag då trigger körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="c52a4-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c52a4-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="c52a4-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="c52a4-124">Den tid som en utlöses innan körningen körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="c52a4-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="c52a4-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c52a4-125">INPUTS</span></span>

### <span data-ttu-id="c52a4-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c52a4-126">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="c52a4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c52a4-127">System.String</span></span>


## <span data-ttu-id="c52a4-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c52a4-128">OUTPUTS</span></span>

### <span data-ttu-id="c52a4-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c52a4-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c52a4-130">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="c52a4-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>


## <span data-ttu-id="c52a4-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c52a4-131">NOTES</span></span>

## <span data-ttu-id="c52a4-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c52a4-132">RELATED LINKS</span></span>
[<span data-ttu-id="c52a4-133">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c52a4-133">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="c52a4-134">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="c52a4-134">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

