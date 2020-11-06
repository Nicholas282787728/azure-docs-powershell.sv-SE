---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 17CB76E7-2F91-4EFE-9DA3-F083F02235E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightstreamingmapreducejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightStreamingMapReduceJobDefinition.md
ms.openlocfilehash: f74d0e56265e5b976de9cf289f3b6a4900b76d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577221"
---
# <span data-ttu-id="19cc6-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="19cc6-101">New-AzureRmHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="19cc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="19cc6-103">Skapar ett Job-MapReduce.</span><span class="sxs-lookup"><span data-stu-id="19cc6-103">Creates a Streaming MapReduce job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19cc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19cc6-104">SYNTAX</span></span>

```
New-AzureRmHDInsightStreamingMapReduceJobDefinition [-Arguments <String[]>] [-File <String>]
 [-Files <String[]>] [-StatusFolder <String>] [-CommandEnvironment <Hashtable>] [-Defines <Hashtable>]
 -InputPath <String> [-Mapper <String>] [-OutputPath <String>] [-Reducer <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19cc6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="19cc6-106">Cmdleten **New-AzureRmHDInsightStreamingMapReduceJobDefinition** definierar ett strömmande MapReduce-jobbnamn för användning med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="19cc6-106">The **New-AzureRmHDInsightStreamingMapReduceJobDefinition** cmdlet defines a Streaming MapReduce job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="19cc6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="19cc6-108">Exempel 1: skapa en MapReduce</span><span class="sxs-lookup"><span data-stu-id="19cc6-108">Example 1: Create a Streaming MapReduce job definition</span></span>
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

<span data-ttu-id="19cc6-109">Det här kommandot skapar en MapReduce.</span><span class="sxs-lookup"><span data-stu-id="19cc6-109">This command creates a Streaming MapReduce job definition.</span></span>

## <span data-ttu-id="19cc6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19cc6-110">PARAMETERS</span></span>

### <span data-ttu-id="19cc6-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="19cc6-111">-Arguments</span></span>
<span data-ttu-id="19cc6-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="19cc6-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="19cc6-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="19cc6-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="19cc6-114">-CommandEnvironment</span><span class="sxs-lookup"><span data-stu-id="19cc6-114">-CommandEnvironment</span></span>
<span data-ttu-id="19cc6-115">Anger en matris med kommando rads miljövariabler som ska anges när ett jobb körs på en arbets nod.</span><span class="sxs-lookup"><span data-stu-id="19cc6-115">Specifies an array of command-line environment variables to set when a job runs on worker nodes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cc6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cc6-116">-DefaultProfile</span></span>
<span data-ttu-id="19cc6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="19cc6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19cc6-118">-Definierar</span><span class="sxs-lookup"><span data-stu-id="19cc6-118">-Defines</span></span>
<span data-ttu-id="19cc6-119">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="19cc6-119">Specifies Hadoop configuration values to set for when the job runs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cc6-120">-Fil</span><span class="sxs-lookup"><span data-stu-id="19cc6-120">-File</span></span>
<span data-ttu-id="19cc6-121">Anger sökvägen till en fil som innehåller en fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="19cc6-121">Specifies the path to a file that contains a query to run.</span></span>
<span data-ttu-id="19cc6-122">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="19cc6-122">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="19cc6-123">-Filer</span><span class="sxs-lookup"><span data-stu-id="19cc6-123">-Files</span></span>
<span data-ttu-id="19cc6-124">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="19cc6-124">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="19cc6-125">-InputPath</span><span class="sxs-lookup"><span data-stu-id="19cc6-125">-InputPath</span></span>
<span data-ttu-id="19cc6-126">Anger sökvägen till indatafilerna.</span><span class="sxs-lookup"><span data-stu-id="19cc6-126">Specifies the path to the input files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cc6-127">-Mapper</span><span class="sxs-lookup"><span data-stu-id="19cc6-127">-Mapper</span></span>
<span data-ttu-id="19cc6-128">Anger ett fil namn för mapper.</span><span class="sxs-lookup"><span data-stu-id="19cc6-128">Specifies a Mapper file name.</span></span>

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

### <span data-ttu-id="19cc6-129">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="19cc6-129">-OutputPath</span></span>
<span data-ttu-id="19cc6-130">Anger sökvägen till utskriften.</span><span class="sxs-lookup"><span data-stu-id="19cc6-130">Specifies the path for the job output.</span></span>

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

### <span data-ttu-id="19cc6-131">-Reducerare</span><span class="sxs-lookup"><span data-stu-id="19cc6-131">-Reducer</span></span>
<span data-ttu-id="19cc6-132">Anger ett avminskande fil namn.</span><span class="sxs-lookup"><span data-stu-id="19cc6-132">Specifies a Reducer file name.</span></span>

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

### <span data-ttu-id="19cc6-133">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="19cc6-133">-StatusFolder</span></span>
<span data-ttu-id="19cc6-134">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="19cc6-134">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="19cc6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cc6-135">CommonParameters</span></span>
<span data-ttu-id="19cc6-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19cc6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cc6-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cc6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cc6-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19cc6-138">INPUTS</span></span>

### <span data-ttu-id="19cc6-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="19cc6-139">None</span></span>
<span data-ttu-id="19cc6-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="19cc6-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19cc6-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19cc6-141">OUTPUTS</span></span>

### <span data-ttu-id="19cc6-142">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightStreamingMapReduceJobDefinition</span><span class="sxs-lookup"><span data-stu-id="19cc6-142">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightStreamingMapReduceJobDefinition</span></span>

## <span data-ttu-id="19cc6-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19cc6-143">NOTES</span></span>

## <span data-ttu-id="19cc6-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19cc6-144">RELATED LINKS</span></span>

[<span data-ttu-id="19cc6-145">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="19cc6-145">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


