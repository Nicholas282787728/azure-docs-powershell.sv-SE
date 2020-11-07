---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 668abe661eebfe600625ea85d5694838ef0e12f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757265"
---
# <span data-ttu-id="05947-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="05947-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="05947-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05947-102">SYNOPSIS</span></span>
<span data-ttu-id="05947-103">Tar bort ett användar konto från en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="05947-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05947-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05947-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05947-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05947-105">DESCRIPTION</span></span>
<span data-ttu-id="05947-106">Cmdleten **Remove-AzureBatchComputeNodeUser** tar bort ett användar konto från en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="05947-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="05947-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05947-107">EXAMPLES</span></span>

### <span data-ttu-id="05947-108">Exempel 1: ta bort en användare från en datornod utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="05947-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="05947-109">Det här kommandot tar bort den användare som heter User14 från noden ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="05947-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="05947-110">Noden Compute finns i poolen Pool01.</span><span class="sxs-lookup"><span data-stu-id="05947-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="05947-111">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="05947-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="05947-112">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="05947-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="05947-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05947-113">PARAMETERS</span></span>

### <span data-ttu-id="05947-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="05947-114">-BatchContext</span></span>
<span data-ttu-id="05947-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="05947-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="05947-116">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="05947-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="05947-117">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="05947-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="05947-118">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="05947-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="05947-119">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="05947-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="05947-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="05947-120">-ComputeNodeId</span></span>
<span data-ttu-id="05947-121">Anger ID för den datornod som cmdleten tar bort användar kontot för.</span><span class="sxs-lookup"><span data-stu-id="05947-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05947-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05947-122">-DefaultProfile</span></span>
<span data-ttu-id="05947-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05947-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05947-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="05947-124">-Name</span></span>
<span data-ttu-id="05947-125">Anger namnet på det användar konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="05947-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="05947-126">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="05947-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05947-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="05947-127">-PoolId</span></span>
<span data-ttu-id="05947-128">Anger ID för den pool som innehåller den datornod som användar kontot ska tas bort på.</span><span class="sxs-lookup"><span data-stu-id="05947-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="05947-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05947-129">-Confirm</span></span>
<span data-ttu-id="05947-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05947-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05947-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05947-131">-WhatIf</span></span>
<span data-ttu-id="05947-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05947-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05947-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05947-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05947-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05947-134">CommonParameters</span></span>
<span data-ttu-id="05947-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05947-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05947-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05947-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05947-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05947-137">INPUTS</span></span>

### <span data-ttu-id="05947-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="05947-138">BatchAccountContext</span></span>
<span data-ttu-id="05947-139">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="05947-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="05947-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05947-140">OUTPUTS</span></span>

## <span data-ttu-id="05947-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05947-141">NOTES</span></span>

## <span data-ttu-id="05947-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05947-142">RELATED LINKS</span></span>

[<span data-ttu-id="05947-143">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="05947-143">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="05947-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="05947-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="05947-145">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="05947-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


