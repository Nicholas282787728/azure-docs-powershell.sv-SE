---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: f874432bc26ae2a579a54e4068c719b236ad4c45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101138"
---
# <span data-ttu-id="ff016-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ff016-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="ff016-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff016-102">SYNOPSIS</span></span>
<span data-ttu-id="ff016-103">Inaktiverar schemaläggning av batchjobb.</span><span class="sxs-lookup"><span data-stu-id="ff016-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="ff016-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff016-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff016-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff016-105">DESCRIPTION</span></span>
<span data-ttu-id="ff016-106">Cmdleten **disable-AzBatchJobSchedule** inaktiverar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="ff016-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="ff016-107">Om du inaktiverar ett schema skapas inte jobb enligt det schemat.</span><span class="sxs-lookup"><span data-stu-id="ff016-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="ff016-108">Du kan aktivera ett inaktiverat schema senare.</span><span class="sxs-lookup"><span data-stu-id="ff016-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="ff016-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff016-109">EXAMPLES</span></span>

### <span data-ttu-id="ff016-110">Exempel 1: inaktivera en finplanera</span><span class="sxs-lookup"><span data-stu-id="ff016-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="ff016-111">Det här kommandot inaktiverar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="ff016-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="ff016-112">Använd cmdleten **Get-AzBatchAccountKey** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="ff016-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ff016-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff016-113">PARAMETERS</span></span>

### <span data-ttu-id="ff016-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ff016-114">-BatchContext</span></span>
<span data-ttu-id="ff016-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ff016-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ff016-116">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ff016-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ff016-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ff016-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ff016-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ff016-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ff016-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ff016-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ff016-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff016-120">-DefaultProfile</span></span>
<span data-ttu-id="ff016-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff016-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff016-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ff016-122">-Id</span></span>
<span data-ttu-id="ff016-123">Anger ID för det jobb schema som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="ff016-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff016-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff016-124">CommonParameters</span></span>
<span data-ttu-id="ff016-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff016-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff016-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff016-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff016-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff016-127">INPUTS</span></span>

### <span data-ttu-id="ff016-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ff016-128">System.String</span></span>

### <span data-ttu-id="ff016-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ff016-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ff016-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff016-130">OUTPUTS</span></span>

### <span data-ttu-id="ff016-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="ff016-131">System.Void</span></span>

## <span data-ttu-id="ff016-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff016-132">NOTES</span></span>

## <span data-ttu-id="ff016-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff016-133">RELATED LINKS</span></span>

[<span data-ttu-id="ff016-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ff016-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="ff016-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff016-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ff016-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ff016-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="ff016-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ff016-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="ff016-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ff016-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="ff016-139">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ff016-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="ff016-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ff016-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
