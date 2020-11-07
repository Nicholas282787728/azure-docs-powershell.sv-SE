---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7D0D8B46-4BF0-47D5-9261-3306AEB9E7DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsubtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSubtask.md
ms.openlocfilehash: 463f19b5ed459f0c2b2f4a4fdeff40bf69db2682
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754695"
---
# <span data-ttu-id="10656-101">Get-AzBatchSubtask</span><span class="sxs-lookup"><span data-stu-id="10656-101">Get-AzBatchSubtask</span></span>

## <span data-ttu-id="10656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10656-102">SYNOPSIS</span></span>
<span data-ttu-id="10656-103">Hämtar under aktivitetens information för den angivna aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="10656-103">Gets the subtask information of the specified task.</span></span>

## <span data-ttu-id="10656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10656-104">SYNTAX</span></span>

### <span data-ttu-id="10656-105">ODataFilter (standard)</span><span class="sxs-lookup"><span data-stu-id="10656-105">ODataFilter (Default)</span></span>
```
Get-AzBatchSubtask [-JobId] <String> [-TaskId] <String> [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10656-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="10656-106">ParentObject</span></span>
```
Get-AzBatchSubtask [[-Task] <PSCloudTask>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10656-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10656-107">DESCRIPTION</span></span>
<span data-ttu-id="10656-108">Cmdleten **Get-AzBatchSubtask** hämtar under aktivitetens information om den angivna uppgiften.</span><span class="sxs-lookup"><span data-stu-id="10656-108">The **Get-AzBatchSubtask** cmdlet retrieves the subtask information about the specified task.</span></span>
<span data-ttu-id="10656-109">Under aktiviteter ger parallell bearbetning för enskilda uppgifter och möjliggör noggrann övervakning av aktivitets körning och förlopp.</span><span class="sxs-lookup"><span data-stu-id="10656-109">Subtasks provide parallel processing for individual tasks, and enable precise monitoring of task execution and progress.</span></span>

## <span data-ttu-id="10656-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10656-110">EXAMPLES</span></span>

### <span data-ttu-id="10656-111">Exempel 1: returnera alla under aktiviteter för en viss aktivitet</span><span class="sxs-lookup"><span data-stu-id="10656-111">Example 1: Return all subtasks for a specified task</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "contosobatchaccount"
PS C:\> Get-AzBatchSubtask -JobId "Job-01" -TaskID "myTask" -BatchContext $Context
```

<span data-ttu-id="10656-112">De här kommandona returnerar alla under aktiviteter för aktiviteten med aktivitets-ID: t.</span><span class="sxs-lookup"><span data-stu-id="10656-112">These commands return all the subtasks for the task with the ID myTask.</span></span>
<span data-ttu-id="10656-113">För att göra detta skapar det första kommandot i exemplet en objekt referens till konto nycklarna för batch-contosobatchaccount.</span><span class="sxs-lookup"><span data-stu-id="10656-113">To do this, the first command in the example creates an object reference to the account keys for the batch account contosobatchaccount.</span></span>
<span data-ttu-id="10656-114">Denna objekt referens lagras i en variabel som heter $context.</span><span class="sxs-lookup"><span data-stu-id="10656-114">This object reference is stored in a variable named $context.</span></span>
<span data-ttu-id="10656-115">Med det andra kommandot används den objekt referensen och cmdleten **Get-AzBatchSubtask** för att returnera alla under aktiviteter för min aktivitet, en aktivitet som körs som en del av jobb jobbet – 01.</span><span class="sxs-lookup"><span data-stu-id="10656-115">The second command then uses that object reference and the **Get-AzBatchSubtask** cmdlet to return all the subtasks for myTask, a task that runs as part of job Job-01.</span></span>

## <span data-ttu-id="10656-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10656-116">PARAMETERS</span></span>

### <span data-ttu-id="10656-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="10656-117">-BatchContext</span></span>
<span data-ttu-id="10656-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="10656-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="10656-119">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="10656-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="10656-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="10656-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="10656-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="10656-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="10656-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="10656-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="10656-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10656-123">-DefaultProfile</span></span>
<span data-ttu-id="10656-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10656-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10656-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="10656-125">-JobId</span></span>
<span data-ttu-id="10656-126">Anger ID för det jobb som innehåller den aktivitet vars under aktiviteter den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="10656-126">Specifies the ID of the job that contains the task whose subtasks this cmdlet gets.</span></span>

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

### <span data-ttu-id="10656-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="10656-127">-MaxCount</span></span>
<span data-ttu-id="10656-128">Anger det maximala antalet under aktiviteter som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="10656-128">Specifies the maximum number of subtasks to return.</span></span>
<span data-ttu-id="10656-129">Om du anger ett värde som är noll (0) eller mindre används ingen övre gräns av cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10656-129">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="10656-130">Standardvärdet är 1000.</span><span class="sxs-lookup"><span data-stu-id="10656-130">The default value is 1000.</span></span>

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

### <span data-ttu-id="10656-131">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="10656-131">-Task</span></span>
<span data-ttu-id="10656-132">Anger en objekt referens till aktiviteten som innehåller de under aktiviteter som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="10656-132">Specifies an object reference to the task that contain the subtasks that this cmdlet returns.</span></span>
<span data-ttu-id="10656-133">Denna objekt referens skapas med Get-AzBatchTask cmdlet och det returnerade objektet lagras i en variabel.</span><span class="sxs-lookup"><span data-stu-id="10656-133">This object reference is created by using the Get-AzBatchTask cmdlet and storing the returned object in a variable.</span></span>

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

### <span data-ttu-id="10656-134">-TaskId</span><span class="sxs-lookup"><span data-stu-id="10656-134">-TaskId</span></span>
<span data-ttu-id="10656-135">Anger ID för den aktivitet vars under aktiviteter den här cmdleten returnerar.</span><span class="sxs-lookup"><span data-stu-id="10656-135">Specifies the ID of the task whose subtasks this cmdlet returns.</span></span>

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

### <span data-ttu-id="10656-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10656-136">CommonParameters</span></span>
<span data-ttu-id="10656-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10656-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10656-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10656-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10656-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10656-139">INPUTS</span></span>

### <span data-ttu-id="10656-140">System. String</span><span class="sxs-lookup"><span data-stu-id="10656-140">System.String</span></span>

### <span data-ttu-id="10656-141">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="10656-141">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="10656-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="10656-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="10656-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10656-143">OUTPUTS</span></span>

### <span data-ttu-id="10656-144">Microsoft.Azure.Commands.BatCH. Modeller. PSSubtaskInformation</span><span class="sxs-lookup"><span data-stu-id="10656-144">Microsoft.Azure.Commands.Batch.Models.PSSubtaskInformation</span></span>

## <span data-ttu-id="10656-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10656-145">NOTES</span></span>

## <span data-ttu-id="10656-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10656-146">RELATED LINKS</span></span>

[<span data-ttu-id="10656-147">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="10656-147">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)


