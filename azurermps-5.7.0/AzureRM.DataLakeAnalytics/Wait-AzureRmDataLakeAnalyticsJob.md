---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584367"
---
# <span data-ttu-id="75d8e-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="75d8e-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="75d8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="75d8e-103">Väntar på att ett jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="75d8e-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75d8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75d8e-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75d8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="75d8e-106">Cmdleten **wait-AzureRmDataLakeAnalyticsJob** väntar på att ett Azure Data Lake Analytics-jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="75d8e-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="75d8e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75d8e-107">EXAMPLES</span></span>

### <span data-ttu-id="75d8e-108">Exempel 1: vänta tills jobbet är klart</span><span class="sxs-lookup"><span data-stu-id="75d8e-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="75d8e-109">Följande kommando väntar på jobbet med det ID som ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="75d8e-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="75d8e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75d8e-110">PARAMETERS</span></span>

### <span data-ttu-id="75d8e-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="75d8e-111">-Account</span></span>
<span data-ttu-id="75d8e-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="75d8e-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d8e-113">-DefaultProfile</span></span>
<span data-ttu-id="75d8e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="75d8e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75d8e-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="75d8e-115">-JobId</span></span>
<span data-ttu-id="75d8e-116">Anger ID för det jobb som du vill vänta på.</span><span class="sxs-lookup"><span data-stu-id="75d8e-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d8e-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="75d8e-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="75d8e-118">Anger antalet sekunder som ska vänta innan väntan avbryts.</span><span class="sxs-lookup"><span data-stu-id="75d8e-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d8e-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="75d8e-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="75d8e-120">Ange antal sekunder som förflutit mellan varje kontroll av jobb tillståndet.</span><span class="sxs-lookup"><span data-stu-id="75d8e-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75d8e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d8e-121">CommonParameters</span></span>
<span data-ttu-id="75d8e-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d8e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d8e-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75d8e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d8e-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75d8e-124">INPUTS</span></span>

### <span data-ttu-id="75d8e-125">Ande</span><span class="sxs-lookup"><span data-stu-id="75d8e-125">Guid</span></span>
<span data-ttu-id="75d8e-126">Parametern ' JobId ' godkänner värdet av typen ' GUID ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="75d8e-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="75d8e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75d8e-127">OUTPUTS</span></span>

### <span data-ttu-id="75d8e-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="75d8e-128">JobInformation</span></span>
<span data-ttu-id="75d8e-129">Den slutliga jobb informationen för det färdiga jobbet.</span><span class="sxs-lookup"><span data-stu-id="75d8e-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="75d8e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75d8e-130">NOTES</span></span>

## <span data-ttu-id="75d8e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75d8e-131">RELATED LINKS</span></span>

[<span data-ttu-id="75d8e-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="75d8e-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="75d8e-133">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="75d8e-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="75d8e-134">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="75d8e-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


