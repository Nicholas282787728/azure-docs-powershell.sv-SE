---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099478"
---
# <span data-ttu-id="e2564-101">Invoke-AzureHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="e2564-101">Invoke-AzureHDInsightHiveJob</span></span>

## <span data-ttu-id="e2564-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e2564-102">SYNOPSIS</span></span>
<span data-ttu-id="e2564-103">Skickar struktur frågor till ett HDInsight-kluster, visar förloppet för frågekörningen och får frågeresultat i en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="e2564-103">Submits Hive queries to an HDInsight cluster, shows progress of the query execution, and gets query results in one operation.</span></span>

## <span data-ttu-id="e2564-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e2564-104">SYNTAX</span></span>

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e2564-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e2564-105">DESCRIPTION</span></span>
<span data-ttu-id="e2564-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="e2564-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="e2564-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="e2564-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="e2564-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="e2564-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="e2564-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="e2564-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="e2564-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="e2564-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="e2564-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e2564-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="e2564-112">Cmdleten **Invoke-AzureHDInsightHiveJob** skickar struktur frågor till ett HDInsight-kluster, visar förloppet för frågekörningen och får frågeresultatet i en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="e2564-112">The **Invoke-AzureHDInsightHiveJob** cmdlet submits Hive queries to an HDInsight cluster, displays the progress of the query execution, and gets the query results in one operation.</span></span>
<span data-ttu-id="e2564-113">Du måste köra cmdleten Use-AzureHDInsightCluster innan du kör **Invoke-AzureHDInsightHiveJob** för att ange det HDInsight-kluster som du vill skicka en fråga till.</span><span class="sxs-lookup"><span data-stu-id="e2564-113">You must run the Use-AzureHDInsightCluster cmdlet before running **Invoke-AzureHDInsightHiveJob** to specify the HDInsight cluster to which to submit a query.</span></span>

## <span data-ttu-id="e2564-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e2564-114">EXAMPLES</span></span>

### <span data-ttu-id="e2564-115">Exempel 1: skicka en struktur fråga</span><span class="sxs-lookup"><span data-stu-id="e2564-115">Example 1: Submit a Hive query</span></span>
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

<span data-ttu-id="e2564-116">Det första kommandot använder cmdleten **use-AzureHDInsightCluster** för att ange ett kluster i den aktuella prenumerationen som ska användas för en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="e2564-116">The first command uses the **Use-AzureHDInsightCluster** cmdlet to specify a cluster in the current subscription to use for a Hive query.</span></span>

<span data-ttu-id="e2564-117">Det andra kommandot använder cmdleten **Invoke-AzureHDInsightHiveJob** för att skicka in registrerings data filen.</span><span class="sxs-lookup"><span data-stu-id="e2564-117">The second command uses the **Invoke-AzureHDInsightHiveJob** cmdlet to submit the Hive query.</span></span>

## <span data-ttu-id="e2564-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e2564-118">PARAMETERS</span></span>

### <span data-ttu-id="e2564-119">-Argument</span><span class="sxs-lookup"><span data-stu-id="e2564-119">-Arguments</span></span>
<span data-ttu-id="e2564-120">Anger en matris med argument för ett Hadoop-jobb.</span><span class="sxs-lookup"><span data-stu-id="e2564-120">Specifies an array of arguments for a Hadoop job.</span></span>
<span data-ttu-id="e2564-121">Argumenten skickas som kommando rads argument till varje aktivitet.</span><span class="sxs-lookup"><span data-stu-id="e2564-121">The arguments are passed as command-line arguments to each task.</span></span>

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

### <span data-ttu-id="e2564-122">-Definierar</span><span class="sxs-lookup"><span data-stu-id="e2564-122">-Defines</span></span>
<span data-ttu-id="e2564-123">Anger Hadoop-konfigurationsinställningar som ska anges när ett jobb körs.</span><span class="sxs-lookup"><span data-stu-id="e2564-123">Specifies Hadoop configuration values to set when a job runs.</span></span>

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

