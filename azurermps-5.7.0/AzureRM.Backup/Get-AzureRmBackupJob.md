---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575724"
---
# <span data-ttu-id="8535d-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8535d-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="8535d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8535d-102">SYNOPSIS</span></span>
<span data-ttu-id="8535d-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="8535d-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8535d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8535d-104">SYNTAX</span></span>

### <span data-ttu-id="8535d-105">FiltersSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8535d-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8535d-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="8535d-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8535d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8535d-107">DESCRIPTION</span></span>
<span data-ttu-id="8535d-108">Cmdleten **Get-AzureRmBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="8535d-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="8535d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8535d-109">EXAMPLES</span></span>

### <span data-ttu-id="8535d-110">Exempel 1: Hämta alla jobb i ett säkerhets kopierings valv</span><span class="sxs-lookup"><span data-stu-id="8535d-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="8535d-111">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="8535d-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="8535d-112">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="8535d-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="8535d-113">Det andra kommandot får alla jobb för valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="8535d-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="8535d-114">Exempel 2: Hämta färdiga jobb</span><span class="sxs-lookup"><span data-stu-id="8535d-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="8535d-115">Det här kommandot hämtar jobb från valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="8535d-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="8535d-116">Exempel 3: Hämta misslyckade jobb under den senaste veckan</span><span class="sxs-lookup"><span data-stu-id="8535d-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="8535d-117">Det här kommandot hämtar misslyckade jobb från förra veckan från valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="8535d-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="8535d-118">Parametern *från* anger en tid sju dagar förr.</span><span class="sxs-lookup"><span data-stu-id="8535d-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="8535d-119">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="8535d-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="8535d-120">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="8535d-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="8535d-121">Exempel 4: Avsök säkerhets kopiering för ett pågående jobb som är klart</span><span class="sxs-lookup"><span data-stu-id="8535d-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="8535d-122">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="8535d-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="8535d-123">Den första raden i skriptet får alla jobb i $Vault som pågår och lagrar sedan de jobben i $Jobs mat ris variabeln.</span><span class="sxs-lookup"><span data-stu-id="8535d-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="8535d-124">Den andra raden sparar det första jobbet från $Jobs matris i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="8535d-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="8535d-125">Den tredje raden startar en **while** -slinga som kontrollerar jobbets aktuella status tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="8535d-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="8535d-126">Om du vill ha information om nyckelordet **while** skriver du `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="8535d-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="8535d-127">**While** -slingan skriver ett meddelande till konsolen, väntar i tio sekunder och uppdaterar variabeln $Job.</span><span class="sxs-lookup"><span data-stu-id="8535d-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="8535d-128">Skriptet uppdaterar $Job-variabeln genom att använda det befintliga värdet för $Job och den aktuella cmdleten för att få aktuell status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="8535d-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="8535d-129">Om du vill ha information om Windows PowerShell-cmdletar skriver du `Get-Help Write-Host` och `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="8535d-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="8535d-130">Den sista raden i skriptet visar att skriptet är klart.</span><span class="sxs-lookup"><span data-stu-id="8535d-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="8535d-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8535d-131">PARAMETERS</span></span>

