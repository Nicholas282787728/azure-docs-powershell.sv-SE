---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272456"
---
# <span data-ttu-id="a7421-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="a7421-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="a7421-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7421-102">SYNOPSIS</span></span>
<span data-ttu-id="a7421-103">Hämtar de avbildningar som stöds för batch-konto.</span><span class="sxs-lookup"><span data-stu-id="a7421-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="a7421-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7421-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7421-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7421-105">DESCRIPTION</span></span>
<span data-ttu-id="a7421-106">Cmdleten **Get-AzBatchSupportedImage** har stöd för virtuella dator bilder som är tillgängliga i ett Azure Batch-konto.</span><span class="sxs-lookup"><span data-stu-id="a7421-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="a7421-107">Ange kontot med hjälp av parametern *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="a7421-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="a7421-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7421-108">EXAMPLES</span></span>

### <span data-ttu-id="a7421-109">Exempel 1: Hämta alla tillgängliga bilder</span><span class="sxs-lookup"><span data-stu-id="a7421-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="a7421-110">Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="a7421-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="a7421-111">Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.</span><span class="sxs-lookup"><span data-stu-id="a7421-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="a7421-112">Med det andra kommandot hämtas alla tillgängliga bilder för det batch-kontot.</span><span class="sxs-lookup"><span data-stu-id="a7421-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="a7421-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7421-113">PARAMETERS</span></span>

### <span data-ttu-id="a7421-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a7421-114">-BatchContext</span></span>
<span data-ttu-id="a7421-115">Den BatchAccountContext-instans som ska användas vid interaktion med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a7421-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="a7421-116">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="a7421-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="a7421-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="a7421-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="a7421-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="a7421-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="a7421-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a7421-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a7421-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7421-120">-DefaultProfile</span></span>
<span data-ttu-id="a7421-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a7421-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7421-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="a7421-122">-Filter</span></span>
<span data-ttu-id="a7421-123">Anger en OData filter-sats för bilder som stöds.</span><span class="sxs-lookup"><span data-stu-id="a7421-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="a7421-124">Om du inte anger något filter returnerar denna cmdlet alla bilder som batch-kontot har stöd för.</span><span class="sxs-lookup"><span data-stu-id="a7421-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="a7421-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a7421-125">-MaxCount</span></span>
<span data-ttu-id="a7421-126">Anger maximalt antal bilder som stöds för att returneras.</span><span class="sxs-lookup"><span data-stu-id="a7421-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="a7421-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7421-127">CommonParameters</span></span>
<span data-ttu-id="a7421-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7421-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7421-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7421-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7421-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7421-130">INPUTS</span></span>

### <span data-ttu-id="a7421-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a7421-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a7421-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7421-132">OUTPUTS</span></span>

### <span data-ttu-id="a7421-133">Microsoft.Azure.Commands.BatCH. Modeller. PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="a7421-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="a7421-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7421-134">NOTES</span></span>

## <span data-ttu-id="a7421-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7421-135">RELATED LINKS</span></span>

[<span data-ttu-id="a7421-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a7421-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)