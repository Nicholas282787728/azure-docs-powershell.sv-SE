---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: 91ac0d6202eb02f724f3ea17e57846e6db6b7412
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745409"
---
# <span data-ttu-id="98a57-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="98a57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98a57-102">SYNOPSIS</span></span>
<span data-ttu-id="98a57-103">Anger ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="98a57-103">Sets a job schedule.</span></span>

## <span data-ttu-id="98a57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98a57-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98a57-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98a57-105">DESCRIPTION</span></span>
<span data-ttu-id="98a57-106">Cmdleten **set-AzBatchJobSchedule** anger ett schema i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="98a57-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="98a57-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98a57-107">EXAMPLES</span></span>

### <span data-ttu-id="98a57-108">Exempel 1: uppdatera ett jobb schema</span><span class="sxs-lookup"><span data-stu-id="98a57-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="98a57-109">Det första kommandot får jobbet genom att använda **Get-AzBatchJobSchedule** och lagrar det sedan i $JobSchedule variabel.</span><span class="sxs-lookup"><span data-stu-id="98a57-109">The first command gets a job by using **Get-AzBatchJobSchedule** , and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="98a57-110">Det andra kommandot ändrar upprepnings intervallet för `$JobSchedule.Schedule` objektet.</span><span class="sxs-lookup"><span data-stu-id="98a57-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="98a57-111">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="98a57-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="98a57-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98a57-112">PARAMETERS</span></span>

### <span data-ttu-id="98a57-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="98a57-113">-BatchContext</span></span>
<span data-ttu-id="98a57-114">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="98a57-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="98a57-115">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="98a57-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="98a57-116">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="98a57-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="98a57-117">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="98a57-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="98a57-118">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="98a57-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="98a57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98a57-119">-DefaultProfile</span></span>
<span data-ttu-id="98a57-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98a57-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98a57-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-121">-JobSchedule</span></span>
<span data-ttu-id="98a57-122">Anger ett **PSCloudJobSchedule** -objekt som representerar ett jobb schema.</span><span class="sxs-lookup"><span data-stu-id="98a57-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="98a57-123">För att hämta ett **PSCloudJobSchedule** -objekt, Använd cmdleten Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="98a57-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98a57-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98a57-124">CommonParameters</span></span>
<span data-ttu-id="98a57-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98a57-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98a57-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98a57-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98a57-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98a57-127">INPUTS</span></span>

### <span data-ttu-id="98a57-128">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="98a57-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="98a57-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="98a57-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98a57-130">OUTPUTS</span></span>

### <span data-ttu-id="98a57-131">System. Void</span><span class="sxs-lookup"><span data-stu-id="98a57-131">System.Void</span></span>

## <span data-ttu-id="98a57-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98a57-132">NOTES</span></span>

## <span data-ttu-id="98a57-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98a57-133">RELATED LINKS</span></span>

[<span data-ttu-id="98a57-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="98a57-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="98a57-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="98a57-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="98a57-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="98a57-139">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="98a57-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


