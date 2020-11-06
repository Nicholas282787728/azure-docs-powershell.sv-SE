---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 8c9b48046393a55bc0d37e0fe6d08361dcf04246
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579640"
---
# <span data-ttu-id="cb750-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="cb750-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="cb750-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb750-102">SYNOPSIS</span></span>
<span data-ttu-id="cb750-103">Får agenten för batchattribut tillgängliga i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="cb750-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb750-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb750-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb750-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb750-105">DESCRIPTION</span></span>
<span data-ttu-id="cb750-106">Cmdleten **Get-AzureBatchNodeAgentSku** hämtar nodadresser-SKU: er som är tillgängliga i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="cb750-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="cb750-107">Ange kontot med hjälp av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="cb750-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="cb750-108">Du kan begränsa sökningen till SKU: er som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="cb750-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="cb750-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb750-109">EXAMPLES</span></span>

### <span data-ttu-id="cb750-110">Exempel 1: Hämta alla tillgängliga Node agent-SKU: er</span><span class="sxs-lookup"><span data-stu-id="cb750-110">Example 1: Get all available node agent SKUs</span></span>
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

<span data-ttu-id="cb750-111">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="cb750-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="cb750-112">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="cb750-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="cb750-113">Det andra kommandot får alla tillgängliga Node agent-SKU: er som batch stöder.</span><span class="sxs-lookup"><span data-stu-id="cb750-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="cb750-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb750-114">PARAMETERS</span></span>

### <span data-ttu-id="cb750-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cb750-115">-BatchContext</span></span>
<span data-ttu-id="cb750-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb750-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cb750-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cb750-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cb750-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="cb750-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cb750-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="cb750-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cb750-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cb750-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cb750-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb750-121">-DefaultProfile</span></span>
<span data-ttu-id="cb750-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb750-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb750-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="cb750-123">-Filter</span></span>
<span data-ttu-id="cb750-124">Anger en OData filter-sats för Node agent-SKU: er.</span><span class="sxs-lookup"><span data-stu-id="cb750-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="cb750-125">Om du inte anger något filter returnerar denna cmdlet alla nodernas SKU: er som stöds.</span><span class="sxs-lookup"><span data-stu-id="cb750-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb750-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="cb750-126">-MaxCount</span></span>
<span data-ttu-id="cb750-127">Anger det maximala antalet Node-SKU: er som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="cb750-127">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb750-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb750-128">CommonParameters</span></span>
<span data-ttu-id="cb750-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb750-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb750-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb750-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb750-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb750-131">INPUTS</span></span>

### <span data-ttu-id="cb750-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cb750-132">BatchAccountContext</span></span>
<span data-ttu-id="cb750-133">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="cb750-133">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="cb750-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb750-134">OUTPUTS</span></span>

### <span data-ttu-id="cb750-135">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="cb750-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="cb750-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb750-136">NOTES</span></span>

## <span data-ttu-id="cb750-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb750-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb750-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cb750-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


