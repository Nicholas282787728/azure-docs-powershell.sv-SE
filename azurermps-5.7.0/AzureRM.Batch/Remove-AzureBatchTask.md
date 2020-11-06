---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 775425b0da46ef6c2b22e1c28725b323b3071974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583655"
---
# <span data-ttu-id="ecc3a-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ecc3a-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="ecc3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc3a-103">Tar bort en batchuppgiften.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecc3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecc3a-104">SYNTAX</span></span>

### <span data-ttu-id="ecc3a-105">Et</span><span class="sxs-lookup"><span data-stu-id="ecc3a-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc3a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecc3a-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecc3a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecc3a-107">DESCRIPTION</span></span>
<span data-ttu-id="ecc3a-108">Cmdleten **Remove-AzureBatchTask** tar bort en Azure Batch-uppgift.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="ecc3a-109">Denna cmdlet uppmanar dig att bekräfta om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="ecc3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecc3a-110">EXAMPLES</span></span>

### <span data-ttu-id="ecc3a-111">Exempel 1: ta bort en batch-uppgift efter ID</span><span class="sxs-lookup"><span data-stu-id="ecc3a-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="ecc3a-112">Det här kommandot tar bort en aktivitet med ID-Task23 under jobbet som har ID-jobbet-000001.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="ecc3a-113">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="ecc3a-114">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ecc3a-115">Exempel 2: ta bort en batchuppgiften med hjälp av försäljnings förloppet utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="ecc3a-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="ecc3a-116">Med det här kommandot får du den batch-uppgift som har det ID-Task26 i jobbet som har ID-jobbet 000001 genom att använda cmdleten **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="ecc3a-117">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ecc3a-118">Kommandot tar bort uppgiften.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-118">The command deletes that task.</span></span>
<span data-ttu-id="ecc3a-119">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ecc3a-120">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ecc3a-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecc3a-121">PARAMETERS</span></span>

### <span data-ttu-id="ecc3a-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ecc3a-122">-BatchContext</span></span>
<span data-ttu-id="ecc3a-123">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ecc3a-124">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ecc3a-125">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ecc3a-126">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ecc3a-127">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ecc3a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc3a-128">-DefaultProfile</span></span>
<span data-ttu-id="ecc3a-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc3a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="ecc3a-130">-Force</span></span>
<span data-ttu-id="ecc3a-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ecc3a-132">-ID</span><span class="sxs-lookup"><span data-stu-id="ecc3a-132">-Id</span></span>
<span data-ttu-id="ecc3a-133">Anger ID för den aktivitet som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="ecc3a-134">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ecc3a-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecc3a-135">-InputObject</span></span>
<span data-ttu-id="ecc3a-136">Anger den uppgift som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="ecc3a-137">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="ecc3a-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="ecc3a-138">-JobId</span></span>
<span data-ttu-id="ecc3a-139">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="ecc3a-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ecc3a-140">-Confirm</span></span>
<span data-ttu-id="ecc3a-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc3a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc3a-142">-WhatIf</span></span>
<span data-ttu-id="ecc3a-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecc3a-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc3a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc3a-145">CommonParameters</span></span>
<span data-ttu-id="ecc3a-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc3a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc3a-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecc3a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc3a-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecc3a-148">INPUTS</span></span>

### <span data-ttu-id="ecc3a-149">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ecc3a-149">BatchAccountContext</span></span>
<span data-ttu-id="ecc3a-150">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ecc3a-150">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="ecc3a-151">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="ecc3a-151">PSCloudTask</span></span>
<span data-ttu-id="ecc3a-152">Parametern ' InputObject ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ecc3a-152">Parameter 'InputObject' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="ecc3a-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecc3a-153">OUTPUTS</span></span>

## <span data-ttu-id="ecc3a-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecc3a-154">NOTES</span></span>

## <span data-ttu-id="ecc3a-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecc3a-155">RELATED LINKS</span></span>

[<span data-ttu-id="ecc3a-156">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ecc3a-156">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ecc3a-157">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ecc3a-157">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="ecc3a-158">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ecc3a-158">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="ecc3a-159">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ecc3a-159">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="ecc3a-160">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="ecc3a-160">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="ecc3a-161">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ecc3a-161">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


