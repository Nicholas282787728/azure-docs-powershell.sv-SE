---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: ac63bbdb95551ff5ff08661a92f0924d5853ade5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580676"
---
# <span data-ttu-id="4ecf3-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4ecf3-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="4ecf3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ecf3-102">SYNOPSIS</span></span>
<span data-ttu-id="4ecf3-103">Stoppar en batchuppgiften.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ecf3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ecf3-104">SYNTAX</span></span>

### <span data-ttu-id="4ecf3-105">Et</span><span class="sxs-lookup"><span data-stu-id="4ecf3-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ecf3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4ecf3-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ecf3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ecf3-107">DESCRIPTION</span></span>
<span data-ttu-id="4ecf3-108">Cmdleten **Stop-AzureBatchTask** stoppar en Azure Batch-uppgift.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="4ecf3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ecf3-109">EXAMPLES</span></span>

### <span data-ttu-id="4ecf3-110">Exempel 1: ta bort en batch-uppgift efter ID</span><span class="sxs-lookup"><span data-stu-id="4ecf3-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="4ecf3-111">Det här kommandot stoppar en aktivitet med ID-Task23 under det jobb som har ID-jobbet 000001.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="4ecf3-112">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="4ecf3-113">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="4ecf3-114">Exempel 2: stoppa en batchprocess genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="4ecf3-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="4ecf3-115">Med det här kommandot får du den batch-uppgift som har det ID-Task26 i jobbet som har ID-jobbet 000001 genom att använda Get-AzureBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="4ecf3-116">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4ecf3-117">Kommandot stoppar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-117">The command stops that task.</span></span>

## <span data-ttu-id="4ecf3-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ecf3-118">PARAMETERS</span></span>

### <span data-ttu-id="4ecf3-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4ecf3-119">-BatchContext</span></span>
<span data-ttu-id="4ecf3-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4ecf3-121">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4ecf3-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4ecf3-122">-Id</span></span>
<span data-ttu-id="4ecf3-123">Anger ID för den aktivitet som cmdleten slutar.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-123">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecf3-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="4ecf3-124">-JobId</span></span>
<span data-ttu-id="4ecf3-125">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-125">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecf3-126">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="4ecf3-126">-Task</span></span>
<span data-ttu-id="4ecf3-127">Anger den uppgift som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-127">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="4ecf3-128">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-128">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ecf3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ecf3-129">-DefaultProfile</span></span>
<span data-ttu-id="4ecf3-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ecf3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ecf3-131">CommonParameters</span></span>
<span data-ttu-id="4ecf3-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ecf3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ecf3-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ecf3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ecf3-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ecf3-134">INPUTS</span></span>

### <span data-ttu-id="4ecf3-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4ecf3-135">BatchAccountContext</span></span>
<span data-ttu-id="4ecf3-136">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4ecf3-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4ecf3-137">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="4ecf3-137">PSCloudTask</span></span>
<span data-ttu-id="4ecf3-138">Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4ecf3-138">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="4ecf3-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ecf3-139">OUTPUTS</span></span>

## <span data-ttu-id="4ecf3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ecf3-140">NOTES</span></span>

## <span data-ttu-id="4ecf3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ecf3-141">RELATED LINKS</span></span>

[<span data-ttu-id="4ecf3-142">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4ecf3-142">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="4ecf3-143">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4ecf3-143">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="4ecf3-144">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="4ecf3-144">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="4ecf3-145">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="4ecf3-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


