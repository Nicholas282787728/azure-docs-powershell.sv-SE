---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchSubtask.md
ms.openlocfilehash: 58bed6fda4040c1af48469f4aa85f717c26c898c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586231"
---
# <span data-ttu-id="6b646-101">Get-AzureBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="6b646-101">Get-AzureBatchSubtask</span></span>

## <span data-ttu-id="6b646-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b646-102">SYNOPSIS</span></span>
<span data-ttu-id="6b646-103">Hämtar under aktivitetens information för den angivna aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="6b646-103">Gets the subtask information of the specified task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b646-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b646-104">SYNTAX</span></span>

### <span data-ttu-id="6b646-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="6b646-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b646-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="6b646-106">ParentObject</span></span>
```
Get-AzureBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b646-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b646-107">DESCRIPTION</span></span>
<span data-ttu-id="6b646-108">Cmdleten **Get-AzureBatchSubtask** hämtar under aktivitetens information om den angivna uppgiften.</span><span class="sxs-lookup"><span data-stu-id="6b646-108">The **Get-AzureBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="6b646-109">Under aktiviteter ger parallell bearbetning för enskilda uppgifter och möjliggör noggrann övervakning av aktivitets körning och förlopp.</span><span class="sxs-lookup"><span data-stu-id="6b646-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="6b646-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b646-110">EXAMPLES</span></span>

### <span data-ttu-id="6b646-111">Exempel 1: returnera alla under aktiviteter för en viss aktivitet</span><span class="sxs-lookup"><span data-stu-id="6b646-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzureBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="6b646-112">De här kommandona returnerar alla under aktiviteter för aktiviteten med aktivitets-ID: t.</span><span class="sxs-lookup"><span data-stu-id="6b646-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="6b646-113">För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="6b646-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="6b646-114">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="6b646-114">This object reference is stored in a variable named $context.</span></span>

<span data-ttu-id="6b646-115">Med det andra kommandot används den objekt referensen och cmdleten **Get-AzureBatchSubtask** för att returnera alla under aktiviteter för min aktivitet, en aktivitet som körs som en del av jobb jobbet – 01.</span><span class="sxs-lookup"><span data-stu-id="6b646-115">The second command then uses that object reference and the **Get-AzureBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="6b646-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b646-116">PARAMETERS</span></span>

### <span data-ttu-id="6b646-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="6b646-117">-BatchContext</span></span>
<span data-ttu-id="6b646-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="6b646-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="6b646-119">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6b646-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b646-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b646-120">-JobId</span></span>
<span data-ttu-id="6b646-121">Anger ID för det jobb som innehåller den aktivitet vars under aktiviteter den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6b646-121">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b646-122">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="6b646-122">-MaxCount</span></span>
<span data-ttu-id="6b646-123">Anger det maximala antalet under aktiviteter som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="6b646-123">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="6b646-124">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6b646-124">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="6b646-125">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="6b646-125">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b646-126">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="6b646-126">-Task</span></span>
<span data-ttu-id="6b646-127">Anger en objekt referens till aktiviteten som innehåller de under aktiviteter som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="6b646-127">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="6b646-128">Denna objekt referens skapas med Get-AzureBatchTask cmdlet och det returnerade objektet lagras i en variabel.</span><span class="sxs-lookup"><span data-stu-id="6b646-128">This object reference is created by using the Get-AzureBatchTask cmdlet and storing the returned object in a variable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b646-129">-TaskId</span><span class="sxs-lookup"><span data-stu-id="6b646-129">-TaskId</span></span>
<span data-ttu-id="6b646-130">Anger ID för den aktivitet vars under aktiviteter den här cmdleten returnerar.</span><span class="sxs-lookup"><span data-stu-id="6b646-130">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b646-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b646-131">-DefaultProfile</span></span>
<span data-ttu-id="6b646-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b646-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b646-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b646-133">CommonParameters</span></span>
<span data-ttu-id="6b646-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b646-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b646-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b646-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b646-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b646-136">INPUTS</span></span>

### <span data-ttu-id="6b646-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="6b646-137">BatchAccountContext</span></span>
<span data-ttu-id="6b646-138">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6b646-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="6b646-139">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="6b646-139">PSCloudTask</span></span>
<span data-ttu-id="6b646-140">Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6b646-140">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="6b646-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b646-141">OUTPUTS</span></span>

###  
<span data-ttu-id="6b646-142">Denna cmdlet returnerar instanser av **PSSubtaskInformation** -objektet.</span><span class="sxs-lookup"><span data-stu-id="6b646-142">This cmdlet returns instances of the **PSSubtaskInformation** object.</span></span>

## <span data-ttu-id="6b646-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b646-143">NOTES</span></span>

## <span data-ttu-id="6b646-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b646-144">RELATED LINKS</span></span>

[<span data-ttu-id="6b646-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="6b646-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)


