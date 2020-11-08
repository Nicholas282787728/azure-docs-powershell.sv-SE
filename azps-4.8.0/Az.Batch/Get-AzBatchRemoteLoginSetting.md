---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260331"
---
# <span data-ttu-id="c1b9d-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="c1b9d-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="c1b9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b9d-103">Hämtar inställningar för fjärrinloggning för en datornod.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="c1b9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1b9d-104">SYNTAX</span></span>

### <span data-ttu-id="c1b9d-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="c1b9d-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1b9d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1b9d-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b9d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1b9d-107">DESCRIPTION</span></span>
<span data-ttu-id="c1b9d-108">Cmdleten **Get-AzBatchRemoteLoginSetting** hämtar inställningar för fjärrinloggning för en datornod i en infrastruktur baserad pool med virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="c1b9d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1b9d-109">EXAMPLES</span></span>

### <span data-ttu-id="c1b9d-110">Exempel 1: Hämta inställningar för fjärrinloggning för alla noder i en pool</span><span class="sxs-lookup"><span data-stu-id="c1b9d-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="c1b9d-111">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="c1b9d-112">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="c1b9d-113">Det andra kommandot får varje datornod i poolen med ID-ContosoPool genom att använda **Get-AzBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="c1b9d-114">Kommandot skickar varje datornod till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c1b9d-115">Med kommandot får du inställningar för fjärrinloggning för varje datornod.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="c1b9d-116">Exempel 2: Hämta inställningar för fjärrinloggning för en nod</span><span class="sxs-lookup"><span data-stu-id="c1b9d-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="c1b9d-117">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang och lagrar det sedan i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="c1b9d-118">Det andra kommandot får fjärrinloggnings inställningarna för den datornod som har angivet ID i poolen med ID-ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="c1b9d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1b9d-119">PARAMETERS</span></span>

### <span data-ttu-id="c1b9d-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c1b9d-120">-BatchContext</span></span>
<span data-ttu-id="c1b9d-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c1b9d-122">Använd Get-AzBatchAccountKey cmdlet för att få en **BatchAccountContext** som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="c1b9d-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="c1b9d-123">-ComputeNode</span></span>
<span data-ttu-id="c1b9d-124">Anger en datornod som ett **PSComputeNode** -objekt, för vilken denna cmdlet får inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="c1b9d-125">Använd cmdleten Get-AzBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="c1b9d-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c1b9d-126">-ComputeNodeId</span></span>
<span data-ttu-id="c1b9d-127">Anger ID för den datornod för vilken du ska få inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="c1b9d-128">för vilken denna cmdlet får inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1b9d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b9d-129">-DefaultProfile</span></span>
<span data-ttu-id="c1b9d-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b9d-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c1b9d-131">-PoolId</span></span>
<span data-ttu-id="c1b9d-132">Anger ID för den pool som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="c1b9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b9d-133">CommonParameters</span></span>
<span data-ttu-id="c1b9d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1b9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b9d-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1b9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b9d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1b9d-136">INPUTS</span></span>

### <span data-ttu-id="c1b9d-137">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="c1b9d-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="c1b9d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c1b9d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c1b9d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1b9d-139">OUTPUTS</span></span>

### <span data-ttu-id="c1b9d-140">Microsoft.Azure.Commands.BatCH. Modeller. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="c1b9d-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="c1b9d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1b9d-141">NOTES</span></span>

## <span data-ttu-id="c1b9d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1b9d-142">RELATED LINKS</span></span>

[<span data-ttu-id="c1b9d-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c1b9d-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c1b9d-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="c1b9d-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="c1b9d-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="c1b9d-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="c1b9d-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c1b9d-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
