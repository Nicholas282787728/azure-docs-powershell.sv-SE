---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: 7d3f1ca73712753ad38b46c186a51bd7aa159b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755502"
---
# <span data-ttu-id="cd537-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="cd537-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="cd537-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd537-102">SYNOPSIS</span></span>
<span data-ttu-id="cd537-103">Returnerar information om trigger körs.</span><span class="sxs-lookup"><span data-stu-id="cd537-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd537-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd537-104">SYNTAX</span></span>

### <span data-ttu-id="cd537-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="cd537-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd537-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cd537-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd537-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd537-107">DESCRIPTION</span></span>
<span data-ttu-id="cd537-108">Kommandot **Get-AzureRmDataFactoryV2TriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="cd537-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="cd537-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd537-109">EXAMPLES</span></span>

### <span data-ttu-id="cd537-110">Exempel 1: få information om trigger-körning</span><span class="sxs-lookup"><span data-stu-id="cd537-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="cd537-111">Det här kommandot visar information om hur du kör "WikiTrigger" i fabriken "WikiADF" som startade med "2017-09-01" och "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="cd537-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="cd537-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd537-112">PARAMETERS</span></span>

### <span data-ttu-id="cd537-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cd537-113">-DataFactory</span></span>
<span data-ttu-id="cd537-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="cd537-114">The data factory object.</span></span>

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

### <span data-ttu-id="cd537-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cd537-115">-DataFactoryName</span></span>
<span data-ttu-id="cd537-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="cd537-116">The data factory name.</span></span>

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

### <span data-ttu-id="cd537-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd537-117">-Name</span></span>
<span data-ttu-id="cd537-118">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="cd537-118">The trigger name.</span></span>

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

### <span data-ttu-id="cd537-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd537-119">-ResourceGroupName</span></span>
<span data-ttu-id="cd537-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="cd537-120">The resource group name.</span></span>

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

### <span data-ttu-id="cd537-121">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="cd537-121">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="cd537-122">Den tid eller det klock slag då trigger körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="cd537-122">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="cd537-123">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="cd537-123">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="cd537-124">Den tid som en utlöses innan körningen körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="cd537-124">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="cd537-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd537-125">-DefaultProfile</span></span>
<span data-ttu-id="cd537-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd537-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd537-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd537-127">CommonParameters</span></span>
<span data-ttu-id="cd537-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd537-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd537-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd537-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd537-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd537-130">INPUTS</span></span>

### <span data-ttu-id="cd537-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cd537-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="cd537-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cd537-132">System.String</span></span>

## <span data-ttu-id="cd537-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd537-133">OUTPUTS</span></span>

### <span data-ttu-id="cd537-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cd537-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="cd537-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="cd537-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="cd537-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd537-136">NOTES</span></span>

## <span data-ttu-id="cd537-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd537-137">RELATED LINKS</span></span>

[<span data-ttu-id="cd537-138">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd537-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="cd537-139">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="cd537-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()
