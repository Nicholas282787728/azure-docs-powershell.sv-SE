---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 672a992dd86fcbd95e17f0795147231b1b62cd5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756993"
---
# <span data-ttu-id="3f9f3-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f9f3-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="3f9f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f9f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f9f3-103">Väntar på att ett jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f9f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f9f3-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f9f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f9f3-105">DESCRIPTION</span></span>
<span data-ttu-id="3f9f3-106">Cmdleten **wait-AzureRmDataLakeAnalyticsJob** väntar på att ett Azure Data Lake Analytics-jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="3f9f3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f9f3-107">EXAMPLES</span></span>

### <span data-ttu-id="3f9f3-108">Exempel 1: vänta tills jobbet är klart</span><span class="sxs-lookup"><span data-stu-id="3f9f3-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="3f9f3-109">Följande kommando väntar på jobbet med det ID som ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="3f9f3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f9f3-110">PARAMETERS</span></span>

### <span data-ttu-id="3f9f3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3f9f3-111">-Account</span></span>
<span data-ttu-id="3f9f3-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9f3-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="3f9f3-113">-JobId</span></span>
<span data-ttu-id="3f9f3-114">Anger ID för det jobb som du vill vänta på.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-114">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9f3-115">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f9f3-115">-TimeoutInSeconds</span></span>
<span data-ttu-id="3f9f3-116">Anger antalet sekunder som ska vänta innan väntan avbryts.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-116">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9f3-117">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f9f3-117">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="3f9f3-118">Ange antal sekunder som förflutit mellan varje kontroll av jobb tillståndet.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-118">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f9f3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f9f3-119">-DefaultProfile</span></span>
<span data-ttu-id="3f9f3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f9f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f9f3-121">CommonParameters</span></span>
<span data-ttu-id="3f9f3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f9f3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f9f3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f9f3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f9f3-124">INPUTS</span></span>

### <span data-ttu-id="3f9f3-125">Ande</span><span class="sxs-lookup"><span data-stu-id="3f9f3-125">Guid</span></span>
<span data-ttu-id="3f9f3-126">Parametern ' JobId ' godkänner värdet av typen ' GUID ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3f9f3-126">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="3f9f3-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f9f3-127">OUTPUTS</span></span>

### <span data-ttu-id="3f9f3-128">JobInformation</span><span class="sxs-lookup"><span data-stu-id="3f9f3-128">JobInformation</span></span>
<span data-ttu-id="3f9f3-129">Den slutliga jobb informationen för det färdiga jobbet.</span><span class="sxs-lookup"><span data-stu-id="3f9f3-129">The final job details for the completed job.</span></span>

## <span data-ttu-id="3f9f3-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f9f3-130">NOTES</span></span>

## <span data-ttu-id="3f9f3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f9f3-131">RELATED LINKS</span></span>

[<span data-ttu-id="3f9f3-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f9f3-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="3f9f3-133">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f9f3-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="3f9f3-134">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3f9f3-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


