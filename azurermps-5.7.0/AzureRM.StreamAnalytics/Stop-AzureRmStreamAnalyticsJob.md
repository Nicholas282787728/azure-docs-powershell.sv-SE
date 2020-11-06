---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573139"
---
# <span data-ttu-id="05bd1-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="05bd1-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="05bd1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="05bd1-103">Stoppar ett ström analys jobb.</span><span class="sxs-lookup"><span data-stu-id="05bd1-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05bd1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05bd1-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05bd1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05bd1-105">DESCRIPTION</span></span>
<span data-ttu-id="05bd1-106">Cmdleten **Stop-AzureRmStreamAnalyticsJob** asynkront stoppar ett ström analys jobb som körs i Azure och avallokerar resurser som användes.</span><span class="sxs-lookup"><span data-stu-id="05bd1-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="05bd1-107">Jobb definitionen och metadata är tillgängliga i ditt abonnemang via både Azure Portal och Management API: er, så att jobbet kan redige ras och startas om.</span><span class="sxs-lookup"><span data-stu-id="05bd1-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="05bd1-108">Du kommer inte att debiteras för ett jobb i stoppat tillstånd.</span><span class="sxs-lookup"><span data-stu-id="05bd1-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="05bd1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05bd1-109">EXAMPLES</span></span>

### <span data-ttu-id="05bd1-110">EXEMPEL 1: stoppa ett pågående jobb</span><span class="sxs-lookup"><span data-stu-id="05bd1-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="05bd1-111">Det här kommandot stoppar jobbets StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="05bd1-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="05bd1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05bd1-112">PARAMETERS</span></span>

### <span data-ttu-id="05bd1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bd1-113">-DefaultProfile</span></span>
<span data-ttu-id="05bd1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05bd1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05bd1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="05bd1-115">-Name</span></span>
<span data-ttu-id="05bd1-116">Anger namnet på Azure Stream Analytics-jobbet som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="05bd1-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="05bd1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05bd1-117">-ResourceGroupName</span></span>
<span data-ttu-id="05bd1-118">Anger namnet på den resurs grupp som Azure Stream Analytics-jobbet tillhör.</span><span class="sxs-lookup"><span data-stu-id="05bd1-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="05bd1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bd1-119">CommonParameters</span></span>
<span data-ttu-id="05bd1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bd1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bd1-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05bd1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bd1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05bd1-122">INPUTS</span></span>

### <span data-ttu-id="05bd1-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="05bd1-123">None</span></span>
<span data-ttu-id="05bd1-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="05bd1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05bd1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05bd1-125">OUTPUTS</span></span>

### <span data-ttu-id="05bd1-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="05bd1-126">System.Object</span></span>

## <span data-ttu-id="05bd1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05bd1-127">NOTES</span></span>

## <span data-ttu-id="05bd1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05bd1-128">RELATED LINKS</span></span>

[<span data-ttu-id="05bd1-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="05bd1-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="05bd1-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="05bd1-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="05bd1-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="05bd1-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="05bd1-132">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="05bd1-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="05bd1-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="05bd1-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


