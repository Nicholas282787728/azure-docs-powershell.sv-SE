---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 3E736E85-0488-4D10-BEA1-4F9B8DA54C4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchPoolResize.md
ms.openlocfilehash: d8ce1ec138decb5769aebba431db2accd671f100
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580680"
---
# <span data-ttu-id="c563c-101">Stop-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c563c-101">Stop-AzureBatchPoolResize</span></span>

## <span data-ttu-id="c563c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c563c-102">SYNOPSIS</span></span>
<span data-ttu-id="c563c-103">Stoppar en ändring av poolens storlek.</span><span class="sxs-lookup"><span data-stu-id="c563c-103">Stops a pool resize operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c563c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c563c-104">SYNTAX</span></span>

```
Stop-AzureBatchPoolResize [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c563c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c563c-105">DESCRIPTION</span></span>
<span data-ttu-id="c563c-106">Cmdleten **Stop-AzureBatchPoolResize** stoppar en storleks ändring i Azure-satsen på en pool.</span><span class="sxs-lookup"><span data-stu-id="c563c-106">The **Stop-AzureBatchPoolResize** cmdlet stops an Azure Batch resize operation on a pool.</span></span>

## <span data-ttu-id="c563c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c563c-107">EXAMPLES</span></span>

### <span data-ttu-id="c563c-108">Exempel 1: stoppa storleks ändring för en pool</span><span class="sxs-lookup"><span data-stu-id="c563c-108">Example 1: Stop resizing a pool</span></span>
```
PS C:\>Stop-AzureBatchPoolResize -Id "ContosoPool06" -BatchContext $Context
```

<span data-ttu-id="c563c-109">Det här kommandot stoppar en storleks ändring på poolen med ID-ContosoPool06.</span><span class="sxs-lookup"><span data-stu-id="c563c-109">This command stops a resize operation on the pool that has the ID ContosoPool06.</span></span>
<span data-ttu-id="c563c-110">Använd Get-AzureRmBatchAccountKeys cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="c563c-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="c563c-111">Exempel 2: stoppa storleks ändring för en pool med pipelinen</span><span class="sxs-lookup"><span data-stu-id="c563c-111">Example 2: Stop resizing a pool by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchPool -Id "ContosoPool06" -BatchContext $Context | Stop-AzureBatchPoolResize -BatchContext $Context
```

<span data-ttu-id="c563c-112">Det här kommandot slutar att ändra storlek på en pool med pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="c563c-112">This command stops resizing a pool by using the pipeline operator.</span></span>
<span data-ttu-id="c563c-113">Kommandot hämtar den pool som har ID-ContosoPool06 med hjälp av Get-AzureBatchPool cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c563c-113">The command gets the pool that has the ID ContosoPool06 by using the Get-AzureBatchPool cmdlet.</span></span>
<span data-ttu-id="c563c-114">Kommandot skickar detta pool-objekt till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c563c-114">The command passes that pool object to the current cmdlet.</span></span>
<span data-ttu-id="c563c-115">Kommandot stoppar storleks ändringen för poolen.</span><span class="sxs-lookup"><span data-stu-id="c563c-115">The command stops the resize operation on that pool.</span></span>

## <span data-ttu-id="c563c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c563c-116">PARAMETERS</span></span>

### <span data-ttu-id="c563c-117">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c563c-117">-BatchContext</span></span>
<span data-ttu-id="c563c-118">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c563c-118">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c563c-119">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c563c-119">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c563c-120">-ID</span><span class="sxs-lookup"><span data-stu-id="c563c-120">-Id</span></span>
<span data-ttu-id="c563c-121">Anger ID för den pool där denna cmdlet stoppar en storleks ändring.</span><span class="sxs-lookup"><span data-stu-id="c563c-121">Specifies the ID of the pool for which this cmdlet stops a resizing operation.</span></span>

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

### <span data-ttu-id="c563c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c563c-122">-DefaultProfile</span></span>
<span data-ttu-id="c563c-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c563c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c563c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c563c-124">CommonParameters</span></span>
<span data-ttu-id="c563c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c563c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c563c-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c563c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c563c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c563c-127">INPUTS</span></span>

### <span data-ttu-id="c563c-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c563c-128">BatchAccountContext</span></span>
<span data-ttu-id="c563c-129">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c563c-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c563c-130">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c563c-130">String</span></span>
<span data-ttu-id="c563c-131">Parametern ' ID ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c563c-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c563c-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c563c-132">OUTPUTS</span></span>

## <span data-ttu-id="c563c-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c563c-133">NOTES</span></span>

## <span data-ttu-id="c563c-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c563c-134">RELATED LINKS</span></span>

[<span data-ttu-id="c563c-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c563c-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c563c-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c563c-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c563c-137">Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="c563c-137">Start-AzureBatchPoolResize</span></span>](./Start-AzureBatchPoolResize.md)

[<span data-ttu-id="c563c-138">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c563c-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


