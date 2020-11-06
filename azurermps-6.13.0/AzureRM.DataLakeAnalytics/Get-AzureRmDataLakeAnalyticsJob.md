---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 59ec07b253b30d9cc7f03153706afba20331022c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582719"
---
# <span data-ttu-id="a4b58-101">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4b58-101">Get-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="a4b58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4b58-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b58-103">Hämtar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="a4b58-103">Gets a Data Lake Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4b58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4b58-104">SYNTAX</span></span>

### <span data-ttu-id="a4b58-105">GetAllInResourceGroupAndAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="a4b58-105">GetAllInResourceGroupAndAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b58-106">GetBySpecificJobInformation</span><span class="sxs-lookup"><span data-stu-id="a4b58-106">GetBySpecificJobInformation</span></span>
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b58-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4b58-107">DESCRIPTION</span></span>
<span data-ttu-id="a4b58-108">Cmdleten **Get-AzureRmDataLakeAnalyticsJob** får ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="a4b58-108">The **Get-AzureRmDataLakeAnalyticsJob** cmdlet gets an Azure Data Lake Analytics job.</span></span>
<span data-ttu-id="a4b58-109">Om du inte anger något jobb får denna cmdlet alla jobb.</span><span class="sxs-lookup"><span data-stu-id="a4b58-109">If you do not specify a job, this cmdlet gets all jobs.</span></span>

## <span data-ttu-id="a4b58-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4b58-110">EXAMPLES</span></span>

### <span data-ttu-id="a4b58-111">Exempel 1: Hämta ett angivet jobb</span><span class="sxs-lookup"><span data-stu-id="a4b58-111">Example 1: Get a specified job</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

<span data-ttu-id="a4b58-112">Det här kommandot får jobbet med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="a4b58-112">This command gets the job with the specified ID.</span></span>

### <span data-ttu-id="a4b58-113">Exempel 2: få jobb skickade under den senaste veckan</span><span class="sxs-lookup"><span data-stu-id="a4b58-113">Example 2: Get jobs submitted in the past week</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

<span data-ttu-id="a4b58-114">Med det här kommandot hämtas jobb som skickas under den senaste veckan.</span><span class="sxs-lookup"><span data-stu-id="a4b58-114">This command gets jobs submitted in the past week.</span></span>

## <span data-ttu-id="a4b58-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4b58-115">PARAMETERS</span></span>

