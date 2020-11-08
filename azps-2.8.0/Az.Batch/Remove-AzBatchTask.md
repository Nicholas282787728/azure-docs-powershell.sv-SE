---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D79AEF8C-F0DC-40F8-9EEE-A2BB6AE5C4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchTask.md
ms.openlocfilehash: c2b198359bbd793353c9b416a631d94cad0709fa
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928434"
---
# <span data-ttu-id="f7907-101">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f7907-101">Remove-AzBatchTask</span></span>

## <span data-ttu-id="f7907-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f7907-102">SYNOPSIS</span></span>
<span data-ttu-id="f7907-103">Tar bort en batchuppgiften.</span><span class="sxs-lookup"><span data-stu-id="f7907-103">Deletes a Batch task.</span></span>

## <span data-ttu-id="f7907-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f7907-104">SYNTAX</span></span>

### <span data-ttu-id="f7907-105">Et</span><span class="sxs-lookup"><span data-stu-id="f7907-105">Id</span></span>
```
Remove-AzBatchTask [-JobId] <String> [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7907-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f7907-106">InputObject</span></span>
```
Remove-AzBatchTask [-InputObject] <PSCloudTask> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7907-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f7907-107">DESCRIPTION</span></span>
<span data-ttu-id="f7907-108">Cmdleten **Remove-AzBatchTask** tar bort en Azure Batch-uppgift.</span><span class="sxs-lookup"><span data-stu-id="f7907-108">The **Remove-AzBatchTask** cmdlet deletes an Azure Batch task.</span></span>
<span data-ttu-id="f7907-109">Denna cmdlet uppmanar dig att bekräfta om du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="f7907-109">This cmdlet prompts you for confirmation, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="f7907-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f7907-110">EXAMPLES</span></span>

### <span data-ttu-id="f7907-111">Exempel 1: ta bort en batch-uppgift efter ID</span><span class="sxs-lookup"><span data-stu-id="f7907-111">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Remove-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="f7907-112">Det här kommandot tar bort en aktivitet med ID-Task23 under jobbet som har ID-jobbet-000001.</span><span class="sxs-lookup"><span data-stu-id="f7907-112">This command deletes a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f7907-113">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f7907-113">The command prompts you for confirmation.</span></span>
<span data-ttu-id="f7907-114">Använd cmdleten **Get-AzBatchAccountKeys** för att tilldela en kontext till variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="f7907-114">Use the **Get-AzBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="f7907-115">Exempel 2: ta bort en batchuppgiften med hjälp av försäljnings förloppet utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="f7907-115">Example 2: Delete a Batch task by using the pipeline without confirmation</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Remove-AzBatchTask -Force -BatchContext $Context
```

<span data-ttu-id="f7907-116">Med det här kommandot får du den batch-uppgift som har det ID-Task26 i jobbet som har ID-jobbet 000001 genom att använda cmdleten **Get-AzBatchTask** .</span><span class="sxs-lookup"><span data-stu-id="f7907-116">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the **Get-AzBatchTask** cmdlet.</span></span>
<span data-ttu-id="f7907-117">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f7907-117">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f7907-118">Kommandot tar bort uppgiften.</span><span class="sxs-lookup"><span data-stu-id="f7907-118">The command deletes that task.</span></span>
<span data-ttu-id="f7907-119">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="f7907-119">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f7907-120">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f7907-120">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f7907-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f7907-121">PARAMETERS</span></span>

### <span data-ttu-id="f7907-122">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f7907-122">-BatchContext</span></span>
<span data-ttu-id="f7907-123">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f7907-123">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f7907-124">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f7907-124">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f7907-125">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="f7907-125">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f7907-126">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="f7907-126">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f7907-127">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f7907-127">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f7907-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7907-128">-DefaultProfile</span></span>
<span data-ttu-id="f7907-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f7907-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7907-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f7907-130">-Force</span></span>
<span data-ttu-id="f7907-131">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f7907-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7907-132">-ID</span><span class="sxs-lookup"><span data-stu-id="f7907-132">-Id</span></span>
<span data-ttu-id="f7907-133">Anger ID för den aktivitet som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="f7907-133">Specifies the ID of the task that this cmdlet deletes.</span></span>
<span data-ttu-id="f7907-134">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="f7907-134">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="f7907-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7907-135">-InputObject</span></span>
<span data-ttu-id="f7907-136">Anger den uppgift som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f7907-136">Specifies the task that this cmdlet deletes.</span></span>
<span data-ttu-id="f7907-137">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="f7907-137">To obtain a **PSCloudTask** object, use  the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="f7907-138">-JobId</span><span class="sxs-lookup"><span data-stu-id="f7907-138">-JobId</span></span>
<span data-ttu-id="f7907-139">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="f7907-139">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="f7907-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f7907-140">-Confirm</span></span>
<span data-ttu-id="f7907-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f7907-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7907-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7907-142">-WhatIf</span></span>
<span data-ttu-id="f7907-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f7907-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7907-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f7907-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7907-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7907-145">CommonParameters</span></span>
<span data-ttu-id="f7907-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7907-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7907-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7907-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7907-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f7907-148">INPUTS</span></span>

### <span data-ttu-id="f7907-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f7907-149">System.String</span></span>

### <span data-ttu-id="f7907-150">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="f7907-150">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="f7907-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f7907-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f7907-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f7907-152">OUTPUTS</span></span>

### <span data-ttu-id="f7907-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="f7907-153">System.Void</span></span>

## <span data-ttu-id="f7907-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f7907-154">NOTES</span></span>

## <span data-ttu-id="f7907-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f7907-155">RELATED LINKS</span></span>

[<span data-ttu-id="f7907-156">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f7907-156">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f7907-157">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f7907-157">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="f7907-158">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f7907-158">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="f7907-159">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f7907-159">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="f7907-160">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="f7907-160">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="f7907-161">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f7907-161">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

