---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 1EA57372-6FA5-45C9-94A1-50D53830FC10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchtask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchTask.md
ms.openlocfilehash: 8b84028bc9da854b5aa749867a8759b71d9f7b63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409840"
---
# <span data-ttu-id="d9e14-101">Stop-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9e14-101">Stop-AzBatchTask</span></span>

## <span data-ttu-id="d9e14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9e14-102">SYNOPSIS</span></span>
<span data-ttu-id="d9e14-103">Stoppar en batchuppgiften.</span><span class="sxs-lookup"><span data-stu-id="d9e14-103">Stops a Batch task.</span></span>

## <span data-ttu-id="d9e14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9e14-104">SYNTAX</span></span>

### <span data-ttu-id="d9e14-105">Et</span><span class="sxs-lookup"><span data-stu-id="d9e14-105">Id</span></span>
```
Stop-AzBatchTask [-JobId] <String> [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9e14-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9e14-106">InputObject</span></span>
```
Stop-AzBatchTask [-Task] <PSCloudTask> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9e14-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9e14-107">DESCRIPTION</span></span>
<span data-ttu-id="d9e14-108">Cmdleten **Stop-AzBatchTask** stoppar en Azure Batch-uppgift.</span><span class="sxs-lookup"><span data-stu-id="d9e14-108">The **Stop-AzBatchTask** cmdlet stops an Azure Batch task.</span></span>

## <span data-ttu-id="d9e14-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9e14-109">EXAMPLES</span></span>

### <span data-ttu-id="d9e14-110">Exempel 1: ta bort en batch-uppgift efter ID</span><span class="sxs-lookup"><span data-stu-id="d9e14-110">Example 1: Delete a Batch task by ID</span></span>
```
PS C:\>Stop-AzBatchTask -JobId "Job-000001" -Id "Task23" -BatchContext $Context
```

<span data-ttu-id="d9e14-111">Det här kommandot stoppar en aktivitet med ID-Task23 under det jobb som har ID-jobbet 000001.</span><span class="sxs-lookup"><span data-stu-id="d9e14-111">This command stops a task that has the ID Task23 under the job that has the ID Job-000001.</span></span>
<span data-ttu-id="d9e14-112">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d9e14-112">The command prompts you for confirmation.</span></span>
<span data-ttu-id="d9e14-113">Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.</span><span class="sxs-lookup"><span data-stu-id="d9e14-113">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="d9e14-114">Exempel 2: stoppa en batchprocess genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="d9e14-114">Example 2: Stop a Batch task by using the pipeline</span></span>
```
PS C:\>Get-AzBatchTask -JobId "Job-000001" -Id "Task26" -BatchContext $Context | Stop-AzBatchTask -BatchContext $Context
```

<span data-ttu-id="d9e14-115">Med det här kommandot får du den batch-uppgift som har det ID-Task26 i jobbet som har ID-jobbet 000001 genom att använda Get-AzBatchTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9e14-115">This command gets the Batch task that has the ID Task26 in the job that has the ID Job-000001 by using the Get-AzBatchTask cmdlet.</span></span>
<span data-ttu-id="d9e14-116">Kommandot skickar uppgiften till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="d9e14-116">The command passes that task to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d9e14-117">Kommandot stoppar uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d9e14-117">The command stops that task.</span></span>

## <span data-ttu-id="d9e14-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9e14-118">PARAMETERS</span></span>

### <span data-ttu-id="d9e14-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d9e14-119">-BatchContext</span></span>
<span data-ttu-id="d9e14-120">Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d9e14-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d9e14-121">Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d9e14-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d9e14-122">Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda.</span><span class="sxs-lookup"><span data-stu-id="d9e14-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d9e14-123">När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard.</span><span class="sxs-lookup"><span data-stu-id="d9e14-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d9e14-124">Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d9e14-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d9e14-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9e14-125">-DefaultProfile</span></span>
<span data-ttu-id="d9e14-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9e14-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9e14-127">-ID</span><span class="sxs-lookup"><span data-stu-id="d9e14-127">-Id</span></span>
<span data-ttu-id="d9e14-128">Anger ID för den aktivitet som cmdleten slutar.</span><span class="sxs-lookup"><span data-stu-id="d9e14-128">Specifies the ID of the task that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e14-129">-JobId</span><span class="sxs-lookup"><span data-stu-id="d9e14-129">-JobId</span></span>
<span data-ttu-id="d9e14-130">Anger ID för jobbet som innehåller uppgiften.</span><span class="sxs-lookup"><span data-stu-id="d9e14-130">Specifies the ID of the job that contains the task.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e14-131">-Aktivitets</span><span class="sxs-lookup"><span data-stu-id="d9e14-131">-Task</span></span>
<span data-ttu-id="d9e14-132">Anger den uppgift som denna cmdlet stoppar.</span><span class="sxs-lookup"><span data-stu-id="d9e14-132">Specifies the task that this cmdlet stops.</span></span>
<span data-ttu-id="d9e14-133">För att hämta ett **PSCloudTask** -objekt, Använd cmdleten Get-AzBatchTask.</span><span class="sxs-lookup"><span data-stu-id="d9e14-133">To obtain a **PSCloudTask** object, use the Get-AzBatchTask cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudTask
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9e14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9e14-134">CommonParameters</span></span>
<span data-ttu-id="d9e14-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9e14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9e14-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9e14-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9e14-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9e14-137">INPUTS</span></span>

### <span data-ttu-id="d9e14-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d9e14-138">System.String</span></span>

### <span data-ttu-id="d9e14-139">Microsoft.Azure.Commands.BatCH. Modeller. PSCloudTask</span><span class="sxs-lookup"><span data-stu-id="d9e14-139">Microsoft.Azure.Commands.Batch.Models.PSCloudTask</span></span>

### <span data-ttu-id="d9e14-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d9e14-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d9e14-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9e14-141">OUTPUTS</span></span>

### <span data-ttu-id="d9e14-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="d9e14-142">System.Void</span></span>

## <span data-ttu-id="d9e14-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9e14-143">NOTES</span></span>

## <span data-ttu-id="d9e14-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9e14-144">RELATED LINKS</span></span>

[<span data-ttu-id="d9e14-145">Get-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9e14-145">Get-AzBatchTask</span></span>](./Get-AzBatchTask.md)

[<span data-ttu-id="d9e14-146">New-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9e14-146">New-AzBatchTask</span></span>](./New-AzBatchTask.md)

[<span data-ttu-id="d9e14-147">Remove-AzBatchTask</span><span class="sxs-lookup"><span data-stu-id="d9e14-147">Remove-AzBatchTask</span></span>](./Remove-AzBatchTask.md)

[<span data-ttu-id="d9e14-148">Cmdlets för Azure Batch</span><span class="sxs-lookup"><span data-stu-id="d9e14-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
