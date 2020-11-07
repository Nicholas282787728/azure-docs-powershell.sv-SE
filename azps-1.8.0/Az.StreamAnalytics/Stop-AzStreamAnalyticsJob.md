---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 050bfccef2b6286ef45a96a9feedc99ef4745115
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746157"
---
# <span data-ttu-id="51bcc-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="51bcc-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="51bcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="51bcc-103">Stoppar ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="51bcc-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="51bcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51bcc-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51bcc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51bcc-105">DESCRIPTION</span></span>
<span data-ttu-id="51bcc-106">Cmdleten **Stop-AzStreamAnalyticsJob** asynkront stoppar ett ström analys jobb som körs i Azure och avallokerar resurser som användes.</span><span class="sxs-lookup"><span data-stu-id="51bcc-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="51bcc-107">Jobb definitionen och metadata är tillgängliga i ditt abonnemang via både Azure Portal och Management API: er, så att jobbet kan redige ras och startas om.</span><span class="sxs-lookup"><span data-stu-id="51bcc-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="51bcc-108">Du kommer inte att debiteras för ett jobb i stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="51bcc-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="51bcc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51bcc-109">EXAMPLES</span></span>

### <span data-ttu-id="51bcc-110">EXEMPEL 1: stoppa ett pågående jobb</span><span class="sxs-lookup"><span data-stu-id="51bcc-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="51bcc-111">Det här kommandot stoppar jobbets StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="51bcc-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="51bcc-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51bcc-112">PARAMETERS</span></span>

### <span data-ttu-id="51bcc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bcc-113">-DefaultProfile</span></span>
<span data-ttu-id="51bcc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51bcc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51bcc-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="51bcc-115">-Name</span></span>
<span data-ttu-id="51bcc-116">Anger namnet på Azure Stream Analytics-jobbet som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="51bcc-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="51bcc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51bcc-117">-ResourceGroupName</span></span>
<span data-ttu-id="51bcc-118">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="51bcc-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="51bcc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bcc-119">CommonParameters</span></span>
<span data-ttu-id="51bcc-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51bcc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bcc-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bcc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bcc-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51bcc-122">INPUTS</span></span>

### <span data-ttu-id="51bcc-123">System. String</span><span class="sxs-lookup"><span data-stu-id="51bcc-123">System.String</span></span>

## <span data-ttu-id="51bcc-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51bcc-124">OUTPUTS</span></span>

### <span data-ttu-id="51bcc-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51bcc-125">System.Boolean</span></span>

## <span data-ttu-id="51bcc-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51bcc-126">NOTES</span></span>

## <span data-ttu-id="51bcc-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51bcc-127">RELATED LINKS</span></span>

[<span data-ttu-id="51bcc-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="51bcc-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="51bcc-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="51bcc-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="51bcc-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="51bcc-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="51bcc-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="51bcc-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="51bcc-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="51bcc-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


