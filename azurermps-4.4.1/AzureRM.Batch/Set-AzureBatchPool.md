---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579788"
---
# <span data-ttu-id="c274e-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c274e-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="c274e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c274e-102">SYNOPSIS</span></span>
<span data-ttu-id="c274e-103">Uppdaterar egenskaperna för en pool.</span><span class="sxs-lookup"><span data-stu-id="c274e-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c274e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c274e-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c274e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c274e-105">DESCRIPTION</span></span>
<span data-ttu-id="c274e-106">Cmdleten **set-AzureBatchPool** uppdaterar egenskaperna för en pool i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c274e-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="c274e-107">Använd Get-AzureBatchPool cmdlet för att hämta ett **PSCloudPool** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c274e-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="c274e-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c274e-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="c274e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c274e-109">EXAMPLES</span></span>

### <span data-ttu-id="c274e-110">Exempel 1: uppdatera en pool</span><span class="sxs-lookup"><span data-stu-id="c274e-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="c274e-111">Det första kommandot får en pool genom att använda **Get-AzureBatchPool** och lagrar den sedan i $pool variabel.</span><span class="sxs-lookup"><span data-stu-id="c274e-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="c274e-112">Nästa tre kommandon ändrar specifikationen för start uppgiften för $Pool-objektet.</span><span class="sxs-lookup"><span data-stu-id="c274e-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="c274e-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Pool.</span><span class="sxs-lookup"><span data-stu-id="c274e-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="c274e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c274e-114">PARAMETERS</span></span>

### <span data-ttu-id="c274e-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c274e-115">-BatchContext</span></span>
<span data-ttu-id="c274e-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c274e-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c274e-117">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c274e-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c274e-118">-Pool</span><span class="sxs-lookup"><span data-stu-id="c274e-118">-Pool</span></span>
<span data-ttu-id="c274e-119">Anger den **PSCloudPool** som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="c274e-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

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

### <span data-ttu-id="c274e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c274e-120">-DefaultProfile</span></span>
<span data-ttu-id="c274e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c274e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c274e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c274e-122">CommonParameters</span></span>
<span data-ttu-id="c274e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c274e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c274e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c274e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c274e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c274e-125">INPUTS</span></span>

### <span data-ttu-id="c274e-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c274e-126">BatchAccountContext</span></span>
<span data-ttu-id="c274e-127">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c274e-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c274e-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="c274e-128">PSCloudPool</span></span>
<span data-ttu-id="c274e-129">Parametern ' pool ' godkänner värdet av typen ' PSCloudPool ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c274e-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="c274e-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c274e-130">OUTPUTS</span></span>

## <span data-ttu-id="c274e-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c274e-131">NOTES</span></span>

## <span data-ttu-id="c274e-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c274e-132">RELATED LINKS</span></span>

[<span data-ttu-id="c274e-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c274e-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c274e-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c274e-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c274e-135">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c274e-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="c274e-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c274e-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="c274e-137">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c274e-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


