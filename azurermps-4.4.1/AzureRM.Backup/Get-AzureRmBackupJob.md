---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 48c1a3c3b7422f76bfbea0fbff8c3df541764606
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574735"
---
# <span data-ttu-id="d80e3-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d80e3-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="d80e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d80e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d80e3-103">Hämtar säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="d80e3-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d80e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d80e3-104">SYNTAX</span></span>

### <span data-ttu-id="d80e3-105">FiltersSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d80e3-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d80e3-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="d80e3-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d80e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d80e3-107">DESCRIPTION</span></span>
<span data-ttu-id="d80e3-108">Cmdleten **Get-AzureRmBackupJob** får Azure Backup-jobb för ett specifikt valv.</span><span class="sxs-lookup"><span data-stu-id="d80e3-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="d80e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d80e3-109">EXAMPLES</span></span>

### <span data-ttu-id="d80e3-110">Exempel 1: Hämta alla jobb i ett säkerhets kopierings valv</span><span class="sxs-lookup"><span data-stu-id="d80e3-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="d80e3-111">Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="d80e3-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="d80e3-112">Kommandot lagrar objektet i $Vault variabel.</span><span class="sxs-lookup"><span data-stu-id="d80e3-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="d80e3-113">Det andra kommandot får alla jobb för valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="d80e3-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="d80e3-114">Exempel 2: Hämta färdiga jobb</span><span class="sxs-lookup"><span data-stu-id="d80e3-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="d80e3-115">Det här kommandot hämtar jobb från valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="d80e3-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="d80e3-116">Exempel 3: Hämta misslyckade jobb under den senaste veckan</span><span class="sxs-lookup"><span data-stu-id="d80e3-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="d80e3-117">Det här kommandot hämtar misslyckade jobb från förra veckan från valvet i $Vault.</span><span class="sxs-lookup"><span data-stu-id="d80e3-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="d80e3-118">Parametern *från* anger en tid sju dagar förr.</span><span class="sxs-lookup"><span data-stu-id="d80e3-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="d80e3-119">Kommandot anger inte ett värde för parametern *to* .</span><span class="sxs-lookup"><span data-stu-id="d80e3-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="d80e3-120">Därför används standardvärdet för den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="d80e3-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="d80e3-121">Exempel 4: Avsök säkerhets kopiering för ett pågående jobb som är klart</span><span class="sxs-lookup"><span data-stu-id="d80e3-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
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

<span data-ttu-id="d80e3-122">Det här skriptet utför det första jobbet som pågår tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="d80e3-122">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="d80e3-123">Den första raden i skriptet får alla jobb i $Vault som pågår och lagrar sedan de jobben i $Jobs mat ris variabeln.</span><span class="sxs-lookup"><span data-stu-id="d80e3-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>

<span data-ttu-id="d80e3-124">Den andra raden sparar det första jobbet från $Jobs matris i $Job variabel.</span><span class="sxs-lookup"><span data-stu-id="d80e3-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>

<span data-ttu-id="d80e3-125">Den tredje raden startar en **while** -slinga som kontrollerar jobbets aktuella status tills jobbet är klart.</span><span class="sxs-lookup"><span data-stu-id="d80e3-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="d80e3-126">Om du vill ha information om nyckelordet **while** skriver du `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="d80e3-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>

<span data-ttu-id="d80e3-127">**While** -slingan skriver ett meddelande till konsolen, väntar i tio sekunder och uppdaterar variabeln $Job.</span><span class="sxs-lookup"><span data-stu-id="d80e3-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="d80e3-128">Skriptet uppdaterar $Job-variabeln genom att använda det befintliga värdet för $Job och den aktuella cmdleten för att få aktuell status för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d80e3-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="d80e3-129">Om du vill ha information om Windows PowerShell-cmdletar skriver du `Get-Help Write-Host` och `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="d80e3-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>

<span data-ttu-id="d80e3-130">Den sista raden i skriptet visar att skriptet är klart.</span><span class="sxs-lookup"><span data-stu-id="d80e3-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="d80e3-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d80e3-131">PARAMETERS</span></span>

