---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099257"
---
# <span data-ttu-id="66a02-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="66a02-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="66a02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66a02-102">SYNOPSIS</span></span>
<span data-ttu-id="66a02-103">Startar ett nytt jobb som skapar en säkerhets kopia från en befintlig säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="66a02-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="66a02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66a02-104">SYNTAX</span></span>

### <span data-ttu-id="66a02-105">Tom (standard)</span><span class="sxs-lookup"><span data-stu-id="66a02-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="66a02-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="66a02-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66a02-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66a02-107">DESCRIPTION</span></span>
<span data-ttu-id="66a02-108">Cmdleten **Start-AzureStorSimpleDeviceBackupJob** startar ett nytt jobb med en säkerhets kopia från en befintlig säkerhets kopierings princip på en StorSimple-enhet.</span><span class="sxs-lookup"><span data-stu-id="66a02-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="66a02-109">Denna cmdlet skapar som standard en säkerhets kopia av en lokal ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="66a02-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="66a02-110">Om du vill skapa en säkerhets kopia av molnet anger du ett värde för CloudSnapshot för parametern *BackupType* .</span><span class="sxs-lookup"><span data-stu-id="66a02-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="66a02-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66a02-111">EXAMPLES</span></span>

### <span data-ttu-id="66a02-112">Exempel 1: skapa en lokal säkerhets kopia av ögonblicks bild</span><span class="sxs-lookup"><span data-stu-id="66a02-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="66a02-113">Det här kommandot skapar en lokal säkerhets kopia av den angivna princip-ID: t.</span><span class="sxs-lookup"><span data-stu-id="66a02-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="66a02-114">Det här kommandot startar jobbet och returnerar sedan ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="66a02-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="66a02-115">Använd cmdleten **Get-AzureStorSimpleTask** för att se status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="66a02-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="66a02-116">Exempel 2: skapa en säkerhets kopia av en moln ögonblicks bild och vänta tills den är klar</span><span class="sxs-lookup"><span data-stu-id="66a02-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="66a02-117">Det här kommandot skapar en säkerhets kopia av en moln ögonblicks bild för angivet princip-ID.</span><span class="sxs-lookup"><span data-stu-id="66a02-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="66a02-118">Det här kommandot anger parametern *WaitForComplete* så att kommandot slutför uppgiften och returnerar sedan ett **TaskStatusInfo** -objekt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="66a02-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="66a02-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66a02-119">PARAMETERS</span></span>

### <span data-ttu-id="66a02-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="66a02-120">-BackupPolicyId</span></span>
<span data-ttu-id="66a02-121">Anger ID för säkerhets kopierings principen som ska användas för att skapa säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="66a02-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

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

### <span data-ttu-id="66a02-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="66a02-122">-BackupType</span></span>
<span data-ttu-id="66a02-123">Anger säkerhets kopierings typen.</span><span class="sxs-lookup"><span data-stu-id="66a02-123">Specifies the backup type.</span></span>
<span data-ttu-id="66a02-124">Giltiga värden är: LocalSnapshot och CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="66a02-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a02-125">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="66a02-125">-DeviceName</span></span>
<span data-ttu-id="66a02-126">Anger namnet på den StorSimple-enhet som du vill starta säkerhets kopierings jobbet på.</span><span class="sxs-lookup"><span data-stu-id="66a02-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

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

### <span data-ttu-id="66a02-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="66a02-127">-Profile</span></span>
<span data-ttu-id="66a02-128">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="66a02-128">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="66a02-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="66a02-129">-WaitForComplete</span></span>
<span data-ttu-id="66a02-130">Anger att denna cmdlet väntar på att åtgärden ska slutföras innan den återfår kontroll till Windows PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="66a02-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="66a02-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a02-131">CommonParameters</span></span>
<span data-ttu-id="66a02-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a02-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a02-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a02-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a02-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66a02-134">INPUTS</span></span>

### <span data-ttu-id="66a02-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="66a02-135">None</span></span>

## <span data-ttu-id="66a02-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66a02-136">OUTPUTS</span></span>

### <span data-ttu-id="66a02-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="66a02-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="66a02-138">Denna cmdlet returnerar ett **TaskStatusInfo** -objekt om du anger parametern *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="66a02-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="66a02-139">Om du inte anger den parametern returnerar den ett **TaskResponse** -objekt.</span><span class="sxs-lookup"><span data-stu-id="66a02-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="66a02-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66a02-140">NOTES</span></span>

## <span data-ttu-id="66a02-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66a02-141">RELATED LINKS</span></span>

[<span data-ttu-id="66a02-142">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="66a02-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="66a02-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="66a02-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


