---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: B5914F65-CAF8-4647-BA78-49B65DD6D67A
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/start-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Start-AzStreamAnalyticsJob.md
ms.openlocfilehash: bdbd590f2c6c158759d439e473274c8b4508863d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746163"
---
# <span data-ttu-id="13f6a-101">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="13f6a-101">Start-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="13f6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13f6a-102">SYNOPSIS</span></span>
<span data-ttu-id="13f6a-103">Startar ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="13f6a-103">Starts a Stream Analytics job.</span></span>

## <span data-ttu-id="13f6a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13f6a-104">SYNTAX</span></span>

```
Start-AzStreamAnalyticsJob [-Name] <String> [[-OutputStartMode] <String>] [[-OutputStartTime] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13f6a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13f6a-105">DESCRIPTION</span></span>
<span data-ttu-id="13f6a-106">Cmdleten **Start-AzStreamAnalyticsJob** asynkront distribuera och startar ett ström analys jobb i Azure.</span><span class="sxs-lookup"><span data-stu-id="13f6a-106">The **Start-AzStreamAnalyticsJob** cmdlet asynchronously deploys and starts a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="13f6a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13f6a-107">EXAMPLES</span></span>

### <span data-ttu-id="13f6a-108">EXEMPEL 1: starta ett ström analys jobb</span><span class="sxs-lookup"><span data-stu-id="13f6a-108">EXAMPLE 1: Start a Stream Analytics job</span></span>
```
PS C:\> Start-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob" -OutputStartMode "CustomTime" -OutputStartTime "2014-07-03T01:00Z"
```

<span data-ttu-id="13f6a-109">Det här kommandot startar jobbets StreamingJob och anger att data strömmen för utdata ska starta vid tidsstämpel 2014 – 07-03T01:00Z.</span><span class="sxs-lookup"><span data-stu-id="13f6a-109">This command starts the job StreamingJob and specifies that the output event stream should start at timestamp 2014-07-03T01:00Z.</span></span>

## <span data-ttu-id="13f6a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13f6a-110">PARAMETERS</span></span>

### <span data-ttu-id="13f6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f6a-111">-DefaultProfile</span></span>
<span data-ttu-id="13f6a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13f6a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f6a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="13f6a-113">-Name</span></span>
<span data-ttu-id="13f6a-114">Anger namnet på Azure Stream Analytics-jobbet att starta.</span><span class="sxs-lookup"><span data-stu-id="13f6a-114">Specifies the name of the Azure Stream Analytics job to start.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f6a-115">-OutputStartMode</span><span class="sxs-lookup"><span data-stu-id="13f6a-115">-OutputStartMode</span></span>
<span data-ttu-id="13f6a-116">Anger start läget för jobbet.</span><span class="sxs-lookup"><span data-stu-id="13f6a-116">Specifies the start mode for the job.</span></span>
<span data-ttu-id="13f6a-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="13f6a-117">Valid values are:</span></span> 
- <span data-ttu-id="13f6a-118">JobStartTime-det här värdet anger att start punkten för händelse strömmen för utdata ska starta när jobbet startas.</span><span class="sxs-lookup"><span data-stu-id="13f6a-118">JobStartTime - This value indicates that the starting point of the output event stream should start when the job is started.</span></span>
- <span data-ttu-id="13f6a-119">CustomTime-det här värdet anger att start punkten för händelse strömmen för utdata ska starta vid en anpassad tid som anges i parametern *OutputStartTime* .</span><span class="sxs-lookup"><span data-stu-id="13f6a-119">CustomTime - This value indicates that the starting point of the output event stream should start at a custom time that is specified in the *OutputStartTime* parameter.</span></span> 
 - <span data-ttu-id="13f6a-120">LastOutputEventTime-det här värdet anger att start punkten för händelse strömmen för utdata ska starta från den sista händelsen.</span><span class="sxs-lookup"><span data-stu-id="13f6a-120">LastOutputEventTime - This value indicates that the starting point of the output event stream should start from the last event output time.</span></span>
<span data-ttu-id="13f6a-121">Om egenskapen saknas är standardvärdet för JobStartTime.</span><span class="sxs-lookup"><span data-stu-id="13f6a-121">If the property is absent, the default is JobStartTime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f6a-122">-OutputStartTime</span><span class="sxs-lookup"><span data-stu-id="13f6a-122">-OutputStartTime</span></span>
<span data-ttu-id="13f6a-123">Anger start tiden för utdata.</span><span class="sxs-lookup"><span data-stu-id="13f6a-123">Specifies the output start time.</span></span>
<span data-ttu-id="13f6a-124">Det här värdet är antingen en ISO-8601 formaterad tidsstämpel som anger start punkten för händelse strömmen för utdata, eller $Null för att indikera att utdata-dataströmmen kommer att starta när ett strömnings jobb startas.</span><span class="sxs-lookup"><span data-stu-id="13f6a-124">This value is either an ISO-8601 formatted time stamp that indicates the starting point of the output event stream, or $Null to indicate that the output event stream will start whenever the streaming job is started.</span></span>
<span data-ttu-id="13f6a-125">Egenskapen måste ha ett värde om *OutputStartMode* är inställt på CustomTime.</span><span class="sxs-lookup"><span data-stu-id="13f6a-125">This property must have a value if *OutputStartMode* is set to CustomTime.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="13f6a-127">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="13f6a-127">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f6a-128">CommonParameters</span></span>
<span data-ttu-id="13f6a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f6a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f6a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f6a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13f6a-131">INPUTS</span></span>

### <span data-ttu-id="13f6a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="13f6a-132">System.String</span></span>

### <span data-ttu-id="13f6a-133">System. Nullable ' 1 [[system. DateTime, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="13f6a-133">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="13f6a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13f6a-134">OUTPUTS</span></span>

### <span data-ttu-id="13f6a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="13f6a-135">System.Boolean</span></span>

## <span data-ttu-id="13f6a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13f6a-136">NOTES</span></span>

## <span data-ttu-id="13f6a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13f6a-137">RELATED LINKS</span></span>

[<span data-ttu-id="13f6a-138">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="13f6a-138">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="13f6a-139">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="13f6a-139">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="13f6a-140">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="13f6a-140">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="13f6a-141">Stopp-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="13f6a-141">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


