---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523981"
---
# <span data-ttu-id="dc43f-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="dc43f-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="dc43f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc43f-102">SYNOPSIS</span></span>

<span data-ttu-id="dc43f-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="dc43f-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="dc43f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc43f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc43f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc43f-105">DESCRIPTION</span></span>

<span data-ttu-id="dc43f-106">Cmdleten **Get-AzRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="dc43f-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="dc43f-107">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="dc43f-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="dc43f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc43f-108">EXAMPLES</span></span>

### <span data-ttu-id="dc43f-109">Exempel 1: Hämta alla pågående jobb</span><span class="sxs-lookup"><span data-stu-id="dc43f-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="dc43f-110">Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.</span><span class="sxs-lookup"><span data-stu-id="dc43f-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="dc43f-111">Det andra kommandot visar det första objektet i $Joblist matrisen.</span><span class="sxs-lookup"><span data-stu-id="dc43f-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="dc43f-112">Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna</span><span class="sxs-lookup"><span data-stu-id="dc43f-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="dc43f-113">Det här kommandot får inte jobbet från den förra veckan i valvet.</span><span class="sxs-lookup"><span data-stu-id="dc43f-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="dc43f-114">Parametern *från* anger en tid sju dagar tidigare angiven i UTC.</span><span class="sxs-lookup"><span data-stu-id="dc43f-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="dc43f-115">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="dc43f-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="dc43f-116">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="dc43f-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="dc43f-117">Exempel 3: få ett pågående jobb och vänta tills det är färdigt</span><span class="sxs-lookup"><span data-stu-id="dc43f-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="dc43f-118">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="dc43f-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="dc43f-119">Obs! Du kan använda **wait-AzRecoveryServicesBackupJob** cmdlet för att vänta på att ett Azure Backup-jobb ska avslutas i stället för while-slingan.</span><span class="sxs-lookup"><span data-stu-id="dc43f-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="dc43f-120">Exempel 4: Hämta alla AzureVM-jobb under de senaste 2 dagarna som har slutförts</span><span class="sxs-lookup"><span data-stu-id="dc43f-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="dc43f-121">Den första cmdleten hämtar valv objekt.</span><span class="sxs-lookup"><span data-stu-id="dc43f-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="dc43f-122">Andra cmdlet lagrar alla AzureVM-jobb i det angivna valvet som har slutförts under de senaste två dagarna till $jobs.</span><span class="sxs-lookup"><span data-stu-id="dc43f-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="dc43f-123">Ändra värdet för BackupManagementType-parametern till testfunktion för att hämta testjobb för testagenten.</span><span class="sxs-lookup"><span data-stu-id="dc43f-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="dc43f-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc43f-124">PARAMETERS</span></span>

### <span data-ttu-id="dc43f-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="dc43f-125">-BackupManagementType</span></span>

<span data-ttu-id="dc43f-126">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="dc43f-126">The class of resources being protected.</span></span> <span data-ttu-id="dc43f-127">För närvarande är de värden som stöds för denna cmdlet AzureVM, AzureStorage, AzureWorkload, monoklonal.</span><span class="sxs-lookup"><span data-stu-id="dc43f-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc43f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc43f-128">-DefaultProfile</span></span>

<span data-ttu-id="dc43f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc43f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc43f-130">-Från</span><span class="sxs-lookup"><span data-stu-id="dc43f-130">-From</span></span>

<span data-ttu-id="dc43f-131">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="dc43f-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="dc43f-132">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="dc43f-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="dc43f-133">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="dc43f-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="dc43f-134">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="dc43f-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="dc43f-135">-Jobb</span><span class="sxs-lookup"><span data-stu-id="dc43f-135">-Job</span></span>

<span data-ttu-id="dc43f-136">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="dc43f-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="dc43f-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="dc43f-137">-JobId</span></span>

<span data-ttu-id="dc43f-138">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="dc43f-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="dc43f-139">ID är egenskapen JobId för en **Microsoft. Azure.-kommandon. RecoveryServices. backup. cmdletar. Models. JobBase** -objekt.</span><span class="sxs-lookup"><span data-stu-id="dc43f-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="dc43f-140">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="dc43f-140">-Operation</span></span>

<span data-ttu-id="dc43f-141">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="dc43f-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="dc43f-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dc43f-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc43f-143">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="dc43f-143">Backup</span></span>
- <span data-ttu-id="dc43f-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="dc43f-144">ConfigureBackup</span></span>
- <span data-ttu-id="dc43f-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="dc43f-145">DeleteBackupData</span></span>
- <span data-ttu-id="dc43f-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="dc43f-146">DisableBackup</span></span>
- <span data-ttu-id="dc43f-147">Terställa</span><span class="sxs-lookup"><span data-stu-id="dc43f-147">Restore</span></span>
- <span data-ttu-id="dc43f-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="dc43f-148">BackupDataMove</span></span>

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

### <span data-ttu-id="dc43f-149">-Status</span><span class="sxs-lookup"><span data-stu-id="dc43f-149">-Status</span></span>

<span data-ttu-id="dc43f-150">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="dc43f-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="dc43f-151">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dc43f-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dc43f-152">Inaktive</span><span class="sxs-lookup"><span data-stu-id="dc43f-152">InProgress</span></span>
- <span data-ttu-id="dc43f-153">Startade</span><span class="sxs-lookup"><span data-stu-id="dc43f-153">Failed</span></span>
- <span data-ttu-id="dc43f-154">Annullerats</span><span class="sxs-lookup"><span data-stu-id="dc43f-154">Cancelled</span></span>
- <span data-ttu-id="dc43f-155">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="dc43f-155">Cancelling</span></span>
- <span data-ttu-id="dc43f-156">Rätta</span><span class="sxs-lookup"><span data-stu-id="dc43f-156">Completed</span></span>
- <span data-ttu-id="dc43f-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="dc43f-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="dc43f-158">-För att</span><span class="sxs-lookup"><span data-stu-id="dc43f-158">-To</span></span>

<span data-ttu-id="dc43f-159">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="dc43f-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="dc43f-160">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="dc43f-160">The default value is the current system time.</span></span>
<span data-ttu-id="dc43f-161">Om du anger den här parametern måste du också ange parametern **-from** .</span><span class="sxs-lookup"><span data-stu-id="dc43f-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="dc43f-162">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="dc43f-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="dc43f-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="dc43f-163">-VaultId</span></span>

<span data-ttu-id="dc43f-164">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="dc43f-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="dc43f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc43f-165">CommonParameters</span></span>
<span data-ttu-id="dc43f-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc43f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc43f-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc43f-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc43f-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc43f-168">INPUTS</span></span>

### <span data-ttu-id="dc43f-169">System. String</span><span class="sxs-lookup"><span data-stu-id="dc43f-169">System.String</span></span>

## <span data-ttu-id="dc43f-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc43f-170">OUTPUTS</span></span>

### <span data-ttu-id="dc43f-171">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="dc43f-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="dc43f-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc43f-172">NOTES</span></span>

## <span data-ttu-id="dc43f-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc43f-173">RELATED LINKS</span></span>

[<span data-ttu-id="dc43f-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="dc43f-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="dc43f-175">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="dc43f-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="dc43f-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="dc43f-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
