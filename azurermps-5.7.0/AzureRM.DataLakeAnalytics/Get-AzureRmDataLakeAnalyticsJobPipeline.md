---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: f8cb65d1884cff247c5debcf347ab50bff0b6ce3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757690"
---
# <span data-ttu-id="d1767-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="d1767-101">Get-AzureRmDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="d1767-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1767-102">SYNOPSIS</span></span>
<span data-ttu-id="d1767-103">Hämtar en pipeline för data Lake Analytics-jobb eller-rörledningar.</span><span class="sxs-lookup"><span data-stu-id="d1767-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1767-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1767-104">SYNTAX</span></span>

### <span data-ttu-id="d1767-105">GetAllInAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="d1767-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1767-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="d1767-106">GetBySpecificJobPipeline</span></span>
```
Get-AzureRmDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1767-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1767-107">DESCRIPTION</span></span>
<span data-ttu-id="d1767-108">**Get-AzureRmDataLakeAnalyticsJobPipeline** får ett angivet Azure Data Lake Analytics-jobbs pipeline eller en lista över rörledningar.</span><span class="sxs-lookup"><span data-stu-id="d1767-108">The **Get-AzureRmDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="d1767-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1767-109">EXAMPLES</span></span>

### <span data-ttu-id="d1767-110">Exempel 1: skaffa en angiven rörledning</span><span class="sxs-lookup"><span data-stu-id="d1767-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="d1767-111">Det här kommandot hämtar pipeline med ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="d1767-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="d1767-112">Exempel 2: Hämta en lista över alla rörledningar i kontot</span><span class="sxs-lookup"><span data-stu-id="d1767-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="d1767-113">Det här kommandot får en lista över alla rörledningar i kontot "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="d1767-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="d1767-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1767-114">PARAMETERS</span></span>

### <span data-ttu-id="d1767-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="d1767-115">-Account</span></span>
<span data-ttu-id="d1767-116">Namnet på det data Lake Analytics-konto namn som du vill hämta jobb pipeline för.</span><span class="sxs-lookup"><span data-stu-id="d1767-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="d1767-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1767-117">-DefaultProfile</span></span>
<span data-ttu-id="d1767-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d1767-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1767-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="d1767-119">-PipelineId</span></span>
<span data-ttu-id="d1767-120">ID för det specifika jobb försäljnings förlopp du vill returnera information om.</span><span class="sxs-lookup"><span data-stu-id="d1767-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1767-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="d1767-121">-SubmittedAfter</span></span>
<span data-ttu-id="d1767-122">Ett valfritt filter som returnerar jobb ledning (ar) som skickas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="d1767-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1767-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="d1767-123">-SubmittedBefore</span></span>
<span data-ttu-id="d1767-124">Ett valfritt filter som returnerar jobbets pipeline (ar) som skickas före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="d1767-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1767-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1767-125">CommonParameters</span></span>
<span data-ttu-id="d1767-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1767-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1767-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1767-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1767-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1767-128">INPUTS</span></span>

### <span data-ttu-id="d1767-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d1767-129">System.String</span></span>

### <span data-ttu-id="d1767-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d1767-130">System.Guid</span></span>

## <span data-ttu-id="d1767-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1767-131">OUTPUTS</span></span>

### <span data-ttu-id="d1767-132">Microsoft. Azure. commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="d1767-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="d1767-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1767-133">NOTES</span></span>

## <span data-ttu-id="d1767-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1767-134">RELATED LINKS</span></span>

