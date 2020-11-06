---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJob.md
ms.openlocfilehash: 0d210056670baa974c7bf11e9c44142c11f2721e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582515"
---
# <span data-ttu-id="d6386-101">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6386-101">Remove-AzureBatchJob</span></span>

## <span data-ttu-id="d6386-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6386-102">SYNOPSIS</span></span>
<span data-ttu-id="d6386-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="d6386-103">Deletes a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6386-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6386-104">SYNTAX</span></span>

```
Remove-AzureBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6386-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6386-105">DESCRIPTION</span></span>
<span data-ttu-id="d6386-106">Cmdleten **Remove-AzureBatchJob** tar bort ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="d6386-106">The **Remove-AzureBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="d6386-107">Denna cmdlet ber dig bekräfta att du vill ta bort ett jobb, såvida du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="d6386-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="d6386-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6386-108">EXAMPLES</span></span>

### <span data-ttu-id="d6386-109">Exempel 1: ta bort ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="d6386-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="d6386-110">Det här kommandot tar bort jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="d6386-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d6386-111">Med kommandot uppmanas du att bekräfta innan jobbet tas bort.</span><span class="sxs-lookup"><span data-stu-id="d6386-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="d6386-112">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="d6386-112">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d6386-113">Exempel 2: ta bort ett batchjobb utan bekräftelse genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="d6386-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzureBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="d6386-114">Det här kommandot får jobbet som har ID-000002 med hjälp av Get-AzureBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6386-114">This command gets the job that has the ID Job-000002 by using the Get-AzureBatchJob cmdlet.</span></span>
<span data-ttu-id="d6386-115">Kommandot skickar jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d6386-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d6386-116">Kommandot tar bort jobbet.</span><span class="sxs-lookup"><span data-stu-id="d6386-116">The command deletes that job.</span></span>
<span data-ttu-id="d6386-117">Eftersom kommandot @ innehåller parametern *Force* uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d6386-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="d6386-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6386-118">PARAMETERS</span></span>

### <span data-ttu-id="d6386-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d6386-119">-BatchContext</span></span>
<span data-ttu-id="d6386-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d6386-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d6386-121">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="d6386-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d6386-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d6386-122">-Force</span></span>
<span data-ttu-id="d6386-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d6386-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6386-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d6386-124">-Id</span></span>
<span data-ttu-id="d6386-125">Anger ID för det jobb som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="d6386-125">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="d6386-126">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="d6386-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="d6386-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6386-127">-Confirm</span></span>
<span data-ttu-id="d6386-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6386-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6386-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6386-129">-WhatIf</span></span>
<span data-ttu-id="d6386-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6386-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6386-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6386-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6386-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6386-132">-DefaultProfile</span></span>
<span data-ttu-id="d6386-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6386-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6386-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6386-134">CommonParameters</span></span>
<span data-ttu-id="d6386-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6386-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6386-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6386-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6386-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6386-137">INPUTS</span></span>

### <span data-ttu-id="d6386-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d6386-138">BatchAccountContext</span></span>
<span data-ttu-id="d6386-139">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d6386-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="d6386-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6386-140">OUTPUTS</span></span>

## <span data-ttu-id="d6386-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6386-141">NOTES</span></span>

## <span data-ttu-id="d6386-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6386-142">RELATED LINKS</span></span>

[<span data-ttu-id="d6386-143">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6386-143">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="d6386-144">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6386-144">Enable-AzureBatchJob</span></span>](./Enable-AzureBatchJob.md)

[<span data-ttu-id="d6386-145">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6386-145">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="d6386-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d6386-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d6386-147">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6386-147">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="d6386-148">Stopp-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="d6386-148">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="d6386-149">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d6386-149">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


