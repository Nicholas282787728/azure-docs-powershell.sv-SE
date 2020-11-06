---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: 9f9b2a406d5fc728e9297fc4093a60b3f6ec4bf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582068"
---
# <span data-ttu-id="bce99-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bce99-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="bce99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bce99-102">SYNOPSIS</span></span>
<span data-ttu-id="bce99-103">Uppdaterar egenskaperna för en pool.</span><span class="sxs-lookup"><span data-stu-id="bce99-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bce99-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce99-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bce99-105">DESCRIPTION</span></span>
<span data-ttu-id="bce99-106">Cmdleten **set-AzureBatchPool** uppdaterar egenskaperna för en pool i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bce99-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="bce99-107">Använd Get-AzureBatchPool cmdlet för att hämta ett **PSCloudPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bce99-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="bce99-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bce99-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="bce99-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bce99-109">EXAMPLES</span></span>

### <span data-ttu-id="bce99-110">Exempel 1: uppdatera en pool</span><span class="sxs-lookup"><span data-stu-id="bce99-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="bce99-111">Det första kommandot får en pool genom att använda **Get-AzureBatchPool** och lagrar den sedan i $pool variabel.</span><span class="sxs-lookup"><span data-stu-id="bce99-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="bce99-112">Nästa tre kommandon ändrar specifikationen för start uppgiften för $Pool-objektet.</span><span class="sxs-lookup"><span data-stu-id="bce99-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="bce99-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Pool.</span><span class="sxs-lookup"><span data-stu-id="bce99-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="bce99-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bce99-114">PARAMETERS</span></span>

### <span data-ttu-id="bce99-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bce99-115">-BatchContext</span></span>
<span data-ttu-id="bce99-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bce99-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bce99-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bce99-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bce99-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="bce99-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bce99-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="bce99-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bce99-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bce99-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bce99-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce99-121">-DefaultProfile</span></span>
<span data-ttu-id="bce99-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bce99-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bce99-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="bce99-123">-Pool</span></span>
<span data-ttu-id="bce99-124">Anger den **PSCloudPool** som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="bce99-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bce99-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce99-125">CommonParameters</span></span>
<span data-ttu-id="bce99-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce99-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce99-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce99-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce99-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bce99-128">INPUTS</span></span>

### <span data-ttu-id="bce99-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bce99-129">BatchAccountContext</span></span>
<span data-ttu-id="bce99-130">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bce99-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bce99-131">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="bce99-131">PSCloudPool</span></span>
<span data-ttu-id="bce99-132">Parametern ' pool ' godkänner värdet av typen ' PSCloudPool ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="bce99-132">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="bce99-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bce99-133">OUTPUTS</span></span>

## <span data-ttu-id="bce99-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bce99-134">NOTES</span></span>

## <span data-ttu-id="bce99-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bce99-135">RELATED LINKS</span></span>

[<span data-ttu-id="bce99-136">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bce99-136">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="bce99-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bce99-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bce99-138">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bce99-138">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="bce99-139">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="bce99-139">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="bce99-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="bce99-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


