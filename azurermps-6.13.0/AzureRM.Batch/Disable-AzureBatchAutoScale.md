---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 403e38ae72f927b4b98107161b62859aa57bacf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755550"
---
# <span data-ttu-id="e8203-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e8203-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="e8203-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8203-102">SYNOPSIS</span></span>
<span data-ttu-id="e8203-103">Inaktiverar automatisk skalning av en pool.</span><span class="sxs-lookup"><span data-stu-id="e8203-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8203-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8203-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8203-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8203-105">DESCRIPTION</span></span>
<span data-ttu-id="e8203-106">Cmdleten **disable-AzureBatchAutoScale** inaktiverar automatisk skalning för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="e8203-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="e8203-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8203-107">EXAMPLES</span></span>

### <span data-ttu-id="e8203-108">Exempel 1: inaktivera automatisk skalning av en pool</span><span class="sxs-lookup"><span data-stu-id="e8203-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="e8203-109">Det här kommandot inaktiverar automatisk skalning för poolen med namnet min pool.</span><span class="sxs-lookup"><span data-stu-id="e8203-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="e8203-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8203-110">PARAMETERS</span></span>

### <span data-ttu-id="e8203-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e8203-111">-BatchContext</span></span>
<span data-ttu-id="e8203-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e8203-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e8203-113">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e8203-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e8203-114">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="e8203-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e8203-115">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="e8203-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e8203-116">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e8203-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e8203-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8203-117">-DefaultProfile</span></span>
<span data-ttu-id="e8203-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8203-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8203-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e8203-119">-Id</span></span>
<span data-ttu-id="e8203-120">Anger poolens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="e8203-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="e8203-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8203-121">CommonParameters</span></span>
<span data-ttu-id="e8203-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8203-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8203-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8203-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8203-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8203-124">INPUTS</span></span>

### <span data-ttu-id="e8203-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e8203-125">System.String</span></span>

### <span data-ttu-id="e8203-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e8203-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e8203-127">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8203-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e8203-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8203-128">OUTPUTS</span></span>

### <span data-ttu-id="e8203-129">System. Void</span><span class="sxs-lookup"><span data-stu-id="e8203-129">System.Void</span></span>

## <span data-ttu-id="e8203-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8203-130">NOTES</span></span>

## <span data-ttu-id="e8203-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8203-131">RELATED LINKS</span></span>

[<span data-ttu-id="e8203-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e8203-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="e8203-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e8203-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="e8203-134">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e8203-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


