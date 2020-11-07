---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: cfc5d0999ed9c77e38b83eee99eabbd19dd1e493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758094"
---
# <span data-ttu-id="828fe-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="828fe-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="828fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="828fe-102">SYNOPSIS</span></span>
<span data-ttu-id="828fe-103">Hämtar återkommande och återkommande jobb för data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="828fe-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="828fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="828fe-104">SYNTAX</span></span>

### <span data-ttu-id="828fe-105">Alla i-konto (standard)</span><span class="sxs-lookup"><span data-stu-id="828fe-105">All In Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="828fe-106">Återkommande jobb</span><span class="sxs-lookup"><span data-stu-id="828fe-106">Specific Job Recurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="828fe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="828fe-107">DESCRIPTION</span></span>
<span data-ttu-id="828fe-108">Funktionen **Get-AzureRmDataLakeAnalyticsJobRecurrence** får ett angivet återkommande Azure Data Lake Analytics-jobb eller en lista över upprepningar.</span><span class="sxs-lookup"><span data-stu-id="828fe-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="828fe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="828fe-109">EXAMPLES</span></span>

### <span data-ttu-id="828fe-110">Exempel 1: Hämta en viss upprepning</span><span class="sxs-lookup"><span data-stu-id="828fe-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="828fe-111">Det här kommandot får det angivna jobbet återkommande med ID ' 83cb7ad2-3523-4b82-b909-d478b0d8aea3 ' i kontot ' contosoadla '.</span><span class="sxs-lookup"><span data-stu-id="828fe-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="828fe-112">Exempel 2: få en lista över alla upprepningar i kontot</span><span class="sxs-lookup"><span data-stu-id="828fe-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="828fe-113">Det här kommandot får en lista över alla upprepningar i kontot "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="828fe-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="828fe-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="828fe-114">PARAMETERS</span></span>

### <span data-ttu-id="828fe-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="828fe-115">-Account</span></span>
<span data-ttu-id="828fe-116">Namnet på det data Lake Analytics-konto namn som du vill hämta återkommande jobb för.</span><span class="sxs-lookup"><span data-stu-id="828fe-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="828fe-117">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="828fe-117">-RecurrenceId</span></span>
<span data-ttu-id="828fe-118">ID för det specifika jobbet återkommande för att returnera information om.</span><span class="sxs-lookup"><span data-stu-id="828fe-118">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific Job Recurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="828fe-119">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="828fe-119">-SubmittedAfter</span></span>
<span data-ttu-id="828fe-120">Ett valfritt filter som returnerar återkommande jobb (er) efter den angivna tiden.</span><span class="sxs-lookup"><span data-stu-id="828fe-120">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="828fe-121">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="828fe-121">-SubmittedBefore</span></span>
<span data-ttu-id="828fe-122">Ett valfritt filter som returnerar återkommande jobb (er) endast före angiven tid.</span><span class="sxs-lookup"><span data-stu-id="828fe-122">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="828fe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828fe-123">-DefaultProfile</span></span>
<span data-ttu-id="828fe-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="828fe-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="828fe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828fe-125">CommonParameters</span></span>
<span data-ttu-id="828fe-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828fe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828fe-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828fe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828fe-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="828fe-128">INPUTS</span></span>

### <span data-ttu-id="828fe-129">System. String</span><span class="sxs-lookup"><span data-stu-id="828fe-129">System.String</span></span>
<span data-ttu-id="828fe-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="828fe-130">System.Guid</span></span>

## <span data-ttu-id="828fe-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="828fe-131">OUTPUTS</span></span>

### <span data-ttu-id="828fe-132">Microsoft. Azure. commands. DataLakeAnalytics. Models. PSJobRecurrenceInformation</span><span class="sxs-lookup"><span data-stu-id="828fe-132">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="828fe-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="828fe-133">NOTES</span></span>

## <span data-ttu-id="828fe-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="828fe-134">RELATED LINKS</span></span>

