---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobpipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobPipeline.md
ms.openlocfilehash: 1d13d1b6e55831c972457c5a6a5aadc427ecb3a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320723"
---
# <span data-ttu-id="6d7ab-101">Get-AzDataLakeAnalyticsJobPipeline</span><span class="sxs-lookup"><span data-stu-id="6d7ab-101">Get-AzDataLakeAnalyticsJobPipeline</span></span>

## <span data-ttu-id="6d7ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7ab-103">Hämtar en pipeline för data Lake Analytics-jobb eller-rörledningar.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-103">Gets a Data Lake Analytics Job pipeline or pipelines.</span></span>

## <span data-ttu-id="6d7ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d7ab-104">SYNTAX</span></span>

### <span data-ttu-id="6d7ab-105">GetAllInAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="6d7ab-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d7ab-106">GetBySpecificJobPipeline</span><span class="sxs-lookup"><span data-stu-id="6d7ab-106">GetBySpecificJobPipeline</span></span>
```
Get-AzDataLakeAnalyticsJobPipeline [-Account] <String> [-PipelineId] <Guid> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d7ab-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d7ab-107">DESCRIPTION</span></span>
<span data-ttu-id="6d7ab-108">**Get-AzDataLakeAnalyticsJobPipeline** får ett angivet Azure Data Lake Analytics-jobbs pipeline eller en lista över rörledningar.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-108">The **Get-AzDataLakeAnalyticsJobPipeline** gets a specified Azure Data Lake Analytics Job pipeline or a list of pipelines.</span></span>

## <span data-ttu-id="6d7ab-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d7ab-109">EXAMPLES</span></span>

### <span data-ttu-id="6d7ab-110">Exempel 1: skaffa en angiven rörledning</span><span class="sxs-lookup"><span data-stu-id="6d7ab-110">Example 1: Get a specified pipeline</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -Account "contosoadla" -PipelineId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="6d7ab-111">Det här kommandot hämtar pipeline med ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-111">This command gets the specified pipeline with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="6d7ab-112">Exempel 2: Hämta en lista över alla rörledningar i kontot</span><span class="sxs-lookup"><span data-stu-id="6d7ab-112">Example 2: Get a list of all pipelines in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobPipeline -AccountName "contosoadla"
```

<span data-ttu-id="6d7ab-113">Det här kommandot får en lista över alla rörledningar i kontot "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="6d7ab-113">This command gets a list of all pipelines in the account "contosoadla"</span></span>

## <span data-ttu-id="6d7ab-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d7ab-114">PARAMETERS</span></span>

### <span data-ttu-id="6d7ab-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="6d7ab-115">-Account</span></span>
<span data-ttu-id="6d7ab-116">Namnet på det data Lake Analytics-konto namn som du vill hämta jobb pipeline för.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-116">Name of the Data Lake Analytics account name under which want to retrieve the job pipeline.</span></span>

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

### <span data-ttu-id="6d7ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7ab-117">-DefaultProfile</span></span>
<span data-ttu-id="6d7ab-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6d7ab-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d7ab-119">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="6d7ab-119">-PipelineId</span></span>
<span data-ttu-id="6d7ab-120">ID för det specifika jobb försäljnings förlopp du vill returnera information om.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-120">ID of the specific job pipeline to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobPipeline
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7ab-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="6d7ab-121">-SubmittedAfter</span></span>
<span data-ttu-id="6d7ab-122">Ett valfritt filter som returnerar jobb ledning (ar) som skickas efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-122">An optional filter which returns job pipeline(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7ab-123">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="6d7ab-123">-SubmittedBefore</span></span>
<span data-ttu-id="6d7ab-124">Ett valfritt filter som returnerar jobbets pipeline (ar) som skickas före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-124">An optional filter which returns job pipeline(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7ab-125">CommonParameters</span></span>
<span data-ttu-id="6d7ab-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7ab-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d7ab-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7ab-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d7ab-128">INPUTS</span></span>

### <span data-ttu-id="6d7ab-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6d7ab-129">System.String</span></span>

### <span data-ttu-id="6d7ab-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6d7ab-130">System.Guid</span></span>

### <span data-ttu-id="6d7ab-131">System. Nullable ' 1 [[system. DateTimeOffset, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d7ab-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6d7ab-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d7ab-132">OUTPUTS</span></span>

### <span data-ttu-id="6d7ab-133">Microsoft. Azure. commands. DataLakeAnalytics. Models. PSJobPipelineInformation</span><span class="sxs-lookup"><span data-stu-id="6d7ab-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobPipelineInformation</span></span>

## <span data-ttu-id="6d7ab-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d7ab-134">NOTES</span></span>

## <span data-ttu-id="6d7ab-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d7ab-135">RELATED LINKS</span></span>
