---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576635"
---
# <span data-ttu-id="4f190-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="4f190-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f190-102">SYNOPSIS</span></span>
<span data-ttu-id="4f190-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="4f190-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f190-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f190-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f190-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f190-105">DESCRIPTION</span></span>
<span data-ttu-id="4f190-106">Cmdleten **Remove-AzureBatchJobSchedule** tar bort ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="4f190-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="4f190-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f190-107">EXAMPLES</span></span>

## <span data-ttu-id="4f190-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f190-108">PARAMETERS</span></span>

### <span data-ttu-id="4f190-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4f190-109">-BatchContext</span></span>
<span data-ttu-id="4f190-110">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4f190-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4f190-111">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4f190-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4f190-112">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="4f190-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4f190-113">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="4f190-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4f190-114">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4f190-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4f190-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f190-115">-DefaultProfile</span></span>
<span data-ttu-id="4f190-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f190-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f190-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4f190-117">-Force</span></span>
<span data-ttu-id="4f190-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4f190-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f190-119">-ID</span><span class="sxs-lookup"><span data-stu-id="4f190-119">-Id</span></span>
<span data-ttu-id="4f190-120">Anger ID för den fin planering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="4f190-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f190-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f190-121">-Confirm</span></span>
<span data-ttu-id="4f190-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f190-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f190-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f190-123">-WhatIf</span></span>
<span data-ttu-id="4f190-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f190-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f190-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f190-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f190-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f190-126">CommonParameters</span></span>
<span data-ttu-id="4f190-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f190-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f190-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f190-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f190-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f190-129">INPUTS</span></span>

### <span data-ttu-id="4f190-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4f190-130">BatchAccountContext</span></span>
<span data-ttu-id="4f190-131">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4f190-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="4f190-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f190-132">OUTPUTS</span></span>

## <span data-ttu-id="4f190-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f190-133">NOTES</span></span>

## <span data-ttu-id="4f190-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f190-134">RELATED LINKS</span></span>

[<span data-ttu-id="4f190-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4f190-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4f190-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="4f190-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="4f190-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="4f190-140">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4f190-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