### <span data-ttu-id="a4b58-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="a4b58-116">-Account</span></span>
<span data-ttu-id="a4b58-117">Anger namnet på ett data Lake Analytics-konto.</span><span class="sxs-lookup"><span data-stu-id="a4b58-117">Specifies the name of a Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="a4b58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b58-118">-DefaultProfile</span></span>
<span data-ttu-id="a4b58-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a4b58-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4b58-120">-Inkludera</span><span class="sxs-lookup"><span data-stu-id="a4b58-120">-Include</span></span>
<span data-ttu-id="a4b58-121">Anger alternativ som anger vilken typ av ytterligare information som ska hämtas om jobbet.</span><span class="sxs-lookup"><span data-stu-id="a4b58-121">Specifies options that indicate the type of additional information to retrieve about the job.</span></span>
<span data-ttu-id="a4b58-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a4b58-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4b58-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4b58-123">None</span></span>
- <span data-ttu-id="a4b58-124">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a4b58-124">DebugInfo</span></span>
- <span data-ttu-id="a4b58-125">Statistik</span><span class="sxs-lookup"><span data-stu-id="a4b58-125">Statistics</span></span>
- <span data-ttu-id="a4b58-126">Alla</span><span class="sxs-lookup"><span data-stu-id="a4b58-126">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-127">-JobId</span><span class="sxs-lookup"><span data-stu-id="a4b58-127">-JobId</span></span>
<span data-ttu-id="a4b58-128">Anger ID för det jobb som ska visas.</span><span class="sxs-lookup"><span data-stu-id="a4b58-128">Specifies the ID of the job to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4b58-129">-Name</span></span>
<span data-ttu-id="a4b58-130">Anger ett namn som ska användas för att filtrera jobb listans resultat.</span><span class="sxs-lookup"><span data-stu-id="a4b58-130">Specifies a name to use to filter the job list results.</span></span>
<span data-ttu-id="a4b58-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a4b58-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4b58-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4b58-132">None</span></span>
- <span data-ttu-id="a4b58-133">DebugInfo</span><span class="sxs-lookup"><span data-stu-id="a4b58-133">DebugInfo</span></span>
- <span data-ttu-id="a4b58-134">Statistik</span><span class="sxs-lookup"><span data-stu-id="a4b58-134">Statistics</span></span>
- <span data-ttu-id="a4b58-135">Alla</span><span class="sxs-lookup"><span data-stu-id="a4b58-135">All</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="a4b58-136">-PipelineId</span></span>
<span data-ttu-id="a4b58-137">Ett valfritt ID som endast anger jobb delar av den angivna pipeline ska returneras.</span><span class="sxs-lookup"><span data-stu-id="a4b58-137">An optional ID that indicates only jobs part of the specified pipeline should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-138">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="a4b58-138">-RecurrenceId</span></span>
<span data-ttu-id="a4b58-139">Ett valfritt ID som endast anger att jobb delar av den angivna upprepningen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="a4b58-139">An optional ID that indicates only jobs part of the specified recurrence should be returned.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-140">-Resultat</span><span class="sxs-lookup"><span data-stu-id="a4b58-140">-Result</span></span>
<span data-ttu-id="a4b58-141">Anger ett resultat filter för jobb resultaten.</span><span class="sxs-lookup"><span data-stu-id="a4b58-141">Specifies a result filter for the job results.</span></span>
<span data-ttu-id="a4b58-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a4b58-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4b58-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="a4b58-143">None</span></span>
- <span data-ttu-id="a4b58-144">Annullerats</span><span class="sxs-lookup"><span data-stu-id="a4b58-144">Cancelled</span></span>
- <span data-ttu-id="a4b58-145">Startade</span><span class="sxs-lookup"><span data-stu-id="a4b58-145">Failed</span></span>
- <span data-ttu-id="a4b58-146">Utför</span><span class="sxs-lookup"><span data-stu-id="a4b58-146">Succeeded</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-147">-State</span><span class="sxs-lookup"><span data-stu-id="a4b58-147">-State</span></span>
<span data-ttu-id="a4b58-148">Anger ett status filter för jobb resultaten.</span><span class="sxs-lookup"><span data-stu-id="a4b58-148">Specifies a state filter for the job results.</span></span>
<span data-ttu-id="a4b58-149">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a4b58-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a4b58-150">Allmänt</span><span class="sxs-lookup"><span data-stu-id="a4b58-150">Accepted</span></span>
- <span data-ttu-id="a4b58-151">Nya</span><span class="sxs-lookup"><span data-stu-id="a4b58-151">New</span></span>
- <span data-ttu-id="a4b58-152">Kompilera</span><span class="sxs-lookup"><span data-stu-id="a4b58-152">Compiling</span></span>
- <span data-ttu-id="a4b58-153">Scheman</span><span class="sxs-lookup"><span data-stu-id="a4b58-153">Scheduling</span></span>
- <span data-ttu-id="a4b58-154">I kö</span><span class="sxs-lookup"><span data-stu-id="a4b58-154">Queued</span></span>
- <span data-ttu-id="a4b58-155">Sidnumrering</span><span class="sxs-lookup"><span data-stu-id="a4b58-155">Starting</span></span>
- <span data-ttu-id="a4b58-156">Pausad</span><span class="sxs-lookup"><span data-stu-id="a4b58-156">Paused</span></span>
- <span data-ttu-id="a4b58-157">Aktiv</span><span class="sxs-lookup"><span data-stu-id="a4b58-157">Running</span></span>
- <span data-ttu-id="a4b58-158">Avslutade</span><span class="sxs-lookup"><span data-stu-id="a4b58-158">Ended</span></span>

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-159">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="a4b58-159">-SubmittedAfter</span></span>
<span data-ttu-id="a4b58-160">Anger ett datum filter.</span><span class="sxs-lookup"><span data-stu-id="a4b58-160">Specifies a date filter.</span></span>
<span data-ttu-id="a4b58-161">Använd den här parametern för att filtrera jobb resultaten till jobb som har inlämnats efter det angivna datumet.</span><span class="sxs-lookup"><span data-stu-id="a4b58-161">Use this parameter to filter the job list result to jobs submitted after the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-162">-SubmittedBefore</span><span class="sxs-lookup"><span data-stu-id="a4b58-162">-SubmittedBefore</span></span>
<span data-ttu-id="a4b58-163">Anger ett datum filter.</span><span class="sxs-lookup"><span data-stu-id="a4b58-163">Specifies a date filter.</span></span>
<span data-ttu-id="a4b58-164">Använd den här parametern för att filtrera jobb resultaten till jobb som skickas före angivet datum.</span><span class="sxs-lookup"><span data-stu-id="a4b58-164">Use this parameter to filter the job list result to jobs submitted before the specified date.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-165">-Sändning</span><span class="sxs-lookup"><span data-stu-id="a4b58-165">-Submitter</span></span>
<span data-ttu-id="a4b58-166">Anger e-postadressen för en användare.</span><span class="sxs-lookup"><span data-stu-id="a4b58-166">Specifies the email address of a user.</span></span>
<span data-ttu-id="a4b58-167">Använd den här parametern för att filtrera jobb listans resultat till jobb som skickas av en viss användare.</span><span class="sxs-lookup"><span data-stu-id="a4b58-167">Use this parameter to filter the job list results to jobs submitted by a specified user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-168">-Överst</span><span class="sxs-lookup"><span data-stu-id="a4b58-168">-Top</span></span>
<span data-ttu-id="a4b58-169">Ett valfritt värde som anger hur många jobb som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="a4b58-169">An optional value which indicates the number of jobs to return.</span></span> <span data-ttu-id="a4b58-170">Standardvärdet är 500</span><span class="sxs-lookup"><span data-stu-id="a4b58-170">Default value is 500</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b58-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b58-171">CommonParameters</span></span>
<span data-ttu-id="a4b58-172">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b58-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b58-173">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b58-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b58-174">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4b58-174">INPUTS</span></span>

