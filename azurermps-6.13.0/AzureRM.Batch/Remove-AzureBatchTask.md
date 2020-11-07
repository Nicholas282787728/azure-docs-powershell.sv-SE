---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchTask.md
ms.openlocfilehash: 3012abfca2ca257ad7b72fb974a8c062bfe196d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755354"
---
# <span data-ttu-id="0b20b-101">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0b20b-101">Remove-AzureBatchTask</span></span>

## <span data-ttu-id="0b20b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b20b-102">SYNOPSIS</span></span>
<span data-ttu-id="0b20b-103">Tar bort en batchuppgiften.</span><span class="sxs-lookup"><span data-stu-id="0b20b-103">Deletes a Batch task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b20b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b20b-104">SYNTAX</span></span>

### <span data-ttu-id="0b20b-105">Et</span><span class="sxs-lookup"><span data-stu-id="0b20b-105">Id</span></span>
```
Remove-AzureBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b20b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0b20b-106">InputObject</span></span>
```
Remove-AzureBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b20b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b20b-107">DESCRIPTION</span></span>
<span data-ttu-id="0b20b-108">Cmdleten **Remove-AzureBatchTask** tar bort en Azure Batch-uppgift.</span><span class="sxs-lookup"><span data-stu-id="0b20b-108">The **Remove-AzureBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="0b20b-109">Denna cmdlet uppmanar dig att bekräfta om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="0b20b-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="0b20b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b20b-110">EXAMPLES</span></span>

### <span data-ttu-id="0b20b-111">Exempel 1: ta bort en batch-uppgift efter ID</span><span class="sxs-lookup"><span data-stu-id="0b20b-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzureBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="0b20b-112">Det här kommandot tar bort en aktivitet med ID-Task23 under jobbet som har ID-jobbet-000001.</span><span class="sxs-lookup"><span data-stu-id="0b20b-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="0b20b-113">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0b20b-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="0b20b-114">Använd cmdleten **Get-AzureRmBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="0b20b-114">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="0b20b-115">Exempel 2: ta bort en batchuppgiften med hjälp av försäljnings förloppet utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="0b20b-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzureBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="0b20b-116">Med det här kommandot får du den batch-uppgift som har det ID-Task26 i jobbet som har ID-jobbet 000001 genom att använda cmdleten **Get-AzureBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="0b20b-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzureBatchTask** cmdlet.</span></span>
<span data-ttu-id="0b20b-117">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="0b20b-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0b20b-118">Kommandot tar bort uppgiften.</span><span class="sxs-lookup"><span data-stu-id="0b20b-118">The command deletes that task.</span></span>
<span data-ttu-id="0b20b-119">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="0b20b-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0b20b-120">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0b20b-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0b20b-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b20b-121">PARAMETERS</span></span>

### <span data-ttu-id="0b20b-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b20b-122">-BatchContext</span></span>
<span data-ttu-id="0b20b-123">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0b20b-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b20b-124">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0b20b-124">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0b20b-125">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="0b20b-125">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0b20b-126">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="0b20b-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0b20b-127">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0b20b-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0b20b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b20b-128">-DefaultProfile</span></span>
<span data-ttu-id="0b20b-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b20b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b20b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="0b20b-130">-Force</span></span>
<span data-ttu-id="0b20b-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0b20b-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b20b-132">-ID</span><span class="sxs-lookup"><span data-stu-id="0b20b-132">-Id</span></span>
<span data-ttu-id="0b20b-133">Anger ID för den aktivitet som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="0b20b-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="0b20b-134">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="0b20b-134">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b20b-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b20b-135">-InputObject</span></span>
<span data-ttu-id="0b20b-136">Anger den uppgift som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0b20b-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="0b20b-137">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="0b20b-137">To obtain a **PSCloudTask** object, use  the Get-AzureBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b20b-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="0b20b-138">-JobId</span></span>
<span data-ttu-id="0b20b-139">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="0b20b-139">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b20b-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b20b-140">-Confirm</span></span>
<span data-ttu-id="0b20b-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b20b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b20b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b20b-142">-WhatIf</span></span>
<span data-ttu-id="0b20b-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b20b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b20b-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b20b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b20b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b20b-145">CommonParameters</span></span>
<span data-ttu-id="0b20b-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b20b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b20b-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b20b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b20b-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b20b-148">INPUTS</span></span>

### <span data-ttu-id="0b20b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0b20b-149">System.String</span></span>

### <span data-ttu-id="0b20b-150">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="0b20b-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="0b20b-151">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b20b-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0b20b-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b20b-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="0b20b-153">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0b20b-153">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="0b20b-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b20b-154">OUTPUTS</span></span>

### <span data-ttu-id="0b20b-155">System. Void</span><span class="sxs-lookup"><span data-stu-id="0b20b-155">System.Void</span></span>

## <span data-ttu-id="0b20b-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b20b-156">NOTES</span></span>

## <span data-ttu-id="0b20b-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b20b-157">RELATED LINKS</span></span>

[<span data-ttu-id="0b20b-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0b20b-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0b20b-159">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0b20b-159">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="0b20b-160">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0b20b-160">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="0b20b-161">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0b20b-161">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="0b20b-162">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="0b20b-162">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="0b20b-163">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0b20b-163">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


