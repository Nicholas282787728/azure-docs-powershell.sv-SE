---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583367"
---
# <span data-ttu-id="3c0cd-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="3c0cd-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="3c0cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0cd-103">Får agenten för batchattribut tillgängliga i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c0cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c0cd-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c0cd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c0cd-105">DESCRIPTION</span></span>
<span data-ttu-id="3c0cd-106">Cmdleten **Get-AzureBatchNodeAgentSku** hämtar nodadresser-SKU: er som är tillgängliga i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="3c0cd-107">Ange kontot med hjälp av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="3c0cd-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="3c0cd-108">Du kan begränsa sökningen till SKU: er som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="3c0cd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c0cd-109">EXAMPLES</span></span>

### <span data-ttu-id="3c0cd-110">Exempel 1: Hämta alla tillgängliga Node agent-SKU: er</span><span class="sxs-lookup"><span data-stu-id="3c0cd-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="3c0cd-111">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="3c0cd-112">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="3c0cd-113">Det andra kommandot får alla tillgängliga Node agent-SKU: er som batch stöder.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="3c0cd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c0cd-114">PARAMETERS</span></span>

### <span data-ttu-id="3c0cd-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3c0cd-115">-BatchContext</span></span>
<span data-ttu-id="3c0cd-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3c0cd-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="3c0cd-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="3c0cd-118">-Filter</span></span>
<span data-ttu-id="3c0cd-119">Anger en OData filter-sats för Node agent-SKU: er.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="3c0cd-120">Om du inte anger något filter returnerar denna cmdlet alla nodernas SKU: er som stöds.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c0cd-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3c0cd-121">-MaxCount</span></span>
<span data-ttu-id="3c0cd-122">Anger det maximala antalet Node-SKU: er som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-122">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c0cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0cd-123">-DefaultProfile</span></span>
<span data-ttu-id="3c0cd-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c0cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0cd-125">CommonParameters</span></span>
<span data-ttu-id="3c0cd-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0cd-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0cd-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c0cd-128">INPUTS</span></span>

### <span data-ttu-id="3c0cd-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3c0cd-129">BatchAccountContext</span></span>
<span data-ttu-id="3c0cd-130">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3c0cd-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="3c0cd-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c0cd-131">OUTPUTS</span></span>

### <span data-ttu-id="3c0cd-132">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="3c0cd-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="3c0cd-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c0cd-133">NOTES</span></span>

## <span data-ttu-id="3c0cd-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c0cd-134">RELATED LINKS</span></span>

[<span data-ttu-id="3c0cd-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3c0cd-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


