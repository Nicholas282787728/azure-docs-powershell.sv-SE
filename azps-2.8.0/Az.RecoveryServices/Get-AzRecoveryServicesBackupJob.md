---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: cc23d8535e7aaca656379811121ed09bad2f64bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919754"
---
# <span data-ttu-id="6b585-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b585-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="6b585-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b585-102">SYNOPSIS</span></span>

<span data-ttu-id="6b585-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="6b585-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="6b585-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b585-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b585-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b585-105">DESCRIPTION</span></span>

<span data-ttu-id="6b585-106">Cmdleten **Get-AzRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="6b585-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="6b585-107">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="6b585-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="6b585-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b585-108">EXAMPLES</span></span>

### <span data-ttu-id="6b585-109">Exempel 1: Hämta alla pågående jobb</span><span class="sxs-lookup"><span data-stu-id="6b585-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="6b585-110">Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.</span><span class="sxs-lookup"><span data-stu-id="6b585-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="6b585-111">Det andra kommandot visar det första objektet i $Joblist matrisen.</span><span class="sxs-lookup"><span data-stu-id="6b585-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="6b585-112">Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna</span><span class="sxs-lookup"><span data-stu-id="6b585-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="6b585-113">Det här kommandot får inte jobbet från den förra veckan i valvet.</span><span class="sxs-lookup"><span data-stu-id="6b585-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="6b585-114">Parametern *från* anger en tid sju dagar tidigare angiven i UTC.</span><span class="sxs-lookup"><span data-stu-id="6b585-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="6b585-115">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="6b585-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="6b585-116">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="6b585-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="6b585-117">Exempel 3: få ett pågående jobb och vänta tills det är färdigt</span><span class="sxs-lookup"><span data-stu-id="6b585-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="6b585-118">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="6b585-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="6b585-119">Obs! Du kan använda **wait-AzRecoveryServicesBackupJob** cmdlet för att vänta på att ett Azure Backup-jobb ska avslutas i stället för while-slingan.</span><span class="sxs-lookup"><span data-stu-id="6b585-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="6b585-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b585-120">PARAMETERS</span></span>

### <span data-ttu-id="6b585-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="6b585-121">-BackupManagementType</span></span>

<span data-ttu-id="6b585-122">Anger typen av säkerhets kopierings hantering.</span><span class="sxs-lookup"><span data-stu-id="6b585-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="6b585-123">För närvarande stöds endast AzureVM, AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="6b585-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="6b585-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b585-124">-DefaultProfile</span></span>

<span data-ttu-id="6b585-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b585-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b585-126">-Från</span><span class="sxs-lookup"><span data-stu-id="6b585-126">-From</span></span>

<span data-ttu-id="6b585-127">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6b585-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b585-128">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6b585-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="6b585-129">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6b585-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="6b585-130">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="6b585-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="6b585-131">-Jobb</span><span class="sxs-lookup"><span data-stu-id="6b585-131">-Job</span></span>

<span data-ttu-id="6b585-132">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="6b585-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="6b585-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="6b585-133">-JobId</span></span>

<span data-ttu-id="6b585-134">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="6b585-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="6b585-135">ID är egenskapen JobId för en **Microsoft. Azure.-kommandon. RecoveryServices. backup. cmdletar. Models. JobBase** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6b585-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="6b585-136">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="6b585-136">-Operation</span></span>

<span data-ttu-id="6b585-137">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6b585-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b585-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6b585-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b585-139">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="6b585-139">Backup</span></span>
- <span data-ttu-id="6b585-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="6b585-140">ConfigureBackup</span></span>
- <span data-ttu-id="6b585-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="6b585-141">DeleteBackupData</span></span>
- <span data-ttu-id="6b585-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="6b585-142">DisableBackup</span></span>
- <span data-ttu-id="6b585-143">Terställa</span><span class="sxs-lookup"><span data-stu-id="6b585-143">Restore</span></span>

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

### <span data-ttu-id="6b585-144">-Status</span><span class="sxs-lookup"><span data-stu-id="6b585-144">-Status</span></span>

<span data-ttu-id="6b585-145">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6b585-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b585-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6b585-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6b585-147">Inaktive</span><span class="sxs-lookup"><span data-stu-id="6b585-147">InProgress</span></span>
- <span data-ttu-id="6b585-148">Startade</span><span class="sxs-lookup"><span data-stu-id="6b585-148">Failed</span></span>
- <span data-ttu-id="6b585-149">Annullerats</span><span class="sxs-lookup"><span data-stu-id="6b585-149">Cancelled</span></span>
- <span data-ttu-id="6b585-150">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="6b585-150">Cancelling</span></span>
- <span data-ttu-id="6b585-151">Rätta</span><span class="sxs-lookup"><span data-stu-id="6b585-151">Completed</span></span>
- <span data-ttu-id="6b585-152">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="6b585-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="6b585-153">-För att</span><span class="sxs-lookup"><span data-stu-id="6b585-153">-To</span></span>

<span data-ttu-id="6b585-154">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="6b585-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="6b585-155">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="6b585-155">The default value is the current system time.</span></span>
<span data-ttu-id="6b585-156">Om du anger den här parametern måste du också ange parametern **-from** .</span><span class="sxs-lookup"><span data-stu-id="6b585-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="6b585-157">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="6b585-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="6b585-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6b585-158">-VaultId</span></span>

<span data-ttu-id="6b585-159">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="6b585-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6b585-160">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b585-160">-CommonParameters</span></span>

<span data-ttu-id="6b585-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b585-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b585-162">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b585-162">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b585-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b585-163">INPUTS</span></span>

### <span data-ttu-id="6b585-164">System. String</span><span class="sxs-lookup"><span data-stu-id="6b585-164">System.String</span></span>

## <span data-ttu-id="6b585-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b585-165">OUTPUTS</span></span>

### <span data-ttu-id="6b585-166">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="6b585-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6b585-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b585-167">NOTES</span></span>

## <span data-ttu-id="6b585-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b585-168">RELATED LINKS</span></span>

[<span data-ttu-id="6b585-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="6b585-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="6b585-170">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b585-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="6b585-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6b585-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
