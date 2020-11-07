---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 67FB5D02-4F4B-4119-B3AC-0D205247253E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchTask.md
ms.openlocfilehash: 1eef03db73e6b1afcb2c9ca92f507e8b0f3ff0ae
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755130"
---
# <span data-ttu-id="5e6e0-101">Enable-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-101">Enable-AzBatchTask</span></span>

## <span data-ttu-id="5e6e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5e6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6e0-103">Återaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-103">Reactivates a task.</span></span>

## <span data-ttu-id="5e6e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5e6e0-104">SYNTAX</span></span>

### <span data-ttu-id="5e6e0-105">Et</span><span class="sxs-lookup"><span data-stu-id="5e6e0-105">Id</span></span>
```
Enable-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e6e0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5e6e0-106">InputObject</span></span>
```
Enable-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e6e0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5e6e0-107">DESCRIPTION</span></span>
<span data-ttu-id="5e6e0-108">Cmdleten **Enable-AzBatchTask** reaktiverar en uppgift.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-108">The **Enable-AzBatchTask** cmdlet reactivates a task.</span></span>
<span data-ttu-id="5e6e0-109">Om en aktivitet har tömts på nytt, aktiverar denna cmdlet ändå att den körs.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-109">If a task has exhausted its retry count, this cmdlet nevertheless enables it to run.</span></span>

## <span data-ttu-id="5e6e0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5e6e0-110">EXAMPLES</span></span>

### <span data-ttu-id="5e6e0-111">Exempel 1: återaktivera en uppgift</span><span class="sxs-lookup"><span data-stu-id="5e6e0-111">Example 1: Reactivate a task</span></span>
```
PS C:\>Enable-AzBatchTask -JobId "Job7" -Id "Task2" -BatchContext $Context
```

<span data-ttu-id="5e6e0-112">Det här kommandot återaktiverar uppgiften Task2 i Job Job7.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-112">This command reactivates the task Task2 in job Job7.</span></span>

### <span data-ttu-id="5e6e0-113">Exempel 2: återaktivera en uppgift med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="5e6e0-113">Example 2: Reactivate a task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job8" -Id "Task3" -BatchContext $Context | Enable-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="5e6e0-114">Med det här kommandot får du den batch-uppgift som har det ID-Task3 i jobbet som har ID-Job8 med hjälp av Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-114">This command gets the Batch task that has the ID Task3 in the job that has the ID Job8 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="5e6e0-115">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-115">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5e6e0-116">Kommandot återaktiverar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-116">The command reactivates that task.</span></span>

## <span data-ttu-id="5e6e0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5e6e0-117">PARAMETERS</span></span>

### <span data-ttu-id="5e6e0-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e6e0-118">-BatchContext</span></span>
<span data-ttu-id="5e6e0-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e6e0-120">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5e6e0-121">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-121">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5e6e0-122">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5e6e0-123">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5e6e0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6e0-124">-DefaultProfile</span></span>
<span data-ttu-id="5e6e0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e6e0-126">-ID</span><span class="sxs-lookup"><span data-stu-id="5e6e0-126">-Id</span></span>
<span data-ttu-id="5e6e0-127">Anger ID för den aktivitet som ska återaktiveras.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-127">Specifies the ID of the task to reactivate.</span></span>

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

### <span data-ttu-id="5e6e0-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="5e6e0-128">-JobId</span></span>
<span data-ttu-id="5e6e0-129">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-129">Specifies the ID of the job that contains the task.</span></span>

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

### <span data-ttu-id="5e6e0-130">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="5e6e0-130">-Task</span></span>
<span data-ttu-id="5e6e0-131">Anger den aktivitet som denna cmdlet reaktiverar.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-131">Specifies the task that this cmdlet reactivates.</span></span>
<span data-ttu-id="5e6e0-132">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-132">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

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

### <span data-ttu-id="5e6e0-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5e6e0-133">-Confirm</span></span>
<span data-ttu-id="5e6e0-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e6e0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e6e0-135">-WhatIf</span></span>
<span data-ttu-id="5e6e0-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e6e0-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e6e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6e0-138">CommonParameters</span></span>
<span data-ttu-id="5e6e0-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e6e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6e0-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e6e0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6e0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5e6e0-141">INPUTS</span></span>

### <span data-ttu-id="5e6e0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5e6e0-142">System.String</span></span>

### <span data-ttu-id="5e6e0-143">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-143">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="5e6e0-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e6e0-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5e6e0-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5e6e0-145">OUTPUTS</span></span>

### <span data-ttu-id="5e6e0-146">System. Void</span><span class="sxs-lookup"><span data-stu-id="5e6e0-146">System.Void</span></span>

## <span data-ttu-id="5e6e0-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5e6e0-147">NOTES</span></span>

## <span data-ttu-id="5e6e0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5e6e0-148">RELATED LINKS</span></span>

[<span data-ttu-id="5e6e0-149">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5e6e0-149">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5e6e0-150">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-150">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="5e6e0-151">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-151">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="5e6e0-152">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-152">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="5e6e0-153">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-153">Set-AzBatchTask</span></span>](./Set-AzBatchTask.md)

[<span data-ttu-id="5e6e0-154">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="5e6e0-154">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)


