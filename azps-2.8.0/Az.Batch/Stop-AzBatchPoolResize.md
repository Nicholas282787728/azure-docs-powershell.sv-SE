---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchpoolresize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchPoolResize.md
ms.openlocfilehash: 9e970251671297a6fa4a0019bb663c9e34cbe4d7
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928402"
---
# <span data-ttu-id="2dcd6-101">Stop-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="2dcd6-101">Stop-AzBatchPoolResize</span></span>

## <span data-ttu-id="2dcd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2dcd6-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcd6-103">Stoppar en ändring av poolens storlek.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-103">Stops a pool resize operation.</span></span>

## <span data-ttu-id="2dcd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2dcd6-104">SYNTAX</span></span>

```
Stop-AzBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dcd6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2dcd6-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcd6-106">Cmdleten **Stop-AzBatchPoolResize** stoppar en storleks ändring i Azure-satsen på en pool.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-106">The **Stop-AzBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="2dcd6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2dcd6-107">EXAMPLES</span></span>

### <span data-ttu-id="2dcd6-108">Exempel 1: stoppa storleks ändring för en pool</span><span class="sxs-lookup"><span data-stu-id="2dcd6-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="2dcd6-109">Det här kommandot stoppar en storleks ändring på poolen med ID-ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="2dcd6-110">Använd Get-AzBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="2dcd6-111">Exempel 2: stoppa storleks ändring för en pool med pipelinen</span><span class="sxs-lookup"><span data-stu-id="2dcd6-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="2dcd6-112">Det här kommandot slutar att ändra storlek på en pool med pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="2dcd6-113">Kommandot hämtar den pool som har ID-ContosoPool06 med hjälp av Get-AzBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzBatchPool cmdlet.</span></span>
<span data-ttu-id="2dcd6-114">Kommandot skickar detta pool-objekt till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="2dcd6-115">Kommandot stoppar storleks ändringen för poolen.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="2dcd6-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2dcd6-116">PARAMETERS</span></span>

### <span data-ttu-id="2dcd6-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2dcd6-117">-BatchContext</span></span>
<span data-ttu-id="2dcd6-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2dcd6-119">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-119">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2dcd6-120">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-120">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2dcd6-121">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-121">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2dcd6-122">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-122">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2dcd6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcd6-123">-DefaultProfile</span></span>
<span data-ttu-id="2dcd6-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dcd6-125">-ID</span><span class="sxs-lookup"><span data-stu-id="2dcd6-125">-Id</span></span>
<span data-ttu-id="2dcd6-126">Anger ID för den pool där denna cmdlet stoppar en storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-126">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="2dcd6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcd6-127">CommonParameters</span></span>
<span data-ttu-id="2dcd6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcd6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcd6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dcd6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcd6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2dcd6-130">INPUTS</span></span>

### <span data-ttu-id="2dcd6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2dcd6-131">System.String</span></span>

### <span data-ttu-id="2dcd6-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2dcd6-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2dcd6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2dcd6-133">OUTPUTS</span></span>

### <span data-ttu-id="2dcd6-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="2dcd6-134">System.Void</span></span>

## <span data-ttu-id="2dcd6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2dcd6-135">NOTES</span></span>

## <span data-ttu-id="2dcd6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2dcd6-136">RELATED LINKS</span></span>

[<span data-ttu-id="2dcd6-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="2dcd6-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="2dcd6-138">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="2dcd6-138">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="2dcd6-139">Start-AzBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="2dcd6-139">Start-AzBatchPoolResize</span></span>](./Start-AzBatchPoolResize.md)

[<span data-ttu-id="2dcd6-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="2dcd6-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

