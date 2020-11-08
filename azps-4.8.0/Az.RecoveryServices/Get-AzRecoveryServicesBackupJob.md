---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102608"
---
# <span data-ttu-id="b9456-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b9456-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="b9456-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9456-102">SYNOPSIS</span></span>

<span data-ttu-id="b9456-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="b9456-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="b9456-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9456-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9456-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9456-105">DESCRIPTION</span></span>

<span data-ttu-id="b9456-106">Cmdleten **Get-AzRecoveryServicesBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="b9456-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="b9456-107">Ange valv kontexten med parametern-VaultId.</span><span class="sxs-lookup"><span data-stu-id="b9456-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b9456-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9456-108">EXAMPLES</span></span>

### <span data-ttu-id="b9456-109">Exempel 1: Hämta alla pågående jobb</span><span class="sxs-lookup"><span data-stu-id="b9456-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="b9456-110">Det första kommandot får statusen för ett pågående jobb som en matris och lagrar det sedan i $Joblist variabel.</span><span class="sxs-lookup"><span data-stu-id="b9456-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="b9456-111">Det andra kommandot visar det första objektet i $Joblist matrisen.</span><span class="sxs-lookup"><span data-stu-id="b9456-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="b9456-112">Exempel 2: Hämta alla misslyckade jobb under de senaste 7 dagarna</span><span class="sxs-lookup"><span data-stu-id="b9456-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="b9456-113">Det här kommandot får inte jobbet från den förra veckan i valvet.</span><span class="sxs-lookup"><span data-stu-id="b9456-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="b9456-114">Parametern *från* anger en tid sju dagar tidigare angiven i UTC.</span><span class="sxs-lookup"><span data-stu-id="b9456-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="b9456-115">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="b9456-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="b9456-116">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="b9456-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="b9456-117">Exempel 3: få ett pågående jobb och vänta tills det är färdigt</span><span class="sxs-lookup"><span data-stu-id="b9456-117">Example 3: Get an in-progress job and wait for completion</span></span>

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

<span data-ttu-id="b9456-118">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="b9456-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="b9456-119">Obs! Du kan använda **wait-AzRecoveryServicesBackupJob** cmdlet för att vänta på att ett Azure Backup-jobb ska avslutas i stället för while-slingan.</span><span class="sxs-lookup"><span data-stu-id="b9456-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

### <span data-ttu-id="b9456-120">Exempel 4: Hämta alla AzureVM-jobb under de senaste 2 dagarna som har slutförts</span><span class="sxs-lookup"><span data-stu-id="b9456-120">Example 4: Get all AzureVM jobs in last 2 days which finished successfully</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
<span data-ttu-id="b9456-121">Den första cmdleten hämtar valv objekt.</span><span class="sxs-lookup"><span data-stu-id="b9456-121">First cmdlet fetches the vault object.</span></span> <span data-ttu-id="b9456-122">Andra cmdlet lagrar alla AzureVM-jobb i det angivna valvet som har slutförts under de senaste två dagarna till $jobs.</span><span class="sxs-lookup"><span data-stu-id="b9456-122">Second cmdlet stores all the AzureVM jobs in the given vault which completed in last 2 days to $jobs.</span></span> <span data-ttu-id="b9456-123">Ändra värdet för BackupManagementType-parametern till testfunktion för att hämta testjobb för testagenten.</span><span class="sxs-lookup"><span data-stu-id="b9456-123">Change the value of BackupManagementType parameter to MAB in order to fetch MAB agent jobs.</span></span>

## <span data-ttu-id="b9456-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9456-124">PARAMETERS</span></span>

### <span data-ttu-id="b9456-125">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b9456-125">-BackupManagementType</span></span>

<span data-ttu-id="b9456-126">Den klass med resurser som skyddas.</span><span class="sxs-lookup"><span data-stu-id="b9456-126">The class of resources being protected.</span></span> <span data-ttu-id="b9456-127">För närvarande är de värden som stöds för denna cmdlet AzureVM, AzureStorage, AzureWorkload, monoklonal.</span><span class="sxs-lookup"><span data-stu-id="b9456-127">Currently the values supported for this cmdlet are AzureVM, AzureStorage, AzureWorkload, MAB.</span></span>

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

### <span data-ttu-id="b9456-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9456-128">-DefaultProfile</span></span>

