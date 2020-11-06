---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 6a172de918e8b0675abaf01edf2ec198dae75b5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585656"
---
# <span data-ttu-id="dfbf0-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfbf0-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="dfbf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dfbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbf0-103">Hämtar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfbf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dfbf0-104">SYNTAX</span></span>

### <span data-ttu-id="dfbf0-105">Alla i resurs grupp och konto (standard)</span><span class="sxs-lookup"><span data-stu-id="dfbf0-105">All In Resource Group and Account (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfbf0-106">Specifik JobInformation</span><span class="sxs-lookup"><span data-stu-id="dfbf0-106">Specific JobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfbf0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dfbf0-107">DESCRIPTION</span></span>
<span data-ttu-id="dfbf0-108">Cmdleten **Get-AzureRmDataLakeAnalyticsJob** får ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="dfbf0-109">Om du inte anger något jobb får denna cmdlet alla jobb.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="dfbf0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dfbf0-110">EXAMPLES</span></span>

### <span data-ttu-id="dfbf0-111">Exempel 1: Hämta ett angivet jobb</span><span class="sxs-lookup"><span data-stu-id="dfbf0-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="dfbf0-112">Det här kommandot får jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="dfbf0-113">Exempel 2: få jobb skickade under den senaste veckan</span><span class="sxs-lookup"><span data-stu-id="dfbf0-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="dfbf0-114">Med det här kommandot hämtas jobb som skickas under den senaste veckan.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="dfbf0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dfbf0-115">PARAMETERS</span></span>

