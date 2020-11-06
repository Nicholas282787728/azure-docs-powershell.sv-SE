---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582524"
---
# <span data-ttu-id="0c3fd-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0c3fd-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="0c3fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3fd-103">Tar bort ett användar konto från en batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c3fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c3fd-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c3fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3fd-106">Cmdleten **Remove-AzureBatchComputeNodeUser** tar bort ett användar konto från en Azure Batch-datornod.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="0c3fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3fd-108">Exempel 1: ta bort en användare från en datornod utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="0c3fd-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="0c3fd-109">Det här kommandot tar bort den användare som heter User14 från noden ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="0c3fd-110">Noden Compute finns i poolen Pool01.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="0c3fd-111">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="0c3fd-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0c3fd-112">Därför uppmanas du inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0c3fd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c3fd-113">PARAMETERS</span></span>

### <span data-ttu-id="0c3fd-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0c3fd-114">-BatchContext</span></span>
<span data-ttu-id="0c3fd-115">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0c3fd-116">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0c3fd-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="0c3fd-117">-ComputeNodeId</span></span>
<span data-ttu-id="0c3fd-118">Anger ID för den datornod som cmdleten tar bort användar kontot för.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="0c3fd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c3fd-119">-Name</span></span>
<span data-ttu-id="0c3fd-120">Anger namnet på det användar konto som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="0c3fd-121">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-121">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="0c3fd-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0c3fd-122">-PoolId</span></span>
<span data-ttu-id="0c3fd-123">Anger ID för den pool som innehåller den datornod som användar kontot ska tas bort på.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="0c3fd-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c3fd-124">-Confirm</span></span>
<span data-ttu-id="0c3fd-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3fd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3fd-126">-WhatIf</span></span>
<span data-ttu-id="0c3fd-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3fd-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3fd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3fd-129">-DefaultProfile</span></span>
<span data-ttu-id="0c3fd-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c3fd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3fd-131">CommonParameters</span></span>
<span data-ttu-id="0c3fd-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c3fd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3fd-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3fd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3fd-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c3fd-134">INPUTS</span></span>

### <span data-ttu-id="0c3fd-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0c3fd-135">BatchAccountContext</span></span>
<span data-ttu-id="0c3fd-136">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0c3fd-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="0c3fd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c3fd-137">OUTPUTS</span></span>

## <span data-ttu-id="0c3fd-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c3fd-138">NOTES</span></span>

## <span data-ttu-id="0c3fd-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c3fd-139">RELATED LINKS</span></span>

[<span data-ttu-id="0c3fd-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0c3fd-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="0c3fd-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0c3fd-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0c3fd-142">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="0c3fd-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