### <span data-ttu-id="e2564-124">-Fil</span><span class="sxs-lookup"><span data-stu-id="e2564-124">-File</span></span>
<span data-ttu-id="e2564-125">Anger sökvägen till Windows Azure Storage BLOB (WASB) till en fil i Azure Blob Storage som innehåller frågan som ska köras.</span><span class="sxs-lookup"><span data-stu-id="e2564-125">Specifies the Windows Azure Storage Blob (WASB) path to a file in Azure blob storage that contains the query to run.</span></span>
<span data-ttu-id="e2564-126">Du kan använda den här parametern i stället för *Frågeparametern* .</span><span class="sxs-lookup"><span data-stu-id="e2564-126">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2564-127">-Filer</span><span class="sxs-lookup"><span data-stu-id="e2564-127">-Files</span></span>
<span data-ttu-id="e2564-128">Anger en samling filer som krävs för ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="e2564-128">Specifies a collection of files that are required for a Hive job.</span></span>

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

### <span data-ttu-id="e2564-129">-JobName</span><span class="sxs-lookup"><span data-stu-id="e2564-129">-JobName</span></span>
<span data-ttu-id="e2564-130">Anger namnet på ett struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="e2564-130">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="e2564-131">Om du inte anger den här parametern använder denna cmdlet standardvärdet: "struktur: \<first 100 characters of Query\> ".</span><span class="sxs-lookup"><span data-stu-id="e2564-131">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

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

### <span data-ttu-id="e2564-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="e2564-132">-Profile</span></span>
<span data-ttu-id="e2564-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e2564-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e2564-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e2564-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e2564-135">-Fråga</span><span class="sxs-lookup"><span data-stu-id="e2564-135">-Query</span></span>
<span data-ttu-id="e2564-136">Anger en struktur fråga.</span><span class="sxs-lookup"><span data-stu-id="e2564-136">Specifies a Hive query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2564-137">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="e2564-137">-RunAsFileJob</span></span>
<span data-ttu-id="e2564-138">Anger att denna cmdlet skapar en fil i det standard-Azure Storage-konto där du vill lagra en fråga.</span><span class="sxs-lookup"><span data-stu-id="e2564-138">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="e2564-139">Denna cmdlet skickar jobbet som refererar till den här filen som ett skript att köra.</span><span class="sxs-lookup"><span data-stu-id="e2564-139">This cmdlet submits the job that references this file as a script to run.</span></span>

<span data-ttu-id="e2564-140">Du kan använda den här funktionen för att hantera specialtecken som procent tecken (%) Det innebär att det inte går att skicka jobb via Templeton eftersom Templeton tolkar en fråga med ett procent tecken som en URL-parameter.</span><span class="sxs-lookup"><span data-stu-id="e2564-140">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="e2564-141">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="e2564-141">-StatusFolder</span></span>
<span data-ttu-id="e2564-142">Anger platsen för mappen som innehåller standard utmatning och fel utdata för ett jobb, inklusive dess slutkod och aktivitets loggar.</span><span class="sxs-lookup"><span data-stu-id="e2564-142">Specifies the location of the folder that contains standard outputs and error outputs for a job, including its exit code and task logs.</span></span>

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

### <span data-ttu-id="e2564-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2564-143">CommonParameters</span></span>
<span data-ttu-id="e2564-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2564-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2564-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2564-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2564-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e2564-146">INPUTS</span></span>

## <span data-ttu-id="e2564-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e2564-147">OUTPUTS</span></span>

## <span data-ttu-id="e2564-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e2564-148">NOTES</span></span>

## <span data-ttu-id="e2564-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e2564-149">RELATED LINKS</span></span>

[<span data-ttu-id="e2564-150">New-AzureHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="e2564-150">New-AzureHDInsightHiveJobDefinition</span></span>](./New-AzureHDInsightHiveJobDefinition.md)

[<span data-ttu-id="e2564-151">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e2564-151">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


