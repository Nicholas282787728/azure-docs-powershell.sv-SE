---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573446"
---
# <span data-ttu-id="68069-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="68069-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="68069-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="68069-102">SYNOPSIS</span></span>
<span data-ttu-id="68069-103">Hämtar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="68069-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68069-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="68069-104">SYNTAX</span></span>

### <span data-ttu-id="68069-105">GetAllInResourceGroupAndAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="68069-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68069-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="68069-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68069-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="68069-107">DESCRIPTION</span></span>
<span data-ttu-id="68069-108">Cmdleten **Get-AzureRmDataLakeAnalyticsJob** får ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="68069-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="68069-109">Om du inte anger något jobb får denna cmdlet alla jobb.</span><span class="sxs-lookup"><span data-stu-id="68069-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="68069-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="68069-110">EXAMPLES</span></span>

### <span data-ttu-id="68069-111">Exempel 1: Hämta ett angivet jobb</span><span class="sxs-lookup"><span data-stu-id="68069-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="68069-112">Det här kommandot får jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="68069-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="68069-113">Exempel 2: få jobb skickade under den senaste veckan</span><span class="sxs-lookup"><span data-stu-id="68069-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="68069-114">Med det här kommandot hämtas jobb som skickas under den senaste veckan.</span><span class="sxs-lookup"><span data-stu-id="68069-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="68069-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="68069-115">PARAMETERS</span></span>