### <span data-ttu-id="dfbf0-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="dfbf0-116">-Account</span></span>
<span data-ttu-id="dfbf0-117">Anger namnet på ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-117">Specifies the name of a Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-118">-Inkludera</span><span class="sxs-lookup"><span data-stu-id="dfbf0-118">-Include</span></span>
<span data-ttu-id="dfbf0-119">Anger alternativ som anger vilken typ av ytterligare information som ska hämtas om jobbet.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-119">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="dfbf0-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfbf0-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfbf0-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="dfbf0-121">None</span></span>
- <span data-ttu-id="dfbf0-122">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="dfbf0-122">DebugInfo</span></span>
- <span data-ttu-id="dfbf0-123">Statistik</span><span class="sxs-lookup"><span data-stu-id="dfbf0-123">Statistics</span></span>
- <span data-ttu-id="dfbf0-124">Alla</span><span class="sxs-lookup"><span data-stu-id="dfbf0-124">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: Specific JobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-125">-JobId</span><span class="sxs-lookup"><span data-stu-id="dfbf0-125">-JobId</span></span>
<span data-ttu-id="dfbf0-126">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-126">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Specific JobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="dfbf0-127">-Name</span></span>
<span data-ttu-id="dfbf0-128">Anger ett namn som ska användas för att filtrera jobb listans resultat.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-128">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="dfbf0-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfbf0-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfbf0-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="dfbf0-130">None</span></span>
- <span data-ttu-id="dfbf0-131">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="dfbf0-131">DebugInfo</span></span>
- <span data-ttu-id="dfbf0-132">Statistik</span><span class="sxs-lookup"><span data-stu-id="dfbf0-132">Statistics</span></span>
- <span data-ttu-id="dfbf0-133">Alla</span><span class="sxs-lookup"><span data-stu-id="dfbf0-133">All</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-134">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="dfbf0-134">-PipelineId</span></span>
<span data-ttu-id="dfbf0-135">Ett valfritt ID som endast anger jobb delar av den angivna pipeline ska returneras.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-135">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-136">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="dfbf0-136">-RecurrenceId</span></span>
<span data-ttu-id="dfbf0-137">Ett valfritt ID som endast anger att jobb delar av den angivna upprepningen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-137">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-138">-Resultat</span><span class="sxs-lookup"><span data-stu-id="dfbf0-138">-Result</span></span>
<span data-ttu-id="dfbf0-139">Anger ett resultat filter för jobb resultaten.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-139">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="dfbf0-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfbf0-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfbf0-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="dfbf0-141">None</span></span>
- <span data-ttu-id="dfbf0-142">Annullerats</span><span class="sxs-lookup"><span data-stu-id="dfbf0-142">Cancelled</span></span>
- <span data-ttu-id="dfbf0-143">Startade</span><span class="sxs-lookup"><span data-stu-id="dfbf0-143">Failed</span></span>
- <span data-ttu-id="dfbf0-144">Utför</span><span class="sxs-lookup"><span data-stu-id="dfbf0-144">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-145">-State</span><span class="sxs-lookup"><span data-stu-id="dfbf0-145">-State</span></span>
<span data-ttu-id="dfbf0-146">Anger ett status filter för jobb resultaten.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-146">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="dfbf0-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="dfbf0-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dfbf0-148">Allmänt</span><span class="sxs-lookup"><span data-stu-id="dfbf0-148">Accepted</span></span>
- <span data-ttu-id="dfbf0-149">Nya</span><span class="sxs-lookup"><span data-stu-id="dfbf0-149">New</span></span>
- <span data-ttu-id="dfbf0-150">Kompilera</span><span class="sxs-lookup"><span data-stu-id="dfbf0-150">Compiling</span></span>
- <span data-ttu-id="dfbf0-151">Scheman</span><span class="sxs-lookup"><span data-stu-id="dfbf0-151">Scheduling</span></span>
- <span data-ttu-id="dfbf0-152">I kö</span><span class="sxs-lookup"><span data-stu-id="dfbf0-152">Queued</span></span>
- <span data-ttu-id="dfbf0-153">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="dfbf0-153">Starting</span></span>
- <span data-ttu-id="dfbf0-154">Pausad</span><span class="sxs-lookup"><span data-stu-id="dfbf0-154">Paused</span></span>
- <span data-ttu-id="dfbf0-155">Aktiv</span><span class="sxs-lookup"><span data-stu-id="dfbf0-155">Running</span></span>
- <span data-ttu-id="dfbf0-156">Avslutade</span><span class="sxs-lookup"><span data-stu-id="dfbf0-156">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: All In Resource Group and Account
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-157">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="dfbf0-157">-SubmittedAfter</span></span>
<span data-ttu-id="dfbf0-158">Anger ett datum filter.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-158">Specifies a date filter.</span></span>
<span data-ttu-id="dfbf0-159">Använd den här parametern för att filtrera jobb resultaten till jobb som har inlämnats efter det angivna datumet.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-159">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-160">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="dfbf0-160">-SubmittedBefore</span></span>
<span data-ttu-id="dfbf0-161">Anger ett datum filter.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-161">Specifies a date filter.</span></span>
<span data-ttu-id="dfbf0-162">Använd den här parametern för att filtrera jobb resultaten till jobb som skickas före angivet datum.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-162">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-163">-Sändning</span><span class="sxs-lookup"><span data-stu-id="dfbf0-163">-Submitter</span></span>
<span data-ttu-id="dfbf0-164">Anger e-postadressen för en användare.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-164">Specifies the email address of a user.</span></span>
<span data-ttu-id="dfbf0-165">Använd den här parametern för att filtrera jobb listans resultat till jobb som skickas av en viss användare.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-165">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-166">-Överst</span><span class="sxs-lookup"><span data-stu-id="dfbf0-166">-Top</span></span>
<span data-ttu-id="dfbf0-167">Ett valfritt värde som anger hur många jobb som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-167">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="dfbf0-168">Standardvärdet är 500</span><span class="sxs-lookup"><span data-stu-id="dfbf0-168">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: All In Resource Group and Account
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbf0-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbf0-169">-DefaultProfile</span></span>
<span data-ttu-id="dfbf0-170">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfbf0-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbf0-171">CommonParameters</span></span>
<span data-ttu-id="dfbf0-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbf0-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbf0-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbf0-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dfbf0-174">INPUTS</span></span>

### <span data-ttu-id="dfbf0-175">Ande</span><span class="sxs-lookup"><span data-stu-id="dfbf0-175">Guid</span></span>
<span data-ttu-id="dfbf0-176">Parametern ' JobId ' godkänner värdet av typen ' GUID ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dfbf0-176">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="dfbf0-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dfbf0-177">OUTPUTS</span></span>

### <span data-ttu-id="dfbf0-178">JobInformation</span><span class="sxs-lookup"><span data-stu-id="dfbf0-178">JobInformation</span></span>
<span data-ttu-id="dfbf0-179">Den angivna jobb informations informationen</span><span class="sxs-lookup"><span data-stu-id="dfbf0-179">The specified job information details</span></span>

### <span data-ttu-id="dfbf0-180">Förteckning<JobInformation></span><span class="sxs-lookup"><span data-stu-id="dfbf0-180">List<JobInformation></span></span>
<span data-ttu-id="dfbf0-181">Listan med jobb i angivet data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="dfbf0-181">The list of jobs in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="dfbf0-182">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dfbf0-182">NOTES</span></span>

## <span data-ttu-id="dfbf0-183">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dfbf0-183">RELATED LINKS</span></span>

[<span data-ttu-id="dfbf0-184">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfbf0-184">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="dfbf0-185">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfbf0-185">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="dfbf0-186">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dfbf0-186">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


