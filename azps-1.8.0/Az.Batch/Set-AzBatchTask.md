---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 6A6D6C7D-EED7-4AD4-ACE6-BFA64404455E
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchTask.md
ms.openlocfilehash: b49ab8a6a08802ec670fb605e707ae46c51ddab2
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755050"
---
# <span data-ttu-id="bd751-101">Set-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd751-101">Set-AzBatchTask</span></span>

## <span data-ttu-id="bd751-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd751-102">SYNOPSIS</span></span>
<span data-ttu-id="bd751-103">Uppdaterar egenskaperna för en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="bd751-103">Updates the properties of a task.</span></span>

## <span data-ttu-id="bd751-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd751-104">SYNTAX</span></span>

```
Set-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd751-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd751-105">DESCRIPTION</span></span>
<span data-ttu-id="bd751-106">Cmdleten **set-AzBatchTask** uppdaterar egenskaperna för en aktivitet i Azure Batch-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd751-106">The **Set-AzBatchTask** cmdlet updates the properties of a task in the Azure Batch service.</span></span>
<span data-ttu-id="bd751-107">Använd Get-AzBatchTask cmdlet för att hämta ett **PSCloudTask** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bd751-107">Use the Get-AzBatchTask cmdlet to get a **PSCloudTask** object.</span></span>
<span data-ttu-id="bd751-108">Ändra egenskaperna för objektet och Använd sedan aktuell cmdlet för att bekräfta ändringarna i kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd751-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="bd751-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd751-109">EXAMPLES</span></span>

### <span data-ttu-id="bd751-110">Exempel 1: uppdatera en aktivitet</span><span class="sxs-lookup"><span data-stu-id="bd751-110">Example 1: Update a task</span></span>
```
PS C:\>$Task = Get-AzBatchTask -JobId "Job16" -Id "Task22" -BatchContext $Context
PS C:\> $Constraints = New-Object Microsoft.Azure.Commands.Batch.Models.PSTaskConstraints -ArgumentList @([TimeSpan}::FromDays(5), [TimeSpan]::FromDays(2), 3)
PS C:\> $Task.Constraints = $Constraints
PS C:\> Set-AzBatchTask -Task $Task -BatchContext $Context
```

<span data-ttu-id="bd751-111">Det första kommandot får en aktivitet genom att använda **Get-AzBatchTask** och lagrar den sedan i $Task variabel.</span><span class="sxs-lookup"><span data-stu-id="bd751-111">The first command gets a task by using **Get-AzBatchTask** , and then stores it in the $Task variable.</span></span>
<span data-ttu-id="bd751-112">Nästa två kommandon ändrar aktivitetens villkor i $Task.</span><span class="sxs-lookup"><span data-stu-id="bd751-112">The next two commands modify the constraints of the task in $Task.</span></span>
<span data-ttu-id="bd751-113">Det sista kommandot uppdaterar kommando tjänsten för att matcha det lokala objektet i $Task.</span><span class="sxs-lookup"><span data-stu-id="bd751-113">The final command updates the Batch service to match the local object in $Task.</span></span>

## <span data-ttu-id="bd751-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd751-114">PARAMETERS</span></span>

### <span data-ttu-id="bd751-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bd751-115">-BatchContext</span></span>
<span data-ttu-id="bd751-116">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd751-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bd751-117">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bd751-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bd751-118">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKeys cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="bd751-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bd751-119">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="bd751-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bd751-120">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bd751-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bd751-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd751-121">-DefaultProfile</span></span>
<span data-ttu-id="bd751-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd751-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd751-123">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="bd751-123">-Task</span></span>
<span data-ttu-id="bd751-124">Anger den **PSCloudTask** som den här cmdleten uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="bd751-124">Specifies the **PSCloudTask** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd751-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd751-125">CommonParameters</span></span>
<span data-ttu-id="bd751-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd751-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd751-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd751-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd751-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd751-128">INPUTS</span></span>

### <span data-ttu-id="bd751-129">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="bd751-129">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="bd751-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bd751-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="bd751-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd751-131">OUTPUTS</span></span>

### <span data-ttu-id="bd751-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="bd751-132">System.Void</span></span>

## <span data-ttu-id="bd751-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd751-133">NOTES</span></span>

## <span data-ttu-id="bd751-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd751-134">RELATED LINKS</span></span>

[<span data-ttu-id="bd751-135">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd751-135">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="bd751-136">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bd751-136">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="bd751-137">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd751-137">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="bd751-138">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd751-138">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="bd751-139">Stopp-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="bd751-139">Stop-AzBatchTask</span></span>](./Stop-AzBatchTask.md)

[<span data-ttu-id="bd751-140">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="bd751-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


