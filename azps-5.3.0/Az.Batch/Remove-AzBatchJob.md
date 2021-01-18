---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CB2F472B-C792-4A11-A055-F4161DCFBB28
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchJob.md
ms.openlocfilehash: 1b55aae98db72f7c4d4fe262329889182a189c80
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524733"
---
# <span data-ttu-id="87a32-101">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87a32-101">Remove-AzBatchJob</span></span>

## <span data-ttu-id="87a32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87a32-102">SYNOPSIS</span></span>
<span data-ttu-id="87a32-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="87a32-103">Deletes a Batch job.</span></span>

## <span data-ttu-id="87a32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87a32-104">SYNTAX</span></span>

```
Remove-AzBatchJob [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87a32-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87a32-105">DESCRIPTION</span></span>
<span data-ttu-id="87a32-106">Cmdleten **Remove-AzBatchJob** tar bort ett Azure-batchjobb.</span><span class="sxs-lookup"><span data-stu-id="87a32-106">The **Remove-AzBatchJob** cmdlet deletes an Azure Batch job.</span></span>
<span data-ttu-id="87a32-107">Denna cmdlet ber dig bekräfta att du vill ta bort ett jobb, såvida du inte anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="87a32-107">This cmdlet prompts you for confirmation before it removes a job, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="87a32-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87a32-108">EXAMPLES</span></span>

### <span data-ttu-id="87a32-109">Exempel 1: ta bort ett batchjobb</span><span class="sxs-lookup"><span data-stu-id="87a32-109">Example 1: Delete a Batch job</span></span>
```
PS C:\>Remove-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="87a32-110">Det här kommandot tar bort jobbet med ID-000001.</span><span class="sxs-lookup"><span data-stu-id="87a32-110">This command deletes the job that has the ID Job-000001.</span></span>
<span data-ttu-id="87a32-111">Med kommandot uppmanas du att bekräfta innan jobbet tas bort.</span><span class="sxs-lookup"><span data-stu-id="87a32-111">The command prompts you for confirmation before it deletes the job.</span></span>
<span data-ttu-id="87a32-112">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="87a32-112">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="87a32-113">Exempel 2: ta bort ett batchjobb utan bekräftelse genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="87a32-113">Example 2: Delete a Batch job without confirmation by using the pipeline</span></span>
```
PS C:\>Get-AzBatchJob -Id "Job-000002" -BatchContext $Context | Remove-AzBatchJob -Force -BatchContext $Context
```

<span data-ttu-id="87a32-114">Det här kommandot får jobbet som har ID-000002 med hjälp av Get-AzBatchJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87a32-114">This command gets the job that has the ID Job-000002 by using the Get-AzBatchJob cmdlet.</span></span>
<span data-ttu-id="87a32-115">Kommandot skickar jobbet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="87a32-115">The command passes that job to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87a32-116">Kommandot tar bort jobbet.</span><span class="sxs-lookup"><span data-stu-id="87a32-116">The command deletes that job.</span></span>
<span data-ttu-id="87a32-117">Eftersom kommandot @ innehåller parametern *Force* uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="87a32-117">Because the command includes the *Force* parameter, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="87a32-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87a32-118">PARAMETERS</span></span>

### <span data-ttu-id="87a32-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="87a32-119">-BatchContext</span></span>
<span data-ttu-id="87a32-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="87a32-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="87a32-121">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="87a32-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="87a32-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="87a32-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="87a32-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="87a32-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="87a32-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="87a32-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="87a32-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a32-125">-DefaultProfile</span></span>
<span data-ttu-id="87a32-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="87a32-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87a32-127">-Force</span><span class="sxs-lookup"><span data-stu-id="87a32-127">-Force</span></span>
<span data-ttu-id="87a32-128">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="87a32-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87a32-129">-ID</span><span class="sxs-lookup"><span data-stu-id="87a32-129">-Id</span></span>
<span data-ttu-id="87a32-130">Anger ID för det jobb som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="87a32-130">Specifies the ID of the job that this cmdlet deletes.</span></span>
<span data-ttu-id="87a32-131">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="87a32-131">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="87a32-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="87a32-132">-Confirm</span></span>
<span data-ttu-id="87a32-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="87a32-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a32-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a32-134">-WhatIf</span></span>
<span data-ttu-id="87a32-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="87a32-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a32-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="87a32-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a32-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a32-137">CommonParameters</span></span>
<span data-ttu-id="87a32-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87a32-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a32-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87a32-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a32-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87a32-140">INPUTS</span></span>

### <span data-ttu-id="87a32-141">System. String</span><span class="sxs-lookup"><span data-stu-id="87a32-141">System.String</span></span>

### <span data-ttu-id="87a32-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="87a32-142">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="87a32-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87a32-143">OUTPUTS</span></span>

### <span data-ttu-id="87a32-144">System. Void</span><span class="sxs-lookup"><span data-stu-id="87a32-144">System.Void</span></span>

## <span data-ttu-id="87a32-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87a32-145">NOTES</span></span>

## <span data-ttu-id="87a32-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87a32-146">RELATED LINKS</span></span>

[<span data-ttu-id="87a32-147">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87a32-147">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="87a32-148">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87a32-148">Enable-AzBatchJob</span></span>](./Enable-AzBatchJob.md)

[<span data-ttu-id="87a32-149">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87a32-149">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="87a32-150">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="87a32-150">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="87a32-151">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87a32-151">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="87a32-152">Stopp-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="87a32-152">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="87a32-153">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="87a32-153">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
