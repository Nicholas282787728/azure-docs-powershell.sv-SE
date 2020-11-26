---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightHiveJobDefinition.md
ms.openlocfilehash: 242161a7a02cf3767ecd87dfc6e91a7ffba97eb3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263081"
---
# <span data-ttu-id="d35e1-101">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d35e1-101">New-AzHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="d35e1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d35e1-102">SYNOPSIS</span></span>
<span data-ttu-id="d35e1-103">Skapar ett Hive Job-objekt.</span><span class="sxs-lookup"><span data-stu-id="d35e1-103">Creates a Hive job object.</span></span>

## <span data-ttu-id="d35e1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d35e1-104">SYNTAX</span></span>

```
New-AzHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d35e1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d35e1-105">DESCRIPTION</span></span>
<span data-ttu-id="d35e1-106">Cmdleten **New-AzHDInsightHiveJobDefinition** definierar ett Hive Job-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="d35e1-106">The **New-AzHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d35e1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d35e1-107">EXAMPLES</span></span>

### <span data-ttu-id="d35e1-108">Exempel 1: skapa en struktur jobb definition</span><span class="sxs-lookup"><span data-stu-id="d35e1-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="d35e1-109">Det här kommandot skapar en struktur för registrerings jobb.</span><span class="sxs-lookup"><span data-stu-id="d35e1-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="d35e1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d35e1-110">PARAMETERS</span></span>

### <span data-ttu-id="d35e1-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="d35e1-111">-Arguments</span></span>
<span data-ttu-id="d35e1-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="d35e1-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="d35e1-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="d35e1-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="d35e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d35e1-114">-DefaultProfile</span></span>
<span data-ttu-id="d35e1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d35e1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d35e1-116">-Definierar</span><span class="sxs-lookup"><span data-stu-id="d35e1-116">-Defines</span></span>
<span data-ttu-id="d35e1-117">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="d35e1-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="d35e1-118">-Fil</span><span class="sxs-lookup"><span data-stu-id="d35e1-118">-File</span></span>
<span data-ttu-id="d35e1-119">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="d35e1-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="d35e1-120">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="d35e1-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="d35e1-121">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="d35e1-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="d35e1-122">-Filer</span><span class="sxs-lookup"><span data-stu-id="d35e1-122">-Files</span></span>
<span data-ttu-id="d35e1-123">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="d35e1-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="d35e1-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d35e1-124">-JobName</span></span>
<span data-ttu-id="d35e1-125">Anger namnet på jobbet.</span><span class="sxs-lookup"><span data-stu-id="d35e1-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="d35e1-126">-Fråga</span><span class="sxs-lookup"><span data-stu-id="d35e1-126">-Query</span></span>
<span data-ttu-id="d35e1-127">Anger en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="d35e1-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="d35e1-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="d35e1-128">-RunAsFileJob</span></span>
<span data-ttu-id="d35e1-129">Anger att denna cmdlet skapar en fil i det standard-Azure Storage-konto där du vill lagra en fråga.</span><span class="sxs-lookup"><span data-stu-id="d35e1-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="d35e1-130">Denna cmdlet skickar jobbet som refererar till den här filen som ett skript att köra.</span><span class="sxs-lookup"><span data-stu-id="d35e1-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="d35e1-131">Du kan använda den här funktionen för att hantera specialtecken som procent tecken (%) Det innebär att det inte går att skicka jobb via Templeton eftersom Templeton tolkar en fråga med ett procent tecken som en URL-parameter.</span><span class="sxs-lookup"><span data-stu-id="d35e1-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d35e1-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="d35e1-132">-StatusFolder</span></span>
<span data-ttu-id="d35e1-133">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="d35e1-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="d35e1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d35e1-134">CommonParameters</span></span>
<span data-ttu-id="d35e1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d35e1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d35e1-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d35e1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d35e1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d35e1-137">INPUTS</span></span>

### <span data-ttu-id="d35e1-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="d35e1-138">None</span></span>

## <span data-ttu-id="d35e1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d35e1-139">OUTPUTS</span></span>

### <span data-ttu-id="d35e1-140">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="d35e1-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="d35e1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d35e1-141">NOTES</span></span>

## <span data-ttu-id="d35e1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d35e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="d35e1-143">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="d35e1-143">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

