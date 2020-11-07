---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747432"
---
# <span data-ttu-id="8031c-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8031c-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="8031c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8031c-102">SYNOPSIS</span></span>
<span data-ttu-id="8031c-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="8031c-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="8031c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8031c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8031c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8031c-105">DESCRIPTION</span></span>
<span data-ttu-id="8031c-106">Cmdleten **Get-AzRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="8031c-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="8031c-107">Ställ in valv kontexten med hjälp av Set-AzRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8031c-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8031c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8031c-108">EXAMPLES</span></span>

### <span data-ttu-id="8031c-109">Exempel 1: Hämta alla pågående jobb</span><span class="sxs-lookup"><span data-stu-id="8031c-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="8031c-110">Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.</span><span class="sxs-lookup"><span data-stu-id="8031c-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="8031c-111">Det andra kommandot visar det första objektet i $Joblist matrisen.</span><span class="sxs-lookup"><span data-stu-id="8031c-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="8031c-112">Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna</span><span class="sxs-lookup"><span data-stu-id="8031c-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="8031c-113">Det här kommandot får inte jobbet från den förra veckan i valvet.</span><span class="sxs-lookup"><span data-stu-id="8031c-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="8031c-114">Parametern *från* anger en tid sju dagar tidigare angiven i UTC.</span><span class="sxs-lookup"><span data-stu-id="8031c-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="8031c-115">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="8031c-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="8031c-116">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="8031c-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="8031c-117">Exempel 3: få ett pågående jobb och vänta tills det är färdigt</span><span class="sxs-lookup"><span data-stu-id="8031c-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="8031c-118">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="8031c-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="8031c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8031c-119">PARAMETERS</span></span>

### <span data-ttu-id="8031c-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8031c-120">-BackupManagementType</span></span>
<span data-ttu-id="8031c-121">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="8031c-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="8031c-122">För närvarande stöds endast AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="8031c-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8031c-123">-DefaultProfile</span></span>
<span data-ttu-id="8031c-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8031c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8031c-125">-Från</span><span class="sxs-lookup"><span data-stu-id="8031c-125">-From</span></span>
<span data-ttu-id="8031c-126">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8031c-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8031c-127">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8031c-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8031c-128">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8031c-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="8031c-129">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="8031c-129">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-130">-Jobb</span><span class="sxs-lookup"><span data-stu-id="8031c-130">-Job</span></span>
<span data-ttu-id="8031c-131">Anger namnet på det säkerhets kopierings jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="8031c-131">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="8031c-132">-JobId</span></span>
<span data-ttu-id="8031c-133">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8031c-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="8031c-134">ID är InstanceId-egenskapen för ett **AzureRmRecoveryServicesBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8031c-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="8031c-135">För att få ett **AzureRmRecoveryServicesBackupJob** -objekt, Använd Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="8031c-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-136">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="8031c-136">-Operation</span></span>
<span data-ttu-id="8031c-137">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8031c-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8031c-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8031c-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8031c-139">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="8031c-139">Backup</span></span>
- <span data-ttu-id="8031c-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="8031c-140">ConfigureBackup</span></span>
- <span data-ttu-id="8031c-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="8031c-141">DeleteBackupData</span></span>
- <span data-ttu-id="8031c-142">Registrera dig</span><span class="sxs-lookup"><span data-stu-id="8031c-142">Register</span></span>
- <span data-ttu-id="8031c-143">Terställa</span><span class="sxs-lookup"><span data-stu-id="8031c-143">Restore</span></span>
- <span data-ttu-id="8031c-144">Låsa upp</span><span class="sxs-lookup"><span data-stu-id="8031c-144">UnProtect</span></span>
- <span data-ttu-id="8031c-145">Avregistrera</span><span class="sxs-lookup"><span data-stu-id="8031c-145">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-146">-Status</span><span class="sxs-lookup"><span data-stu-id="8031c-146">-Status</span></span>
<span data-ttu-id="8031c-147">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8031c-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8031c-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8031c-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8031c-149">Inaktive</span><span class="sxs-lookup"><span data-stu-id="8031c-149">InProgress</span></span>
- <span data-ttu-id="8031c-150">Startade</span><span class="sxs-lookup"><span data-stu-id="8031c-150">Failed</span></span>
- <span data-ttu-id="8031c-151">Annullerats</span><span class="sxs-lookup"><span data-stu-id="8031c-151">Cancelled</span></span>
- <span data-ttu-id="8031c-152">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="8031c-152">Cancelling</span></span>
- <span data-ttu-id="8031c-153">Rätta</span><span class="sxs-lookup"><span data-stu-id="8031c-153">Completed</span></span>
- <span data-ttu-id="8031c-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="8031c-154">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-155">-För att</span><span class="sxs-lookup"><span data-stu-id="8031c-155">-To</span></span>
<span data-ttu-id="8031c-156">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8031c-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8031c-157">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="8031c-157">The default value is the current system time.</span></span>
<span data-ttu-id="8031c-158">Om du anger den här parametern måste du också ange parametern *från* .</span><span class="sxs-lookup"><span data-stu-id="8031c-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="8031c-159">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="8031c-159">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8031c-160">-VaultId</span></span>
<span data-ttu-id="8031c-161">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="8031c-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8031c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8031c-162">CommonParameters</span></span>
<span data-ttu-id="8031c-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8031c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8031c-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8031c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8031c-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8031c-165">INPUTS</span></span>

### <span data-ttu-id="8031c-166">System. String</span><span class="sxs-lookup"><span data-stu-id="8031c-166">System.String</span></span>

## <span data-ttu-id="8031c-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8031c-167">OUTPUTS</span></span>

### <span data-ttu-id="8031c-168">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="8031c-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8031c-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8031c-169">NOTES</span></span>

## <span data-ttu-id="8031c-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8031c-170">RELATED LINKS</span></span>

[<span data-ttu-id="8031c-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="8031c-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="8031c-172">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8031c-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="8031c-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8031c-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