<span data-ttu-id="b9456-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9456-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9456-130">-Från</span><span class="sxs-lookup"><span data-stu-id="b9456-130">-From</span></span>

<span data-ttu-id="b9456-131">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b9456-131">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b9456-132">Använd cmdleten **Get-date** för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b9456-132">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="b9456-133">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b9456-133">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b9456-134">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="b9456-134">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="b9456-135">-Jobb</span><span class="sxs-lookup"><span data-stu-id="b9456-135">-Job</span></span>

<span data-ttu-id="b9456-136">Anger vilket jobb som ska erhållas.</span><span class="sxs-lookup"><span data-stu-id="b9456-136">Specifies the job to get.</span></span>

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

### <span data-ttu-id="b9456-137">-JobId</span><span class="sxs-lookup"><span data-stu-id="b9456-137">-JobId</span></span>

<span data-ttu-id="b9456-138">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b9456-138">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="b9456-139">ID är egenskapen JobId för en **Microsoft. Azure.-kommandon. RecoveryServices. backup. cmdletar. Models. JobBase** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b9456-139">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="b9456-140">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="b9456-140">-Operation</span></span>

<span data-ttu-id="b9456-141">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b9456-141">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b9456-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b9456-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9456-143">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="b9456-143">Backup</span></span>
- <span data-ttu-id="b9456-144">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="b9456-144">ConfigureBackup</span></span>
- <span data-ttu-id="b9456-145">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="b9456-145">DeleteBackupData</span></span>
- <span data-ttu-id="b9456-146">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="b9456-146">DisableBackup</span></span>
- <span data-ttu-id="b9456-147">Terställa</span><span class="sxs-lookup"><span data-stu-id="b9456-147">Restore</span></span>
- <span data-ttu-id="b9456-148">BackupDataMove</span><span class="sxs-lookup"><span data-stu-id="b9456-148">BackupDataMove</span></span>

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

### <span data-ttu-id="b9456-149">-Status</span><span class="sxs-lookup"><span data-stu-id="b9456-149">-Status</span></span>

<span data-ttu-id="b9456-150">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b9456-150">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b9456-151">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b9456-151">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b9456-152">Inaktive</span><span class="sxs-lookup"><span data-stu-id="b9456-152">InProgress</span></span>
- <span data-ttu-id="b9456-153">Startade</span><span class="sxs-lookup"><span data-stu-id="b9456-153">Failed</span></span>
- <span data-ttu-id="b9456-154">Annullerats</span><span class="sxs-lookup"><span data-stu-id="b9456-154">Cancelled</span></span>
- <span data-ttu-id="b9456-155">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="b9456-155">Cancelling</span></span>
- <span data-ttu-id="b9456-156">Rätta</span><span class="sxs-lookup"><span data-stu-id="b9456-156">Completed</span></span>
- <span data-ttu-id="b9456-157">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="b9456-157">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="b9456-158">-För att</span><span class="sxs-lookup"><span data-stu-id="b9456-158">-To</span></span>

<span data-ttu-id="b9456-159">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="b9456-159">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b9456-160">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="b9456-160">The default value is the current system time.</span></span>
<span data-ttu-id="b9456-161">Om du anger den här parametern måste du också ange parametern **-from** .</span><span class="sxs-lookup"><span data-stu-id="b9456-161">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="b9456-162">Använd UTC-format för datum.</span><span class="sxs-lookup"><span data-stu-id="b9456-162">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="b9456-163">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b9456-163">-VaultId</span></span>

<span data-ttu-id="b9456-164">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="b9456-164">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b9456-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9456-165">CommonParameters</span></span>
<span data-ttu-id="b9456-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9456-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9456-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9456-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9456-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9456-168">INPUTS</span></span>

### <span data-ttu-id="b9456-169">System. String</span><span class="sxs-lookup"><span data-stu-id="b9456-169">System.String</span></span>

## <span data-ttu-id="b9456-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9456-170">OUTPUTS</span></span>

### <span data-ttu-id="b9456-171">Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="b9456-171">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b9456-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9456-172">NOTES</span></span>

## <span data-ttu-id="b9456-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9456-173">RELATED LINKS</span></span>

[<span data-ttu-id="b9456-174">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="b9456-174">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="b9456-175">Stopp-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b9456-175">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="b9456-176">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="b9456-176">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
