---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: c1dab20f44edfd4e3714e4465a0bf295e8e78fb5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916590"
---
# <span data-ttu-id="26654-101">New-AzHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="26654-101">New-AzHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="26654-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26654-102">SYNOPSIS</span></span>
<span data-ttu-id="26654-103">Skapar ett MapReduce.</span><span class="sxs-lookup"><span data-stu-id="26654-103">Creates a MapReduce job object.</span></span>

## <span data-ttu-id="26654-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26654-104">SYNTAX</span></span>

```
New-AzHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26654-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26654-105">DESCRIPTION</span></span>
<span data-ttu-id="26654-106">Cmdleten **New-AzHDInsightMapReduceJobDefinition** definierar ett nytt MapReduce-jobb för användning med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="26654-106">The **New-AzHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="26654-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26654-107">EXAMPLES</span></span>

### <span data-ttu-id="26654-108">Exempel 1: skapa en MapReduce</span><span class="sxs-lookup"><span data-stu-id="26654-108">Example 1: Create a MapReduce job definition</span></span>
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

<span data-ttu-id="26654-109">Det här kommandot skapar en MapReduce.</span><span class="sxs-lookup"><span data-stu-id="26654-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="26654-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26654-110">PARAMETERS</span></span>

### <span data-ttu-id="26654-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="26654-111">-Arguments</span></span>
<span data-ttu-id="26654-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="26654-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="26654-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="26654-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="26654-114">-Klass namn</span><span class="sxs-lookup"><span data-stu-id="26654-114">-ClassName</span></span>
<span data-ttu-id="26654-115">Anger jobb klass i JAR-filen.</span><span class="sxs-lookup"><span data-stu-id="26654-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="26654-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26654-116">-DefaultProfile</span></span>
<span data-ttu-id="26654-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="26654-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26654-118">-Definierar</span><span class="sxs-lookup"><span data-stu-id="26654-118">-Defines</span></span>
<span data-ttu-id="26654-119">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="26654-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="26654-120">-Filer</span><span class="sxs-lookup"><span data-stu-id="26654-120">-Files</span></span>
<span data-ttu-id="26654-121">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="26654-121">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="26654-122">-JarFile</span><span class="sxs-lookup"><span data-stu-id="26654-122">-JarFile</span></span>
<span data-ttu-id="26654-123">Anger JAR-filen som ska användas för jobbet.</span><span class="sxs-lookup"><span data-stu-id="26654-123">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="26654-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="26654-124">-JobName</span></span>
<span data-ttu-id="26654-125">Anger namnet på jobbet.</span><span class="sxs-lookup"><span data-stu-id="26654-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="26654-126">-LibJars</span><span class="sxs-lookup"><span data-stu-id="26654-126">-LibJars</span></span>
<span data-ttu-id="26654-127">Anger lib-JARS för jobbet.</span><span class="sxs-lookup"><span data-stu-id="26654-127">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="26654-128">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="26654-128">-StatusFolder</span></span>
<span data-ttu-id="26654-129">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="26654-129">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="26654-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26654-130">CommonParameters</span></span>
<span data-ttu-id="26654-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26654-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26654-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26654-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26654-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26654-133">INPUTS</span></span>

### <span data-ttu-id="26654-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="26654-134">None</span></span>

## <span data-ttu-id="26654-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26654-135">OUTPUTS</span></span>

### <span data-ttu-id="26654-136">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="26654-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="26654-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26654-137">NOTES</span></span>

## <span data-ttu-id="26654-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26654-138">RELATED LINKS</span></span>

[<span data-ttu-id="26654-139">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="26654-139">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

