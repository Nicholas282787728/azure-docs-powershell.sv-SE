---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526155"
---
# <span data-ttu-id="9d88d-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9d88d-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="9d88d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d88d-102">SYNOPSIS</span></span>
<span data-ttu-id="9d88d-103">Skickar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="9d88d-103">Submits a job.</span></span>

## <span data-ttu-id="9d88d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d88d-104">SYNTAX</span></span>

### <span data-ttu-id="9d88d-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="9d88d-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d88d-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="9d88d-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d88d-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="9d88d-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d88d-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="9d88d-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d88d-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="9d88d-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d88d-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="9d88d-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d88d-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d88d-111">DESCRIPTION</span></span>
<span data-ttu-id="9d88d-112">Cmdleten **Submit-AzDataLakeAnalyticsJob** skickar ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="9d88d-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="9d88d-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d88d-113">EXAMPLES</span></span>

### <span data-ttu-id="9d88d-114">Exempel 1: Skicka ett jobb</span><span class="sxs-lookup"><span data-stu-id="9d88d-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="9d88d-115">Det här kommandot skickar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="9d88d-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="9d88d-116">Exempel 2: Skicka ett jobb med skript parametrar</span><span class="sxs-lookup"><span data-stu-id="9d88d-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="9d88d-117">Parametrarna U-SQL-skript är läggs till ovanför huvud skript innehållet, t. ex.: DECLARE- @Department sträng = "försäljning"; DEKLARERA @NumRecords int = 1000; DECLARE @StartDateTime datetime = ny datetime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="9d88d-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="9d88d-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d88d-118">PARAMETERS</span></span>

