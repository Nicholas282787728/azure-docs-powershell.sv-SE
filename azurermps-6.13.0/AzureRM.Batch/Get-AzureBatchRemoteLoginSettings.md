---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: d25e9aeb75c58bcce560043d87f5ce9eef065b97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580856"
---
# <span data-ttu-id="02f0a-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="02f0a-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="02f0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="02f0a-103">Hämtar inställningar för fjärrinloggning för en datornod.</span><span class="sxs-lookup"><span data-stu-id="02f0a-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02f0a-104">SYNTAX</span></span>

### <span data-ttu-id="02f0a-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="02f0a-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02f0a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="02f0a-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02f0a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02f0a-107">DESCRIPTION</span></span>
<span data-ttu-id="02f0a-108">Cmdleten **Get-AzureBatchRemoteLoginSettings** hämtar inställningar för fjärrinloggning för en datornod i en infrastruktur baserad pool med virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="02f0a-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="02f0a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02f0a-109">EXAMPLES</span></span>

### <span data-ttu-id="02f0a-110">Exempel 1: Hämta inställningar för fjärrinloggning för alla noder i en pool</span><span class="sxs-lookup"><span data-stu-id="02f0a-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="02f0a-111">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="02f0a-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="02f0a-112">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="02f0a-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="02f0a-113">Det andra kommandot får varje datornod i poolen med ID-ContosoPool genom att använda **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="02f0a-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="02f0a-114">Kommandot skickar varje datornod till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="02f0a-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="02f0a-115">Med kommandot får du inställningar för fjärrinloggning för varje datornod.</span><span class="sxs-lookup"><span data-stu-id="02f0a-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="02f0a-116">Exempel 2: Hämta inställningar för fjärrinloggning för en nod</span><span class="sxs-lookup"><span data-stu-id="02f0a-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="02f0a-117">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang och lagrar det sedan i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="02f0a-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="02f0a-118">Det andra kommandot får fjärrinloggnings inställningarna för den datornod som har angivet ID i poolen med ID-ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="02f0a-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="02f0a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02f0a-119">PARAMETERS</span></span>

### <span data-ttu-id="02f0a-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="02f0a-120">-BatchContext</span></span>
<span data-ttu-id="02f0a-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="02f0a-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02f0a-122">Använd Get-AzureRmBatchAccountKeys cmdlet för att få en **BatchAccountContext** som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="02f0a-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="02f0a-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="02f0a-123">-ComputeNode</span></span>
<span data-ttu-id="02f0a-124">Anger en datornod som ett **PSComputeNode** -objekt, för vilken denna cmdlet får inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="02f0a-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="02f0a-125">Använd cmdleten Get-AzureBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="02f0a-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="02f0a-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="02f0a-126">-ComputeNodeId</span></span>
<span data-ttu-id="02f0a-127">Anger ID för den datornod för vilken du ska få inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="02f0a-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="02f0a-128">för vilken denna cmdlet får inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="02f0a-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="02f0a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f0a-129">-DefaultProfile</span></span>
<span data-ttu-id="02f0a-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02f0a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02f0a-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="02f0a-131">-PoolId</span></span>
<span data-ttu-id="02f0a-132">Anger ID för den pool som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="02f0a-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="02f0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f0a-133">CommonParameters</span></span>
<span data-ttu-id="02f0a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f0a-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f0a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f0a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02f0a-136">INPUTS</span></span>

### <span data-ttu-id="02f0a-137">Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="02f0a-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="02f0a-138">Parametrar: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02f0a-138">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="02f0a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02f0a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="02f0a-140">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="02f0a-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="02f0a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02f0a-141">OUTPUTS</span></span>

### <span data-ttu-id="02f0a-142">Microsoft.Azure.Commands.BatCH. Modeller. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="02f0a-142">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="02f0a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02f0a-143">NOTES</span></span>

## <span data-ttu-id="02f0a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02f0a-144">RELATED LINKS</span></span>

[<span data-ttu-id="02f0a-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="02f0a-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="02f0a-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="02f0a-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="02f0a-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="02f0a-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="02f0a-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="02f0a-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


