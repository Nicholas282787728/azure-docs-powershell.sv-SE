---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: 153e566df3e2ab6f758d139719af1e812e0476ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574408"
---
# <span data-ttu-id="b3bc5-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="b3bc5-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="b3bc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bc5-103">Stoppar en ändring av poolens storlek.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3bc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3bc5-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3bc5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bc5-106">Cmdleten **Stop-AzureBatchPoolResize** stoppar en storleks ändring i Azure-satsen på en pool.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="b3bc5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="b3bc5-108">Exempel 1: stoppa storleks ändring för en pool</span><span class="sxs-lookup"><span data-stu-id="b3bc5-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="b3bc5-109">Det här kommandot stoppar en storleks ändring på poolen med ID-ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="b3bc5-110">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="b3bc5-111">Exempel 2: stoppa storleks ändring för en pool med pipelinen</span><span class="sxs-lookup"><span data-stu-id="b3bc5-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="b3bc5-112">Det här kommandot slutar att ändra storlek på en pool med pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="b3bc5-113">Kommandot hämtar den pool som har ID-ContosoPool06 med hjälp av Get-AzureBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="b3bc5-114">Kommandot skickar detta pool-objekt till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="b3bc5-115">Kommandot stoppar storleks ändringen för poolen.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="b3bc5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3bc5-116">PARAMETERS</span></span>

### <span data-ttu-id="b3bc5-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b3bc5-117">-BatchContext</span></span>
<span data-ttu-id="b3bc5-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b3bc5-119">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-119">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b3bc5-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-120">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b3bc5-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b3bc5-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b3bc5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bc5-123">-DefaultProfile</span></span>
<span data-ttu-id="b3bc5-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3bc5-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b3bc5-125">-Id</span></span>
<span data-ttu-id="b3bc5-126">Anger ID för den pool där denna cmdlet stoppar en storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3bc5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bc5-127">CommonParameters</span></span>
<span data-ttu-id="b3bc5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bc5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bc5-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3bc5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bc5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3bc5-130">INPUTS</span></span>

### <span data-ttu-id="b3bc5-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b3bc5-131">BatchAccountContext</span></span>
<span data-ttu-id="b3bc5-132">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b3bc5-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b3bc5-133">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="b3bc5-133">String</span></span>
<span data-ttu-id="b3bc5-134">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b3bc5-134">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b3bc5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3bc5-135">OUTPUTS</span></span>

## <span data-ttu-id="b3bc5-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3bc5-136">NOTES</span></span>

## <span data-ttu-id="b3bc5-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3bc5-137">RELATED LINKS</span></span>

[<span data-ttu-id="b3bc5-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b3bc5-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b3bc5-139">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="b3bc5-139">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="b3bc5-140">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="b3bc5-140">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="b3bc5-141">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="b3bc5-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


