---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: fc09560bca0d825cc65d8a4f964119cd50898190
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574308"
---
# <span data-ttu-id="f866c-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f866c-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="f866c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f866c-102">SYNOPSIS</span></span>
<span data-ttu-id="f866c-103">Skickar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f866c-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f866c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f866c-104">SYNTAX</span></span>

### <span data-ttu-id="f866c-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="f866c-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f866c-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="f866c-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f866c-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="f866c-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f866c-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="f866c-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f866c-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="f866c-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f866c-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="f866c-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f866c-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f866c-111">DESCRIPTION</span></span>
<span data-ttu-id="f866c-112">Cmdleten **Submit-AzureRmDataLakeAnalyticsJob** skickar ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="f866c-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="f866c-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f866c-113">EXAMPLES</span></span>

### <span data-ttu-id="f866c-114">Exempel 1: Skicka ett jobb</span><span class="sxs-lookup"><span data-stu-id="f866c-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="f866c-115">Det här kommandot skickar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="f866c-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="f866c-116">Exempel 2: Skicka ett jobb med skript parametrar</span><span class="sxs-lookup"><span data-stu-id="f866c-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="f866c-117">Parametrarna U-SQL-skript är läggs till ovanför huvud skript innehållet, till exempel:</span><span class="sxs-lookup"><span data-stu-id="f866c-117">U-SQL script parameters are prepended above the main script contents, e.g.:</span></span>

<span data-ttu-id="f866c-118">DECLARE @Department String = "försäljning"; DEKLARERA @NumRecords int = 1000; DECLARE @StartDateTime datetime = ny datetime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="f866c-118">DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="f866c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f866c-119">PARAMETERS</span></span>

### <span data-ttu-id="f866c-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="f866c-120">-Account</span></span>
<span data-ttu-id="f866c-121">Namnet på det data Lake Analytics-konto som jobbet ska skickas till.</span><span class="sxs-lookup"><span data-stu-id="f866c-121">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="f866c-122">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="f866c-122">-CompileMode</span></span>
<span data-ttu-id="f866c-123">Den typ av kompilering som ska göras för detta jobb.</span><span class="sxs-lookup"><span data-stu-id="f866c-123">The type of compilation to be done on this job.</span></span> <span data-ttu-id="f866c-124">Giltiga värden:</span><span class="sxs-lookup"><span data-stu-id="f866c-124">Valid values:</span></span> 

