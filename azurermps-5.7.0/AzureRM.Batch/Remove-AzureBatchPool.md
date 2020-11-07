---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: a42e6876336e409cca8df9e0fc72e65e8b6e1b3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583663"
---
# <span data-ttu-id="dde04-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="dde04-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="dde04-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dde04-102">SYNOPSIS</span></span>
<span data-ttu-id="dde04-103">Tar bort angiven gruppbearbetningssekvens.</span><span class="sxs-lookup"><span data-stu-id="dde04-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dde04-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dde04-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde04-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dde04-105">DESCRIPTION</span></span>
<span data-ttu-id="dde04-106">Cmdleten **Remove-AzureBatchPool** tar bort angiven Azure-grupppool.</span><span class="sxs-lookup"><span data-stu-id="dde04-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="dde04-107">Du uppmanas att bekräfta om du inte använder parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="dde04-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="dde04-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dde04-108">EXAMPLES</span></span>

### <span data-ttu-id="dde04-109">Exempel 1: ta bort en grupppool utifrån pool-ID</span><span class="sxs-lookup"><span data-stu-id="dde04-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="dde04-110">Det här kommandot tar bort poolen med ID-nummer.</span><span class="sxs-lookup"><span data-stu-id="dde04-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="dde04-111">Användaren uppmanas att bekräfta innan borttagningen utförs.</span><span class="sxs-lookup"><span data-stu-id="dde04-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="dde04-112">Exempel 2: ta bort alla batchattribut per tvång</span><span class="sxs-lookup"><span data-stu-id="dde04-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="dde04-113">Det här kommandot tar bort alla batchattribut.</span><span class="sxs-lookup"><span data-stu-id="dde04-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="dde04-114">Eftersom *Force* -parametern finns ignoreras bekräftelse meddelandet.</span><span class="sxs-lookup"><span data-stu-id="dde04-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="dde04-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dde04-115">PARAMETERS</span></span>

### <span data-ttu-id="dde04-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dde04-116">-BatchContext</span></span>
<span data-ttu-id="dde04-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dde04-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dde04-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dde04-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="dde04-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="dde04-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="dde04-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="dde04-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="dde04-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="dde04-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="dde04-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde04-122">-DefaultProfile</span></span>
<span data-ttu-id="dde04-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dde04-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde04-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dde04-124">-Force</span></span>
<span data-ttu-id="dde04-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dde04-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde04-126">-ID</span><span class="sxs-lookup"><span data-stu-id="dde04-126">-Id</span></span>
<span data-ttu-id="dde04-127">Anger ID för poolen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="dde04-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="dde04-128">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="dde04-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dde04-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dde04-129">-Confirm</span></span>
<span data-ttu-id="dde04-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dde04-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde04-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde04-131">-WhatIf</span></span>
<span data-ttu-id="dde04-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dde04-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde04-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dde04-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dde04-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde04-134">CommonParameters</span></span>
<span data-ttu-id="dde04-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde04-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde04-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde04-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde04-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dde04-137">INPUTS</span></span>

### <span data-ttu-id="dde04-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dde04-138">BatchAccountContext</span></span>
<span data-ttu-id="dde04-139">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dde04-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="dde04-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dde04-140">OUTPUTS</span></span>

## <span data-ttu-id="dde04-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dde04-141">NOTES</span></span>

## <span data-ttu-id="dde04-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dde04-142">RELATED LINKS</span></span>

[<span data-ttu-id="dde04-143">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dde04-143">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dde04-144">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="dde04-144">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="dde04-145">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="dde04-145">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="dde04-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="dde04-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)

