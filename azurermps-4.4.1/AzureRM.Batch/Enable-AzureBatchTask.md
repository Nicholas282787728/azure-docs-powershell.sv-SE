---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchTask.md
ms.openlocfilehash: 8e7636d83b953997ac1f9269e45fbf3c2278612f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758133"
---
# <span data-ttu-id="b296e-101">Enable-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b296e-101">Enable-AzureBatchTask</span></span>

## <span data-ttu-id="b296e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b296e-102">SYNOPSIS</span></span>
<span data-ttu-id="b296e-103">Återaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="b296e-103">Reactivates a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b296e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b296e-104">SYNTAX</span></span>

### <span data-ttu-id="b296e-105">Et</span><span class="sxs-lookup"><span data-stu-id="b296e-105">Id</span></span>
```
Enable-AzureBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b296e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b296e-106">InputObject</span></span>
```
Enable-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b296e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b296e-107">DESCRIPTION</span></span>
<span data-ttu-id="b296e-108">Cmdleten **Enable-AzureBatchTask** reaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="b296e-108">The **Enable-AzureBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="b296e-109">Om en aktivitet har tömts på nytt, aktiverar denna cmdlet ändå att den körs.</span><span class="sxs-lookup"><span data-stu-id="b296e-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="b296e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b296e-110">EXAMPLES</span></span>

### <span data-ttu-id="b296e-111">Exempel 1: återaktivera en uppgift</span><span class="sxs-lookup"><span data-stu-id="b296e-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzureBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="b296e-112">Det här kommandot återaktiverar uppgiften Task2 i Job Job7.</span><span class="sxs-lookup"><span data-stu-id="b296e-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="b296e-113">Exempel 2: återaktivera en uppgift med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="b296e-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzureBatchTask -BatchContext $Context
```

<span data-ttu-id="b296e-114">Med det här kommandot får du den batch-uppgift som har det ID-Task3 i jobbet som har ID-Job8 med hjälp av Get-AzureBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b296e-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzureBatchTask cmdlet.</span></span>
<span data-ttu-id="b296e-115">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b296e-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b296e-116">Kommandot återaktiverar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="b296e-116">The command reactivates that task.</span></span>

## <span data-ttu-id="b296e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b296e-117">PARAMETERS</span></span>

### <span data-ttu-id="b296e-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b296e-118">-BatchContext</span></span>
<span data-ttu-id="b296e-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b296e-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b296e-120">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="b296e-120">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b296e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="b296e-121">-Id</span></span>
<span data-ttu-id="b296e-122">Anger ID för den aktivitet som ska återaktiveras.</span><span class="sxs-lookup"><span data-stu-id="b296e-122">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="b296e-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="b296e-123">-JobId</span></span>
<span data-ttu-id="b296e-124">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="b296e-124">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="b296e-125">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="b296e-125">-Task</span></span>
<span data-ttu-id="b296e-126">Anger den aktivitet som denna cmdlet reaktiverar.</span><span class="sxs-lookup"><span data-stu-id="b296e-126">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="b296e-127">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzureBatchTask.</span><span class="sxs-lookup"><span data-stu-id="b296e-127">To obtain a **PSCloudTask** object, use the Get-AzureBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="b296e-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b296e-128">-Confirm</span></span>
<span data-ttu-id="b296e-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b296e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b296e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b296e-130">-WhatIf</span></span>
<span data-ttu-id="b296e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b296e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b296e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b296e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b296e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b296e-133">-DefaultProfile</span></span>
<span data-ttu-id="b296e-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b296e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b296e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b296e-135">CommonParameters</span></span>
<span data-ttu-id="b296e-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b296e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b296e-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b296e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b296e-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b296e-138">INPUTS</span></span>

### <span data-ttu-id="b296e-139">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b296e-139">BatchAccountContext</span></span>
<span data-ttu-id="b296e-140">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b296e-140">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b296e-141">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="b296e-141">PSCloudTask</span></span>
<span data-ttu-id="b296e-142">Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b296e-142">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="b296e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b296e-143">OUTPUTS</span></span>

## <span data-ttu-id="b296e-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b296e-144">NOTES</span></span>

## <span data-ttu-id="b296e-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b296e-145">RELATED LINKS</span></span>

[<span data-ttu-id="b296e-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b296e-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b296e-147">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b296e-147">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="b296e-148">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b296e-148">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="b296e-149">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b296e-149">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="b296e-150">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b296e-150">Set-AzureBatchTask</span></span>](./Set-AzureBatchTask.md)

[<span data-ttu-id="b296e-151">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="b296e-151">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)


