---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 99ed451e43062cd5411a7a8bc1577646226aa8b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582691"
---
# <span data-ttu-id="2039b-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2039b-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="2039b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2039b-102">SYNOPSIS</span></span>
<span data-ttu-id="2039b-103">Skapar ett Hive Job-objekt.</span><span class="sxs-lookup"><span data-stu-id="2039b-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2039b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2039b-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2039b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2039b-105">DESCRIPTION</span></span>
<span data-ttu-id="2039b-106">Cmdleten **New-AzureRmHDInsightHiveJobDefinition** definierar ett Hive Job-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="2039b-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="2039b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2039b-107">EXAMPLES</span></span>

### <span data-ttu-id="2039b-108">Exempel 1: skapa en struktur jobb definition</span><span class="sxs-lookup"><span data-stu-id="2039b-108">Example 1: Create a Hive job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

# Hive job details
PS C:\>$statusFolder = "<status folder>"        
PS C:\>$query = "SHOW TABLES"

PS C:\>New-AzureRmHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzureRmHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="2039b-109">Det här kommandot skapar en struktur för registrerings jobb.</span><span class="sxs-lookup"><span data-stu-id="2039b-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="2039b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2039b-110">PARAMETERS</span></span>

### <span data-ttu-id="2039b-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="2039b-111">-Arguments</span></span>
<span data-ttu-id="2039b-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="2039b-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="2039b-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="2039b-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="2039b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2039b-114">-DefaultProfile</span></span>
<span data-ttu-id="2039b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2039b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2039b-116">-Definierar</span><span class="sxs-lookup"><span data-stu-id="2039b-116">-Defines</span></span>
<span data-ttu-id="2039b-117">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="2039b-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="2039b-118">-Fil</span><span class="sxs-lookup"><span data-stu-id="2039b-118">-File</span></span>
<span data-ttu-id="2039b-119">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="2039b-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="2039b-120">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="2039b-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="2039b-121">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="2039b-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="2039b-122">-Filer</span><span class="sxs-lookup"><span data-stu-id="2039b-122">-Files</span></span>
<span data-ttu-id="2039b-123">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="2039b-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="2039b-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="2039b-124">-JobName</span></span>
<span data-ttu-id="2039b-125">Anger namnet på jobbet.</span><span class="sxs-lookup"><span data-stu-id="2039b-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="2039b-126">-Fråga</span><span class="sxs-lookup"><span data-stu-id="2039b-126">-Query</span></span>
<span data-ttu-id="2039b-127">Anger en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="2039b-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="2039b-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="2039b-128">-RunAsFileJob</span></span>
<span data-ttu-id="2039b-129">Anger att denna cmdlet skapar en fil i det standard-Azure Storage-konto där du vill lagra en fråga.</span><span class="sxs-lookup"><span data-stu-id="2039b-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="2039b-130">Denna cmdlet skickar jobbet som refererar till den här filen som ett skript att köra.</span><span class="sxs-lookup"><span data-stu-id="2039b-130">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="2039b-131">Du kan använda den här funktionen för att hantera specialtecken som procent tecken (%) Det innebär att det inte går att skicka jobb via Templeton eftersom Templeton tolkar en fråga med ett procent tecken som en URL-parameter.</span><span class="sxs-lookup"><span data-stu-id="2039b-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="2039b-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="2039b-132">-StatusFolder</span></span>
<span data-ttu-id="2039b-133">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="2039b-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="2039b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2039b-134">CommonParameters</span></span>
<span data-ttu-id="2039b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2039b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2039b-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2039b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2039b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2039b-137">INPUTS</span></span>

### <span data-ttu-id="2039b-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="2039b-138">None</span></span>

## <span data-ttu-id="2039b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2039b-139">OUTPUTS</span></span>

### <span data-ttu-id="2039b-140">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="2039b-140">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="2039b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2039b-141">NOTES</span></span>

## <span data-ttu-id="2039b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2039b-142">RELATED LINKS</span></span>

[<span data-ttu-id="2039b-143">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="2039b-143">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


