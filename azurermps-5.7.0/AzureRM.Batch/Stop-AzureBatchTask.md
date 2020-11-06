---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchTask.md
ms.openlocfilehash: 979c136f1bdbd216cebe367060ebdc5d8360ea24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574407"
---
# <span data-ttu-id="d3137-101">Stop-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d3137-101">Stop-AzureBatchTask</span></span>

## <span data-ttu-id="d3137-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3137-102">SYNOPSIS</span></span>
<span data-ttu-id="d3137-103">Stoppar en batchuppgiften.</span><span class="sxs-lookup"><span data-stu-id="d3137-103">Stops a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3137-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3137-104">SYNTAX</span></span>

### <span data-ttu-id="d3137-105">Et</span><span class="sxs-lookup"><span data-stu-id="d3137-105">Id</span></span>
```
Stop-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3137-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d3137-106">InputObject</span></span>
```
Stop-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3137-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3137-107">DESCRIPTION</span></span>
<span data-ttu-id="d3137-108">Cmdleten **Stop-AzureBatchTask** stoppar en Azure Batch-uppgift.</span><span class="sxs-lookup"><span data-stu-id="d3137-108">The **Stop-AzureBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="d3137-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3137-109">EXAMPLES</span></span>

### <span data-ttu-id="d3137-110">Exempel 1: ta bort en batch-uppgift efter ID</span><span class="sxs-lookup"><span data-stu-id="d3137-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="d3137-111">Det här kommandot stoppar en aktivitet med ID-Task23 under det jobb som har ID-jobbet 000001.</span><span class="sxs-lookup"><span data-stu-id="d3137-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d3137-112">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d3137-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d3137-113">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="d3137-113">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d3137-114">Exempel 2: stoppa en batchprocess genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="d3137-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="d3137-115">Med det här kommandot får du den batch-uppgift som har det ID-Task26 i jobbet som har ID-jobbet 000001 genom att använda Get-AzureBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3137-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="d3137-116">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d3137-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d3137-117">Kommandot stoppar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d3137-117">The command stops that task.</span></span>

## <span data-ttu-id="d3137-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3137-118">PARAMETERS</span></span>

### <span data-ttu-id="d3137-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d3137-119">-BatchContext</span></span>
<span data-ttu-id="d3137-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d3137-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d3137-121">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d3137-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d3137-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="d3137-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d3137-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="d3137-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d3137-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d3137-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3137-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3137-125">-DefaultProfile</span></span>
<span data-ttu-id="d3137-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3137-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3137-127">-ID</span><span class="sxs-lookup"><span data-stu-id="d3137-127">-Id</span></span>
<span data-ttu-id="d3137-128">Anger ID för den aktivitet som cmdleten slutar.</span><span class="sxs-lookup"><span data-stu-id="d3137-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3137-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="d3137-129">-JobId</span></span>
<span data-ttu-id="d3137-130">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d3137-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3137-131">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="d3137-131">-Task</span></span>
<span data-ttu-id="d3137-132">Anger den uppgift som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="d3137-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="d3137-133">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="d3137-133">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: InputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3137-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3137-134">CommonParameters</span></span>
<span data-ttu-id="d3137-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3137-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3137-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3137-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3137-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3137-137">INPUTS</span></span>

### <span data-ttu-id="d3137-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d3137-138">BatchAccountContext</span></span>
<span data-ttu-id="d3137-139">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d3137-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d3137-140">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d3137-140">PSCloudTask</span></span>
<span data-ttu-id="d3137-141">Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d3137-141">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="d3137-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3137-142">OUTPUTS</span></span>

## <span data-ttu-id="d3137-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3137-143">NOTES</span></span>

## <span data-ttu-id="d3137-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3137-144">RELATED LINKS</span></span>

[<span data-ttu-id="d3137-145">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d3137-145">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="d3137-146">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d3137-146">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="d3137-147">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="d3137-147">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="d3137-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d3137-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


