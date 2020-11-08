---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPool.md
ms.openlocfilehash: 423f249a7971883cbe47d8f499fdd780980362f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270043"
---
# <span data-ttu-id="3ad43-101">Set-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="3ad43-101">Set-AzBatchPool</span></span>

## <span data-ttu-id="3ad43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ad43-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad43-103">Uppdaterar egenskaperna för en pool.</span><span class="sxs-lookup"><span data-stu-id="3ad43-103">Updates the properties of a pool.</span></span>

## <span data-ttu-id="3ad43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ad43-104">SYNTAX</span></span>

```
Set-AzBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ad43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ad43-105">DESCRIPTION</span></span>
<span data-ttu-id="3ad43-106">Cmdleten **set-AzBatchPool** uppdaterar egenskaperna för en pool i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ad43-106">The **Set-AzBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="3ad43-107">Använd Get-AzBatchPool cmdlet för att hämta ett **PSCloudPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3ad43-107">Use the Get-AzBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="3ad43-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ad43-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="3ad43-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ad43-109">EXAMPLES</span></span>

### <span data-ttu-id="3ad43-110">Exempel 1: uppdatera en pool</span><span class="sxs-lookup"><span data-stu-id="3ad43-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="3ad43-111">Det första kommandot får en pool genom att använda **Get-AzBatchPool** och lagrar den sedan i $pool variabel.</span><span class="sxs-lookup"><span data-stu-id="3ad43-111">The first command gets a pool by using **Get-AzBatchPool** , and then stores it in the $Pool variable.</span></span>
<span data-ttu-id="3ad43-112">Nästa tre kommandon ändrar specifikationen för start uppgiften för $Pool-objektet.</span><span class="sxs-lookup"><span data-stu-id="3ad43-112">The next three commands modify the start task specification on the $Pool object.</span></span>
<span data-ttu-id="3ad43-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Pool.</span><span class="sxs-lookup"><span data-stu-id="3ad43-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="3ad43-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ad43-114">PARAMETERS</span></span>

### <span data-ttu-id="3ad43-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3ad43-115">-BatchContext</span></span>
<span data-ttu-id="3ad43-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ad43-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3ad43-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3ad43-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3ad43-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="3ad43-118">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3ad43-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="3ad43-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3ad43-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3ad43-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3ad43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad43-121">-DefaultProfile</span></span>
<span data-ttu-id="3ad43-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad43-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ad43-123">-Pool</span><span class="sxs-lookup"><span data-stu-id="3ad43-123">-Pool</span></span>
<span data-ttu-id="3ad43-124">Anger den **PSCloudPool** som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="3ad43-124">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ad43-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad43-125">CommonParameters</span></span>
<span data-ttu-id="3ad43-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad43-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad43-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ad43-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad43-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ad43-128">INPUTS</span></span>

### <span data-ttu-id="3ad43-129">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="3ad43-129">Microsoft.Azure.Commands.Batch.Models.PSCloudPool</span></span>

### <span data-ttu-id="3ad43-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3ad43-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3ad43-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ad43-131">OUTPUTS</span></span>

### <span data-ttu-id="3ad43-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="3ad43-132">System.Void</span></span>

## <span data-ttu-id="3ad43-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ad43-133">NOTES</span></span>

## <span data-ttu-id="3ad43-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ad43-134">RELATED LINKS</span></span>

[<span data-ttu-id="3ad43-135">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="3ad43-135">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="3ad43-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ad43-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3ad43-137">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="3ad43-137">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="3ad43-138">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="3ad43-138">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="3ad43-139">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="3ad43-139">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
