---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 824F6302-6285-4AEC-A63C-E2519DE4C7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2597d66e87de682bbf5702085612f7338d75deac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099239"
---
# <span data-ttu-id="84b56-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="84b56-101">New-AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="84b56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84b56-102">SYNOPSIS</span></span>
<span data-ttu-id="84b56-103">Definierar ett nytt strömmande MapReduce-jobb.</span><span class="sxs-lookup"><span data-stu-id="84b56-103">Defines a new streaming MapReduce job.</span></span>

## <span data-ttu-id="84b56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84b56-104">SYNTAX</span></span>

```
New-AzureHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-CmdEnv <String[]>]
 [-Combiner <String>] [-Defines <Hashtable>] [-Files <String[]>] [-InputPath <String>] [-JobName <String>]
 [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="84b56-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84b56-105">DESCRIPTION</span></span>
<span data-ttu-id="84b56-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="84b56-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="84b56-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="84b56-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="84b56-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="84b56-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="84b56-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="84b56-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="84b56-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="84b56-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="84b56-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="84b56-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="84b56-112">Cmdleten **New-AzureHDInsightStreamingMapReduceJobDefinition** definierar ett nytt jobb definitions objekt som representerar parametrarna för ett Hadoop-strömningen.</span><span class="sxs-lookup"><span data-stu-id="84b56-112">The **New-AzureHDInsightStreamingMapReduceJobDefinition** cmdlet defines a new job definition object that represents the parameters of a Hadoop streaming job.</span></span>

## <span data-ttu-id="84b56-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84b56-113">EXAMPLES</span></span>

### <span data-ttu-id="84b56-114">Exempel 1: skapa en MapReduce</span><span class="sxs-lookup"><span data-stu-id="84b56-114">Example 1: Create a streaming MapReduce job definition</span></span>
```
PS C:\>$StreamingWordCount = New-AzureHDInsightStreamingMapReduceJobDefinition -Files "/Example/Apps/WordCount.exe", "/Example/Apps/Cat.exe" -InputPath "/Example/Data/Gutenberg/Davinci.txt" -OutputPath "/Example/Data/StreamingOutput/WordCount.txt" -Mapper "Cat.exe" -Reducer "WordCount.exe"
```

<span data-ttu-id="84b56-115">Det här kommandot skapar den angivna jobb definitionen för strömnings MapReduce och lagrar den sedan i $StreamingWordCount variabel.</span><span class="sxs-lookup"><span data-stu-id="84b56-115">This command creates the specified streaming MapReduce job definition, and then stores it in the $StreamingWordCount variable.</span></span>

## <span data-ttu-id="84b56-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84b56-116">PARAMETERS</span></span>

### <span data-ttu-id="84b56-117">-Argument</span><span class="sxs-lookup"><span data-stu-id="84b56-117">-Arguments</span></span>
<span data-ttu-id="84b56-118">Anger en matris med argument för ett Hadoop-jobb.</span><span class="sxs-lookup"><span data-stu-id="84b56-118">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="84b56-119">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="84b56-119">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Args

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-120">-CmdEnv</span><span class="sxs-lookup"><span data-stu-id="84b56-120">-CmdEnv</span></span>
<span data-ttu-id="84b56-121">Anger en matris med kommando rads miljövariabler som ska anges när ett jobb körs på datanoder.</span><span class="sxs-lookup"><span data-stu-id="84b56-121">Specifies an array of command-line environment variables to set when a job runs on data nodes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-122">-Kombinerare</span><span class="sxs-lookup"><span data-stu-id="84b56-122">-Combiner</span></span>
<span data-ttu-id="84b56-123">Anger ett kombinations fil namn.</span><span class="sxs-lookup"><span data-stu-id="84b56-123">Specifies a Combiner file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-124">-Definierar</span><span class="sxs-lookup"><span data-stu-id="84b56-124">-Defines</span></span>
<span data-ttu-id="84b56-125">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="84b56-125">Specifies Hadoop configuration values to set when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-126">-Filer</span><span class="sxs-lookup"><span data-stu-id="84b56-126">-Files</span></span>
<span data-ttu-id="84b56-127">Anger en matris med filer som krävs för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="84b56-127">Specifies an array of files that are required for a job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-128">-InputPath</span><span class="sxs-lookup"><span data-stu-id="84b56-128">-InputPath</span></span>
<span data-ttu-id="84b56-129">Anger sökvägen till WASB.</span><span class="sxs-lookup"><span data-stu-id="84b56-129">Specifies the WASB path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Input

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="84b56-130">-JobName</span></span>
<span data-ttu-id="84b56-131">Anger namnet på den nya MapReduce.</span><span class="sxs-lookup"><span data-stu-id="84b56-131">Specifies the name of the new MapReduce job definition.</span></span>
<span data-ttu-id="84b56-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="84b56-132">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-133">-Mapper</span><span class="sxs-lookup"><span data-stu-id="84b56-133">-Mapper</span></span>
<span data-ttu-id="84b56-134">Anger ett fil namn för mapper.</span><span class="sxs-lookup"><span data-stu-id="84b56-134">Specifies a Mapper file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-135">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="84b56-135">-OutputPath</span></span>
<span data-ttu-id="84b56-136">Anger WASB-sökvägen för jobb utskriften.</span><span class="sxs-lookup"><span data-stu-id="84b56-136">Specifies the WASB path for the job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Output

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="84b56-137">-Profile</span></span>
<span data-ttu-id="84b56-138">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="84b56-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84b56-139">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="84b56-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-140">-Reducerare</span><span class="sxs-lookup"><span data-stu-id="84b56-140">-Reducer</span></span>
<span data-ttu-id="84b56-141">Anger ett avminskande fil namn.</span><span class="sxs-lookup"><span data-stu-id="84b56-141">Specifies a Reducer file name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-142">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="84b56-142">-StatusFolder</span></span>
<span data-ttu-id="84b56-143">Anger den mapp som innehåller standardutdata och fel utdata för jobbet, inklusive slutkod och aktivitets loggar.</span><span class="sxs-lookup"><span data-stu-id="84b56-143">Specifies the folder that contains the standard outputs and error outputs for the job, including its exit code and task logs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84b56-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b56-144">CommonParameters</span></span>
<span data-ttu-id="84b56-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b56-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b56-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84b56-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b56-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84b56-147">INPUTS</span></span>

## <span data-ttu-id="84b56-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84b56-148">OUTPUTS</span></span>

## <span data-ttu-id="84b56-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84b56-149">NOTES</span></span>

## <span data-ttu-id="84b56-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84b56-150">RELATED LINKS</span></span>

[<span data-ttu-id="84b56-151">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="84b56-151">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="84b56-152">New-AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="84b56-152">New-AzureHDInsightMapReduceJobDefinition</span></span>](./New-AzureHDInsightMapReduceJobDefinition.md)

[<span data-ttu-id="84b56-153">New-AzureHDInsightPigJobDefinition</span><span class="sxs-lookup"><span data-stu-id="84b56-153">New-AzureHDInsightPigJobDefinition</span></span>](./New-AzureHDInsightPigJobDefinition.md)

[<span data-ttu-id="84b56-154">New-AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="84b56-154">New-AzureHDInsightSqoopJobDefinition</span></span>](./New-AzureHDInsightSqoopJobDefinition.md)


