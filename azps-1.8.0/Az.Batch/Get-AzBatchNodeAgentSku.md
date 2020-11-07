---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755114"
---
# <span data-ttu-id="c1120-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="c1120-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="c1120-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1120-102">SYNOPSIS</span></span>
<span data-ttu-id="c1120-103">Får agenten för batchattribut tillgängliga i ett batch-konto.</span><span class="sxs-lookup"><span data-stu-id="c1120-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="c1120-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1120-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1120-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1120-105">DESCRIPTION</span></span>
<span data-ttu-id="c1120-106">Cmdleten **Get-AzBatchNodeAgentSku** hämtar nodadresser-SKU: er som är tillgängliga i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="c1120-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="c1120-107">Ange kontot med hjälp av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="c1120-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="c1120-108">Du kan begränsa sökningen till SKU: er som matchar ett open data Protocol (OData)-filter.</span><span class="sxs-lookup"><span data-stu-id="c1120-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="c1120-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1120-109">EXAMPLES</span></span>

### <span data-ttu-id="c1120-110">Exempel 1: Hämta alla tillgängliga Node agent-SKU: er</span><span class="sxs-lookup"><span data-stu-id="c1120-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="c1120-111">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="c1120-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="c1120-112">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="c1120-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="c1120-113">Det andra kommandot får alla tillgängliga Node agent-SKU: er som batch stöder.</span><span class="sxs-lookup"><span data-stu-id="c1120-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="c1120-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1120-114">PARAMETERS</span></span>

### <span data-ttu-id="c1120-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c1120-115">-BatchContext</span></span>
<span data-ttu-id="c1120-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c1120-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c1120-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c1120-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c1120-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="c1120-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c1120-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="c1120-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c1120-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c1120-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c1120-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1120-121">-DefaultProfile</span></span>
<span data-ttu-id="c1120-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1120-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1120-123">-Filter</span><span class="sxs-lookup"><span data-stu-id="c1120-123">-Filter</span></span>
<span data-ttu-id="c1120-124">Anger en OData filter-sats för Node agent-SKU: er.</span><span class="sxs-lookup"><span data-stu-id="c1120-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="c1120-125">Om du inte anger något filter returnerar denna cmdlet alla nodernas SKU: er som stöds.</span><span class="sxs-lookup"><span data-stu-id="c1120-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="c1120-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="c1120-126">-MaxCount</span></span>
<span data-ttu-id="c1120-127">Anger det maximala antalet Node-SKU: er som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="c1120-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="c1120-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1120-128">CommonParameters</span></span>
<span data-ttu-id="c1120-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1120-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1120-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1120-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1120-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1120-131">INPUTS</span></span>

### <span data-ttu-id="c1120-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c1120-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c1120-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1120-133">OUTPUTS</span></span>

### <span data-ttu-id="c1120-134">Microsoft.Azure.Commands.BatCH. Modeller. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="c1120-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="c1120-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1120-135">NOTES</span></span>

## <span data-ttu-id="c1120-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1120-136">RELATED LINKS</span></span>

[<span data-ttu-id="c1120-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c1120-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


