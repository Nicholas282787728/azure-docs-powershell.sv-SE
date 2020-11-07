---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756000"
---
# <span data-ttu-id="406aa-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="406aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="406aa-102">SYNOPSIS</span></span>
<span data-ttu-id="406aa-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="406aa-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="406aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="406aa-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="406aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="406aa-105">DESCRIPTION</span></span>
<span data-ttu-id="406aa-106">Cmdleten **Remove-AzureBatchJobSchedule** tar bort ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="406aa-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="406aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="406aa-107">EXAMPLES</span></span>

## <span data-ttu-id="406aa-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="406aa-108">PARAMETERS</span></span>

### <span data-ttu-id="406aa-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="406aa-109">-BatchContext</span></span>
<span data-ttu-id="406aa-110">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="406aa-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="406aa-111">Använd Get-AzureRmBatchAccountKeys cmdlet för att få ett **BatchAccountContext** -objekt som innehåller åtkomst nycklar för prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="406aa-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="406aa-112">-Force</span><span class="sxs-lookup"><span data-stu-id="406aa-112">-Force</span></span>
<span data-ttu-id="406aa-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="406aa-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="406aa-114">-ID</span><span class="sxs-lookup"><span data-stu-id="406aa-114">-Id</span></span>
<span data-ttu-id="406aa-115">Anger ID för den fin planering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="406aa-115">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="406aa-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="406aa-116">-Confirm</span></span>
<span data-ttu-id="406aa-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="406aa-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406aa-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406aa-118">-WhatIf</span></span>
<span data-ttu-id="406aa-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="406aa-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="406aa-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="406aa-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406aa-121">-DefaultProfile</span></span>
<span data-ttu-id="406aa-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="406aa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="406aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406aa-123">CommonParameters</span></span>
<span data-ttu-id="406aa-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="406aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406aa-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="406aa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406aa-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="406aa-126">INPUTS</span></span>

### <span data-ttu-id="406aa-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="406aa-127">BatchAccountContext</span></span>
<span data-ttu-id="406aa-128">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="406aa-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="406aa-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="406aa-129">OUTPUTS</span></span>

## <span data-ttu-id="406aa-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="406aa-130">NOTES</span></span>

## <span data-ttu-id="406aa-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="406aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="406aa-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="406aa-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="406aa-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="406aa-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="406aa-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="406aa-137">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="406aa-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


