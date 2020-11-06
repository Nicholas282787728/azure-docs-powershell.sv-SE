---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchTask.md
ms.openlocfilehash: 6e6bb12aeb5b5d319b0997578991c87e91c81003
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577260"
---
# <span data-ttu-id="92252-101">Set-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92252-101">Set-AzureBatchTask</span></span>

## <span data-ttu-id="92252-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92252-102">SYNOPSIS</span></span>
<span data-ttu-id="92252-103">Uppdaterar egenskaperna för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="92252-103">Updates the properties of a task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92252-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92252-104">SYNTAX</span></span>

```
Set-AzureBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92252-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92252-105">DESCRIPTION</span></span>
<span data-ttu-id="92252-106">Cmdleten **set-AzureBatchTask** uppdaterar egenskaperna för en aktivitet i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="92252-106">The **Set-AzureBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="92252-107">Använd Get-AzureBatchTask cmdlet för att hämta ett **PSCloudTask** -objekt.</span><span class="sxs-lookup"><span data-stu-id="92252-107">Use the Get-AzureBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="92252-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="92252-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="92252-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92252-109">EXAMPLES</span></span>

### <span data-ttu-id="92252-110">Exempel 1: uppdatera en aktivitet</span><span class="sxs-lookup"><span data-stu-id="92252-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzureBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzureBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="92252-111">Det första kommandot får en aktivitet genom att använda **Get-AzureBatchTask** och lagrar den sedan i $Task variabel.</span><span class="sxs-lookup"><span data-stu-id="92252-111">The first command gets a task by using **Get-AzureBatchTask** , and then stores it in the $Task variable.</span></span>

<span data-ttu-id="92252-112">Nästa två kommandon ändrar aktivitetens villkor i $Task.</span><span class="sxs-lookup"><span data-stu-id="92252-112">The next two commands modify the constraints of the task in $Task.</span></span>

<span data-ttu-id="92252-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Task.</span><span class="sxs-lookup"><span data-stu-id="92252-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="92252-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92252-114">PARAMETERS</span></span>

### <span data-ttu-id="92252-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="92252-115">-BatchContext</span></span>
<span data-ttu-id="92252-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="92252-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="92252-117">Om du använder Get-AzureRmBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="92252-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="92252-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzureRmBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="92252-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="92252-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="92252-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="92252-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="92252-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="92252-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92252-121">-DefaultProfile</span></span>
<span data-ttu-id="92252-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92252-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92252-123">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="92252-123">-Task</span></span>
<span data-ttu-id="92252-124">Anger den **PSCloudTask** som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="92252-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: PSCloudTask
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92252-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92252-125">CommonParameters</span></span>
<span data-ttu-id="92252-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92252-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92252-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92252-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92252-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92252-128">INPUTS</span></span>

### <span data-ttu-id="92252-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="92252-129">BatchAccountContext</span></span>
<span data-ttu-id="92252-130">Parametern ' BatchContext ' godkänner värdet av typen ' BatchAccountContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="92252-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="92252-131">PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="92252-131">PSCloudTask</span></span>
<span data-ttu-id="92252-132">Parametern ' Task ' godkänner värdet av typen ' PSCloudTask ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="92252-132">Parameter 'Task' accepts value of type 'PSCloudTask' from the pipeline</span></span>

## <span data-ttu-id="92252-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92252-133">OUTPUTS</span></span>

## <span data-ttu-id="92252-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92252-134">NOTES</span></span>

## <span data-ttu-id="92252-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92252-135">RELATED LINKS</span></span>

[<span data-ttu-id="92252-136">Get-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92252-136">Get-AzureBatchTask</span></span>](./Get-AzureBatchTask.md)

[<span data-ttu-id="92252-137">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="92252-137">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="92252-138">New-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92252-138">New-AzureBatchTask</span></span>](./New-AzureBatchTask.md)

[<span data-ttu-id="92252-139">Remove-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92252-139">Remove-AzureBatchTask</span></span>](./Remove-AzureBatchTask.md)

[<span data-ttu-id="92252-140">Stopp-AzureBatchTask</span><span class="sxs-lookup"><span data-stu-id="92252-140">Stop-AzureBatchTask</span></span>](./Stop-AzureBatchTask.md)

[<span data-ttu-id="92252-141">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="92252-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


