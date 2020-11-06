---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: fdcc1b7a119028d792000b10d26aa7900ab0477b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579020"
---
# <span data-ttu-id="678e9-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="678e9-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="678e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="678e9-102">SYNOPSIS</span></span>
<span data-ttu-id="678e9-103">Återaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="678e9-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="678e9-104">SYNTAX</span></span>

### <span data-ttu-id="678e9-105">Et</span><span class="sxs-lookup"><span data-stu-id="678e9-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="678e9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="678e9-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="678e9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="678e9-107">DESCRIPTION</span></span>
<span data-ttu-id="678e9-108">Cmdleten **Enable-AzureBatchTask** reaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="678e9-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="678e9-109">Om en aktivitet har tömts på nytt, aktiverar denna cmdlet ändå att den körs.</span><span class="sxs-lookup"><span data-stu-id="678e9-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="678e9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="678e9-110">EXAMPLES</span></span>

### <span data-ttu-id="678e9-111">Exempel 1: återaktivera en uppgift</span><span class="sxs-lookup"><span data-stu-id="678e9-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="678e9-112">Det här kommandot återaktiverar uppgiften Task2 i Job Job7.</span><span class="sxs-lookup"><span data-stu-id="678e9-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="678e9-113">Exempel 2: återaktivera en uppgift med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="678e9-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="678e9-114">Med det här kommandot får du den batch-uppgift som har det ID-Task3 i jobbet som har ID-Job8 med hjälp av Get-AzureBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="678e9-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="678e9-115">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="678e9-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="678e9-116">Kommandot återaktiverar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="678e9-116">The command reactivates that task.</span></span>

## <span data-ttu-id="678e9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="678e9-117">PARAMETERS</span></span>

### <span data-ttu-id="678e9-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="678e9-118">-BatchContext</span></span>
<span data-ttu-id="678e9-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="678e9-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="678e9-120">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="678e9-120">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="678e9-121">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="678e9-121">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="678e9-122">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="678e9-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="678e9-123">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="678e9-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="678e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678e9-124">-DefaultProfile</span></span>
<span data-ttu-id="678e9-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="678e9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="678e9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="678e9-126">-Id</span></span>
<span data-ttu-id="678e9-127">Anger ID för den aktivitet som ska återaktiveras.</span><span class="sxs-lookup"><span data-stu-id="678e9-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="678e9-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="678e9-128">-JobId</span></span>
<span data-ttu-id="678e9-129">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="678e9-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="678e9-130">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="678e9-130">-Task</span></span>
<span data-ttu-id="678e9-131">Anger den aktivitet som denna cmdlet reaktiverar.</span><span class="sxs-lookup"><span data-stu-id="678e9-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="678e9-132">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="678e9-132">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="678e9-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="678e9-133">-Confirm</span></span>
<span data-ttu-id="678e9-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="678e9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678e9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678e9-135">-WhatIf</span></span>
<span data-ttu-id="678e9-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="678e9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="678e9-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="678e9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="678e9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678e9-138">CommonParameters</span></span>
<span data-ttu-id="678e9-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678e9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678e9-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678e9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678e9-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="678e9-141">INPUTS</span></span>

### <span data-ttu-id="678e9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="678e9-142">System.String</span></span>

### <span data-ttu-id="678e9-143">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="678e9-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>
<span data-ttu-id="678e9-144">Parametrar: uppgift (ByValue)</span><span class="sxs-lookup"><span data-stu-id="678e9-144">Parameters: Task (ByValue)</span></span>

### <span data-ttu-id="678e9-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="678e9-145">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="678e9-146">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="678e9-146">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="678e9-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="678e9-147">OUTPUTS</span></span>

### <span data-ttu-id="678e9-148">System. Void</span><span class="sxs-lookup"><span data-stu-id="678e9-148">System.Void</span></span>

## <span data-ttu-id="678e9-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="678e9-149">NOTES</span></span>

## <span data-ttu-id="678e9-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="678e9-150">RELATED LINKS</span></span>

[<span data-ttu-id="678e9-151">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="678e9-151">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="678e9-152">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="678e9-152">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="678e9-153">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="678e9-153">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="678e9-154">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="678e9-154">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="678e9-155">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="678e9-155">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="678e9-156">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="678e9-156">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


