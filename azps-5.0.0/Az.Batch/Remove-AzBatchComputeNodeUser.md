---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: 52fea755708645173a5f0f3429591a384ec63b01
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270301"
---
# <span data-ttu-id="ed4c9-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ed4c9-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="ed4c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed4c9-103">Tar bort ett användar konto från en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="ed4c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed4c9-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed4c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed4c9-106">Cmdleten **Remove-AzBatchComputeNodeUser** tar bort ett användar konto från en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="ed4c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed4c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed4c9-108">Exempel 1: ta bort en användare från en datornod utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="ed4c9-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="ed4c9-109">Det här kommandot tar bort den användare som heter User14 från noden ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="ed4c9-110">Noden Compute finns i poolen Pool01.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="ed4c9-111">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="ed4c9-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="ed4c9-112">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="ed4c9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed4c9-113">PARAMETERS</span></span>

### <span data-ttu-id="ed4c9-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ed4c9-114">-BatchContext</span></span>
<span data-ttu-id="ed4c9-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ed4c9-116">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ed4c9-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ed4c9-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ed4c9-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ed4c9-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ed4c9-120">-ComputeNodeId</span></span>
<span data-ttu-id="ed4c9-121">Anger ID för den datornod som cmdleten tar bort användar kontot för.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="ed4c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed4c9-122">-DefaultProfile</span></span>
<span data-ttu-id="ed4c9-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed4c9-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed4c9-124">-Name</span></span>
<span data-ttu-id="ed4c9-125">Anger namnet på det användar konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="ed4c9-126">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ed4c9-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ed4c9-127">-PoolId</span></span>
<span data-ttu-id="ed4c9-128">Anger ID för den pool som innehåller den datornod som användar kontot ska tas bort på.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="ed4c9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed4c9-129">-Confirm</span></span>
<span data-ttu-id="ed4c9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed4c9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed4c9-131">-WhatIf</span></span>
<span data-ttu-id="ed4c9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed4c9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed4c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed4c9-134">CommonParameters</span></span>
<span data-ttu-id="ed4c9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed4c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed4c9-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed4c9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed4c9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed4c9-137">INPUTS</span></span>

### <span data-ttu-id="ed4c9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ed4c9-138">System.String</span></span>

### <span data-ttu-id="ed4c9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ed4c9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ed4c9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed4c9-140">OUTPUTS</span></span>

### <span data-ttu-id="ed4c9-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="ed4c9-141">System.Void</span></span>

## <span data-ttu-id="ed4c9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed4c9-142">NOTES</span></span>

## <span data-ttu-id="ed4c9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed4c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed4c9-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="ed4c9-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="ed4c9-145">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed4c9-145">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ed4c9-146">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="ed4c9-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)