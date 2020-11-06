---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578455"
---
# <span data-ttu-id="c97c0-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c97c0-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="c97c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c97c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c97c0-103">Tar bort angiven gruppbearbetningssekvens.</span><span class="sxs-lookup"><span data-stu-id="c97c0-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c97c0-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c97c0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c97c0-105">DESCRIPTION</span></span>
<span data-ttu-id="c97c0-106">Cmdleten **Remove-AzureBatchPool** tar bort angiven Azure-grupppool.</span><span class="sxs-lookup"><span data-stu-id="c97c0-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="c97c0-107">Du uppmanas att bekräfta om du inte använder parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="c97c0-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="c97c0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c97c0-108">EXAMPLES</span></span>

### <span data-ttu-id="c97c0-109">Exempel 1: ta bort en grupppool utifrån pool-ID</span><span class="sxs-lookup"><span data-stu-id="c97c0-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="c97c0-110">Det här kommandot tar bort poolen med ID-nummer.</span><span class="sxs-lookup"><span data-stu-id="c97c0-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="c97c0-111">Användaren uppmanas att bekräfta innan borttagningen utförs.</span><span class="sxs-lookup"><span data-stu-id="c97c0-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="c97c0-112">Exempel 2: ta bort alla batchattribut per tvång</span><span class="sxs-lookup"><span data-stu-id="c97c0-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="c97c0-113">Det här kommandot tar bort alla batchattribut.</span><span class="sxs-lookup"><span data-stu-id="c97c0-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="c97c0-114">Eftersom *Force* -parametern finns ignoreras bekräftelse meddelandet.</span><span class="sxs-lookup"><span data-stu-id="c97c0-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="c97c0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c97c0-115">PARAMETERS</span></span>

### <span data-ttu-id="c97c0-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c97c0-116">-BatchContext</span></span>
<span data-ttu-id="c97c0-117">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c97c0-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c97c0-118">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c97c0-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c97c0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c97c0-119">-Force</span></span>
<span data-ttu-id="c97c0-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c97c0-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c97c0-121">-ID</span><span class="sxs-lookup"><span data-stu-id="c97c0-121">-Id</span></span>
<span data-ttu-id="c97c0-122">Anger ID för poolen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c97c0-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="c97c0-123">Du kan inte ange jokertecken.</span><span class="sxs-lookup"><span data-stu-id="c97c0-123">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="c97c0-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c97c0-124">-Confirm</span></span>
<span data-ttu-id="c97c0-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c97c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c97c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c97c0-126">-WhatIf</span></span>
<span data-ttu-id="c97c0-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c97c0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c97c0-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c97c0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c97c0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97c0-129">-DefaultProfile</span></span>
<span data-ttu-id="c97c0-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c97c0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c97c0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97c0-131">CommonParameters</span></span>
<span data-ttu-id="c97c0-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97c0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97c0-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97c0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97c0-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c97c0-134">INPUTS</span></span>

### <span data-ttu-id="c97c0-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c97c0-135">BatchAccountContext</span></span>
<span data-ttu-id="c97c0-136">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c97c0-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="c97c0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c97c0-137">OUTPUTS</span></span>

## <span data-ttu-id="c97c0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c97c0-138">NOTES</span></span>

## <span data-ttu-id="c97c0-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c97c0-139">RELATED LINKS</span></span>

[<span data-ttu-id="c97c0-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c97c0-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c97c0-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c97c0-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c97c0-142">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c97c0-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="c97c0-143">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="c97c0-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


