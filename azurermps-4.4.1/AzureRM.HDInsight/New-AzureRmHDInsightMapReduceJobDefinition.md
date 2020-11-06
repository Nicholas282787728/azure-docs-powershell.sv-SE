---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6BF6F9A7-BED3-4CCE-9E0A-46ECBFF55DA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightMapReduceJobDefinition.md
ms.openlocfilehash: 7b3bce866712565b5eeb6fc9deccc64f9da69891
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585552"
---
# <span data-ttu-id="b5629-101">New-AzureRmHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b5629-101">New-AzureRmHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="b5629-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5629-102">SYNOPSIS</span></span>
<span data-ttu-id="b5629-103">Skapar ett MapReduce.</span><span class="sxs-lookup"><span data-stu-id="b5629-103">Creates a MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5629-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5629-104">SYNTAX</span></span>

```
New-AzureRmHDInsightMapReduceJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 -ClassName <String> [-Defines <Hashtable>] -JarFile <String> [-JobName <String>] [-LibJars <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5629-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5629-105">DESCRIPTION</span></span>
<span data-ttu-id="b5629-106">Cmdleten **New-AzureRmHDInsightMapReduceJobDefinition** definierar ett nytt MapReduce-jobb för användning med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="b5629-106">The **New-AzureRmHDInsightMapReduceJobDefinition** cmdlet defines a new MapReduce job for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b5629-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5629-107">EXAMPLES</span></span>

### <span data-ttu-id="b5629-108">Exempel 1: skapa en MapReduce</span><span class="sxs-lookup"><span data-stu-id="b5629-108">Example 1: Create a MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightMapReduceJobDefinition -StatusFolder $statusFolder `
            -ClassName $className `
            -JarFile $jarFilePath `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="b5629-109">Det här kommandot skapar en MapReduce.</span><span class="sxs-lookup"><span data-stu-id="b5629-109">This command creates a MapReduce job definition.</span></span>

## <span data-ttu-id="b5629-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5629-110">PARAMETERS</span></span>

### <span data-ttu-id="b5629-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="b5629-111">-Arguments</span></span>
<span data-ttu-id="b5629-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="b5629-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="b5629-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="b5629-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="b5629-114">-Klass namn</span><span class="sxs-lookup"><span data-stu-id="b5629-114">-ClassName</span></span>
<span data-ttu-id="b5629-115">Anger jobb klass i JAR-filen.</span><span class="sxs-lookup"><span data-stu-id="b5629-115">Specifies the job class in the JAR file.</span></span>

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

### <span data-ttu-id="b5629-116">-Definierar</span><span class="sxs-lookup"><span data-stu-id="b5629-116">-Defines</span></span>
<span data-ttu-id="b5629-117">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="b5629-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="b5629-118">-Filer</span><span class="sxs-lookup"><span data-stu-id="b5629-118">-Files</span></span>
<span data-ttu-id="b5629-119">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="b5629-119">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="b5629-120">-JarFile</span><span class="sxs-lookup"><span data-stu-id="b5629-120">-JarFile</span></span>
<span data-ttu-id="b5629-121">Anger JAR-filen som ska användas för jobbet.</span><span class="sxs-lookup"><span data-stu-id="b5629-121">Specifies the JAR file to use for the job.</span></span>

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

### <span data-ttu-id="b5629-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="b5629-122">-JobName</span></span>
<span data-ttu-id="b5629-123">Anger namnet på jobbet.</span><span class="sxs-lookup"><span data-stu-id="b5629-123">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="b5629-124">-LibJars</span><span class="sxs-lookup"><span data-stu-id="b5629-124">-LibJars</span></span>
<span data-ttu-id="b5629-125">Anger lib-JARS för jobbet.</span><span class="sxs-lookup"><span data-stu-id="b5629-125">Specifies the lib JARS for the job.</span></span>

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

### <span data-ttu-id="b5629-126">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="b5629-126">-StatusFolder</span></span>
<span data-ttu-id="b5629-127">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="b5629-127">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="b5629-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5629-128">-DefaultProfile</span></span>
<span data-ttu-id="b5629-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5629-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5629-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5629-130">CommonParameters</span></span>
<span data-ttu-id="b5629-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5629-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5629-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5629-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5629-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5629-133">INPUTS</span></span>

## <span data-ttu-id="b5629-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5629-134">OUTPUTS</span></span>

### <span data-ttu-id="b5629-135">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="b5629-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMapReduceJobDefinition</span></span>

## <span data-ttu-id="b5629-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5629-136">NOTES</span></span>

## <span data-ttu-id="b5629-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5629-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5629-138">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="b5629-138">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