- <span data-ttu-id="f866c-125">Semantisk (utför endast semantiska kontroller och nödvändiga Sanity kontroller)</span><span class="sxs-lookup"><span data-stu-id="f866c-125">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="f866c-126">Fullständig (fullständig kompilering)</span><span class="sxs-lookup"><span data-stu-id="f866c-126">Full (Full compilation)</span></span>
- <span data-ttu-id="f866c-127">Enkel (fullständig kompilering)</span><span class="sxs-lookup"><span data-stu-id="f866c-127">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-128">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="f866c-128">-CompileOnly</span></span>
<span data-ttu-id="f866c-129">Anger att sändningen endast ska bygga jobbet och inte köras om värdet är true.</span><span class="sxs-lookup"><span data-stu-id="f866c-129">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f866c-130">-DefaultProfile</span></span>
<span data-ttu-id="f866c-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f866c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f866c-132">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="f866c-132">-AnalyticsUnits</span></span>
<span data-ttu-id="f866c-133">De analys enheter som ska användas för detta jobb.</span><span class="sxs-lookup"><span data-stu-id="f866c-133">The analytics units to use for this job.</span></span> <span data-ttu-id="f866c-134">Vanligt vis är mer analys enheter som är dedikerade till ett skript att köra tid för snabbare skript.</span><span class="sxs-lookup"><span data-stu-id="f866c-134">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="f866c-135">-Name</span></span>
<span data-ttu-id="f866c-136">Det egna namnet på det jobb som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="f866c-136">The friendly name of the job to submit.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-137">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="f866c-137">-PipelineId</span></span>
<span data-ttu-id="f866c-138">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb och som också är kopplat till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="f866c-138">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-139">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="f866c-139">-PipelineName</span></span>
<span data-ttu-id="f866c-140">Ett valfritt eget namn för den pipeline som är associerad med jobbet.</span><span class="sxs-lookup"><span data-stu-id="f866c-140">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-141">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="f866c-141">-PipelineUri</span></span>
<span data-ttu-id="f866c-142">En valfri URI som länkar till den ursprungliga tjänst som är associerad med den här pipeline.</span><span class="sxs-lookup"><span data-stu-id="f866c-142">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-143">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="f866c-143">-Priority</span></span>
<span data-ttu-id="f866c-144">Prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f866c-144">The priority of the job.</span></span> <span data-ttu-id="f866c-145">Om det inte anges är prioriteten 1000.</span><span class="sxs-lookup"><span data-stu-id="f866c-145">If not specified, the priority is 1000.</span></span> <span data-ttu-id="f866c-146">Ett lägre värde indikerar en högre jobb prioritet.</span><span class="sxs-lookup"><span data-stu-id="f866c-146">A lower number indicates a higher job priority.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-147">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="f866c-147">-RecurrenceId</span></span>
<span data-ttu-id="f866c-148">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb med samma återkommande-ID.</span><span class="sxs-lookup"><span data-stu-id="f866c-148">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-149">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="f866c-149">-RecurrenceName</span></span>
<span data-ttu-id="f866c-150">Ett valfritt eget namn för upprepnings korrelationen mellan jobb.</span><span class="sxs-lookup"><span data-stu-id="f866c-150">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-151">-RunId</span><span class="sxs-lookup"><span data-stu-id="f866c-151">-RunId</span></span>
<span data-ttu-id="f866c-152">Ett ID som identifierar den här specifika kör-iterationen för pipelinen.</span><span class="sxs-lookup"><span data-stu-id="f866c-152">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-153">-Runtime</span><span class="sxs-lookup"><span data-stu-id="f866c-153">-Runtime</span></span>
<span data-ttu-id="f866c-154">Ange eventuellt den version av körnings miljön som ska användas för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f866c-154">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="f866c-155">Om alternativet Left ununset är valt används standard miljön.</span><span class="sxs-lookup"><span data-stu-id="f866c-155">If left unset, the default runtime is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-156">-Skript</span><span class="sxs-lookup"><span data-stu-id="f866c-156">-Script</span></span>
<span data-ttu-id="f866c-157">Skript att köra (skriven infogad).</span><span class="sxs-lookup"><span data-stu-id="f866c-157">Script to execute (written inline).</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-158">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="f866c-158">-ScriptParameter</span></span>
<span data-ttu-id="f866c-159">Skript parametrar för det här jobbet, som en ord lista med parameter namn (sträng) till värden (valfri kombination av byte, SByte, int, uint (eller UInt32), Long, ulong (eller UInt64), flyt, dubbel, decimal, Short (eller Int16), ushort (eller UInt16), char, String, DateTime, bool eller byte []).</span><span class="sxs-lookup"><span data-stu-id="f866c-159">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-160">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="f866c-160">-ScriptPath</span></span>
<span data-ttu-id="f866c-161">Sökväg till skript filen som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="f866c-161">Path to the script file to submit.</span></span>

```yaml
Type: String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f866c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f866c-162">CommonParameters</span></span>
<span data-ttu-id="f866c-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f866c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f866c-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f866c-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f866c-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f866c-165">INPUTS</span></span>

### <span data-ttu-id="f866c-166">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="f866c-166">String</span></span>
<span data-ttu-id="f866c-167">Parametern "skript" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="f866c-167">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="f866c-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f866c-168">OUTPUTS</span></span>

### <span data-ttu-id="f866c-169">JobInformation</span><span class="sxs-lookup"><span data-stu-id="f866c-169">JobInformation</span></span>
<span data-ttu-id="f866c-170">Den ursprungliga jobb informationen för det skickade jobbet.</span><span class="sxs-lookup"><span data-stu-id="f866c-170">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="f866c-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f866c-171">NOTES</span></span>

## <span data-ttu-id="f866c-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f866c-172">RELATED LINKS</span></span>

[<span data-ttu-id="f866c-173">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f866c-173">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f866c-174">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f866c-174">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="f866c-175">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="f866c-175">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


