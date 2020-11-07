---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: d20a52c3e907bd981bc0a692ebb4aa44495d0960
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928470"
---
# <span data-ttu-id="8ce42-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8ce42-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="8ce42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ce42-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce42-103">Inaktiverar automatisk skalning av en pool.</span><span class="sxs-lookup"><span data-stu-id="8ce42-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="8ce42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ce42-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ce42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ce42-105">DESCRIPTION</span></span>
<span data-ttu-id="8ce42-106">Cmdleten **disable-AzBatchAutoScale** inaktiverar automatisk skalning för den angivna poolen.</span><span class="sxs-lookup"><span data-stu-id="8ce42-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="8ce42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ce42-107">EXAMPLES</span></span>

### <span data-ttu-id="8ce42-108">Exempel 1: inaktivera automatisk skalning av en pool</span><span class="sxs-lookup"><span data-stu-id="8ce42-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="8ce42-109">Det här kommandot inaktiverar automatisk skalning för poolen med namnet min pool.</span><span class="sxs-lookup"><span data-stu-id="8ce42-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="8ce42-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ce42-110">PARAMETERS</span></span>

### <span data-ttu-id="8ce42-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8ce42-111">-BatchContext</span></span>
<span data-ttu-id="8ce42-112">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8ce42-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8ce42-113">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8ce42-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="8ce42-114">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="8ce42-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="8ce42-115">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="8ce42-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="8ce42-116">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="8ce42-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="8ce42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce42-117">-DefaultProfile</span></span>
<span data-ttu-id="8ce42-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ce42-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce42-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8ce42-119">-Id</span></span>
<span data-ttu-id="8ce42-120">Anger poolens objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="8ce42-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="8ce42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce42-121">CommonParameters</span></span>
<span data-ttu-id="8ce42-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ce42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce42-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ce42-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce42-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ce42-124">INPUTS</span></span>

### <span data-ttu-id="8ce42-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8ce42-125">System.String</span></span>

### <span data-ttu-id="8ce42-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8ce42-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8ce42-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ce42-127">OUTPUTS</span></span>

### <span data-ttu-id="8ce42-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="8ce42-128">System.Void</span></span>

## <span data-ttu-id="8ce42-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ce42-129">NOTES</span></span>

## <span data-ttu-id="8ce42-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ce42-130">RELATED LINKS</span></span>

[<span data-ttu-id="8ce42-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8ce42-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="8ce42-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="8ce42-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="8ce42-133">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8ce42-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


