---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2TriggerRun.md
ms.openlocfilehash: caa3cd25db706a3d025ee439aebb6dbb5491f7d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756195"
---
# <span data-ttu-id="9d076-101">Get-AzureRmDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="9d076-101">Get-AzureRmDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="9d076-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d076-102">SYNOPSIS</span></span>
<span data-ttu-id="9d076-103">Returnerar information om trigger körs.</span><span class="sxs-lookup"><span data-stu-id="9d076-103">Returns information about trigger runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d076-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d076-104">SYNTAX</span></span>

### <span data-ttu-id="9d076-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="9d076-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d076-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9d076-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2TriggerRun [-Name] <String> [-TriggerRunStartedAfter] <DateTime>
 [-TriggerRunStartedBefore] <DateTime> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d076-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d076-107">DESCRIPTION</span></span>
<span data-ttu-id="9d076-108">Kommandot **Get-AzureRmDataFactoryV2TriggerRun** returnerar detaljerad information om trigger körs för den angivna utlösaren under den angivna tids perioden.</span><span class="sxs-lookup"><span data-stu-id="9d076-108">The **Get-AzureRmDataFactoryV2TriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="9d076-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d076-109">EXAMPLES</span></span>

### <span data-ttu-id="9d076-110">Exempel 1: få information om trigger-körning</span><span class="sxs-lookup"><span data-stu-id="9d076-110">Example 1: Get information about trigger run</span></span>
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

<span data-ttu-id="9d076-111">Det här kommandot visar information om hur du kör "WikiTrigger" i fabriken "WikiADF" som startade med "2017-09-01" och "2019-09-30".</span><span class="sxs-lookup"><span data-stu-id="9d076-111">This command shows information about runs for "WikiTrigger" in the factory "WikiADF" that started between "2017-09-01" and "2019-09-30".</span></span>

## <span data-ttu-id="9d076-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d076-112">PARAMETERS</span></span>

### <span data-ttu-id="9d076-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9d076-113">-DataFactory</span></span>
<span data-ttu-id="9d076-114">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="9d076-114">The data factory object.</span></span>

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

### <span data-ttu-id="9d076-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9d076-115">-DataFactoryName</span></span>
<span data-ttu-id="9d076-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="9d076-116">The data factory name.</span></span>

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

### <span data-ttu-id="9d076-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d076-117">-DefaultProfile</span></span>
<span data-ttu-id="9d076-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d076-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d076-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d076-119">-Name</span></span>
<span data-ttu-id="9d076-120">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="9d076-120">The trigger name.</span></span>

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

### <span data-ttu-id="9d076-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d076-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d076-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9d076-122">The resource group name.</span></span>

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

### <span data-ttu-id="9d076-123">-TriggerRunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="9d076-123">-TriggerRunStartedAfter</span></span>
<span data-ttu-id="9d076-124">Den tid eller det klock slag då trigger körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="9d076-124">The time at or after which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="9d076-125">-TriggerRunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="9d076-125">-TriggerRunStartedBefore</span></span>
<span data-ttu-id="9d076-126">Den tid som en utlöses innan körningen körs i ISO8601-format.</span><span class="sxs-lookup"><span data-stu-id="9d076-126">The time at or before which the trigger run started to execute in ISO8601 format.</span></span>

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

### <span data-ttu-id="9d076-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d076-127">CommonParameters</span></span>
<span data-ttu-id="9d076-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d076-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d076-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d076-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d076-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d076-130">INPUTS</span></span>

### <span data-ttu-id="9d076-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9d076-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="9d076-132">Parametrar: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d076-132">Parameters: DataFactory (ByValue)</span></span>

### <span data-ttu-id="9d076-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9d076-133">System.String</span></span>

## <span data-ttu-id="9d076-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d076-134">OUTPUTS</span></span>

### <span data-ttu-id="9d076-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="9d076-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

## <span data-ttu-id="9d076-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d076-136">NOTES</span></span>

## <span data-ttu-id="9d076-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d076-137">RELATED LINKS</span></span>

[<span data-ttu-id="9d076-138">Start-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d076-138">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="9d076-139">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="9d076-139">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

