---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 59a906420e2326564e779c9358e07a5003946b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755548"
---
# <span data-ttu-id="79700-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="79700-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="79700-102">SYNOPSIS</span></span>
<span data-ttu-id="79700-103">Tar bort ett batchjobb.</span><span class="sxs-lookup"><span data-stu-id="79700-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79700-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="79700-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79700-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="79700-105">DESCRIPTION</span></span>
<span data-ttu-id="79700-106">Cmdleten **Remove-AzureBatchJobSchedule** tar bort ett Azure Batch-schema.</span><span class="sxs-lookup"><span data-stu-id="79700-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="79700-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="79700-107">EXAMPLES</span></span>

## <span data-ttu-id="79700-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="79700-108">PARAMETERS</span></span>

### <span data-ttu-id="79700-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="79700-109">-BatchContext</span></span>
<span data-ttu-id="79700-110">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="79700-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="79700-111">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="79700-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="79700-112">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="79700-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="79700-113">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="79700-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="79700-114">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="79700-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="79700-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79700-115">-DefaultProfile</span></span>
<span data-ttu-id="79700-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="79700-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79700-117">-Force</span><span class="sxs-lookup"><span data-stu-id="79700-117">-Force</span></span>
<span data-ttu-id="79700-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="79700-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="79700-119">-ID</span><span class="sxs-lookup"><span data-stu-id="79700-119">-Id</span></span>
<span data-ttu-id="79700-120">Anger ID för den fin planering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="79700-120">Specifies the ID of the job schedule to remove.</span></span>

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

### <span data-ttu-id="79700-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="79700-121">-Confirm</span></span>
<span data-ttu-id="79700-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="79700-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79700-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79700-123">-WhatIf</span></span>
<span data-ttu-id="79700-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="79700-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79700-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="79700-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79700-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79700-126">CommonParameters</span></span>
<span data-ttu-id="79700-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79700-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79700-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79700-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79700-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="79700-129">INPUTS</span></span>

### <span data-ttu-id="79700-130">System. String</span><span class="sxs-lookup"><span data-stu-id="79700-130">System.String</span></span>

### <span data-ttu-id="79700-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="79700-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="79700-132">Parametrar: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79700-132">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="79700-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="79700-133">OUTPUTS</span></span>

### <span data-ttu-id="79700-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="79700-134">System.Void</span></span>

## <span data-ttu-id="79700-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="79700-135">NOTES</span></span>

## <span data-ttu-id="79700-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="79700-136">RELATED LINKS</span></span>

[<span data-ttu-id="79700-137">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-137">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="79700-138">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-138">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="79700-139">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-139">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="79700-140">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-140">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="79700-141">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-141">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="79700-142">Stopp-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="79700-142">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