### <span data-ttu-id="d80e3-132">-Från</span><span class="sxs-lookup"><span data-stu-id="d80e3-132">-From</span></span>
<span data-ttu-id="d80e3-133">Anger start, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d80e3-133">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d80e3-134">Använd Get-Date cmdlet för att hämta ett **datetime** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d80e3-134">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="d80e3-135">Om du vill ha mer information om **datetime** -objekt skriver du `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="d80e3-135">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-136">-Jobb</span><span class="sxs-lookup"><span data-stu-id="d80e3-136">-Job</span></span>
<span data-ttu-id="d80e3-137">Anger ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d80e3-137">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="d80e3-138">Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d80e3-138">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-139">-JobId</span><span class="sxs-lookup"><span data-stu-id="d80e3-139">-JobId</span></span>
<span data-ttu-id="d80e3-140">Anger ID för ett jobb som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d80e3-140">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="d80e3-141">ID är **InstanceID** -egenskapen för ett **AzureRmBackupJob** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d80e3-141">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="d80e3-142">För att få ett **AzureRmBackupJob** -objekt, Använd Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="d80e3-142">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-143">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="d80e3-143">-Operation</span></span>
<span data-ttu-id="d80e3-144">Anger en åtgärd för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d80e3-144">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d80e3-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d80e3-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d80e3-146">Reservdomänkontrollant</span><span class="sxs-lookup"><span data-stu-id="d80e3-146">Backup</span></span> 
- <span data-ttu-id="d80e3-147">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="d80e3-147">ConfigureBackup</span></span> 
- <span data-ttu-id="d80e3-148">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="d80e3-148">DeleteBackupData</span></span> 
- <span data-ttu-id="d80e3-149">Registrera dig</span><span class="sxs-lookup"><span data-stu-id="d80e3-149">Register</span></span> 
- <span data-ttu-id="d80e3-150">Terställa</span><span class="sxs-lookup"><span data-stu-id="d80e3-150">Restore</span></span> 
- <span data-ttu-id="d80e3-151">Låsa upp</span><span class="sxs-lookup"><span data-stu-id="d80e3-151">UnProtect</span></span> 
- <span data-ttu-id="d80e3-152">Avregistrera</span><span class="sxs-lookup"><span data-stu-id="d80e3-152">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-153">-Status</span><span class="sxs-lookup"><span data-stu-id="d80e3-153">-Status</span></span>
<span data-ttu-id="d80e3-154">Anger en status för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d80e3-154">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d80e3-155">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d80e3-155">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d80e3-156">Inaktive</span><span class="sxs-lookup"><span data-stu-id="d80e3-156">InProgress</span></span>
- <span data-ttu-id="d80e3-157">Startade</span><span class="sxs-lookup"><span data-stu-id="d80e3-157">Failed</span></span>
- <span data-ttu-id="d80e3-158">Annullerats</span><span class="sxs-lookup"><span data-stu-id="d80e3-158">Cancelled</span></span>
- <span data-ttu-id="d80e3-159">Brusdämpande</span><span class="sxs-lookup"><span data-stu-id="d80e3-159">Cancelling</span></span>
- <span data-ttu-id="d80e3-160">Rätta</span><span class="sxs-lookup"><span data-stu-id="d80e3-160">Completed</span></span>
- <span data-ttu-id="d80e3-161">CompletedWithWarnings</span><span class="sxs-lookup"><span data-stu-id="d80e3-161">CompletedWithWarnings</span></span> 

<span data-ttu-id="d80e3-162">Du kan ange den här parametern för att hitta alla pågående jobb eller alla misslyckade jobb.</span><span class="sxs-lookup"><span data-stu-id="d80e3-162">You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-163">-För att</span><span class="sxs-lookup"><span data-stu-id="d80e3-163">-To</span></span>
<span data-ttu-id="d80e3-164">Anger End, som ett **datetime** -objekt, för ett tidsintervall för de jobb som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="d80e3-164">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="d80e3-165">Standardvärdet är den aktuella system tiden.</span><span class="sxs-lookup"><span data-stu-id="d80e3-165">The default value is the current system time.</span></span>
<span data-ttu-id="d80e3-166">Om du anger den här parametern måste du också ange parametern *från* .</span><span class="sxs-lookup"><span data-stu-id="d80e3-166">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-167">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d80e3-167">-Type</span></span>
<span data-ttu-id="d80e3-168">Anger den typ av behållare för vilken denna cmdlet ska säkerhetskopiera jobb.</span><span class="sxs-lookup"><span data-stu-id="d80e3-168">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="d80e3-169">För närvarande är det enda värdet som stöds AzureVM.</span><span class="sxs-lookup"><span data-stu-id="d80e3-169">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-170">-Valv</span><span class="sxs-lookup"><span data-stu-id="d80e3-170">-Vault</span></span>
<span data-ttu-id="d80e3-171">Anger det säkerhets kopierings valv som denna cmdlet hämtar jobb för.</span><span class="sxs-lookup"><span data-stu-id="d80e3-171">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="d80e3-172">Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d80e3-172">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80e3-173">-DefaultProfile</span></span>
<span data-ttu-id="d80e3-174">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d80e3-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80e3-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80e3-175">CommonParameters</span></span>
<span data-ttu-id="d80e3-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80e3-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80e3-177">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80e3-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80e3-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d80e3-178">INPUTS</span></span>

### <span data-ttu-id="d80e3-179">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d80e3-179">AzureRmBackupVault</span></span>

## <span data-ttu-id="d80e3-180">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d80e3-180">OUTPUTS</span></span>

### <span data-ttu-id="d80e3-181">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="d80e3-181">AzureRmBackupJob[]</span></span>
<span data-ttu-id="d80e3-182">Denna cmdlet returnerar en eller flera säkerhets kopierings jobb.</span><span class="sxs-lookup"><span data-stu-id="d80e3-182">This cmdlet returns one or more Backup jobs.</span></span>

## <span data-ttu-id="d80e3-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d80e3-183">NOTES</span></span>
* <span data-ttu-id="d80e3-184">Ingen</span><span class="sxs-lookup"><span data-stu-id="d80e3-184">None</span></span>

## <span data-ttu-id="d80e3-185">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d80e3-185">RELATED LINKS</span></span>

[<span data-ttu-id="d80e3-186">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="d80e3-186">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="d80e3-187">Stopp-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d80e3-187">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="d80e3-188">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="d80e3-188">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