### <span data-ttu-id="8535d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8535d-132">-DefaultProfile</span></span>
<span data-ttu-id="8535d-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8535d-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8535d-134">-Från</span><span class="sxs-lookup"><span data-stu-id="8535d-134">-From</span></span>
<span data-ttu-id="8535d-135">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8535d-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8535d-136">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8535d-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="8535d-137">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8535d-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-138">-Jobb</span><span class="sxs-lookup"><span data-stu-id="8535d-138">-Job</span></span>
<span data-ttu-id="8535d-139">Anger ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8535d-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="8535d-140">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8535d-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="8535d-141">-JobId</span></span>
<span data-ttu-id="8535d-142">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="8535d-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="8535d-143">ID är **InstanceID** -egenskapen för ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8535d-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="8535d-144">För att få ett **AzureRmBackupJob** -objekt, Använd Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="8535d-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-145">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="8535d-145">-Operation</span></span>
<span data-ttu-id="8535d-146">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8535d-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8535d-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8535d-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8535d-148">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="8535d-148">Backup</span></span> 
- <span data-ttu-id="8535d-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="8535d-149">ConfigureBackup</span></span> 
- <span data-ttu-id="8535d-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="8535d-150">DeleteBackupData</span></span> 
- <span data-ttu-id="8535d-151">Registrera dig</span><span class="sxs-lookup"><span data-stu-id="8535d-151">Register</span></span> 
- <span data-ttu-id="8535d-152">Terställa</span><span class="sxs-lookup"><span data-stu-id="8535d-152">Restore</span></span> 
- <span data-ttu-id="8535d-153">Låsa upp</span><span class="sxs-lookup"><span data-stu-id="8535d-153">UnProtect</span></span> 
- <span data-ttu-id="8535d-154">Avregistrera</span><span class="sxs-lookup"><span data-stu-id="8535d-154">Unregister</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-155">-Status</span><span class="sxs-lookup"><span data-stu-id="8535d-155">-Status</span></span>
<span data-ttu-id="8535d-156">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8535d-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8535d-157">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8535d-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8535d-158">Inaktive</span><span class="sxs-lookup"><span data-stu-id="8535d-158">InProgress</span></span>
- <span data-ttu-id="8535d-159">Startade</span><span class="sxs-lookup"><span data-stu-id="8535d-159">Failed</span></span>
- <span data-ttu-id="8535d-160">Annullerats</span><span class="sxs-lookup"><span data-stu-id="8535d-160">Cancelled</span></span>
- <span data-ttu-id="8535d-161">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="8535d-161">Cancelling</span></span>
- <span data-ttu-id="8535d-162">Rätta</span><span class="sxs-lookup"><span data-stu-id="8535d-162">Completed</span></span>
- <span data-ttu-id="8535d-163">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="8535d-163">CompletedWithWarnings</span></span> 

<span data-ttu-id="8535d-164">Du kan ange den här parametern för att hitta alla pågående jobb eller alla misslyckade jobb.</span><span class="sxs-lookup"><span data-stu-id="8535d-164">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-165">-För att</span><span class="sxs-lookup"><span data-stu-id="8535d-165">-To</span></span>
<span data-ttu-id="8535d-166">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="8535d-166">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8535d-167">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="8535d-167">The default value is the current system time.</span></span>
<span data-ttu-id="8535d-168">Om du anger den här parametern måste du också ange parametern *från* .</span><span class="sxs-lookup"><span data-stu-id="8535d-168">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-169">– Skriv</span><span class="sxs-lookup"><span data-stu-id="8535d-169">-Type</span></span>
<span data-ttu-id="8535d-170">Anger den typ av behållare för vilken denna cmdlet ska säkerhetskopiera jobb.</span><span class="sxs-lookup"><span data-stu-id="8535d-170">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="8535d-171">För närvarande är det enda värdet som stöds AzureVM.</span><span class="sxs-lookup"><span data-stu-id="8535d-171">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-172">-Valv</span><span class="sxs-lookup"><span data-stu-id="8535d-172">-Vault</span></span>
<span data-ttu-id="8535d-173">Anger det säkerhets kopierings valv som denna cmdlet hämtar jobb för.</span><span class="sxs-lookup"><span data-stu-id="8535d-173">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="8535d-174">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8535d-174">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8535d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8535d-175">CommonParameters</span></span>
<span data-ttu-id="8535d-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8535d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8535d-177">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8535d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8535d-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8535d-178">INPUTS</span></span>

### <span data-ttu-id="8535d-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8535d-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="8535d-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8535d-180">OUTPUTS</span></span>

### <span data-ttu-id="8535d-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="8535d-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="8535d-182">Denna cmdlet returnerar en eller flera säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="8535d-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="8535d-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8535d-183">NOTES</span></span>
* <span data-ttu-id="8535d-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="8535d-184">None</span></span>

## <span data-ttu-id="8535d-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8535d-185">RELATED LINKS</span></span>

[<span data-ttu-id="8535d-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="8535d-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="8535d-187">Stopp-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8535d-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="8535d-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="8535d-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


