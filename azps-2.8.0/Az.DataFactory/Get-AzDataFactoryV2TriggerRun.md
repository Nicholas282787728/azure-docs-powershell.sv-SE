---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 3f98ff38d5e74b7b167dc3a168a1cc05a42a7a23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744767"
---
# <span data-ttu-id="a03a7-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="a03a7-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="a03a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a03a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a03a7-103">Returnerar information om trigger körs.</span><span class="sxs-lookup"><span data-stu-id="a03a7-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="a03a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a03a7-104">SYNTAX</span></span>

### <span data-ttu-id="a03a7-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="a03a7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a03a7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a03a7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a03a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a03a7-107">DESCRIPTION</span></span>
<span data-ttu-id="a03a7-108">Kommandot **Get-AzDataFactoryV2TriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="a03a7-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="a03a7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a03a7-109">EXAMPLES</span></span>

### <span data-ttu-id="a03a7-110">Exempel 1: få information om trigger-körning</span><span class="sxs-lookup"><span data-stu-id="a03a7-110">Example 1: Get information about trigger run</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "WikiTrigger" -TriggerRunStartedAfter "2017-09-01" -TriggerRunStartedBefore "2019-09-30"

    ResourceGroupName   : ADF
    DataFactoryName     : WikiADF
    TriggerName         : WikiTrigger
    TriggerRunId        : 08586958400454144995526033731
    TriggerType         : ScheduleTrigger
    TriggerRunTimestamp : 9/18/2017 8:34:00 PM
    Status              : Succeeded
```

<span data-ttu-id="a03a7-111">Det här kommandot visar information om hur du kör "WikiTrigger" i fabriken "WikiADF" som startade med "2017-09-01" och "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="a03a7-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="a03a7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a03a7-112">PARAMETERS</span></span>

### <span data-ttu-id="a03a7-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a03a7-113">-DataFactory</span></span>
<span data-ttu-id="a03a7-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="a03a7-114">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a03a7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a03a7-115">-DataFactoryName</span></span>
<span data-ttu-id="a03a7-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="a03a7-116">The data factory name.</span></span>

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

### <span data-ttu-id="a03a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03a7-117">-DefaultProfile</span></span>
<span data-ttu-id="a03a7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a03a7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a03a7-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a03a7-119">-Name</span></span>
<span data-ttu-id="a03a7-120">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="a03a7-120">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03a7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03a7-121">-ResourceGroupName</span></span>
<span data-ttu-id="a03a7-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a03a7-122">The resource group name.</span></span>

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

### <span data-ttu-id="a03a7-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="a03a7-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="a03a7-124">Den tid eller det klock slag då trigger körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="a03a7-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03a7-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="a03a7-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="a03a7-126">Den tid som en utlöses innan körningen körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="a03a7-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a03a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03a7-127">CommonParameters</span></span>
<span data-ttu-id="a03a7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03a7-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03a7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03a7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a03a7-130">INPUTS</span></span>

### <span data-ttu-id="a03a7-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a03a7-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="a03a7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a03a7-132">System.String</span></span>

## <span data-ttu-id="a03a7-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a03a7-133">OUTPUTS</span></span>

### <span data-ttu-id="a03a7-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="a03a7-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="a03a7-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a03a7-135">NOTES</span></span>

## <span data-ttu-id="a03a7-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a03a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="a03a7-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a03a7-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="a03a7-138">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="a03a7-138">Stop-AzDataFactoryV2Trigger</span></span>]()

