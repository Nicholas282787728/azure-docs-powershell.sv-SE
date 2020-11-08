---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 47650E39-758C-4D3C-9653-B70576CA0979
online version: ''
schema: 2.0.0
ms.openlocfilehash: a93791e3184fcabacbf90caebcb2170746922b36
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099697"
---
# <span data-ttu-id="ae71d-101">Remove-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="ae71d-101">Remove-AzureStorSimpleDeviceBackup</span></span>

## <span data-ttu-id="ae71d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae71d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae71d-103">Tar bort ett säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-103">Deletes a backup object.</span></span>

## <span data-ttu-id="ae71d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae71d-104">SYNTAX</span></span>

### <span data-ttu-id="ae71d-105">IdentifyById (standard)</span><span class="sxs-lookup"><span data-stu-id="ae71d-105">IdentifyById (Default)</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupId <String> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae71d-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="ae71d-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleDeviceBackup -DeviceName <String> -Backup <Backup> [-Force] [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae71d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae71d-107">DESCRIPTION</span></span>
<span data-ttu-id="ae71d-108">Cmdleten **Remove-AzureStorSimpleDeviceBackup** tar bort ett enda säkerhets kopie objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-108">The **Remove-AzureStorSimpleDeviceBackup** cmdlet deletes a single backup object.</span></span>
<span data-ttu-id="ae71d-109">Om du försöker ta bort en säkerhets kopia som redan har tagits bort returnerar denna cmdlet ett fel.</span><span class="sxs-lookup"><span data-stu-id="ae71d-109">If you attempt to delete a backup that has already been deleted, this cmdlet returns an error.</span></span>

## <span data-ttu-id="ae71d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae71d-110">EXAMPLES</span></span>

### <span data-ttu-id="ae71d-111">Exempel 1: ta bort en säkerhets kopia för en enhet</span><span class="sxs-lookup"><span data-stu-id="ae71d-111">Example 1: Remove a backup for a device</span></span>
```
PS C:\>Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId "dcb5c991-0485-400f-8d0a-03a1341ee989" -Force
The remove job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId 6c73aff2-f5a1-4b5e-
9a4e-857e128dc216 for tracking the job status
```

