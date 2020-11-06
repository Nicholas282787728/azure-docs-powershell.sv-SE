---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: f6a7d03370184b45cc8066e2f17842187cbab98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584467"
---
# <span data-ttu-id="eb42d-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eb42d-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="eb42d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb42d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb42d-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="eb42d-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb42d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb42d-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb42d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb42d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb42d-106">Cmdleten **Remove-AzureBatchJob** tar bort ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="eb42d-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="eb42d-107">Denna cmdlet ber dig bekräfta att du vill ta bort ett jobb, såvida du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="eb42d-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="eb42d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb42d-108">EXAMPLES</span></span>

### <span data-ttu-id="eb42d-109">Exempel 1: ta bort ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="eb42d-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="eb42d-110">Det här kommandot tar bort jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="eb42d-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="eb42d-111">Med kommandot uppmanas du att bekräfta innan jobbet tas bort.</span><span class="sxs-lookup"><span data-stu-id="eb42d-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="eb42d-112">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="eb42d-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="eb42d-113">Exempel 2: ta bort ett batchjobb utan bekräftelse genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="eb42d-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="eb42d-114">Det här kommandot får jobbet som har ID-000002 med hjälp av Get-AzureBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb42d-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="eb42d-115">Kommandot skickar jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="eb42d-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eb42d-116">Kommandot tar bort jobbet.</span><span class="sxs-lookup"><span data-stu-id="eb42d-116">The command deletes that job.</span></span>
<span data-ttu-id="eb42d-117">Eftersom kommandot @ innehåller parametern *Force* uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="eb42d-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="eb42d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb42d-118">PARAMETERS</span></span>

### <span data-ttu-id="eb42d-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="eb42d-119">-BatchContext</span></span>
<span data-ttu-id="eb42d-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="eb42d-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="eb42d-121">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="eb42d-121">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="eb42d-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="eb42d-122">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="eb42d-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="eb42d-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="eb42d-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="eb42d-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="eb42d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb42d-125">-DefaultProfile</span></span>
<span data-ttu-id="eb42d-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb42d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb42d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="eb42d-127">-Force</span></span>
<span data-ttu-id="eb42d-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="eb42d-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eb42d-129">-ID</span><span class="sxs-lookup"><span data-stu-id="eb42d-129">-Id</span></span>
<span data-ttu-id="eb42d-130">Anger ID för det jobb som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="eb42d-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="eb42d-131">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="eb42d-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="eb42d-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb42d-132">-Confirm</span></span>
<span data-ttu-id="eb42d-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb42d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb42d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb42d-134">-WhatIf</span></span>
<span data-ttu-id="eb42d-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb42d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb42d-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb42d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb42d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb42d-137">CommonParameters</span></span>
<span data-ttu-id="eb42d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb42d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb42d-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb42d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb42d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb42d-140">INPUTS</span></span>

### <span data-ttu-id="eb42d-141">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="eb42d-141">BatchAccountContext</span></span>
<span data-ttu-id="eb42d-142">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="eb42d-142">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="eb42d-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb42d-143">OUTPUTS</span></span>

## <span data-ttu-id="eb42d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb42d-144">NOTES</span></span>

## <span data-ttu-id="eb42d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb42d-145">RELATED LINKS</span></span>

[<span data-ttu-id="eb42d-146">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eb42d-146">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="eb42d-147">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eb42d-147">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="eb42d-148">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eb42d-148">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="eb42d-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="eb42d-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="eb42d-150">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eb42d-150">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="eb42d-151">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="eb42d-151">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="eb42d-152">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="eb42d-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


