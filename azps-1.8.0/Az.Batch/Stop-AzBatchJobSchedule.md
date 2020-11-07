---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928326"
---
# <span data-ttu-id="dbfee-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbfee-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="dbfee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbfee-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfee-103">Stoppar ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="dbfee-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="dbfee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbfee-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbfee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbfee-105">DESCRIPTION</span></span>
<span data-ttu-id="dbfee-106">Cmdleten **Stop-AzBatchJobSchedule** stoppar ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="dbfee-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="dbfee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbfee-107">EXAMPLES</span></span>

### <span data-ttu-id="dbfee-108">Exempel 1: stoppa ett schema</span><span class="sxs-lookup"><span data-stu-id="dbfee-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="dbfee-109">Det här kommandot stoppar projektschemat med ID-JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="dbfee-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="dbfee-110">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="dbfee-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="dbfee-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbfee-111">PARAMETERS</span></span>

### <span data-ttu-id="dbfee-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dbfee-112">-BatchContext</span></span>
<span data-ttu-id="dbfee-113">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dbfee-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dbfee-114">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dbfee-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dbfee-115">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="dbfee-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dbfee-116">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="dbfee-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dbfee-117">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="dbfee-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dbfee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfee-118">-DefaultProfile</span></span>
<span data-ttu-id="dbfee-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbfee-120">-ID</span><span class="sxs-lookup"><span data-stu-id="dbfee-120">-Id</span></span>
<span data-ttu-id="dbfee-121">Anger ID för det fin schema som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="dbfee-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="dbfee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfee-122">CommonParameters</span></span>
<span data-ttu-id="dbfee-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfee-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbfee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfee-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbfee-125">INPUTS</span></span>

### <span data-ttu-id="dbfee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dbfee-126">System.String</span></span>

### <span data-ttu-id="dbfee-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dbfee-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="dbfee-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbfee-128">OUTPUTS</span></span>

### <span data-ttu-id="dbfee-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="dbfee-129">System.Void</span></span>

## <span data-ttu-id="dbfee-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbfee-130">NOTES</span></span>

## <span data-ttu-id="dbfee-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbfee-131">RELATED LINKS</span></span>

[<span data-ttu-id="dbfee-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbfee-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="dbfee-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbfee-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="dbfee-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dbfee-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="dbfee-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbfee-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="dbfee-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbfee-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="dbfee-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="dbfee-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="dbfee-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="dbfee-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