### <span data-ttu-id="9d88d-119">-Konto</span><span class="sxs-lookup"><span data-stu-id="9d88d-119">-Account</span></span>
<span data-ttu-id="9d88d-120">Namnet på det data Lake Analytics-konto som jobbet ska skickas till.</span><span class="sxs-lookup"><span data-stu-id="9d88d-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="9d88d-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="9d88d-121">-AnalyticsUnits</span></span>
<span data-ttu-id="9d88d-122">De analys enheter som ska användas för detta jobb.</span><span class="sxs-lookup"><span data-stu-id="9d88d-122">The analytics units to use for this job.</span></span> <span data-ttu-id="9d88d-123">Vanligt vis är mer analys enheter som är dedikerade till ett skript att köra tid för snabbare skript.</span><span class="sxs-lookup"><span data-stu-id="9d88d-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="9d88d-124">-CompileMode</span></span>
<span data-ttu-id="9d88d-125">Den typ av kompilering som ska göras för detta jobb.</span><span class="sxs-lookup"><span data-stu-id="9d88d-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="9d88d-126">Giltiga värden:</span><span class="sxs-lookup"><span data-stu-id="9d88d-126">Valid values:</span></span> 
- <span data-ttu-id="9d88d-127">Semantisk (utför endast semantiska kontroller och nödvändiga Sanity kontroller)</span><span class="sxs-lookup"><span data-stu-id="9d88d-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="9d88d-128">Fullständig (fullständig kompilering)</span><span class="sxs-lookup"><span data-stu-id="9d88d-128">Full (Full compilation)</span></span>
- <span data-ttu-id="9d88d-129">Enkel (fullständig kompilering)</span><span class="sxs-lookup"><span data-stu-id="9d88d-129">SingleBox (Full compilation performed locally)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="9d88d-130">-CompileOnly</span></span>
<span data-ttu-id="9d88d-131">Anger att sändningen endast ska bygga jobbet och inte köras om värdet är true.</span><span class="sxs-lookup"><span data-stu-id="9d88d-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d88d-132">-DefaultProfile</span></span>
<span data-ttu-id="9d88d-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9d88d-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d88d-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d88d-134">-Name</span></span>
<span data-ttu-id="9d88d-135">Det egna namnet på det jobb som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="9d88d-135">The friendly name of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="9d88d-136">-PipelineId</span></span>
<span data-ttu-id="9d88d-137">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb och som också är kopplat till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="9d88d-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="9d88d-138">-PipelineName</span></span>
<span data-ttu-id="9d88d-139">Ett valfritt eget namn för den pipeline som är associerad med jobbet.</span><span class="sxs-lookup"><span data-stu-id="9d88d-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="9d88d-140">-PipelineUri</span></span>
<span data-ttu-id="9d88d-141">En valfri URI som länkar till den ursprungliga tjänst som är associerad med den här pipeline.</span><span class="sxs-lookup"><span data-stu-id="9d88d-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-142">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="9d88d-142">-Priority</span></span>
<span data-ttu-id="9d88d-143">Prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9d88d-143">The priority of the job.</span></span> <span data-ttu-id="9d88d-144">Om det inte anges är prioriteten 1000.</span><span class="sxs-lookup"><span data-stu-id="9d88d-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="9d88d-145">Ett lägre värde indikerar en högre jobb prioritet.</span><span class="sxs-lookup"><span data-stu-id="9d88d-145">A lower number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="9d88d-146">-RecurrenceId</span></span>
<span data-ttu-id="9d88d-147">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb med samma återkommande-ID.</span><span class="sxs-lookup"><span data-stu-id="9d88d-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="9d88d-148">-RecurrenceName</span></span>
<span data-ttu-id="9d88d-149">Ett valfritt eget namn för upprepnings korrelationen mellan jobb.</span><span class="sxs-lookup"><span data-stu-id="9d88d-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="9d88d-150">-RunId</span></span>
<span data-ttu-id="9d88d-151">Ett ID som identifierar den här specifika kör-iterationen för pipelinen.</span><span class="sxs-lookup"><span data-stu-id="9d88d-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="9d88d-152">-Runtime</span></span>
<span data-ttu-id="9d88d-153">Ange eventuellt den version av körnings miljön som ska användas för jobbet.</span><span class="sxs-lookup"><span data-stu-id="9d88d-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="9d88d-154">Om alternativet Left ununset är valt används standard miljön.</span><span class="sxs-lookup"><span data-stu-id="9d88d-154">If left unset, the default runtime is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-155">-Skript</span><span class="sxs-lookup"><span data-stu-id="9d88d-155">-Script</span></span>
<span data-ttu-id="9d88d-156">Skript att köra (skriven infogad).</span><span class="sxs-lookup"><span data-stu-id="9d88d-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="9d88d-157">-ScriptParameter</span></span>
<span data-ttu-id="9d88d-158">Skript parametrar för det här jobbet, som en ord lista med parameter namn (sträng) till värden (valfri kombination av byte, SByte, int, uint (eller UInt32), Long, ulong (eller UInt64), flyt, dubbel, decimal, Short (eller Int16), ushort (eller UInt16), char, String, DateTime, bool eller byte []).</span><span class="sxs-lookup"><span data-stu-id="9d88d-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="9d88d-159">-ScriptPath</span></span>
<span data-ttu-id="9d88d-160">Sökväg till skript filen som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="9d88d-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d88d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d88d-161">CommonParameters</span></span>
<span data-ttu-id="9d88d-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d88d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d88d-163">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d88d-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d88d-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d88d-164">INPUTS</span></span>

### <span data-ttu-id="9d88d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="9d88d-165">System.String</span></span>

### <span data-ttu-id="9d88d-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9d88d-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9d88d-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9d88d-167">System.Int32</span></span>

### <span data-ttu-id="9d88d-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9d88d-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="9d88d-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9d88d-169">System.Guid</span></span>

### <span data-ttu-id="9d88d-170">System. Nullable ' 1 [[system. GUID, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9d88d-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9d88d-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d88d-171">OUTPUTS</span></span>

### <span data-ttu-id="9d88d-172">Microsoft. Azure. Management. DataLake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="9d88d-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="9d88d-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d88d-173">NOTES</span></span>

## <span data-ttu-id="9d88d-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d88d-174">RELATED LINKS</span></span>

[<span data-ttu-id="9d88d-175">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9d88d-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="9d88d-176">Stopp-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9d88d-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="9d88d-177">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9d88d-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


