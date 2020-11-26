---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNode.md
ms.openlocfilehash: 516d6baacbacb7cab7db590558074024396649a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103066"
---
# <span data-ttu-id="30185-101">Remove-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="30185-101">Remove-AzBatchComputeNode</span></span>

## <span data-ttu-id="30185-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30185-102">SYNOPSIS</span></span>
<span data-ttu-id="30185-103">Tar bort datornoder från en pool.</span><span class="sxs-lookup"><span data-stu-id="30185-103">Removes compute nodes from a pool.</span></span>

## <span data-ttu-id="30185-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30185-104">SYNTAX</span></span>

### <span data-ttu-id="30185-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="30185-105">Id (Default)</span></span>
```
Remove-AzBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30185-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="30185-106">InputObject</span></span>
```
Remove-AzBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30185-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30185-107">DESCRIPTION</span></span>
<span data-ttu-id="30185-108">Cmdleten **Remove-AzBatchComputeNode** tar bort Azure Batch-datornoder från en pool.</span><span class="sxs-lookup"><span data-stu-id="30185-108">The **Remove-AzBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="30185-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30185-109">EXAMPLES</span></span>

### <span data-ttu-id="30185-110">Exempel 1: ta bort en datornod</span><span class="sxs-lookup"><span data-stu-id="30185-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="30185-111">Det här kommandot tar bort Compute-noden med angivet ID från poolen med ID-Pool07.</span><span class="sxs-lookup"><span data-stu-id="30185-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="30185-112">Kommandot anger alternativet avsluta avallokering.</span><span class="sxs-lookup"><span data-stu-id="30185-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="30185-113">Tids gränsen för storleks ändring är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="30185-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="30185-114">Exempel 2: ta bort en datornod med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="30185-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="30185-115">Det här kommandot får Compute-noden som har angivet ID från poolen med ID-Pool07 med hjälp av Get-AzBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30185-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="30185-116">Kommandot skickar noden till den aktuella cmdleten med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="30185-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="30185-117">Den aktuella cmdleten tar bort Compute-noden.</span><span class="sxs-lookup"><span data-stu-id="30185-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="30185-118">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="30185-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="30185-119">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="30185-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="30185-120">Exempel 3: ta bort flera noder</span><span class="sxs-lookup"><span data-stu-id="30185-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="30185-121">Det här kommandot tar bort två datornoder från poolen med ID-Pool07.</span><span class="sxs-lookup"><span data-stu-id="30185-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="30185-122">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="30185-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="30185-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30185-123">PARAMETERS</span></span>

### <span data-ttu-id="30185-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="30185-124">-BatchContext</span></span>
<span data-ttu-id="30185-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="30185-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="30185-126">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="30185-126">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="30185-127">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="30185-127">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="30185-128">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="30185-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="30185-129">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="30185-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="30185-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="30185-130">-ComputeNode</span></span>
<span data-ttu-id="30185-131">Anger det **PSComputeNode** -objekt som representerar den datornod som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="30185-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30185-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="30185-132">-DeallocationOption</span></span>
<span data-ttu-id="30185-133">Anger ett alternativ för debeläggning för borttagnings åtgärden som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="30185-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="30185-134">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="30185-134">The default value is Requeue.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Batch.Common.ComputeNodeDeallocationOption]
Parameter Sets: (All)
Aliases:
Accepted values: Requeue, Terminate, TaskCompletion, RetainedData

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30185-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30185-135">-DefaultProfile</span></span>
<span data-ttu-id="30185-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30185-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30185-137">-Force</span><span class="sxs-lookup"><span data-stu-id="30185-137">-Force</span></span>
<span data-ttu-id="30185-138">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="30185-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30185-139">-ID</span><span class="sxs-lookup"><span data-stu-id="30185-139">-Ids</span></span>
<span data-ttu-id="30185-140">Anger en matris med ID-nummer för datornoder som den här cmdleten tar bort från poolen.</span><span class="sxs-lookup"><span data-stu-id="30185-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Id
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30185-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="30185-141">-PoolId</span></span>
<span data-ttu-id="30185-142">Anger ID för poolen som innehåller de datornoder som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="30185-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30185-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="30185-143">-ResizeTimeout</span></span>
<span data-ttu-id="30185-144">Anger tids gräns intervallet för borttagning av datornoderna från poolen.</span><span class="sxs-lookup"><span data-stu-id="30185-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="30185-145">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="30185-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="30185-146">Minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="30185-146">The minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30185-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="30185-147">-Confirm</span></span>
<span data-ttu-id="30185-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="30185-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30185-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30185-149">-WhatIf</span></span>
<span data-ttu-id="30185-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="30185-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30185-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="30185-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30185-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30185-152">CommonParameters</span></span>
<span data-ttu-id="30185-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30185-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30185-154">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30185-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30185-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30185-155">INPUTS</span></span>

### <span data-ttu-id="30185-156">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="30185-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="30185-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="30185-157">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="30185-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30185-158">OUTPUTS</span></span>

### <span data-ttu-id="30185-159">System. Void</span><span class="sxs-lookup"><span data-stu-id="30185-159">System.Void</span></span>

## <span data-ttu-id="30185-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30185-160">NOTES</span></span>

## <span data-ttu-id="30185-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30185-161">RELATED LINKS</span></span>

[<span data-ttu-id="30185-162">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="30185-162">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="30185-163">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="30185-163">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="30185-164">Restart-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="30185-164">Restart-AzBatchComputeNode</span></span>](./Restart-AzBatchComputeNode.md)

