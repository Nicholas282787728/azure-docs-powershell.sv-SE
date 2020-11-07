---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: a57707b10fc103e860fe579e75d7d4ad09cfd0e3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93928418"
---
# <span data-ttu-id="e3e47-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e3e47-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="e3e47-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3e47-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e47-103">Tar bort ett användar konto från en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="e3e47-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="e3e47-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3e47-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3e47-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3e47-105">DESCRIPTION</span></span>
<span data-ttu-id="e3e47-106">Cmdleten **Remove-AzBatchComputeNodeUser** tar bort ett användar konto från en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="e3e47-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="e3e47-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3e47-107">EXAMPLES</span></span>

### <span data-ttu-id="e3e47-108">Exempel 1: ta bort en användare från en datornod utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="e3e47-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="e3e47-109">Det här kommandot tar bort den användare som heter User14 från noden ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="e3e47-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="e3e47-110">Noden Compute finns i poolen Pool01.</span><span class="sxs-lookup"><span data-stu-id="e3e47-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="e3e47-111">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="e3e47-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e3e47-112">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e3e47-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e3e47-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3e47-113">PARAMETERS</span></span>

### <span data-ttu-id="e3e47-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e3e47-114">-BatchContext</span></span>
<span data-ttu-id="e3e47-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e3e47-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e3e47-116">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e3e47-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e3e47-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="e3e47-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e3e47-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="e3e47-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e3e47-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e3e47-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e3e47-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="e3e47-120">-ComputeNodeId</span></span>
<span data-ttu-id="e3e47-121">Anger ID för den datornod som cmdleten tar bort användar kontot för.</span><span class="sxs-lookup"><span data-stu-id="e3e47-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e47-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e47-122">-DefaultProfile</span></span>
<span data-ttu-id="e3e47-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e3e47-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3e47-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3e47-124">-Name</span></span>
<span data-ttu-id="e3e47-125">Anger namnet på det användar konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e3e47-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="e3e47-126">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="e3e47-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e47-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="e3e47-127">-PoolId</span></span>
<span data-ttu-id="e3e47-128">Anger ID för den pool som innehåller den datornod som användar kontot ska tas bort på.</span><span class="sxs-lookup"><span data-stu-id="e3e47-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="e3e47-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e3e47-129">-Confirm</span></span>
<span data-ttu-id="e3e47-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e3e47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3e47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3e47-131">-WhatIf</span></span>
<span data-ttu-id="e3e47-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e3e47-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3e47-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e3e47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3e47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e47-134">CommonParameters</span></span>
<span data-ttu-id="e3e47-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3e47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e47-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3e47-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e47-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3e47-137">INPUTS</span></span>

### <span data-ttu-id="e3e47-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e3e47-138">System.String</span></span>

### <span data-ttu-id="e3e47-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e3e47-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="e3e47-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3e47-140">OUTPUTS</span></span>

### <span data-ttu-id="e3e47-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="e3e47-141">System.Void</span></span>

## <span data-ttu-id="e3e47-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3e47-142">NOTES</span></span>

## <span data-ttu-id="e3e47-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3e47-143">RELATED LINKS</span></span>

[<span data-ttu-id="e3e47-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="e3e47-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="e3e47-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e3e47-145">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="e3e47-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="e3e47-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


