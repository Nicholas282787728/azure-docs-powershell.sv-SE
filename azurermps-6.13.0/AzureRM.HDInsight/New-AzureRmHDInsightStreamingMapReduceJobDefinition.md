---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: 22ddeeffd696de260e13c1c817afedfabe1887a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757088"
---
# <span data-ttu-id="1d215-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1d215-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="1d215-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1d215-102">SYNOPSIS</span></span>
<span data-ttu-id="1d215-103">Skapar ett Job-MapReduce.</span><span class="sxs-lookup"><span data-stu-id="1d215-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d215-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1d215-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d215-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1d215-105">DESCRIPTION</span></span>
<span data-ttu-id="1d215-106">Cmdleten **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definierar ett strömmande MapReduce-jobbnamn för användning med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="1d215-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1d215-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1d215-107">EXAMPLES</span></span>

### <span data-ttu-id="1d215-108">Exempel 1: skapa en MapReduce</span><span class="sxs-lookup"><span data-stu-id="1d215-108">Example 1: Create a Streaming MapReduce job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Streaming MapReduce job details
PS C:\>$statusFolder = "tempStatusFolder/"
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightStreamingMapReduceJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="1d215-109">Det här kommandot skapar en MapReduce.</span><span class="sxs-lookup"><span data-stu-id="1d215-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="1d215-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1d215-110">PARAMETERS</span></span>

### <span data-ttu-id="1d215-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="1d215-111">-Arguments</span></span>
<span data-ttu-id="1d215-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="1d215-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="1d215-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="1d215-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="1d215-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="1d215-114">-CommandEnvironment</span></span>
<span data-ttu-id="1d215-115">Anger en matris med kommando rads miljövariabler som ska anges när ett jobb körs på en arbets nod.</span><span class="sxs-lookup"><span data-stu-id="1d215-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

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

### <span data-ttu-id="1d215-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d215-116">-DefaultProfile</span></span>
<span data-ttu-id="1d215-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1d215-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d215-118">-Definierar</span><span class="sxs-lookup"><span data-stu-id="1d215-118">-Defines</span></span>
<span data-ttu-id="1d215-119">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="1d215-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="1d215-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="1d215-120">-File</span></span>
<span data-ttu-id="1d215-121">Anger sökvägen till en fil som innehåller en fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="1d215-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="1d215-122">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="1d215-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="1d215-123">-Filer</span><span class="sxs-lookup"><span data-stu-id="1d215-123">-Files</span></span>
<span data-ttu-id="1d215-124">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="1d215-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="1d215-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="1d215-125">-InputPath</span></span>
<span data-ttu-id="1d215-126">Anger sökvägen till indatafilerna.</span><span class="sxs-lookup"><span data-stu-id="1d215-126">Specifies the path to the input files.</span></span>

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

### <span data-ttu-id="1d215-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="1d215-127">-Mapper</span></span>
<span data-ttu-id="1d215-128">Anger ett fil namn för mapper.</span><span class="sxs-lookup"><span data-stu-id="1d215-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="1d215-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="1d215-129">-OutputPath</span></span>
<span data-ttu-id="1d215-130">Anger sökvägen till utskriften.</span><span class="sxs-lookup"><span data-stu-id="1d215-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="1d215-131">-Reducerare</span><span class="sxs-lookup"><span data-stu-id="1d215-131">-Reducer</span></span>
<span data-ttu-id="1d215-132">Anger ett avminskande fil namn.</span><span class="sxs-lookup"><span data-stu-id="1d215-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="1d215-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="1d215-133">-StatusFolder</span></span>
<span data-ttu-id="1d215-134">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="1d215-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="1d215-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d215-135">CommonParameters</span></span>
<span data-ttu-id="1d215-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d215-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d215-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d215-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d215-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1d215-138">INPUTS</span></span>

### <span data-ttu-id="1d215-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="1d215-139">None</span></span>

## <span data-ttu-id="1d215-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1d215-140">OUTPUTS</span></span>

### <span data-ttu-id="1d215-141">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="1d215-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="1d215-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1d215-142">NOTES</span></span>

## <span data-ttu-id="1d215-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1d215-143">RELATED LINKS</span></span>

[<span data-ttu-id="1d215-144">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="1d215-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


