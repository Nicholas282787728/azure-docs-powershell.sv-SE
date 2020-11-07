---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 302129506c516cd0f2864210d5323b83fb54e0df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756190"
---
# <span data-ttu-id="64dfc-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64dfc-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="64dfc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="64dfc-103">Väntar på att ett jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="64dfc-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64dfc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64dfc-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64dfc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="64dfc-106">Cmdleten **wait-AzureRmDataLakeAnalyticsJob** väntar på att ett Azure Data Lake Analytics-jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="64dfc-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="64dfc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="64dfc-108">Exempel 1: vänta tills jobbet är klart</span><span class="sxs-lookup"><span data-stu-id="64dfc-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="64dfc-109">Följande kommando väntar på jobbet med det ID som ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="64dfc-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="64dfc-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="64dfc-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="64dfc-111">-Account</span></span>
<span data-ttu-id="64dfc-112">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="64dfc-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="64dfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64dfc-113">-DefaultProfile</span></span>
<span data-ttu-id="64dfc-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="64dfc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64dfc-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="64dfc-115">-JobId</span></span>
<span data-ttu-id="64dfc-116">Anger ID för det jobb som du vill vänta på.</span><span class="sxs-lookup"><span data-stu-id="64dfc-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="64dfc-117">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="64dfc-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="64dfc-118">Anger antalet sekunder som ska vänta innan väntan avbryts.</span><span class="sxs-lookup"><span data-stu-id="64dfc-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="64dfc-119">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="64dfc-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="64dfc-120">Ange antal sekunder som förflutit mellan varje kontroll av jobb tillståndet.</span><span class="sxs-lookup"><span data-stu-id="64dfc-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="64dfc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64dfc-121">CommonParameters</span></span>
<span data-ttu-id="64dfc-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64dfc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64dfc-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64dfc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64dfc-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64dfc-124">INPUTS</span></span>

### <span data-ttu-id="64dfc-125">System. String</span><span class="sxs-lookup"><span data-stu-id="64dfc-125">System.String</span></span>

### <span data-ttu-id="64dfc-126">System. GUID</span><span class="sxs-lookup"><span data-stu-id="64dfc-126">System.Guid</span></span>

### <span data-ttu-id="64dfc-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="64dfc-127">System.Int32</span></span>

## <span data-ttu-id="64dfc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64dfc-128">OUTPUTS</span></span>

### <span data-ttu-id="64dfc-129">Microsoft. Azure. Management. DataLake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="64dfc-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="64dfc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64dfc-130">NOTES</span></span>

## <span data-ttu-id="64dfc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64dfc-131">RELATED LINKS</span></span>

[<span data-ttu-id="64dfc-132">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64dfc-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="64dfc-133">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64dfc-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="64dfc-134">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="64dfc-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


