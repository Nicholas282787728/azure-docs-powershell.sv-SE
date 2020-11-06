---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/submit-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: acd61ac9da39a56cf03499d0a2a4fcd25d321525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580187"
---
# <span data-ttu-id="34eb4-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="34eb4-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="34eb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="34eb4-103">Skickar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="34eb4-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34eb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34eb4-104">SYNTAX</span></span>

### <span data-ttu-id="34eb4-105">SubmitUSqlJobWithScriptPath</span><span class="sxs-lookup"><span data-stu-id="34eb4-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34eb4-106">SubmitUSqlJob</span><span class="sxs-lookup"><span data-stu-id="34eb4-106">SubmitUSqlJob</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34eb4-107">SubmitUSqlJobWithScriptPathAndRecurrence</span><span class="sxs-lookup"><span data-stu-id="34eb4-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34eb4-108">SubmitUSqlJobWithRecurrence</span><span class="sxs-lookup"><span data-stu-id="34eb4-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34eb4-109">SubmitUSqlJobWithScriptPathAndPipeline</span><span class="sxs-lookup"><span data-stu-id="34eb4-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34eb4-110">SubmitUSqlJobWithPipeline</span><span class="sxs-lookup"><span data-stu-id="34eb4-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>]
 [[-Priority] <Int32>] [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 -PipelineId <Guid> [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34eb4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34eb4-111">DESCRIPTION</span></span>
<span data-ttu-id="34eb4-112">Cmdleten **Submit-AzureRmDataLakeAnalyticsJob** skickar ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="34eb4-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="34eb4-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34eb4-113">EXAMPLES</span></span>

### <span data-ttu-id="34eb4-114">Exempel 1: Skicka ett jobb</span><span class="sxs-lookup"><span data-stu-id="34eb4-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="34eb4-115">Det här kommandot skickar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="34eb4-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="34eb4-116">Exempel 2: Skicka ett jobb med skript parametrar</span><span class="sxs-lookup"><span data-stu-id="34eb4-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="34eb4-117">Parametrarna U-SQL-skript är läggs till ovanför huvud skript innehållet, t. ex.: DECLARE- @Department sträng = "försäljning"; DEKLARERA @NumRecords int = 1000; DECLARE @StartDateTime datetime = ny datetime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="34eb4-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="34eb4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34eb4-118">PARAMETERS</span></span>

### <span data-ttu-id="34eb4-119">-Konto</span><span class="sxs-lookup"><span data-stu-id="34eb4-119">-Account</span></span>
<span data-ttu-id="34eb4-120">Namnet på det data Lake Analytics-konto som jobbet ska skickas till.</span><span class="sxs-lookup"><span data-stu-id="34eb4-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="34eb4-121">-AnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="34eb4-121">-AnalyticsUnits</span></span>
<span data-ttu-id="34eb4-122">De analys enheter som ska användas för detta jobb.</span><span class="sxs-lookup"><span data-stu-id="34eb4-122">The analytics units to use for this job.</span></span> <span data-ttu-id="34eb4-123">Vanligt vis är mer analys enheter som är dedikerade till ett skript att köra tid för snabbare skript.</span><span class="sxs-lookup"><span data-stu-id="34eb4-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

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

### <span data-ttu-id="34eb4-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="34eb4-124">-CompileMode</span></span>
<span data-ttu-id="34eb4-125">Den typ av kompilering som ska göras för detta jobb.</span><span class="sxs-lookup"><span data-stu-id="34eb4-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="34eb4-126">Giltiga värden:</span><span class="sxs-lookup"><span data-stu-id="34eb4-126">Valid values:</span></span> 
- <span data-ttu-id="34eb4-127">Semantisk (utför endast semantiska kontroller och nödvändiga Sanity kontroller)</span><span class="sxs-lookup"><span data-stu-id="34eb4-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="34eb4-128">Fullständig (fullständig kompilering)</span><span class="sxs-lookup"><span data-stu-id="34eb4-128">Full (Full compilation)</span></span>
- <span data-ttu-id="34eb4-129">Enkel (fullständig kompilering)</span><span class="sxs-lookup"><span data-stu-id="34eb4-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="34eb4-130">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="34eb4-130">-CompileOnly</span></span>
<span data-ttu-id="34eb4-131">Anger att sändningen endast ska bygga jobbet och inte köras om värdet är true.</span><span class="sxs-lookup"><span data-stu-id="34eb4-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="34eb4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34eb4-132">-DefaultProfile</span></span>
<span data-ttu-id="34eb4-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="34eb4-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34eb4-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="34eb4-134">-Name</span></span>
<span data-ttu-id="34eb4-135">Det egna namnet på det jobb som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="34eb4-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="34eb4-136">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="34eb4-136">-PipelineId</span></span>
<span data-ttu-id="34eb4-137">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb och som också är kopplat till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="34eb4-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

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

### <span data-ttu-id="34eb4-138">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="34eb4-138">-PipelineName</span></span>
<span data-ttu-id="34eb4-139">Ett valfritt eget namn för den pipeline som är associerad med jobbet.</span><span class="sxs-lookup"><span data-stu-id="34eb4-139">An optional friendly name for the pipeline associated with this job.</span></span>

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

### <span data-ttu-id="34eb4-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="34eb4-140">-PipelineUri</span></span>
<span data-ttu-id="34eb4-141">En valfri URI som länkar till den ursprungliga tjänst som är associerad med den här pipeline.</span><span class="sxs-lookup"><span data-stu-id="34eb4-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

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

### <span data-ttu-id="34eb4-142">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="34eb4-142">-Priority</span></span>
<span data-ttu-id="34eb4-143">Prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="34eb4-143">The priority of the job.</span></span> <span data-ttu-id="34eb4-144">Om det inte anges är prioriteten 1000.</span><span class="sxs-lookup"><span data-stu-id="34eb4-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="34eb4-145">Ett lägre värde indikerar en högre jobb prioritet.</span><span class="sxs-lookup"><span data-stu-id="34eb4-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="34eb4-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="34eb4-146">-RecurrenceId</span></span>
<span data-ttu-id="34eb4-147">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb med samma återkommande-ID.</span><span class="sxs-lookup"><span data-stu-id="34eb4-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

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

### <span data-ttu-id="34eb4-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="34eb4-148">-RecurrenceName</span></span>
<span data-ttu-id="34eb4-149">Ett valfritt eget namn för upprepnings korrelationen mellan jobb.</span><span class="sxs-lookup"><span data-stu-id="34eb4-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

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

### <span data-ttu-id="34eb4-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="34eb4-150">-RunId</span></span>
<span data-ttu-id="34eb4-151">Ett ID som identifierar den här specifika kör-iterationen för pipelinen.</span><span class="sxs-lookup"><span data-stu-id="34eb4-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

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

### <span data-ttu-id="34eb4-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="34eb4-152">-Runtime</span></span>
<span data-ttu-id="34eb4-153">Ange eventuellt den version av körnings miljön som ska användas för jobbet.</span><span class="sxs-lookup"><span data-stu-id="34eb4-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="34eb4-154">Om alternativet Left ununset är valt används standard miljön.</span><span class="sxs-lookup"><span data-stu-id="34eb4-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="34eb4-155">-Skript</span><span class="sxs-lookup"><span data-stu-id="34eb4-155">-Script</span></span>
<span data-ttu-id="34eb4-156">Skript att köra (skriven infogad).</span><span class="sxs-lookup"><span data-stu-id="34eb4-156">Script to execute (written inline).</span></span>

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

### <span data-ttu-id="34eb4-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="34eb4-157">-ScriptParameter</span></span>
<span data-ttu-id="34eb4-158">Skript parametrar för det här jobbet, som en ord lista med parameter namn (sträng) till värden (valfri kombination av byte, SByte, int, uint (eller UInt32), Long, ulong (eller UInt64), flyt, dubbel, decimal, Short (eller Int16), ushort (eller UInt16), char, String, DateTime, bool eller byte []).</span><span class="sxs-lookup"><span data-stu-id="34eb4-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

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

### <span data-ttu-id="34eb4-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="34eb4-159">-ScriptPath</span></span>
<span data-ttu-id="34eb4-160">Sökväg till skript filen som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="34eb4-160">Path to the script file to submit.</span></span>

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

### <span data-ttu-id="34eb4-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34eb4-161">CommonParameters</span></span>
<span data-ttu-id="34eb4-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34eb4-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34eb4-163">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34eb4-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34eb4-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34eb4-164">INPUTS</span></span>

### <span data-ttu-id="34eb4-165">System. String</span><span class="sxs-lookup"><span data-stu-id="34eb4-165">System.String</span></span>

### <span data-ttu-id="34eb4-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="34eb4-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="34eb4-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="34eb4-167">System.Int32</span></span>

### <span data-ttu-id="34eb4-168">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="34eb4-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="34eb4-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="34eb4-169">System.Guid</span></span>

### <span data-ttu-id="34eb4-170">System. Nullable ' 1 [[system. GUID, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="34eb4-170">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="34eb4-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34eb4-171">OUTPUTS</span></span>

### <span data-ttu-id="34eb4-172">Microsoft. Azure. Management. DataLake. Analytics. Models. JobInformation</span><span class="sxs-lookup"><span data-stu-id="34eb4-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="34eb4-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34eb4-173">NOTES</span></span>

## <span data-ttu-id="34eb4-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34eb4-174">RELATED LINKS</span></span>

[<span data-ttu-id="34eb4-175">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="34eb4-175">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="34eb4-176">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="34eb4-176">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="34eb4-177">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="34eb4-177">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