### <span data-ttu-id="68069-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="68069-116">-Account</span></span>
<span data-ttu-id="68069-117">Anger namnet på ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="68069-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68069-118">-DefaultProfile</span></span>
<span data-ttu-id="68069-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="68069-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68069-120">-Inkludera</span><span class="sxs-lookup"><span data-stu-id="68069-120">-Include</span></span>
<span data-ttu-id="68069-121">Anger alternativ som anger vilken typ av ytterligare information som ska hämtas om jobbet.</span><span class="sxs-lookup"><span data-stu-id="68069-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="68069-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="68069-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68069-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="68069-123">None</span></span>
- <span data-ttu-id="68069-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="68069-124">DebugInfo</span></span>
- <span data-ttu-id="68069-125">Statistik</span><span class="sxs-lookup"><span data-stu-id="68069-125">Statistics</span></span>
- <span data-ttu-id="68069-126">Alla</span><span class="sxs-lookup"><span data-stu-id="68069-126">All</span></span>

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="68069-127">-JobId</span></span>
<span data-ttu-id="68069-128">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="68069-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="68069-129">-Name</span></span>
<span data-ttu-id="68069-130">Anger ett namn som ska användas för att filtrera jobb listans resultat.</span><span class="sxs-lookup"><span data-stu-id="68069-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="68069-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="68069-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68069-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="68069-132">None</span></span>
- <span data-ttu-id="68069-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="68069-133">DebugInfo</span></span>
- <span data-ttu-id="68069-134">Statistik</span><span class="sxs-lookup"><span data-stu-id="68069-134">Statistics</span></span>
- <span data-ttu-id="68069-135">Alla</span><span class="sxs-lookup"><span data-stu-id="68069-135">All</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="68069-136">-PipelineId</span></span>
<span data-ttu-id="68069-137">Ett valfritt ID som endast anger jobb delar av den angivna pipeline ska returneras.</span><span class="sxs-lookup"><span data-stu-id="68069-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="68069-138">-RecurrenceId</span></span>
<span data-ttu-id="68069-139">Ett valfritt ID som endast anger att jobb delar av den angivna upprepningen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="68069-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-140">-Resultat</span><span class="sxs-lookup"><span data-stu-id="68069-140">-Result</span></span>
<span data-ttu-id="68069-141">Anger ett resultat filter för jobb resultaten.</span><span class="sxs-lookup"><span data-stu-id="68069-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="68069-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="68069-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68069-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="68069-143">None</span></span>
- <span data-ttu-id="68069-144">Annullerats</span><span class="sxs-lookup"><span data-stu-id="68069-144">Cancelled</span></span>
- <span data-ttu-id="68069-145">Startade</span><span class="sxs-lookup"><span data-stu-id="68069-145">Failed</span></span>
- <span data-ttu-id="68069-146">Utför</span><span class="sxs-lookup"><span data-stu-id="68069-146">Succeeded</span></span>

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-147">-State</span><span class="sxs-lookup"><span data-stu-id="68069-147">-State</span></span>
<span data-ttu-id="68069-148">Anger ett status filter för jobb resultaten.</span><span class="sxs-lookup"><span data-stu-id="68069-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="68069-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="68069-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="68069-150">Allmänt</span><span class="sxs-lookup"><span data-stu-id="68069-150">Accepted</span></span>
- <span data-ttu-id="68069-151">Nya</span><span class="sxs-lookup"><span data-stu-id="68069-151">New</span></span>
- <span data-ttu-id="68069-152">Kompilera</span><span class="sxs-lookup"><span data-stu-id="68069-152">Compiling</span></span>
- <span data-ttu-id="68069-153">Scheman</span><span class="sxs-lookup"><span data-stu-id="68069-153">Scheduling</span></span>
- <span data-ttu-id="68069-154">I kö</span><span class="sxs-lookup"><span data-stu-id="68069-154">Queued</span></span>
- <span data-ttu-id="68069-155">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="68069-155">Starting</span></span>
- <span data-ttu-id="68069-156">Pausad</span><span class="sxs-lookup"><span data-stu-id="68069-156">Paused</span></span>
- <span data-ttu-id="68069-157">Aktiv</span><span class="sxs-lookup"><span data-stu-id="68069-157">Running</span></span>
- <span data-ttu-id="68069-158">Avslutade</span><span class="sxs-lookup"><span data-stu-id="68069-158">Ended</span></span>

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="68069-159">-SubmittedAfter</span></span>
<span data-ttu-id="68069-160">Anger ett datum filter.</span><span class="sxs-lookup"><span data-stu-id="68069-160">Specifies a date filter.</span></span>
<span data-ttu-id="68069-161">Använd den här parametern för att filtrera jobb resultaten till jobb som har inlämnats efter det angivna datumet.</span><span class="sxs-lookup"><span data-stu-id="68069-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="68069-162">-SubmittedBefore</span></span>
<span data-ttu-id="68069-163">Anger ett datum filter.</span><span class="sxs-lookup"><span data-stu-id="68069-163">Specifies a date filter.</span></span>
<span data-ttu-id="68069-164">Använd den här parametern för att filtrera jobb resultaten till jobb som skickas före angivet datum.</span><span class="sxs-lookup"><span data-stu-id="68069-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-165">-Sändning</span><span class="sxs-lookup"><span data-stu-id="68069-165">-Submitter</span></span>
<span data-ttu-id="68069-166">Anger e-postadressen för en användare.</span><span class="sxs-lookup"><span data-stu-id="68069-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="68069-167">Använd den här parametern för att filtrera jobb listans resultat till jobb som skickas av en viss användare.</span><span class="sxs-lookup"><span data-stu-id="68069-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-168">-Överst</span><span class="sxs-lookup"><span data-stu-id="68069-168">-Top</span></span>
<span data-ttu-id="68069-169">Ett valfritt värde som anger hur många jobb som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="68069-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="68069-170">Standardvärdet är 500</span><span class="sxs-lookup"><span data-stu-id="68069-170">Default value is 500</span></span>

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68069-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68069-171">CommonParameters</span></span>
<span data-ttu-id="68069-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68069-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68069-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68069-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68069-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="68069-174">INPUTS</span></span>

### <span data-ttu-id="68069-175">Ande</span><span class="sxs-lookup"><span data-stu-id="68069-175">Guid</span></span>
<span data-ttu-id="68069-176">Parametern ' JobId ' godkänner värdet av typen ' GUID ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="68069-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="68069-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="68069-177">OUTPUTS</span></span>

### <span data-ttu-id="68069-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="68069-178">JobInformation</span></span>
<span data-ttu-id="68069-179">Den angivna jobb informations informationen</span><span class="sxs-lookup"><span data-stu-id="68069-179">The specified job information details</span></span>

### <span data-ttu-id="68069-180">Förteckning<PSJobInformationBasic></span><span class="sxs-lookup"><span data-stu-id="68069-180">List<PSJobInformationBasic></span></span>
<span data-ttu-id="68069-181">Listan med jobb i angivet data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="68069-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="68069-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="68069-182">NOTES</span></span>

## <span data-ttu-id="68069-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="68069-183">RELATED LINKS</span></span>

[<span data-ttu-id="68069-184">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="68069-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="68069-185">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="68069-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="68069-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="68069-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


