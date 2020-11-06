---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 5e6555095563fd5c0589835b28ad293f395fffaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574238"
---
# <span data-ttu-id="62bb2-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="62bb2-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="62bb2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="62bb2-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="62bb2-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62bb2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62bb2-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62bb2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="62bb2-106">Cmdleten **Get-AzureRmRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="62bb2-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

<span data-ttu-id="62bb2-107">Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62bb2-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="62bb2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62bb2-108">EXAMPLES</span></span>

### <span data-ttu-id="62bb2-109">Exempel 1: Hämta alla pågående jobb</span><span class="sxs-lookup"><span data-stu-id="62bb2-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="62bb2-110">Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.</span><span class="sxs-lookup"><span data-stu-id="62bb2-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>

<span data-ttu-id="62bb2-111">Det andra kommandot visar det första objektet i $Joblist matrisen.</span><span class="sxs-lookup"><span data-stu-id="62bb2-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="62bb2-112">Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna</span><span class="sxs-lookup"><span data-stu-id="62bb2-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="62bb2-113">Det här kommandot får inte jobbet från den förra veckan i valvet.</span><span class="sxs-lookup"><span data-stu-id="62bb2-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="62bb2-114">Parametern *från* anger en tid sju dagar tidigare angiven i UTC.</span><span class="sxs-lookup"><span data-stu-id="62bb2-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="62bb2-115">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="62bb2-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="62bb2-116">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="62bb2-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="62bb2-117">Exempel 3: få ett pågående jobb och vänta tills det är färdigt</span><span class="sxs-lookup"><span data-stu-id="62bb2-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="62bb2-118">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="62bb2-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="62bb2-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62bb2-119">PARAMETERS</span></span>

### <span data-ttu-id="62bb2-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="62bb2-120">-BackupManagementType</span></span>
<span data-ttu-id="62bb2-121">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="62bb2-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="62bb2-122">För närvarande stöds endast AzureVM.</span><span class="sxs-lookup"><span data-stu-id="62bb2-122">Currently, only AzureVM is supported.</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bb2-123">-DefaultProfile</span></span>
<span data-ttu-id="62bb2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62bb2-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62bb2-125">-Från</span><span class="sxs-lookup"><span data-stu-id="62bb2-125">-From</span></span>
<span data-ttu-id="62bb2-126">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="62bb2-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="62bb2-127">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62bb2-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="62bb2-128">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="62bb2-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="62bb2-129">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="62bb2-129">Use UTC format for dates.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-130">-Jobb</span><span class="sxs-lookup"><span data-stu-id="62bb2-130">-Job</span></span>
<span data-ttu-id="62bb2-131">Anger namnet på det säkerhets kopierings jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="62bb2-131">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: JobBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="62bb2-132">-JobId</span></span>
<span data-ttu-id="62bb2-133">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="62bb2-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="62bb2-134">ID är InstanceId-egenskapen för ett **AzureRmRecoveryServicesBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62bb2-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="62bb2-135">För att få ett **AzureRmRecoveryServicesBackupJob** -objekt, Använd Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="62bb2-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-136">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="62bb2-136">-Operation</span></span>
<span data-ttu-id="62bb2-137">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="62bb2-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="62bb2-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="62bb2-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62bb2-139">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="62bb2-139">Backup</span></span>
- <span data-ttu-id="62bb2-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="62bb2-140">ConfigureBackup</span></span>
- <span data-ttu-id="62bb2-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="62bb2-141">DeleteBackupData</span></span>
- <span data-ttu-id="62bb2-142">Registrera dig</span><span class="sxs-lookup"><span data-stu-id="62bb2-142">Register</span></span>
- <span data-ttu-id="62bb2-143">Terställa</span><span class="sxs-lookup"><span data-stu-id="62bb2-143">Restore</span></span>
- <span data-ttu-id="62bb2-144">Låsa upp</span><span class="sxs-lookup"><span data-stu-id="62bb2-144">UnProtect</span></span>
- <span data-ttu-id="62bb2-145">Avregistrera</span><span class="sxs-lookup"><span data-stu-id="62bb2-145">Unregister</span></span>

```yaml
Type: JobOperation
Parameter Sets: (All)
Aliases: 
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-146">-Status</span><span class="sxs-lookup"><span data-stu-id="62bb2-146">-Status</span></span>
<span data-ttu-id="62bb2-147">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="62bb2-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="62bb2-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="62bb2-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="62bb2-149">Inaktive</span><span class="sxs-lookup"><span data-stu-id="62bb2-149">InProgress</span></span>
- <span data-ttu-id="62bb2-150">Startade</span><span class="sxs-lookup"><span data-stu-id="62bb2-150">Failed</span></span>
- <span data-ttu-id="62bb2-151">Annullerats</span><span class="sxs-lookup"><span data-stu-id="62bb2-151">Cancelled</span></span>
- <span data-ttu-id="62bb2-152">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="62bb2-152">Cancelling</span></span>
- <span data-ttu-id="62bb2-153">Rätta</span><span class="sxs-lookup"><span data-stu-id="62bb2-153">Completed</span></span>
- <span data-ttu-id="62bb2-154">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="62bb2-154">CompletedWithWarnings</span></span>

```yaml
Type: JobStatus
Parameter Sets: (All)
Aliases: 
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-155">-För att</span><span class="sxs-lookup"><span data-stu-id="62bb2-155">-To</span></span>
<span data-ttu-id="62bb2-156">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="62bb2-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="62bb2-157">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="62bb2-157">The default value is the current system time.</span></span>
<span data-ttu-id="62bb2-158">Om du anger den här parametern måste du också ange parametern *från* .</span><span class="sxs-lookup"><span data-stu-id="62bb2-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="62bb2-159">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="62bb2-159">Use UTC format for dates.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bb2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bb2-160">CommonParameters</span></span>
<span data-ttu-id="62bb2-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62bb2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bb2-162">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62bb2-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bb2-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62bb2-163">INPUTS</span></span>

### <span data-ttu-id="62bb2-164">Ingen</span><span class="sxs-lookup"><span data-stu-id="62bb2-164">None</span></span>
<span data-ttu-id="62bb2-165">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="62bb2-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62bb2-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62bb2-166">OUTPUTS</span></span>

### <span data-ttu-id="62bb2-167">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="62bb2-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="62bb2-168">System. Collections. Generic. IList ' 1 [Microsoft. Azure. kommandon. RecoveryServices. backup. cmdletar. MODELES. JobBase]</span><span class="sxs-lookup"><span data-stu-id="62bb2-168">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="62bb2-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62bb2-169">NOTES</span></span>

## <span data-ttu-id="62bb2-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62bb2-170">RELATED LINKS</span></span>

[<span data-ttu-id="62bb2-171">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="62bb2-171">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="62bb2-172">Stopp-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="62bb2-172">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="62bb2-173">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="62bb2-173">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


