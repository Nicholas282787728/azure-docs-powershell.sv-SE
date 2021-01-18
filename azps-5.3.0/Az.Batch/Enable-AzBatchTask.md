---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 9979a0fa16b8cfbe59eb8412a76cbbebcb2fca4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524815"
---
# <span data-ttu-id="4d1a9-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="4d1a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="4d1a9-103">Återaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-103">Reactivates a task.</span></span>

## <span data-ttu-id="4d1a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d1a9-104">SYNTAX</span></span>

### <span data-ttu-id="4d1a9-105">Et</span><span class="sxs-lookup"><span data-stu-id="4d1a9-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d1a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4d1a9-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d1a9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d1a9-107">DESCRIPTION</span></span>
<span data-ttu-id="4d1a9-108">Cmdleten **Enable-AzBatchTask** reaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="4d1a9-109">Om en aktivitet har tömts på nytt, aktiverar denna cmdlet ändå att den körs.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="4d1a9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d1a9-110">EXAMPLES</span></span>

### <span data-ttu-id="4d1a9-111">Exempel 1: återaktivera en uppgift</span><span class="sxs-lookup"><span data-stu-id="4d1a9-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="4d1a9-112">Det här kommandot återaktiverar uppgiften Task2 i Job Job7.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="4d1a9-113">Exempel 2: återaktivera en uppgift med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="4d1a9-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="4d1a9-114">Med det här kommandot får du den batch-uppgift som har det ID-Task3 i jobbet som har ID-Job8 med hjälp av Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="4d1a9-115">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4d1a9-116">Kommandot återaktiverar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-116">The command reactivates that task.</span></span>

## <span data-ttu-id="4d1a9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d1a9-117">PARAMETERS</span></span>

### <span data-ttu-id="4d1a9-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4d1a9-118">-BatchContext</span></span>
<span data-ttu-id="4d1a9-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4d1a9-120">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4d1a9-121">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4d1a9-122">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4d1a9-123">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="4d1a9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d1a9-124">-DefaultProfile</span></span>
<span data-ttu-id="4d1a9-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d1a9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4d1a9-126">-Id</span></span>
<span data-ttu-id="4d1a9-127">Anger ID för den aktivitet som ska återaktiveras.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="4d1a9-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="4d1a9-128">-JobId</span></span>
<span data-ttu-id="4d1a9-129">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="4d1a9-130">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="4d1a9-130">-Task</span></span>
<span data-ttu-id="4d1a9-131">Anger den aktivitet som denna cmdlet reaktiverar.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="4d1a9-132">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="4d1a9-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d1a9-133">-Confirm</span></span>
<span data-ttu-id="4d1a9-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d1a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d1a9-135">-WhatIf</span></span>
<span data-ttu-id="4d1a9-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d1a9-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d1a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d1a9-138">CommonParameters</span></span>
<span data-ttu-id="4d1a9-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d1a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d1a9-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d1a9-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d1a9-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d1a9-141">INPUTS</span></span>

### <span data-ttu-id="4d1a9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4d1a9-142">System.String</span></span>

### <span data-ttu-id="4d1a9-143">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="4d1a9-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4d1a9-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="4d1a9-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d1a9-145">OUTPUTS</span></span>

### <span data-ttu-id="4d1a9-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="4d1a9-146">System.Void</span></span>

## <span data-ttu-id="4d1a9-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d1a9-147">NOTES</span></span>

## <span data-ttu-id="4d1a9-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d1a9-148">RELATED LINKS</span></span>

[<span data-ttu-id="4d1a9-149">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="4d1a9-149">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="4d1a9-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="4d1a9-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="4d1a9-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="4d1a9-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="4d1a9-154">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="4d1a9-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


