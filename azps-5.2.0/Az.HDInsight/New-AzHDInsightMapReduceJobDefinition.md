---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 45278426ee25337bd484a46b533c72f49dbe9586
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388011"
---
# <span data-ttu-id="f3e6f-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f3e6f-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="f3e6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e6f-103">Skapar ett MapReduce.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="f3e6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3e6f-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3e6f-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e6f-106">Cmdleten **New-AzHDInsightMapReduceJobDefinition** definierar ett nytt MapReduce-jobb för användning med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="f3e6f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3e6f-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e6f-108">Exempel 1: skapa en MapReduce</span><span class="sxs-lookup"><span data-stu-id="f3e6f-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="f3e6f-109">Det här kommandot skapar en MapReduce.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="f3e6f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3e6f-110">PARAMETERS</span></span>

### <span data-ttu-id="f3e6f-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="f3e6f-111">-Arguments</span></span>
<span data-ttu-id="f3e6f-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="f3e6f-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="f3e6f-114">-Klass namn</span><span class="sxs-lookup"><span data-stu-id="f3e6f-114">-ClassName</span></span>
<span data-ttu-id="f3e6f-115">Anger jobb klass i JAR-filen.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="f3e6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e6f-116">-DefaultProfile</span></span>
<span data-ttu-id="f3e6f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f3e6f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3e6f-118">-Definierar</span><span class="sxs-lookup"><span data-stu-id="f3e6f-118">-Defines</span></span>
<span data-ttu-id="f3e6f-119">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="f3e6f-120">-Filer</span><span class="sxs-lookup"><span data-stu-id="f3e6f-120">-Files</span></span>
<span data-ttu-id="f3e6f-121">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="f3e6f-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="f3e6f-122">-JarFile</span></span>
<span data-ttu-id="f3e6f-123">Anger JAR-filen som ska användas för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="f3e6f-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="f3e6f-124">-JobName</span></span>
<span data-ttu-id="f3e6f-125">Anger namnet på jobbet.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-125">Specifies the name of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e6f-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="f3e6f-126">-LibJars</span></span>
<span data-ttu-id="f3e6f-127">Anger lib-JARS för jobbet.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="f3e6f-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="f3e6f-128">-StatusFolder</span></span>
<span data-ttu-id="f3e6f-129">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3e6f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e6f-130">CommonParameters</span></span>
<span data-ttu-id="f3e6f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3e6f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e6f-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3e6f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e6f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3e6f-133">INPUTS</span></span>

### <span data-ttu-id="f3e6f-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="f3e6f-134">None</span></span>

## <span data-ttu-id="f3e6f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3e6f-135">OUTPUTS</span></span>

### <span data-ttu-id="f3e6f-136">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="f3e6f-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="f3e6f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3e6f-137">NOTES</span></span>

## <span data-ttu-id="f3e6f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3e6f-138">RELATED LINKS</span></span>

[<span data-ttu-id="f3e6f-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="f3e6f-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


