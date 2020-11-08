---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: ce2a7c6d01af33de585d4ac8adef83d03dbd33bc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94100435"
---
# <span data-ttu-id="cea3a-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cea3a-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="cea3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cea3a-102">SYNOPSIS</span></span>
<span data-ttu-id="cea3a-103">Tar bort angiven gruppbearbetningssekvens.</span><span class="sxs-lookup"><span data-stu-id="cea3a-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="cea3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cea3a-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cea3a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cea3a-105">DESCRIPTION</span></span>
<span data-ttu-id="cea3a-106">Cmdleten **Remove-AzBatchPool** tar bort angiven Azure-grupppool.</span><span class="sxs-lookup"><span data-stu-id="cea3a-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="cea3a-107">Du uppmanas att bekräfta om du inte använder parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="cea3a-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="cea3a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cea3a-108">EXAMPLES</span></span>

### <span data-ttu-id="cea3a-109">Exempel 1: ta bort en grupppool utifrån pool-ID</span><span class="sxs-lookup"><span data-stu-id="cea3a-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="cea3a-110">Det här kommandot tar bort poolen med ID-nummer.</span><span class="sxs-lookup"><span data-stu-id="cea3a-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="cea3a-111">Användaren uppmanas att bekräfta innan borttagningen utförs.</span><span class="sxs-lookup"><span data-stu-id="cea3a-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="cea3a-112">Exempel 2: ta bort alla batchattribut per tvång</span><span class="sxs-lookup"><span data-stu-id="cea3a-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="cea3a-113">Det här kommandot tar bort alla batchattribut.</span><span class="sxs-lookup"><span data-stu-id="cea3a-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="cea3a-114">Eftersom *Force* -parametern finns ignoreras bekräftelse meddelandet.</span><span class="sxs-lookup"><span data-stu-id="cea3a-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="cea3a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cea3a-115">PARAMETERS</span></span>

### <span data-ttu-id="cea3a-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cea3a-116">-BatchContext</span></span>
<span data-ttu-id="cea3a-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cea3a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cea3a-118">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="cea3a-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cea3a-119">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="cea3a-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cea3a-120">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="cea3a-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cea3a-121">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cea3a-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cea3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea3a-122">-DefaultProfile</span></span>
<span data-ttu-id="cea3a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cea3a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cea3a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cea3a-124">-Force</span></span>
<span data-ttu-id="cea3a-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cea3a-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cea3a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="cea3a-126">-Id</span></span>
<span data-ttu-id="cea3a-127">Anger ID för poolen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="cea3a-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="cea3a-128">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="cea3a-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="cea3a-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cea3a-129">-Confirm</span></span>
<span data-ttu-id="cea3a-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cea3a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cea3a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cea3a-131">-WhatIf</span></span>
<span data-ttu-id="cea3a-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cea3a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cea3a-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cea3a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cea3a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea3a-134">CommonParameters</span></span>
<span data-ttu-id="cea3a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cea3a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea3a-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cea3a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea3a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cea3a-137">INPUTS</span></span>

### <span data-ttu-id="cea3a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cea3a-138">System.String</span></span>

### <span data-ttu-id="cea3a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cea3a-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cea3a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cea3a-140">OUTPUTS</span></span>

### <span data-ttu-id="cea3a-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="cea3a-141">System.Void</span></span>

## <span data-ttu-id="cea3a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cea3a-142">NOTES</span></span>

## <span data-ttu-id="cea3a-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cea3a-143">RELATED LINKS</span></span>

[<span data-ttu-id="cea3a-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="cea3a-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cea3a-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cea3a-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="cea3a-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="cea3a-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="cea3a-147">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="cea3a-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


