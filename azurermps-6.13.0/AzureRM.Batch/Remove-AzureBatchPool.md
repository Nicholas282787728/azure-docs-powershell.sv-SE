---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 4cfb497b98d20b5cf3741c90934e9e104b93ddcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574032"
---
# <span data-ttu-id="f5c8e-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f5c8e-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="f5c8e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c8e-103">Tar bort angiven gruppbearbetningssekvens.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5c8e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5c8e-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5c8e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c8e-106">Cmdleten **Remove-AzureBatchPool** tar bort angiven Azure-grupppool.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="f5c8e-107">Du uppmanas att bekräfta om du inte använder parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="f5c8e-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="f5c8e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5c8e-108">EXAMPLES</span></span>

### <span data-ttu-id="f5c8e-109">Exempel 1: ta bort en grupppool utifrån pool-ID</span><span class="sxs-lookup"><span data-stu-id="f5c8e-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="f5c8e-110">Det här kommandot tar bort poolen med ID-nummer.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="f5c8e-111">Användaren uppmanas att bekräfta innan borttagningen utförs.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="f5c8e-112">Exempel 2: ta bort alla batchattribut per tvång</span><span class="sxs-lookup"><span data-stu-id="f5c8e-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="f5c8e-113">Det här kommandot tar bort alla batchattribut.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="f5c8e-114">Eftersom *Force* -parametern finns ignoreras bekräftelse meddelandet.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="f5c8e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5c8e-115">PARAMETERS</span></span>

### <span data-ttu-id="f5c8e-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f5c8e-116">-BatchContext</span></span>
<span data-ttu-id="f5c8e-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f5c8e-118">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f5c8e-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f5c8e-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f5c8e-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f5c8e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c8e-122">-DefaultProfile</span></span>
<span data-ttu-id="f5c8e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5c8e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f5c8e-124">-Force</span></span>
<span data-ttu-id="f5c8e-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c8e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="f5c8e-126">-Id</span></span>
<span data-ttu-id="f5c8e-127">Anger ID för poolen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="f5c8e-128">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c8e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5c8e-129">-Confirm</span></span>
<span data-ttu-id="f5c8e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c8e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c8e-131">-WhatIf</span></span>
<span data-ttu-id="f5c8e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c8e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5c8e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c8e-134">CommonParameters</span></span>
<span data-ttu-id="f5c8e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c8e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c8e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c8e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c8e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5c8e-137">INPUTS</span></span>

### <span data-ttu-id="f5c8e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f5c8e-138">System.String</span></span>

### <span data-ttu-id="f5c8e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f5c8e-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="f5c8e-140">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f5c8e-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="f5c8e-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5c8e-141">OUTPUTS</span></span>

### <span data-ttu-id="f5c8e-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="f5c8e-142">System.Void</span></span>

## <span data-ttu-id="f5c8e-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5c8e-143">NOTES</span></span>

## <span data-ttu-id="f5c8e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5c8e-144">RELATED LINKS</span></span>

[<span data-ttu-id="f5c8e-145">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f5c8e-145">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="f5c8e-146">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f5c8e-146">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="f5c8e-147">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="f5c8e-147">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="f5c8e-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f5c8e-148">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


