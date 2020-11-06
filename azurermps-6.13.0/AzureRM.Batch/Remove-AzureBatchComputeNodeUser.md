---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: e4ca1d8fe8db34579a8442ed77ce70d320947a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578991"
---
# <span data-ttu-id="afcc2-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="afcc2-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="afcc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="afcc2-102">SYNOPSIS</span></span>
<span data-ttu-id="afcc2-103">Tar bort ett användar konto från en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="afcc2-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afcc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="afcc2-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afcc2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="afcc2-105">DESCRIPTION</span></span>
<span data-ttu-id="afcc2-106">Cmdleten **Remove-AzureBatchComputeNodeUser** tar bort ett användar konto från en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="afcc2-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="afcc2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="afcc2-107">EXAMPLES</span></span>

### <span data-ttu-id="afcc2-108">Exempel 1: ta bort en användare från en datornod utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="afcc2-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="afcc2-109">Det här kommandot tar bort den användare som heter User14 från noden ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="afcc2-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="afcc2-110">Noden Compute finns i poolen Pool01.</span><span class="sxs-lookup"><span data-stu-id="afcc2-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="afcc2-111">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="afcc2-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="afcc2-112">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="afcc2-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="afcc2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="afcc2-113">PARAMETERS</span></span>

### <span data-ttu-id="afcc2-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="afcc2-114">-BatchContext</span></span>
<span data-ttu-id="afcc2-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="afcc2-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="afcc2-116">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="afcc2-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="afcc2-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="afcc2-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="afcc2-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="afcc2-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="afcc2-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="afcc2-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="afcc2-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="afcc2-120">-ComputeNodeId</span></span>
<span data-ttu-id="afcc2-121">Anger ID för den datornod som cmdleten tar bort användar kontot för.</span><span class="sxs-lookup"><span data-stu-id="afcc2-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="afcc2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afcc2-122">-DefaultProfile</span></span>
<span data-ttu-id="afcc2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="afcc2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afcc2-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="afcc2-124">-Name</span></span>
<span data-ttu-id="afcc2-125">Anger namnet på det användar konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="afcc2-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="afcc2-126">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="afcc2-126">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="afcc2-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="afcc2-127">-PoolId</span></span>
<span data-ttu-id="afcc2-128">Anger ID för den pool som innehåller den datornod som användar kontot ska tas bort på.</span><span class="sxs-lookup"><span data-stu-id="afcc2-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="afcc2-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="afcc2-129">-Confirm</span></span>
<span data-ttu-id="afcc2-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="afcc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afcc2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afcc2-131">-WhatIf</span></span>
<span data-ttu-id="afcc2-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="afcc2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afcc2-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="afcc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afcc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afcc2-134">CommonParameters</span></span>
<span data-ttu-id="afcc2-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afcc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afcc2-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afcc2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afcc2-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="afcc2-137">INPUTS</span></span>

### <span data-ttu-id="afcc2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="afcc2-138">System.String</span></span>

### <span data-ttu-id="afcc2-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="afcc2-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="afcc2-140">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="afcc2-140">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="afcc2-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="afcc2-141">OUTPUTS</span></span>

### <span data-ttu-id="afcc2-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="afcc2-142">System.Void</span></span>

## <span data-ttu-id="afcc2-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="afcc2-143">NOTES</span></span>

## <span data-ttu-id="afcc2-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="afcc2-144">RELATED LINKS</span></span>

[<span data-ttu-id="afcc2-145">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="afcc2-145">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="afcc2-146">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="afcc2-146">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="afcc2-147">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="afcc2-147">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


