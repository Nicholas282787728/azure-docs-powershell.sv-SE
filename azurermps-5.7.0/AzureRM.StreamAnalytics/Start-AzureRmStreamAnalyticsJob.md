---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/start-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Start-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: a4e6ac26eeca6150feabaa07dc28a787ea01112d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573140"
---
# <span data-ttu-id="dc15d-101">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dc15d-101">Start-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="dc15d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc15d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc15d-103">Startar ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="dc15d-103">Starts a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc15d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc15d-104">SYNTAX</span></span>

```
Start-AzureRmStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc15d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc15d-105">DESCRIPTION</span></span>
<span data-ttu-id="dc15d-106">Cmdleten **Start-AzureRmStreamAnalyticsJob** asynkront distribuera och startar ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="dc15d-106">The **Start-AzureRmStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="dc15d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc15d-107">EXAMPLES</span></span>

### <span data-ttu-id="dc15d-108">EXEMPEL 1: starta ett ström analys jobb</span><span class="sxs-lookup"><span data-stu-id="dc15d-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\>Start-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="dc15d-109">Det här kommandot startar jobbets StreamingJob och anger att data strömmen för utdata ska starta vid tidsstämpel 2014 – 07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="dc15d-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="dc15d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc15d-110">PARAMETERS</span></span>

### <span data-ttu-id="dc15d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc15d-111">-DefaultProfile</span></span>
<span data-ttu-id="dc15d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc15d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc15d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc15d-113">-Name</span></span>
<span data-ttu-id="dc15d-114">Anger namnet på Azure Stream Analytics-jobbet att starta.</span><span class="sxs-lookup"><span data-stu-id="dc15d-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc15d-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="dc15d-115">-OutputStartMode</span></span>
<span data-ttu-id="dc15d-116">Anger start läget för jobbet.</span><span class="sxs-lookup"><span data-stu-id="dc15d-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="dc15d-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="dc15d-117">Valid values are:</span></span> 

- <span data-ttu-id="dc15d-118">JobStartTime-det här värdet anger att start punkten för händelse strömmen för utdata ska starta när jobbet startas.</span><span class="sxs-lookup"><span data-stu-id="dc15d-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="dc15d-119">CustomTime-det här värdet anger att start punkten för händelse strömmen för utdata ska starta vid en anpassad tid som anges i parametern *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="dc15d-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 <span data-ttu-id="dc15d-120">--LastOutputEventTime-det här värdet anger att start punkten för händelse strömmen för utdata ska starta från den sista händelsen.</span><span class="sxs-lookup"><span data-stu-id="dc15d-120">-- LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>

<span data-ttu-id="dc15d-121">Om egenskapen saknas är standardvärdet för JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="dc15d-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc15d-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="dc15d-122">-OutputStartTime</span></span>
<span data-ttu-id="dc15d-123">Anger start tiden för utdata.</span><span class="sxs-lookup"><span data-stu-id="dc15d-123">Specifies the output start time.</span></span>
<span data-ttu-id="dc15d-124">Det här värdet är antingen en ISO-8601 formaterad tidsstämpel som anger start punkten för händelse strömmen för utdata, eller $Null för att indikera att utdata-dataströmmen kommer att starta när ett strömnings jobb startas.</span><span class="sxs-lookup"><span data-stu-id="dc15d-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="dc15d-125">Egenskapen måste ha ett värde om *OutputStartMode* är inställt på CustomTime.</span><span class="sxs-lookup"><span data-stu-id="dc15d-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc15d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc15d-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc15d-127">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="dc15d-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc15d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc15d-128">CommonParameters</span></span>
<span data-ttu-id="dc15d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc15d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc15d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc15d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc15d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc15d-131">INPUTS</span></span>

### <span data-ttu-id="dc15d-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc15d-132">None</span></span>
<span data-ttu-id="dc15d-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="dc15d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc15d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc15d-134">OUTPUTS</span></span>

### <span data-ttu-id="dc15d-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="dc15d-135">System.Object</span></span>

## <span data-ttu-id="dc15d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc15d-136">NOTES</span></span>

## <span data-ttu-id="dc15d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc15d-137">RELATED LINKS</span></span>

[<span data-ttu-id="dc15d-138">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dc15d-138">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="dc15d-139">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dc15d-139">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="dc15d-140">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dc15d-140">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="dc15d-141">Stopp-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dc15d-141">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


