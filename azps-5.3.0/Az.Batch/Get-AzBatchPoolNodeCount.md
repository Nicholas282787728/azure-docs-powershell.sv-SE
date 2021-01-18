---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchpoolnodecount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchPoolNodeCount.md
ms.openlocfilehash: b3b1adfe9549a7b04a1e7c6d57542cef8a40cfd7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524784"
---
# <span data-ttu-id="0fd3c-101">Get-AzBatchPoolNodeCount</span><span class="sxs-lookup"><span data-stu-id="0fd3c-101">Get-AzBatchPoolNodeCount</span></span>

## <span data-ttu-id="0fd3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fd3c-102">SYNOPSIS</span></span>
<span data-ttu-id="0fd3c-103">Hämtar antalet batchattribut per nod, grupperat efter pool-ID.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-103">Gets Batch node counts per node state grouped by pool id.</span></span>

## <span data-ttu-id="0fd3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fd3c-104">SYNTAX</span></span>

### <span data-ttu-id="0fd3c-105">AzureBatchPoolNodeCounts (standard)</span><span class="sxs-lookup"><span data-stu-id="0fd3c-105">AzureBatchPoolNodeCounts (Default)</span></span>
```
Get-AzBatchPoolNodeCount -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0fd3c-106">PoolId</span><span class="sxs-lookup"><span data-stu-id="0fd3c-106">PoolId</span></span>
```
Get-AzBatchPoolNodeCount [-PoolId <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fd3c-107">ParentObject</span><span class="sxs-lookup"><span data-stu-id="0fd3c-107">ParentObject</span></span>
```
Get-AzBatchPoolNodeCount [-Pool <PSCloudPool>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fd3c-108">ODataFilter</span><span class="sxs-lookup"><span data-stu-id="0fd3c-108">ODataFilter</span></span>
```
Get-AzBatchPoolNodeCount [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fd3c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fd3c-109">DESCRIPTION</span></span>
<span data-ttu-id="0fd3c-110">Med cmdleten Get-AzBatchPoolNodeCount kan kunderna få tillbaka antalet noder per nod, grupperade efter pool.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-110">The Get-AzBatchPoolNodeCount cmdlet allows customers to get back node counts per node state grouped by pool.</span></span> <span data-ttu-id="0fd3c-111">Möjliga nodtyper är att skapa, vilande, leavingPool, offline, blockera, starta om, återanvända, köra, starta, startTaskFailed, okända, oanvändbara och waitingForStartTask.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-111">Possible node states are creating, idle, leavingPool, offline, preempted, rebooting, reimaging, running, starting, startTaskFailed, unknown, unusable and waitingForStartTask.</span></span> <span data-ttu-id="0fd3c-112">Cmdleten tar PoolId eller en adresspool för att endast filtrera poolen med pool-ID.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-112">The cmdlet takes PoolId or Pool parameter to filter only pool with pool id specified.</span></span> 

## <span data-ttu-id="0fd3c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fd3c-113">EXAMPLES</span></span>

### <span data-ttu-id="0fd3c-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0fd3c-114">Example 1</span></span>
```
PS C:\> $batchContext = Get-AzBatchAccountKey -AccountName "contosobatch"
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
contosopool2                   Idle: 1, Rebooting: 1, Total: 2                              Total: 0
```

<span data-ttu-id="0fd3c-115">Visa nod per nod-ID för pooler under den aktuella kommando kontexten.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-115">List node counts per node state for pools under current batch account context.</span></span>

### <span data-ttu-id="0fd3c-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0fd3c-116">Example 2</span></span>

```powershell
PS C:\> Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0

PS C:\> $poolnodecounts = Get-AzBatchPoolNodeCount -BatchContext $batchContext -PoolId "contosopool1"
PS C:\> $poolnodecounts.Dedicated

Creating            : 1
Idle                : 1
LeavingPool         : 0
Offline             : 0
Preempted           : 0
Rebooting           : 1
Reimaging           : 0
Running             : 5
Starting            : 0
StartTaskFailed     : 0
Total               : 8
Unknown             : 0
Unusable            : 0
WaitingForStartTask : 0

PS C:\> Get-AzBatchPool -Id "contosopool1" -BatchContext $batchContext | Get-AzBatchPoolNodeCount -BatchContext $batchContext

PoolId                         Dedicated                                                    LowPriority
------                         ---------                                                    -----------
contosopool1                   Creating: 1, Idle: 1, Rebooting: 1, Running: 5, Total: 8     Total: 0
```

<span data-ttu-id="0fd3c-117">Visa antalet noder per nod för en pool med pool-ID.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-117">Show node counts per node state for a pool given pool id.</span></span>

## <span data-ttu-id="0fd3c-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fd3c-118">PARAMETERS</span></span>

### <span data-ttu-id="0fd3c-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0fd3c-119">-BatchContext</span></span>
<span data-ttu-id="0fd3c-120">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-120">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="0fd3c-121">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="0fd3c-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="0fd3c-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-123">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="0fd3c-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0fd3c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fd3c-125">-DefaultProfile</span></span>
<span data-ttu-id="0fd3c-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fd3c-127">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="0fd3c-127">-MaxCount</span></span>
<span data-ttu-id="0fd3c-128">Anger det maximala antalet pooler som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-128">Specifies the maximum number of pools to return.</span></span>
<span data-ttu-id="0fd3c-129">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-129">The default value is 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3c-130">-Pool</span><span class="sxs-lookup"><span data-stu-id="0fd3c-130">-Pool</span></span>
<span data-ttu-id="0fd3c-131">Anger den **PSCloudPool** som du vill få antalet noder för.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-131">Specifies the **PSCloudPool** for which to get node counts.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: ParentObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3c-132">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0fd3c-132">-PoolId</span></span>
<span data-ttu-id="0fd3c-133">ID för den pool som antalet noder ska få värdet för.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-133">The id of the pool for which to get node counts.</span></span>

```yaml
Type: System.String
Parameter Sets: PoolId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fd3c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fd3c-134">CommonParameters</span></span>
<span data-ttu-id="0fd3c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fd3c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fd3c-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fd3c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fd3c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fd3c-137">INPUTS</span></span>

### <span data-ttu-id="0fd3c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0fd3c-138">System.String</span></span>

### <span data-ttu-id="0fd3c-139">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="0fd3c-139">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="0fd3c-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0fd3c-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0fd3c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fd3c-141">OUTPUTS</span></span>

### <span data-ttu-id="0fd3c-142">Microsoft.Azure.Commands.BatCH. Modeller. PSPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="0fd3c-142">Microsoft.Azure.Commands.Batch.Models.PSPoolNodeCounts</span></span>

## <span data-ttu-id="0fd3c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fd3c-143">NOTES</span></span>

## <span data-ttu-id="0fd3c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fd3c-144">RELATED LINKS</span></span>

[<span data-ttu-id="0fd3c-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="0fd3c-145">Get-AzBatchAccountKey</span></span>]()

[<span data-ttu-id="0fd3c-146">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="0fd3c-146">Get-AzBatchJob</span></span>]()

[<span data-ttu-id="0fd3c-147">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0fd3c-147">Azure Batch Cmdlets</span></span>]()

