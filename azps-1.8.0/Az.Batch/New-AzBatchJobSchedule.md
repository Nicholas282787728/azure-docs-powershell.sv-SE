---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 87E7FA51-427E-4DB8-A6A2-D8638FD3DB8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchJobSchedule.md
ms.openlocfilehash: 836ad4cda6d6631baf0885ac0ec380fdc401fde6
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755083"
---
# <span data-ttu-id="ab563-101">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab563-101">New-AzBatchJobSchedule</span></span>

## <span data-ttu-id="ab563-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab563-102">SYNOPSIS</span></span>
<span data-ttu-id="ab563-103">Skapar ett schema i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ab563-103">Creates a job schedule in the Batch service.</span></span>

## <span data-ttu-id="ab563-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab563-104">SYNTAX</span></span>

```
New-AzBatchJobSchedule [-Id] <String> [-DisplayName <String>] -Schedule <PSSchedule>
 -JobSpecification <PSJobSpecification> [-Metadata <IDictionary>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab563-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab563-105">DESCRIPTION</span></span>
<span data-ttu-id="ab563-106">Cmdleten **New-AzBatchJobSchedule** skapar ett schema i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ab563-106">The **New-AzBatchJobSchedule** cmdlet creates a job schedule in the Azure Batch service.</span></span>
<span data-ttu-id="ab563-107">Parametern *BatchAccountContext* anger det konto där denna cmdlet skapar schemat.</span><span class="sxs-lookup"><span data-stu-id="ab563-107">The *BatchAccountContext* parameter specifies the account in which this cmdlet creates the schedule.</span></span>

## <span data-ttu-id="ab563-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab563-108">EXAMPLES</span></span>

### <span data-ttu-id="ab563-109">Exempel 1: skapa ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="ab563-109">Example 1: Create a job schedule</span></span>
```
PS C:\>$Schedule = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSSchedule"
PS C:\> $Schedule.RecurrenceInterval = [TimeSpan]::FromDays(1)
PS C:\> $JobSpecification = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSJobSpecification"
PS C:\> $JobSpecification.PoolInformation = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSPoolInformation"
PS C:\> $JobSpecification.PoolInformation.PoolId = "ContosoPool06"
PS C:\> New-AzBatchJobSchedule -Id "JobSchedule17" -Schedule $Schedule -JobSpecification $JobSpecification -BatchContext $Context
```

<span data-ttu-id="ab563-110">I det här exemplet skapas ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="ab563-110">This example creates a job schedule.</span></span>
<span data-ttu-id="ab563-111">De första fem kommandona skapar och ändrar **PSSchedule** , **PSJobSpecification** och **PSPoolInformation** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ab563-111">The first five commands create and modify **PSSchedule** , **PSJobSpecification** , and **PSPoolInformation** objects.</span></span>
<span data-ttu-id="ab563-112">Kommandona använder New-Object cmdlet och standard-Azure PowerShell-syntax.</span><span class="sxs-lookup"><span data-stu-id="ab563-112">The commands use the New-Object cmdlet and standard Azure PowerShell syntax.</span></span>
<span data-ttu-id="ab563-113">Kommandona lagrar dessa objekt i $Schedule och $JobSpecification variabler.</span><span class="sxs-lookup"><span data-stu-id="ab563-113">The commands store these objects in the $Schedule and $JobSpecification variables.</span></span>
<span data-ttu-id="ab563-114">Med kommandot slut skapas ett jobb schema med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="ab563-114">The final command creates a job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="ab563-115">Det här schemat skapar jobb med ett upprepnings intervall på en dag.</span><span class="sxs-lookup"><span data-stu-id="ab563-115">This schedule creates jobs with a recurrence interval of one day.</span></span>
<span data-ttu-id="ab563-116">Jobben körs på den pool som har ID-ContosoPool06, enligt vad som anges i det femte kommandot.</span><span class="sxs-lookup"><span data-stu-id="ab563-116">The jobs run on the pool that has the ID ContosoPool06, as specified in the fifth command.</span></span>
<span data-ttu-id="ab563-117">Använd cmdleten **Get-AzBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="ab563-117">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ab563-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab563-118">PARAMETERS</span></span>

### <span data-ttu-id="ab563-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ab563-119">-BatchContext</span></span>
<span data-ttu-id="ab563-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ab563-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ab563-121">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ab563-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ab563-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ab563-122">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ab563-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ab563-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ab563-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ab563-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ab563-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab563-125">-DefaultProfile</span></span>
<span data-ttu-id="ab563-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ab563-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab563-127">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ab563-127">-DisplayName</span></span>
<span data-ttu-id="ab563-128">Anger ett visnings namn för jobbschemat.</span><span class="sxs-lookup"><span data-stu-id="ab563-128">Specifies a display name for the job schedule.</span></span>

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

### <span data-ttu-id="ab563-129">-ID</span><span class="sxs-lookup"><span data-stu-id="ab563-129">-Id</span></span>
<span data-ttu-id="ab563-130">Anger ID för det jobb schema som den här cmdleten skapar.</span><span class="sxs-lookup"><span data-stu-id="ab563-130">Specifies the ID of the job schedule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ab563-131">-JobSpecification</span><span class="sxs-lookup"><span data-stu-id="ab563-131">-JobSpecification</span></span>
<span data-ttu-id="ab563-132">Anger information om de jobb som denna cmdlet inkluderar i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="ab563-132">Specifies the details of the jobs that this cmdlet includes in the job schedule.</span></span>

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

### <span data-ttu-id="ab563-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ab563-133">-Metadata</span></span>
<span data-ttu-id="ab563-134">Anger metadata, som nycklar/värde par, för att lägga till i projektschemat.</span><span class="sxs-lookup"><span data-stu-id="ab563-134">Specifies metadata, as key/value pairs, to add to the job schedule.</span></span>
<span data-ttu-id="ab563-135">Det här är namnet på metadata.</span><span class="sxs-lookup"><span data-stu-id="ab563-135">The key is the metadata name.</span></span>
<span data-ttu-id="ab563-136">Värdet är metadata.</span><span class="sxs-lookup"><span data-stu-id="ab563-136">The value is the metadata value.</span></span>

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

### <span data-ttu-id="ab563-137">– Schema</span><span class="sxs-lookup"><span data-stu-id="ab563-137">-Schedule</span></span>
<span data-ttu-id="ab563-138">Anger det schema som avgör när jobb ska skapas.</span><span class="sxs-lookup"><span data-stu-id="ab563-138">Specifies the schedule that determines when to create jobs.</span></span>

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

### <span data-ttu-id="ab563-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab563-139">CommonParameters</span></span>
<span data-ttu-id="ab563-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab563-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab563-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab563-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab563-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab563-142">INPUTS</span></span>

### <span data-ttu-id="ab563-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ab563-143">System.String</span></span>

### <span data-ttu-id="ab563-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ab563-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ab563-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab563-145">OUTPUTS</span></span>

### <span data-ttu-id="ab563-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="ab563-146">System.Void</span></span>

## <span data-ttu-id="ab563-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab563-147">NOTES</span></span>

## <span data-ttu-id="ab563-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab563-148">RELATED LINKS</span></span>

[<span data-ttu-id="ab563-149">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab563-149">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="ab563-150">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab563-150">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="ab563-151">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ab563-151">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ab563-152">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab563-152">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="ab563-153">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab563-153">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="ab563-154">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ab563-154">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="ab563-155">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ab563-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


