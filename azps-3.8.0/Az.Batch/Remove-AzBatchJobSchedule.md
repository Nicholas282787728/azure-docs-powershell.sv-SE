---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJobSchedule.md
ms.openlocfilehash: 247b2494e002ae6340f38aa626b9661dbf7722ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090156"
---
# <span data-ttu-id="3c7d2-101">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-101">Remove-AzBatchJobSchedule</span></span>

## <span data-ttu-id="3c7d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7d2-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-103">Removes a Batch job schedule.</span></span>

## <span data-ttu-id="3c7d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c7d2-104">SYNTAX</span></span>

```
Remove-AzBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c7d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c7d2-105">DESCRIPTION</span></span>
<span data-ttu-id="3c7d2-106">Cmdleten **Remove-AzBatchJobSchedule** tar bort ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-106">The **Remove-AzBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="3c7d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c7d2-107">EXAMPLES</span></span>

### <span data-ttu-id="3c7d2-108">Exempel 1: ta bort ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="3c7d2-108">Example 1: Delete a Batch job schedule</span></span>
```
PS C:\>Remove-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
```

<span data-ttu-id="3c7d2-109">Det här kommandot tar bort projektschemat med ID-MyJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-109">This command deletes the job schedule that has the ID MyJobSchedule.</span></span>
<span data-ttu-id="3c7d2-110">Med kommandot uppmanas du att bekräfta innan jobbet tas bort.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-110">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="3c7d2-111">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-111">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="3c7d2-112">Exempel 2: ta bort ett batchjobb utan bekräftelse genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="3c7d2-112">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context | Remove-AzBatchJobSchedule -Force -BatchContext $Context
```

<span data-ttu-id="3c7d2-113">Det här kommandot får jobbet schema med ID-MyJobSchedule med hjälp av Get-AzBatchJobSchedule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-113">This command gets the job schedule that has the ID MyJobSchedule by using the Get-AzBatchJobSchedule cmdlet.</span></span>
<span data-ttu-id="3c7d2-114">Kommandot skickar schemat till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-114">The command passes that job schedule to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3c7d2-115">Kommandot tar bort projektschemat.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-115">The command deletes that job schedule.</span></span>
<span data-ttu-id="3c7d2-116">Eftersom kommandot @ innehåller parametern *Force* uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-116">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="3c7d2-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c7d2-117">PARAMETERS</span></span>

### <span data-ttu-id="3c7d2-118">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3c7d2-118">-BatchContext</span></span>
<span data-ttu-id="3c7d2-119">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-119">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3c7d2-120">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-120">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3c7d2-121">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-121">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3c7d2-122">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-122">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3c7d2-123">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-123">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3c7d2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7d2-124">-DefaultProfile</span></span>
<span data-ttu-id="3c7d2-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c7d2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3c7d2-126">-Force</span></span>
<span data-ttu-id="3c7d2-127">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c7d2-128">-ID</span><span class="sxs-lookup"><span data-stu-id="3c7d2-128">-Id</span></span>
<span data-ttu-id="3c7d2-129">Anger ID för den fin planering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-129">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="3c7d2-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3c7d2-130">-Confirm</span></span>
<span data-ttu-id="3c7d2-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c7d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c7d2-132">-WhatIf</span></span>
<span data-ttu-id="3c7d2-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c7d2-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c7d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7d2-135">CommonParameters</span></span>
<span data-ttu-id="3c7d2-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c7d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7d2-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c7d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7d2-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c7d2-138">INPUTS</span></span>

### <span data-ttu-id="3c7d2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3c7d2-139">System.String</span></span>

### <span data-ttu-id="3c7d2-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3c7d2-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3c7d2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c7d2-141">OUTPUTS</span></span>

### <span data-ttu-id="3c7d2-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="3c7d2-142">System.Void</span></span>

## <span data-ttu-id="3c7d2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c7d2-143">NOTES</span></span>

## <span data-ttu-id="3c7d2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c7d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="3c7d2-145">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-145">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="3c7d2-146">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-146">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="3c7d2-147">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-147">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="3c7d2-148">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-148">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="3c7d2-149">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-149">Set-AzBatchJobSchedule</span></span>](./Set-AzBatchJobSchedule.md)

[<span data-ttu-id="3c7d2-150">Stopp-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3c7d2-150">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


