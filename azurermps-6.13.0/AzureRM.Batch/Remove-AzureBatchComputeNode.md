---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 0BB79553-26DA-413C-8086-740DB6B31A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNode.md
ms.openlocfilehash: 39bbc9102d72c469730fe494869bffe5f726b41a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579000"
---
# <span data-ttu-id="a770d-101">Remove-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a770d-101">Remove-AzureBatchComputeNode</span></span>

## <span data-ttu-id="a770d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a770d-102">SYNOPSIS</span></span>
<span data-ttu-id="a770d-103">Tar bort datornoder från en pool.</span><span class="sxs-lookup"><span data-stu-id="a770d-103">Removes compute nodes from a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a770d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a770d-104">SYNTAX</span></span>

### <span data-ttu-id="a770d-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="a770d-105">Id (Default)</span></span>
```
Remove-AzureBatchComputeNode [-PoolId] <String> [-Ids] <String[]>
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a770d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a770d-106">InputObject</span></span>
```
Remove-AzureBatchComputeNode [[-ComputeNode] <PSComputeNode>]
 [-DeallocationOption <ComputeNodeDeallocationOption>] [-ResizeTimeout <TimeSpan>] [-Force]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a770d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a770d-107">DESCRIPTION</span></span>
<span data-ttu-id="a770d-108">Cmdleten **Remove-AzureBatchComputeNode** tar bort Azure Batch-datornoder från en pool.</span><span class="sxs-lookup"><span data-stu-id="a770d-108">The **Remove-AzureBatchComputeNode** cmdlet removes Azure Batch compute nodes from a pool.</span></span>

## <span data-ttu-id="a770d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a770d-109">EXAMPLES</span></span>

### <span data-ttu-id="a770d-110">Exempel 1: ta bort en datornod</span><span class="sxs-lookup"><span data-stu-id="a770d-110">Example 1: Remove a compute node</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" -Ids "tvm-2316545714_1-20150725t213220z" -DeallocationOption Terminate -ResizeTimeout ([TimeSpan]::FromMinutes(10)) -BatchContext $Context
```

<span data-ttu-id="a770d-111">Det här kommandot tar bort Compute-noden med angivet ID från poolen med ID-Pool07.</span><span class="sxs-lookup"><span data-stu-id="a770d-111">This command removes compute node that has the specified ID from pool that has the ID Pool07.</span></span>
<span data-ttu-id="a770d-112">Kommandot anger alternativet avsluta avallokering.</span><span class="sxs-lookup"><span data-stu-id="a770d-112">The command specifies the Terminate deallocation option.</span></span>
<span data-ttu-id="a770d-113">Tids gränsen för storleks ändring är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="a770d-113">The resize time-out is of 10 minutes.</span></span>

### <span data-ttu-id="a770d-114">Exempel 2: ta bort en datornod med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="a770d-114">Example 2: Remove a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool07" -Id "tvm-2316545714_1-20150725t213220z" -BatchContext $Context | Remove-AzureBatchComputeNode -Force -BatchContext $Context
```

<span data-ttu-id="a770d-115">Det här kommandot får Compute-noden som har angivet ID från poolen med ID-Pool07 med hjälp av Get-AzureBatchComputeNode cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a770d-115">This command gets the compute node that has the specified ID from pool that has the ID Pool07 by using the Get-AzureBatchComputeNode cmdlet.</span></span>
<span data-ttu-id="a770d-116">Kommandot skickar noden till den aktuella cmdleten med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="a770d-116">The command passes that node to the current cmdlet by using the pipeline.</span></span>
<span data-ttu-id="a770d-117">Den aktuella cmdleten tar bort Compute-noden.</span><span class="sxs-lookup"><span data-stu-id="a770d-117">The current cmdlet removes the compute node.</span></span>
<span data-ttu-id="a770d-118">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="a770d-118">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a770d-119">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a770d-119">Therefore, the command does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a770d-120">Exempel 3: ta bort flera noder</span><span class="sxs-lookup"><span data-stu-id="a770d-120">Example 3: Remove multiple nodes</span></span>
```
PS C:\>Remove-AzureBatchComputeNode -PoolId "Pool07" @("tvm-1783593343_28-20151117t214257z","tvm-1783593343_29-20151117t214257z") -Force -BatchContext $Context
```

