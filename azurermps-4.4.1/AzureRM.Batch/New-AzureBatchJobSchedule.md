---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchJobSchedule.md
ms.openlocfilehash: 0a31b787b1be6d45caca74d01ee5d15d00071641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578480"
---
# <span data-ttu-id="e50da-101">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e50da-101">New-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="e50da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e50da-102">SYNOPSIS</span></span>
<span data-ttu-id="e50da-103">Skapar ett schema i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e50da-103">Creates a job schedule in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e50da-104">SYNTAX</span></span>

```
New-AzureBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e50da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e50da-105">DESCRIPTION</span></span>
<span data-ttu-id="e50da-106">Cmdleten **New-AzureBatchJobSchedule** skapar ett schema i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e50da-106">The **New-AzureBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="e50da-107">Parametern *BatchAccountContext* anger det konto där denna cmdlet skapar schemat.</span><span class="sxs-lookup"><span data-stu-id="e50da-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="e50da-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e50da-108">EXAMPLES</span></span>

### <span data-ttu-id="e50da-109">Exempel 1: skapa ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="e50da-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzureBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="e50da-110">I det här exemplet skapas ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="e50da-110">This example creates a job schedule.</span></span>

<span data-ttu-id="e50da-111">De första fem kommandona skapar och ändrar **PSSchedule** , **PSJobSpecification** och **PSPoolInformation** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e50da-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="e50da-112">Kommandona använder New-Object cmdlet och standard-Azure PowerShell-syntax.</span><span class="sxs-lookup"><span data-stu-id="e50da-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="e50da-113">Kommandona lagrar dessa objekt i $Schedule och $JobSpecification variabler.</span><span class="sxs-lookup"><span data-stu-id="e50da-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>

<span data-ttu-id="e50da-114">Med kommandot slut skapas ett jobb schema med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="e50da-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="e50da-115">Det här schemat skapar jobb med ett upprepnings intervall på en dag.</span><span class="sxs-lookup"><span data-stu-id="e50da-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="e50da-116">Jobben körs på den pool som har ID-ContosoPool06, enligt vad som anges i det femte kommandot.</span><span class="sxs-lookup"><span data-stu-id="e50da-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="e50da-117">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="e50da-117">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="e50da-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e50da-118">PARAMETERS</span></span>

### <span data-ttu-id="e50da-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e50da-119">-BatchContext</span></span>
<span data-ttu-id="e50da-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e50da-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e50da-121">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e50da-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e50da-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e50da-122">-DisplayName</span></span>
<span data-ttu-id="e50da-123">Anger ett visnings namn för jobbschemat.</span><span class="sxs-lookup"><span data-stu-id="e50da-123">Specifies a display name for the job schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50da-124">-ID</span><span class="sxs-lookup"><span data-stu-id="e50da-124">-Id</span></span>
<span data-ttu-id="e50da-125">Anger ID för det jobb schema som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="e50da-125">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e50da-126">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="e50da-126">-JobSpecification</span></span>
<span data-ttu-id="e50da-127">Anger information om de jobb som denna cmdlet inkluderar i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="e50da-127">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSJobSpecification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50da-128">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e50da-128">-Metadata</span></span>
<span data-ttu-id="e50da-129">Anger metadata, som nycklar/värde par, för att lägga till i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="e50da-129">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="e50da-130">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="e50da-130">The key is the metadata name.</span></span>
<span data-ttu-id="e50da-131">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="e50da-131">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50da-132">– Schema</span><span class="sxs-lookup"><span data-stu-id="e50da-132">-Schedule</span></span>
<span data-ttu-id="e50da-133">Anger det schema som avgör när jobb ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e50da-133">Specifies the schedule that determines when to create jobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSSchedule
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e50da-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50da-134">-DefaultProfile</span></span>
<span data-ttu-id="e50da-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e50da-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e50da-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50da-136">CommonParameters</span></span>
<span data-ttu-id="e50da-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e50da-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50da-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e50da-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50da-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e50da-139">INPUTS</span></span>

### <span data-ttu-id="e50da-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e50da-140">BatchAccountContext</span></span>
<span data-ttu-id="e50da-141">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e50da-141">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="e50da-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e50da-142">OUTPUTS</span></span>

## <span data-ttu-id="e50da-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e50da-143">NOTES</span></span>

## <span data-ttu-id="e50da-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e50da-144">RELATED LINKS</span></span>

[<span data-ttu-id="e50da-145">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e50da-145">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e50da-146">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e50da-146">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="e50da-147">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e50da-147">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="e50da-148">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e50da-148">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="e50da-149">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e50da-149">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="e50da-150">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="e50da-150">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="e50da-151">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e50da-151">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


