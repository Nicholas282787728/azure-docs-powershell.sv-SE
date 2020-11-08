---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 229877db7a3077a4b1951a06914c842e63384ba6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270150"
---
# <span data-ttu-id="cb44b-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cb44b-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="cb44b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb44b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb44b-103">Stoppar en ändring av poolens storlek.</span><span class="sxs-lookup"><span data-stu-id="cb44b-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="cb44b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb44b-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb44b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb44b-105">DESCRIPTION</span></span>
<span data-ttu-id="cb44b-106">Cmdleten **Stop-AzBatchPoolResize** stoppar en storleks ändring i Azure-satsen på en pool.</span><span class="sxs-lookup"><span data-stu-id="cb44b-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="cb44b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb44b-107">EXAMPLES</span></span>

### <span data-ttu-id="cb44b-108">Exempel 1: stoppa storleks ändring för en pool</span><span class="sxs-lookup"><span data-stu-id="cb44b-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="cb44b-109">Det här kommandot stoppar en storleks ändring på poolen med ID-ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="cb44b-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="cb44b-110">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="cb44b-110">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="cb44b-111">Exempel 2: stoppa storleks ändring för en pool med pipelinen</span><span class="sxs-lookup"><span data-stu-id="cb44b-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="cb44b-112">Det här kommandot slutar att ändra storlek på en pool med pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="cb44b-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="cb44b-113">Kommandot hämtar den pool som har ID-ContosoPool06 med hjälp av Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb44b-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="cb44b-114">Kommandot skickar detta pool-objekt till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb44b-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="cb44b-115">Kommandot stoppar storleks ändringen för poolen.</span><span class="sxs-lookup"><span data-stu-id="cb44b-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="cb44b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb44b-116">PARAMETERS</span></span>

### <span data-ttu-id="cb44b-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cb44b-117">-BatchContext</span></span>
<span data-ttu-id="cb44b-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb44b-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cb44b-119">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb44b-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cb44b-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="cb44b-120">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cb44b-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="cb44b-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cb44b-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cb44b-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cb44b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb44b-123">-DefaultProfile</span></span>
<span data-ttu-id="cb44b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb44b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb44b-125">-ID</span><span class="sxs-lookup"><span data-stu-id="cb44b-125">-Id</span></span>
<span data-ttu-id="cb44b-126">Anger ID för den pool där denna cmdlet stoppar en storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="cb44b-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb44b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb44b-127">CommonParameters</span></span>
<span data-ttu-id="cb44b-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb44b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb44b-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb44b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb44b-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb44b-130">INPUTS</span></span>

### <span data-ttu-id="cb44b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cb44b-131">System.String</span></span>

### <span data-ttu-id="cb44b-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cb44b-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cb44b-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb44b-133">OUTPUTS</span></span>

### <span data-ttu-id="cb44b-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="cb44b-134">System.Void</span></span>

## <span data-ttu-id="cb44b-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb44b-135">NOTES</span></span>

## <span data-ttu-id="cb44b-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb44b-136">RELATED LINKS</span></span>

[<span data-ttu-id="cb44b-137">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cb44b-137">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cb44b-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cb44b-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="cb44b-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="cb44b-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="cb44b-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="cb44b-140">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
