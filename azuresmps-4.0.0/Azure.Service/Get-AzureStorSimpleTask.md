---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093278"
---
# <span data-ttu-id="63140-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="63140-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="63140-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63140-102">SYNOPSIS</span></span>
<span data-ttu-id="63140-103">Status för en aktivitet på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="63140-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="63140-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63140-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63140-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63140-105">DESCRIPTION</span></span>
<span data-ttu-id="63140-106">Cmdleten **Get-AzureStorSimpleTask** returnerar statusen för en aktivitet som körs asynkront på en Azure StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="63140-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="63140-107">När du hanterar en StorSimple-enhet kan de flesta åtgärder för att skapa, läsa, uppdatera och ta bort vara asynkront.</span><span class="sxs-lookup"><span data-stu-id="63140-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="63140-108">Windows PowerShell returnerar en **TaskId**.</span><span class="sxs-lookup"><span data-stu-id="63140-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="63140-109">Använd ID för att få aktivitetens aktuella status.</span><span class="sxs-lookup"><span data-stu-id="63140-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="63140-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63140-110">EXAMPLES</span></span>

### <span data-ttu-id="63140-111">Exempel 1: få statusen för en uppgift</span><span class="sxs-lookup"><span data-stu-id="63140-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="63140-112">Det här kommandot får statusen för den aktivitet som har angivet ID.</span><span class="sxs-lookup"><span data-stu-id="63140-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="63140-113">Resultatet visar att aktiviteten har statusen slutförd och att resultatet lyckades.</span><span class="sxs-lookup"><span data-stu-id="63140-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="63140-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63140-114">PARAMETERS</span></span>

### <span data-ttu-id="63140-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="63140-115">-InstanceId</span></span>
<span data-ttu-id="63140-116">Anger ID för den aktivitet som cmdleten ska spåra status för.</span><span class="sxs-lookup"><span data-stu-id="63140-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63140-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="63140-117">-Profile</span></span>
<span data-ttu-id="63140-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="63140-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63140-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="63140-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63140-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63140-120">CommonParameters</span></span>
<span data-ttu-id="63140-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63140-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63140-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63140-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63140-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63140-123">INPUTS</span></span>

### <span data-ttu-id="63140-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="63140-124">None</span></span>

## <span data-ttu-id="63140-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63140-125">OUTPUTS</span></span>

### <span data-ttu-id="63140-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="63140-126">JobStatusInfo</span></span>
<span data-ttu-id="63140-127">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt som innehåller följande fält:</span><span class="sxs-lookup"><span data-stu-id="63140-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="63140-128">**Fel**.</span><span class="sxs-lookup"><span data-stu-id="63140-128">**Error**.</span></span>
<span data-ttu-id="63140-129">**ErrorDetails** , som innehåller **kod** och **meddelande**.</span><span class="sxs-lookup"><span data-stu-id="63140-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="63140-130">**TaskId**.</span><span class="sxs-lookup"><span data-stu-id="63140-130">**TaskId**.</span></span>
<span data-ttu-id="63140-131">**Sträng**.</span><span class="sxs-lookup"><span data-stu-id="63140-131">**String**.</span></span>
<span data-ttu-id="63140-132">ID för den uppgift vars status returneras.</span><span class="sxs-lookup"><span data-stu-id="63140-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="63140-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="63140-133">**TaskSteps**.</span></span>
<span data-ttu-id="63140-134">**Ilist \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="63140-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="63140-135">Varje **TaskStep** -objekt innehåller **detaljerad** , **ErrorCode** , **meddelande** , **resultat** och **status**.</span><span class="sxs-lookup"><span data-stu-id="63140-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="63140-136">**Resultat**.</span><span class="sxs-lookup"><span data-stu-id="63140-136">**Result**.</span></span>
<span data-ttu-id="63140-137">**TaskResult** , som innehåller aktivitetens övergripande resultat.</span><span class="sxs-lookup"><span data-stu-id="63140-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="63140-138">Giltiga värden är: misslyckades, lyckades, PartialSuccess, annullerade och ogiltiga.</span><span class="sxs-lookup"><span data-stu-id="63140-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="63140-139">**Status**.</span><span class="sxs-lookup"><span data-stu-id="63140-139">**Status**.</span></span>
<span data-ttu-id="63140-140">**TaskStatus** , som innehåller aktivitetens övergripande kör status.</span><span class="sxs-lookup"><span data-stu-id="63140-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="63140-141">Giltiga värden är: InProgress, ogiltigt och slutfört.</span><span class="sxs-lookup"><span data-stu-id="63140-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="63140-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="63140-142">**TaskResult**.</span></span>
<span data-ttu-id="63140-143">**TaskResult** , ett värde som beräknas baserat på **resultat** och **status**.</span><span class="sxs-lookup"><span data-stu-id="63140-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="63140-144">Giltiga värden är: misslyckad, lyckad, pågående, PartialSuccess, avbruten och ogiltig.</span><span class="sxs-lookup"><span data-stu-id="63140-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="63140-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63140-145">NOTES</span></span>

## <span data-ttu-id="63140-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63140-146">RELATED LINKS</span></span>

