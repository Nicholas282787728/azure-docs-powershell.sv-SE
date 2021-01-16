---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 5844863cf56008d5d73fae7eef644dfd8e27c239
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412568"
---
# <span data-ttu-id="8688e-101">Get-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="8688e-101">Get-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="8688e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8688e-102">SYNOPSIS</span></span>
<span data-ttu-id="8688e-103">Returnerar information om trigger körs.</span><span class="sxs-lookup"><span data-stu-id="8688e-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="8688e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8688e-104">SYNTAX</span></span>

### <span data-ttu-id="8688e-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8688e-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8688e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8688e-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8688e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8688e-107">DESCRIPTION</span></span>
<span data-ttu-id="8688e-108">Kommandot **Get-AzDataFactoryV2TriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="8688e-108">The **Get-AzDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="8688e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8688e-109">EXAMPLES</span></span>

### <span data-ttu-id="8688e-110">Exempel 1: få information om trigger-körning</span><span class="sxs-lookup"><span data-stu-id="8688e-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="8688e-111">Det här kommandot visar information om hur du kör "WikiTrigger" i fabriken "WikiADF" som startade med "2017-09-01" och "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="8688e-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="8688e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8688e-112">PARAMETERS</span></span>

### <span data-ttu-id="8688e-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8688e-113">-DataFactory</span></span>
<span data-ttu-id="8688e-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="8688e-114">The data factory object.</span></span>

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

### <span data-ttu-id="8688e-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8688e-115">-DataFactoryName</span></span>
<span data-ttu-id="8688e-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8688e-116">The data factory name.</span></span>

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

### <span data-ttu-id="8688e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8688e-117">-DefaultProfile</span></span>
<span data-ttu-id="8688e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8688e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8688e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8688e-119">-Name</span></span>
<span data-ttu-id="8688e-120">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="8688e-120">The trigger name.</span></span>

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

### <span data-ttu-id="8688e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8688e-121">-ResourceGroupName</span></span>
<span data-ttu-id="8688e-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8688e-122">The resource group name.</span></span>

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

### <span data-ttu-id="8688e-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="8688e-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="8688e-124">Den tid eller det klock slag då trigger körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="8688e-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="8688e-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="8688e-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="8688e-126">Den tid som en utlöses innan körningen körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="8688e-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="8688e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8688e-127">CommonParameters</span></span>
<span data-ttu-id="8688e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8688e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8688e-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8688e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8688e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8688e-130">INPUTS</span></span>

### <span data-ttu-id="8688e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8688e-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="8688e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8688e-132">System.String</span></span>

## <span data-ttu-id="8688e-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8688e-133">OUTPUTS</span></span>

### <span data-ttu-id="8688e-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="8688e-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="8688e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8688e-135">NOTES</span></span>

## <span data-ttu-id="8688e-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8688e-136">RELATED LINKS</span></span>

[<span data-ttu-id="8688e-137">Start-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8688e-137">Start-AzDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="8688e-138">Stopp-AzDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="8688e-138">Stop-AzDataFactoryV2Trigger</span></span>]()