### <span data-ttu-id="a4b58-175">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b58-175">System.String</span></span>

### <span data-ttu-id="a4b58-176">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a4b58-176">System.Guid</span></span>

### <span data-ttu-id="a4b58-177">Microsoft. Azure. commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + ExtendedJobData</span><span class="sxs-lookup"><span data-stu-id="a4b58-177">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData</span></span>

### <span data-ttu-id="a4b58-178">System. Nullable ' 1 [[system. DateTimeOffset, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a4b58-178">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a4b58-179">Microsoft. Azure. Management. DataLake. Analytics. Models. JobState []</span><span class="sxs-lookup"><span data-stu-id="a4b58-179">Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]</span></span>

### <span data-ttu-id="a4b58-180">Microsoft. Azure. Management. DataLake. Analytics. Models. JobResult []</span><span class="sxs-lookup"><span data-stu-id="a4b58-180">Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]</span></span>

### <span data-ttu-id="a4b58-181">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a4b58-181">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a4b58-182">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a4b58-182">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a4b58-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4b58-183">OUTPUTS</span></span>

### <span data-ttu-id="a4b58-184">Microsoft. Azure. Management. DataLake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="a4b58-184">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="a4b58-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4b58-185">NOTES</span></span>

## <span data-ttu-id="a4b58-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4b58-186">RELATED LINKS</span></span>

[<span data-ttu-id="a4b58-187">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4b58-187">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a4b58-188">Skicka-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4b58-188">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="a4b58-189">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a4b58-189">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


