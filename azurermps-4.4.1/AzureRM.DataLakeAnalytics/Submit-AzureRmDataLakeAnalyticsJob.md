---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580652"
---
# <span data-ttu-id="c8107-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c8107-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="c8107-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8107-102">SYNOPSIS</span></span>
<span data-ttu-id="c8107-103">Skickar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="c8107-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8107-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8107-104">SYNTAX</span></span>

### <span data-ttu-id="c8107-105">Skicka jobb med skript Sök väg för U-SQL</span><span class="sxs-lookup"><span data-stu-id="c8107-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8107-106">Skicka U-SQL-jobb</span><span class="sxs-lookup"><span data-stu-id="c8107-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8107-107">Skicka jobb med skript Sök väg för U-SQL med reucurrence information</span><span class="sxs-lookup"><span data-stu-id="c8107-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8107-108">Skicka U-SQL-jobb med upprepnings information</span><span class="sxs-lookup"><span data-stu-id="c8107-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8107-109">Skicka jobb med skript Sök väg för U-SQL med reucurrence och pipeline-uppgifter</span><span class="sxs-lookup"><span data-stu-id="c8107-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8107-110">Skicka U-SQL-jobb med information om upprepning och pipeline</span><span class="sxs-lookup"><span data-stu-id="c8107-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8107-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8107-111">DESCRIPTION</span></span>
<span data-ttu-id="c8107-112">Cmdleten **Submit-AzureRmDataLakeAnalyticsJob** skickar ett Azure Data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="c8107-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="c8107-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8107-113">EXAMPLES</span></span>

### <span data-ttu-id="c8107-114">Exempel 1: Skicka ett jobb</span><span class="sxs-lookup"><span data-stu-id="c8107-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="c8107-115">Det här kommandot skickar ett data Lake Analytics-jobb.</span><span class="sxs-lookup"><span data-stu-id="c8107-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="c8107-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8107-116">PARAMETERS</span></span>

### <span data-ttu-id="c8107-117">-Konto</span><span class="sxs-lookup"><span data-stu-id="c8107-117">-Account</span></span>
<span data-ttu-id="c8107-118">Anger namnet på data Lake Analytics-kontot.</span><span class="sxs-lookup"><span data-stu-id="c8107-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c8107-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="c8107-119">-CompileMode</span></span>
<span data-ttu-id="c8107-120">Anger jobbets kompileringstid.</span><span class="sxs-lookup"><span data-stu-id="c8107-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="c8107-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c8107-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c8107-122">Semantik</span><span class="sxs-lookup"><span data-stu-id="c8107-122">Semantic</span></span>
- <span data-ttu-id="c8107-123">Fullständiga</span><span class="sxs-lookup"><span data-stu-id="c8107-123">Full</span></span>
- <span data-ttu-id="c8107-124">En enda</span><span class="sxs-lookup"><span data-stu-id="c8107-124">SingleBox</span></span>

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

### <span data-ttu-id="c8107-125">-CompileOnly</span><span class="sxs-lookup"><span data-stu-id="c8107-125">-CompileOnly</span></span>
<span data-ttu-id="c8107-126">Anger att denna cmdlet kompilerar jobbet utan att köra det.</span><span class="sxs-lookup"><span data-stu-id="c8107-126">Indicates that this cmdlet compiles the job without running it.</span></span>

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

### <span data-ttu-id="c8107-127">-DegreeOfParallelism</span><span class="sxs-lookup"><span data-stu-id="c8107-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="c8107-128">Anger de data Lake Analytics-enheter (DLAU) för jobbet, vilket anger det högsta tillåtna parallellt för jobbet.</span><span class="sxs-lookup"><span data-stu-id="c8107-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8107-129">-Name</span></span>
<span data-ttu-id="c8107-130">Anger jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="c8107-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="c8107-131">-PipelineId</span><span class="sxs-lookup"><span data-stu-id="c8107-131">-PipelineId</span></span>
<span data-ttu-id="c8107-132">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb och som också är kopplat till ett projekt.</span><span class="sxs-lookup"><span data-stu-id="c8107-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-133">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="c8107-133">-PipelineName</span></span>
<span data-ttu-id="c8107-134">Ett valfritt eget namn för den pipeline som är associerad med jobbet.</span><span class="sxs-lookup"><span data-stu-id="c8107-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="c8107-135">-PipelineUri</span></span>
<span data-ttu-id="c8107-136">En valfri URI som länkar till den ursprungliga tjänst som är associerad med den här pipeline.</span><span class="sxs-lookup"><span data-stu-id="c8107-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-137">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="c8107-137">-Priority</span></span>
<span data-ttu-id="c8107-138">Anger prioriteten för jobbet.</span><span class="sxs-lookup"><span data-stu-id="c8107-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="c8107-139">Om det inte anges är prioriteten 1000.</span><span class="sxs-lookup"><span data-stu-id="c8107-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="c8107-140">Ett lågt nummer indikerar en högre jobb prioritet.</span><span class="sxs-lookup"><span data-stu-id="c8107-140">A low number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="c8107-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="c8107-141">-RecurrenceId</span></span>
<span data-ttu-id="c8107-142">Ett ID som anger att det här jobbet skickas är en del av en uppsättning återkommande jobb med samma återkommande-ID.</span><span class="sxs-lookup"><span data-stu-id="c8107-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-143">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="c8107-143">-RecurrenceName</span></span>
<span data-ttu-id="c8107-144">Ett valfritt eget namn för upprepnings korrelationen mellan jobb.</span><span class="sxs-lookup"><span data-stu-id="c8107-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="c8107-145">-RunId</span></span>
<span data-ttu-id="c8107-146">Ett ID som identifierar den här specifika kör-iterationen för pipelinen.</span><span class="sxs-lookup"><span data-stu-id="c8107-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="c8107-147">-Runtime</span></span>
<span data-ttu-id="c8107-148">Anger kör tids versionen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="c8107-148">Specifies the runtime version of the job.</span></span>

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

### <span data-ttu-id="c8107-149">-Skript</span><span class="sxs-lookup"><span data-stu-id="c8107-149">-Script</span></span>
<span data-ttu-id="c8107-150">Anger innehållet i det skript som ska köras.</span><span class="sxs-lookup"><span data-stu-id="c8107-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="c8107-151">-ScriptPath</span></span>
<span data-ttu-id="c8107-152">Anger den lokala fil Sök vägen till det skript som ska köras.</span><span class="sxs-lookup"><span data-stu-id="c8107-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8107-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8107-153">-DefaultProfile</span></span>
<span data-ttu-id="c8107-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8107-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8107-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8107-155">CommonParameters</span></span>
<span data-ttu-id="c8107-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8107-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8107-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8107-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8107-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8107-158">INPUTS</span></span>

### <span data-ttu-id="c8107-159">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c8107-159">String</span></span>
<span data-ttu-id="c8107-160">Parametern "skript" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="c8107-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c8107-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8107-161">OUTPUTS</span></span>

### <span data-ttu-id="c8107-162">JobInformation</span><span class="sxs-lookup"><span data-stu-id="c8107-162">JobInformation</span></span>
<span data-ttu-id="c8107-163">Den ursprungliga jobb informationen för det skickade jobbet.</span><span class="sxs-lookup"><span data-stu-id="c8107-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="c8107-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8107-164">NOTES</span></span>

## <span data-ttu-id="c8107-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8107-165">RELATED LINKS</span></span>

[<span data-ttu-id="c8107-166">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c8107-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c8107-167">Stopp-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c8107-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="c8107-168">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="c8107-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


