---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 580D3388-4E18-4E67-866F-1FCF5E54AB3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsighthivejobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightHiveJobDefinition.md
ms.openlocfilehash: 3e4748a8bc5e5c04868fb7c2d4179c07ea63c905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574944"
---
# <span data-ttu-id="cde59-101">New-AzureRmHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cde59-101">New-AzureRmHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="cde59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cde59-102">SYNOPSIS</span></span>
<span data-ttu-id="cde59-103">Skapar ett Hive Job-objekt.</span><span class="sxs-lookup"><span data-stu-id="cde59-103">Creates a Hive job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cde59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cde59-104">SYNTAX</span></span>

```
New-AzureRmHDInsightHiveJobDefinition [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cde59-105">DESCRIPTION</span></span>
<span data-ttu-id="cde59-106">Cmdleten **New-AzureRmHDInsightHiveJobDefinition** definierar ett Hive Job-objekt som ska användas med ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="cde59-106">The **New-AzureRmHDInsightHiveJobDefinition** cmdlet defines a Hive job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="cde59-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cde59-107">EXAMPLES</span></span>

### <span data-ttu-id="cde59-108">Exempel 1: skapa en struktur jobb definition</span><span class="sxs-lookup"><span data-stu-id="cde59-108">Example 1: Create a Hive job definition</span></span>
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

<span data-ttu-id="cde59-109">Det här kommandot skapar en struktur för registrerings jobb.</span><span class="sxs-lookup"><span data-stu-id="cde59-109">This command creates a Hive job definition.</span></span>

## <span data-ttu-id="cde59-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cde59-110">PARAMETERS</span></span>

### <span data-ttu-id="cde59-111">-Argument</span><span class="sxs-lookup"><span data-stu-id="cde59-111">-Arguments</span></span>
<span data-ttu-id="cde59-112">Anger en matris med argument för jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde59-112">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="cde59-113">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="cde59-113">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="cde59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde59-114">-DefaultProfile</span></span>
<span data-ttu-id="cde59-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cde59-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cde59-116">-Definierar</span><span class="sxs-lookup"><span data-stu-id="cde59-116">-Defines</span></span>
<span data-ttu-id="cde59-117">Anger Hadoop-konfigurationsinställningar som ska anges när jobbet körs.</span><span class="sxs-lookup"><span data-stu-id="cde59-117">Specifies Hadoop configuration values to set for when the job runs.</span></span>

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

### <span data-ttu-id="cde59-118">-Fil</span><span class="sxs-lookup"><span data-stu-id="cde59-118">-File</span></span>
<span data-ttu-id="cde59-119">Anger sökvägen till en fil som innehåller den fråga som ska köras.</span><span class="sxs-lookup"><span data-stu-id="cde59-119">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="cde59-120">Filen måste finnas tillgänglig på det lagrings konto som är kopplat till klustret.</span><span class="sxs-lookup"><span data-stu-id="cde59-120">The file must be available on the storage account associated with the cluster.</span></span>
<span data-ttu-id="cde59-121">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="cde59-121">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="cde59-122">-Filer</span><span class="sxs-lookup"><span data-stu-id="cde59-122">-Files</span></span>
<span data-ttu-id="cde59-123">Anger en samling filer som associeras med ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="cde59-123">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="cde59-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="cde59-124">-JobName</span></span>
<span data-ttu-id="cde59-125">Anger namnet på jobbet.</span><span class="sxs-lookup"><span data-stu-id="cde59-125">Specifies the name of the job.</span></span>

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

### <span data-ttu-id="cde59-126">-Fråga</span><span class="sxs-lookup"><span data-stu-id="cde59-126">-Query</span></span>
<span data-ttu-id="cde59-127">Anger en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="cde59-127">Specifies the Hive query.</span></span>

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

### <span data-ttu-id="cde59-128">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="cde59-128">-RunAsFileJob</span></span>
<span data-ttu-id="cde59-129">Anger att denna cmdlet skapar en fil i det standard-Azure Storage-konto där du vill lagra en fråga.</span><span class="sxs-lookup"><span data-stu-id="cde59-129">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="cde59-130">Denna cmdlet skickar jobbet som refererar till den här filen som ett skript att köra.</span><span class="sxs-lookup"><span data-stu-id="cde59-130">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="cde59-131">Du kan använda den här funktionen för att hantera specialtecken som procent tecken (%) Det innebär att det inte går att skicka jobb via Templeton eftersom Templeton tolkar en fråga med ett procent tecken som en URL-parameter.</span><span class="sxs-lookup"><span data-stu-id="cde59-131">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cde59-132">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="cde59-132">-StatusFolder</span></span>
<span data-ttu-id="cde59-133">Anger platsen för mappen som innehåller standardutdata och fel utdata för ett jobb.</span><span class="sxs-lookup"><span data-stu-id="cde59-133">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="cde59-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde59-134">CommonParameters</span></span>
<span data-ttu-id="cde59-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde59-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde59-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cde59-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde59-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cde59-137">INPUTS</span></span>

### <span data-ttu-id="cde59-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="cde59-138">None</span></span>
<span data-ttu-id="cde59-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cde59-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cde59-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cde59-140">OUTPUTS</span></span>

### <span data-ttu-id="cde59-141">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="cde59-141">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightHiveJobDefinition</span></span>

## <span data-ttu-id="cde59-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cde59-142">NOTES</span></span>

## <span data-ttu-id="cde59-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cde59-143">RELATED LINKS</span></span>

[<span data-ttu-id="cde59-144">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="cde59-144">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


