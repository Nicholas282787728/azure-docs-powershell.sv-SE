---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099326"
---
# <span data-ttu-id="b8c13-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b8c13-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="b8c13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8c13-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c13-103">Tar bort en åtkomst kontroll post från tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b8c13-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="b8c13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8c13-104">SYNTAX</span></span>

### <span data-ttu-id="b8c13-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="b8c13-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b8c13-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="b8c13-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b8c13-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8c13-107">DESCRIPTION</span></span>
<span data-ttu-id="b8c13-108">Cmdleten **Remove-AzureStorSimpleAccessControlRecord** tar bort en åtkomst kontroll post från tjänst konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="b8c13-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="b8c13-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8c13-109">EXAMPLES</span></span>

### <span data-ttu-id="b8c13-110">Exempel 1: ta bort en Access Controlaccess Control recordaccess-kontroll</span><span class="sxs-lookup"><span data-stu-id="b8c13-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="b8c13-111">Det här kommandot tar bort åtkomst kontroll posten med namnet Acr10.</span><span class="sxs-lookup"><span data-stu-id="b8c13-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="b8c13-112">Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c13-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="b8c13-113">Exempel 2: ta bort en Access Controlaccess kontroll post genom att använda pipelineAccess Controlaccess Controlaccess kontroll</span><span class="sxs-lookup"><span data-stu-id="b8c13-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="b8c13-114">Det här kommandot använder cmdleten **Get-AzureStorSimpleAccessControlRecord** för att hämta **AccessControlRecord** med namnet Acr10 och skickar sedan objektet till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b8c13-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b8c13-115">Kommandot startar åtgärden som tar bort **AccessControlRecord** -objektet och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c13-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="b8c13-116">Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.</span><span class="sxs-lookup"><span data-stu-id="b8c13-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="b8c13-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8c13-117">PARAMETERS</span></span>

### <span data-ttu-id="b8c13-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="b8c13-118">-ACR</span></span>
<span data-ttu-id="b8c13-119">Anger ett **AccessControlRecord** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b8c13-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="b8c13-120">För att få ett **AccessControlRecord** -objekt, Använd cmdleten **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="b8c13-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8c13-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="b8c13-121">-ACRName</span></span>
<span data-ttu-id="b8c13-122">Anger ett namn på åtkomst kontroll posten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="b8c13-122">Specifies a name of the access control record to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c13-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c13-123">-Force</span></span>
<span data-ttu-id="b8c13-124">Anger att du inte behöver bekräfta med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b8c13-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c13-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="b8c13-125">-Profile</span></span>
<span data-ttu-id="b8c13-126">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="b8c13-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="b8c13-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="b8c13-127">-WaitForComplete</span></span>
<span data-ttu-id="b8c13-128">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="b8c13-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8c13-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c13-129">CommonParameters</span></span>
<span data-ttu-id="b8c13-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c13-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c13-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c13-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c13-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8c13-132">INPUTS</span></span>

### <span data-ttu-id="b8c13-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b8c13-133">AccessControlRecord</span></span>
<span data-ttu-id="b8c13-134">Denna cmdlet accepterar ett **AccessControlRecord** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c13-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="b8c13-135">Ett **AccessControlRecord** -objekt innehåller följande fält:</span><span class="sxs-lookup"><span data-stu-id="b8c13-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="b8c13-136">**GlobalId** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="b8c13-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="b8c13-137">**InitiatorName** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="b8c13-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="b8c13-138">**InstanceID** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="b8c13-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="b8c13-139">**Namn** ( **sträng** )</span><span class="sxs-lookup"><span data-stu-id="b8c13-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="b8c13-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="b8c13-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="b8c13-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="b8c13-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="b8c13-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8c13-142">OUTPUTS</span></span>

### <span data-ttu-id="b8c13-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="b8c13-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="b8c13-144">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="b8c13-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="b8c13-145">Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b8c13-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="b8c13-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8c13-146">NOTES</span></span>

## <span data-ttu-id="b8c13-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8c13-147">RELATED LINKS</span></span>

[<span data-ttu-id="b8c13-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b8c13-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b8c13-149">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b8c13-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b8c13-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="b8c13-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="b8c13-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="b8c13-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


