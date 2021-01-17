---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/submit-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Submit-AzSynapseSparkJob.md
ms.openlocfilehash: c8e710db383aae6698278ac4fb5ad7eb4344641b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403936"
---
# <span data-ttu-id="90507-101">Submit-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="90507-101">Submit-AzSynapseSparkJob</span></span>

## <span data-ttu-id="90507-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90507-102">SYNOPSIS</span></span>
<span data-ttu-id="90507-103">Skickar ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-103">Submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="90507-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90507-104">SYNTAX</span></span>

### <span data-ttu-id="90507-105">RunSparkJobParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="90507-105">RunSparkJobParameterSetName (Default)</span></span>
```
Submit-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90507-106">RunSparkJobByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90507-106">RunSparkJobByParentObjectParameterSet</span></span>
```
Submit-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -Language <String> -Name <String>
 -MainDefinitionFile <String> [-MainClassName <String>] [-CommandLineArgument <String[]>]
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90507-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90507-107">DESCRIPTION</span></span>
<span data-ttu-id="90507-108">Cmdleten **Submit-AzSynapseSparkJob** skickar ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-108">The **Submit-AzSynapseSparkJob** cmdlet submits a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="90507-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90507-109">EXAMPLES</span></span>

### <span data-ttu-id="90507-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90507-110">Example 1</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language Spark -Name WordCount_Java -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/wordcount.jar -MainClassName WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/java/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="90507-111">Det här kommandot skickar ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-111">This command submits a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="90507-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="90507-112">Example 2</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language SparkDotNet -Name WordCount_Dotnet -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/wordcount.zip -MainExecutableFile WordCount -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.dfs.core.windows.net/samples/dotnet/wordcount/result -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="90507-113">Det här kommandot skickar ett Synapse Analytics Spark .NET-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-113">This command submits a Synapse Analytics Spark .NET job.</span></span>

### <span data-ttu-id="90507-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="90507-114">Example 3</span></span>
```powershell
PS C:\> Submit-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Language PySpark -Name WordCount_Python -MainDefinitionFile abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/wordcount.py -CommandLineArguments abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/shakespeare.txt,abfss://ContosoFileSystem@ContosoGen2Storage.blob.core.windows.net/samples/python/wordcount/result/ -ExecutorCount 2 -ExecutorSize Small
```

<span data-ttu-id="90507-115">Det här kommandot skickar ett Synapse Analytics PySpark-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-115">This command submits a Synapse Analytics PySpark job.</span></span>

## <span data-ttu-id="90507-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90507-116">PARAMETERS</span></span>

### <span data-ttu-id="90507-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="90507-117">-CommandLineArgument</span></span>
<span data-ttu-id="90507-118">Valfria argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="90507-118">Optional arguments to the job.</span></span> <span data-ttu-id="90507-119">t. ex. "--upprepning 10000--timeout 20s"</span><span class="sxs-lookup"><span data-stu-id="90507-119">e.g. "--iteration 10000 --timeout 20s"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-120">-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="90507-120">-Configuration</span></span>
<span data-ttu-id="90507-121">Egenskaper för Spark-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="90507-121">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90507-122">-DefaultProfile</span></span>
<span data-ttu-id="90507-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="90507-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90507-124">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="90507-124">-ExecutorCount</span></span>
<span data-ttu-id="90507-125">Antal exekverare som ska tilldelas i den angivna Spark-poolen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="90507-125">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-126">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="90507-126">-ExecutorSize</span></span>
<span data-ttu-id="90507-127">Antal kärnor och minne som ska användas för utförare som tilldelats till det angivna Spark-poolen för jobbet.</span><span class="sxs-lookup"><span data-stu-id="90507-127">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-128">-Språk</span><span class="sxs-lookup"><span data-stu-id="90507-128">-Language</span></span>
<span data-ttu-id="90507-129">Språk för jobbet som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="90507-129">Language of the job to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-130">-MainClassName</span><span class="sxs-lookup"><span data-stu-id="90507-130">-MainClassName</span></span>
<span data-ttu-id="90507-131">Den fullständigt kvalificerade identifieraren eller den huvud klass som finns i huvud definitions filen.</span><span class="sxs-lookup"><span data-stu-id="90507-131">The fully-qualified identifier or the main class that is in the main definition file.</span></span>
<span data-ttu-id="90507-132">Krävs för Spark-och .NET Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-132">Required for Spark and .NET Spark job.</span></span>
<span data-ttu-id="90507-133">t. ex. "org. apache. Spark. exempel. SparkPi"</span><span class="sxs-lookup"><span data-stu-id="90507-133">e.g. "org.apache.spark.examples.SparkPi"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MainExecutableFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-134">-MainDefinitionFile</span><span class="sxs-lookup"><span data-stu-id="90507-134">-MainDefinitionFile</span></span>
<span data-ttu-id="90507-135">Den huvud fil som används för jobbet.</span><span class="sxs-lookup"><span data-stu-id="90507-135">The main file used for the job.</span></span>
<span data-ttu-id="90507-136">till exempel " abfss://filesystem@account.dfs.core.windows.net/mySpark.jar "</span><span class="sxs-lookup"><span data-stu-id="90507-136">e.g. "abfss://filesystem@account.dfs.core.windows.net/mySpark.jar"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="90507-137">-Name</span></span>
<span data-ttu-id="90507-138">Namn på Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="90507-138">Name of Spark job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-139">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="90507-139">-ReferenceFile</span></span>
<span data-ttu-id="90507-140">Ytterligare filer som används för referens i huvud definitions filen.</span><span class="sxs-lookup"><span data-stu-id="90507-140">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="90507-141">Lista med kommaavgränsade lagrings-URI.</span><span class="sxs-lookup"><span data-stu-id="90507-141">Comma-separated storage URI list.</span></span> <span data-ttu-id="90507-142">till exempel " abfss://filesystem@account.dfs.core.windows.net/file1.txt , abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="90507-142">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-143">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="90507-143">-SparkPoolName</span></span>
<span data-ttu-id="90507-144">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="90507-144">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-145">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="90507-145">-SparkPoolObject</span></span>
<span data-ttu-id="90507-146">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="90507-146">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: RunSparkJobByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90507-147">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="90507-147">-WorkspaceName</span></span>
<span data-ttu-id="90507-148">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="90507-148">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkJobParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90507-149">-Confirm</span></span>
<span data-ttu-id="90507-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90507-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90507-151">-WhatIf</span></span>
<span data-ttu-id="90507-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90507-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90507-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90507-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90507-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90507-154">CommonParameters</span></span>
<span data-ttu-id="90507-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90507-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90507-156">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90507-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90507-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90507-157">INPUTS</span></span>

### <span data-ttu-id="90507-158">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="90507-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="90507-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90507-159">OUTPUTS</span></span>

### <span data-ttu-id="90507-160">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="90507-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="90507-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90507-161">NOTES</span></span>

## <span data-ttu-id="90507-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90507-162">RELATED LINKS</span></span>