<span data-ttu-id="a770d-121">Det här kommandot tar bort två datornoder från poolen med ID-Pool07.</span><span class="sxs-lookup"><span data-stu-id="a770d-121">This command removes two compute nodes from the pool that has the ID Pool07.</span></span>
<span data-ttu-id="a770d-122">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a770d-122">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a770d-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a770d-123">PARAMETERS</span></span>

### <span data-ttu-id="a770d-124">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a770d-124">-BatchContext</span></span>
<span data-ttu-id="a770d-125">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a770d-125">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a770d-126">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a770d-126">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a770d-127">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="a770d-127">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a770d-128">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="a770d-128">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a770d-129">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a770d-129">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a770d-130">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a770d-130">-ComputeNode</span></span>
<span data-ttu-id="a770d-131">Anger det **PSComputeNode** -objekt som representerar den datornod som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a770d-131">Specifies the **PSComputeNode** object that represents the compute node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a770d-132">-DeallocationOption</span><span class="sxs-lookup"><span data-stu-id="a770d-132">-DeallocationOption</span></span>
<span data-ttu-id="a770d-133">Anger ett alternativ för debeläggning för borttagnings åtgärden som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="a770d-133">Specifies a deallocation option for the removal operation that this cmdlet starts.</span></span>
<span data-ttu-id="a770d-134">Standardvärdet är köa.</span><span class="sxs-lookup"><span data-stu-id="a770d-134">The default value is Requeue.</span></span>

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

### <span data-ttu-id="a770d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a770d-135">-DefaultProfile</span></span>
<span data-ttu-id="a770d-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a770d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a770d-137">-Force</span><span class="sxs-lookup"><span data-stu-id="a770d-137">-Force</span></span>
<span data-ttu-id="a770d-138">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a770d-138">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a770d-139">-ID</span><span class="sxs-lookup"><span data-stu-id="a770d-139">-Ids</span></span>
<span data-ttu-id="a770d-140">Anger en matris med ID-nummer för datornoder som den här cmdleten tar bort från poolen.</span><span class="sxs-lookup"><span data-stu-id="a770d-140">Specifies an array of IDs of compute nodes that this cmdlet removes from the pool.</span></span>

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

### <span data-ttu-id="a770d-141">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a770d-141">-PoolId</span></span>
<span data-ttu-id="a770d-142">Anger ID för poolen som innehåller de datornoder som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a770d-142">Specifies the ID of the pool that contains the compute nodes that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a770d-143">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="a770d-143">-ResizeTimeout</span></span>
<span data-ttu-id="a770d-144">Anger tids gräns intervallet för borttagning av datornoderna från poolen.</span><span class="sxs-lookup"><span data-stu-id="a770d-144">Specifies the time-out interval for removal of the compute nodes from the pool.</span></span>
<span data-ttu-id="a770d-145">Standardvärdet är 10 minuter.</span><span class="sxs-lookup"><span data-stu-id="a770d-145">The default value is 10 minutes.</span></span>
<span data-ttu-id="a770d-146">Minimivärdet är 5 minuter.</span><span class="sxs-lookup"><span data-stu-id="a770d-146">The minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="a770d-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a770d-147">-Confirm</span></span>
<span data-ttu-id="a770d-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a770d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a770d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a770d-149">-WhatIf</span></span>
<span data-ttu-id="a770d-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a770d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a770d-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a770d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a770d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a770d-152">CommonParameters</span></span>
<span data-ttu-id="a770d-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a770d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a770d-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a770d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a770d-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a770d-155">INPUTS</span></span>

### <span data-ttu-id="a770d-156">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a770d-156">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="a770d-157">Parametrar: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a770d-157">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="a770d-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a770d-158">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="a770d-159">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a770d-159">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="a770d-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a770d-160">OUTPUTS</span></span>

### <span data-ttu-id="a770d-161">System. Void</span><span class="sxs-lookup"><span data-stu-id="a770d-161">System.Void</span></span>

## <span data-ttu-id="a770d-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a770d-162">NOTES</span></span>

## <span data-ttu-id="a770d-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a770d-163">RELATED LINKS</span></span>

[<span data-ttu-id="a770d-164">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a770d-164">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a770d-165">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a770d-165">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="a770d-166">Restart-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a770d-166">Restart-AzureBatchComputeNode</span></span>](./Restart-AzureBatchComputeNode.md)