<span data-ttu-id="ae71d-112">Det här kommandot tar bort den säkerhets kopia som har angivet ID för enheten som heter Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="ae71d-112">This command removes the backup that has the specified ID for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="ae71d-113">Kommandot startar åtgärden som tar bort **säkerhetskopierade** objekt och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-113">The command starts the operation that removes the **Backup** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="ae71d-114">Använd cmdleten **Get-AzureStorSimpleTask** för att se uppgiftens status.</span><span class="sxs-lookup"><span data-stu-id="ae71d-114">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="ae71d-115">Exempel 2: ta bort den första säkerhets kopian för en enhet med hjälp av dess ID</span><span class="sxs-lookup"><span data-stu-id="ae71d-115">Example 2: Remove the first backup for a device by using its ID</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupId $Backup[0].InstanceId -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 53a656c3-c082-4e1f-afb7-bff3db45c791
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f4411f38d07f68b88095682dbeedd9e9
```

<span data-ttu-id="ae71d-116">Det första kommandot får säkerhets kopiorna för enheten som heter Contoso63-AppVm och lagrar dem sedan i $Backup variabel.</span><span class="sxs-lookup"><span data-stu-id="ae71d-116">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="ae71d-117">Det andra kommandot tar bort en säkerhets kopia från enheten med namnet Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="ae71d-117">The second command deletes a backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="ae71d-118">Kommandot använder standard punkt notation för att referera till **InstanceID** -egenskapen för det första elementet i $Backup matrisen.</span><span class="sxs-lookup"><span data-stu-id="ae71d-118">The command uses standard dot notation to refer to the **InstanceId** property of the first element of the $Backup array.</span></span>
<span data-ttu-id="ae71d-119">Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-119">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="ae71d-120">Exempel 3: ta bort den första säkerhets kopian för en enhet med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="ae71d-120">Example 3: Remove the first backup for a device by using the pipeline</span></span>
```
PS C:\>$Backup = Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -WaitForComplete
PS C:\> $Backup[0] | Remove-AzureStorSimpleDeviceBackup -DeviceName "Contoso-AppVm" -Force -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 48059fd8-e355-4b91-9385-630d24f31df6
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e1753f3bf68e6e44ab719436b5111e41
```

<span data-ttu-id="ae71d-121">Det första kommandot får säkerhets kopiorna för enheten som heter Contoso63-AppVm och lagrar dem sedan i $Backup variabel.</span><span class="sxs-lookup"><span data-stu-id="ae71d-121">The first command gets the backups for the device named Contoso63-AppVm, and then stores them in the $Backup variable.</span></span>

<span data-ttu-id="ae71d-122">Det andra kommandot skickar det första objektet som lagras i $Backup matris till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae71d-122">The second command passes the first object stored in the $Backup array to the current cmdlet.</span></span>
<span data-ttu-id="ae71d-123">Denna cmdlet tar bort den säkerhets kopian från enheten med namnet Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="ae71d-123">That cmdlet deletes that backup from the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="ae71d-124">Det här kommandot anger parametern *WaitForComplete* och därför väntar du tills åtgärden är slutförd och returnerar sedan ett **TaskStatusInfo** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-124">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="ae71d-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae71d-125">PARAMETERS</span></span>

### <span data-ttu-id="ae71d-126">-Säkerhets kopiering</span><span class="sxs-lookup"><span data-stu-id="ae71d-126">-Backup</span></span>
<span data-ttu-id="ae71d-127">Anger det **säkerhetskopierade** objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ae71d-127">Specifies the **Backup** object to delete.</span></span>
<span data-ttu-id="ae71d-128">Använd cmdleten **Get-AzureStorSimpleDeviceBackup** för att få ett **säkerhets kopie** objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-128">To obtain a **Backup** object, use the **Get-AzureStorSimpleDeviceBackup** cmdlet.</span></span>

```yaml
Type: Backup
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae71d-129">-BackupId</span><span class="sxs-lookup"><span data-stu-id="ae71d-129">-BackupId</span></span>
<span data-ttu-id="ae71d-130">Anger instans-ID för en säkerhets kopia som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ae71d-130">Specifies the instance ID of a backup to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae71d-131">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="ae71d-131">-DeviceName</span></span>
<span data-ttu-id="ae71d-132">Anger namnet på den StorSimple-enhet där du vill ta bort en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="ae71d-132">Specifies the name of the StorSimple device on which to delete a backup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae71d-133">-Force</span><span class="sxs-lookup"><span data-stu-id="ae71d-133">-Force</span></span>
<span data-ttu-id="ae71d-134">Anger att du inte behöver bekräfta med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae71d-134">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="ae71d-135">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae71d-135">-Profile</span></span>
<span data-ttu-id="ae71d-136">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="ae71d-136">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ae71d-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ae71d-137">-WaitForComplete</span></span>
<span data-ttu-id="ae71d-138">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="ae71d-138">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ae71d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae71d-139">CommonParameters</span></span>
<span data-ttu-id="ae71d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae71d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae71d-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae71d-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae71d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae71d-142">INPUTS</span></span>

### <span data-ttu-id="ae71d-143">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="ae71d-143">Backup</span></span>

## <span data-ttu-id="ae71d-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae71d-144">OUTPUTS</span></span>

### <span data-ttu-id="ae71d-145">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="ae71d-145">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="ae71d-146">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* om du inte anger den parametern, returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ae71d-146">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="ae71d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae71d-147">NOTES</span></span>

## <span data-ttu-id="ae71d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae71d-148">RELATED LINKS</span></span>

[<span data-ttu-id="ae71d-149">Get-AzureStorSimpleDeviceBackup</span><span class="sxs-lookup"><span data-stu-id="ae71d-149">Get-AzureStorSimpleDeviceBackup</span></span>](./Get-AzureStorSimpleDeviceBackup.md)


