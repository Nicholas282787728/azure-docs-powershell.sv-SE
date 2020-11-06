---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 01ded3d4e9d77edac39e7c632f46d6e7ecf9eeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574427"
---
# <span data-ttu-id="febbb-101">Get-AzureBatchRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="febbb-101">Get-AzureBatchRemoteLoginSettings</span></span>

## <span data-ttu-id="febbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="febbb-102">SYNOPSIS</span></span>
<span data-ttu-id="febbb-103">Hämtar inställningar för fjärrinloggning för en datornod.</span><span class="sxs-lookup"><span data-stu-id="febbb-103">Gets remote logon settings for a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="febbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="febbb-104">SYNTAX</span></span>

### <span data-ttu-id="febbb-105">ID (standard)</span><span class="sxs-lookup"><span data-stu-id="febbb-105">Id (Default)</span></span>
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="febbb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="febbb-106">InputObject</span></span>
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="febbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="febbb-107">DESCRIPTION</span></span>
<span data-ttu-id="febbb-108">Cmdleten **Get-AzureBatchRemoteLoginSettings** hämtar inställningar för fjärrinloggning för en datornod i en infrastruktur baserad pool med virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="febbb-108">The **Get-AzureBatchRemoteLoginSettings** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="febbb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="febbb-109">EXAMPLES</span></span>

### <span data-ttu-id="febbb-110">Exempel 1: Hämta inställningar för fjärrinloggning för alla noder i en pool</span><span class="sxs-lookup"><span data-stu-id="febbb-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="febbb-111">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="febbb-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="febbb-112">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="febbb-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="febbb-113">Det andra kommandot får varje datornod i poolen med ID-ContosoPool genom att använda **Get-AzureBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="febbb-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzureBatchComputeNode**.</span></span>
<span data-ttu-id="febbb-114">Kommandot skickar varje datornod till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="febbb-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="febbb-115">Med kommandot får du inställningar för fjärrinloggning för varje datornod.</span><span class="sxs-lookup"><span data-stu-id="febbb-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="febbb-116">Exempel 2: Hämta inställningar för fjärrinloggning för en nod</span><span class="sxs-lookup"><span data-stu-id="febbb-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="febbb-117">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang och lagrar det sedan i $Context variabel.</span><span class="sxs-lookup"><span data-stu-id="febbb-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>

<span data-ttu-id="febbb-118">Det andra kommandot får fjärrinloggnings inställningarna för den datornod som har angivet ID i poolen med ID-ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="febbb-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="febbb-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="febbb-119">PARAMETERS</span></span>

### <span data-ttu-id="febbb-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="febbb-120">-BatchContext</span></span>
<span data-ttu-id="febbb-121">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="febbb-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="febbb-122">Använd Get-AzureRmBatchAccountKeys cmdlet för att få en **BatchAccountContext** som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="febbb-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="febbb-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="febbb-123">-ComputeNode</span></span>
<span data-ttu-id="febbb-124">Anger en datornod som ett **PSComputeNode** -objekt, för vilken denna cmdlet får inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="febbb-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="febbb-125">Använd cmdleten Get-AzureBatchComputeNode för att hämta ett Compute Node-objekt.</span><span class="sxs-lookup"><span data-stu-id="febbb-125">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="febbb-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="febbb-126">-ComputeNodeId</span></span>
<span data-ttu-id="febbb-127">Anger ID för den datornod för vilken du ska få inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="febbb-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="febbb-128">för vilken denna cmdlet får inställningar för fjärrinloggning.</span><span class="sxs-lookup"><span data-stu-id="febbb-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febbb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febbb-129">-DefaultProfile</span></span>
<span data-ttu-id="febbb-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="febbb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febbb-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="febbb-131">-PoolId</span></span>
<span data-ttu-id="febbb-132">Anger ID för den pool som innehåller den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="febbb-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febbb-133">CommonParameters</span></span>
<span data-ttu-id="febbb-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febbb-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="febbb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febbb-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="febbb-136">INPUTS</span></span>

### <span data-ttu-id="febbb-137">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="febbb-137">BatchAccountContext</span></span>
<span data-ttu-id="febbb-138">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="febbb-138">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="febbb-139">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="febbb-139">PSComputeNode</span></span>
<span data-ttu-id="febbb-140">Parametern ' ComputeNode ' godkänner värdet av typen ' PSComputeNode ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="febbb-140">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="febbb-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="febbb-141">OUTPUTS</span></span>

### <span data-ttu-id="febbb-142">PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="febbb-142">PSRemoteLoginSettings</span></span>

## <span data-ttu-id="febbb-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="febbb-143">NOTES</span></span>

## <span data-ttu-id="febbb-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="febbb-144">RELATED LINKS</span></span>

[<span data-ttu-id="febbb-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="febbb-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="febbb-146">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="febbb-146">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="febbb-147">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="febbb-147">Get-AzureBatchRemoteDesktopProtocolFile</span></span>](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="febbb-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="febbb-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


