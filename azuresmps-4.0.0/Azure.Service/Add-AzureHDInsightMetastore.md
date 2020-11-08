---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EB196CF5-3E2C-4F38-A983-3365A379672A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 637fc6f65c7168db9ba7e45cea7268208b334c99
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093449"
---
# <span data-ttu-id="f3cb0-101">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="f3cb0-101">Add-AzureHDInsightMetastore</span></span>

## <span data-ttu-id="f3cb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3cb0-103">Lägger till ett SQL Server-databasnamn i en HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-103">Adds a SQL Server database account to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="f3cb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3cb0-104">SYNTAX</span></span>

```
Add-AzureHDInsightMetastore -Config <AzureHDInsightConfig> -Credential <PSCredential> -DatabaseName <String>
 -MetastoreType <AzureHDInsightMetastoreType> -SqlAzureServerName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3cb0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3cb0-105">DESCRIPTION</span></span>
<span data-ttu-id="f3cb0-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="f3cb0-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="f3cb0-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="f3cb0-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="f3cb0-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="f3cb0-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="f3cb0-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="f3cb0-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f3cb0-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="f3cb0-112">Cmdleten **Add-AzureHDInsightMetastore** lägger till en Microsoft SQL Server-databas till en Azure HDInsight-konfiguration som skapas av den **nya-AzureHDInsightClusterConfig-** cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-112">The **Add-AzureHDInsightMetastore** cmdlet adds a Microsoft SQL Server database to an Azure HDInsight configuration that is created by the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>
<span data-ttu-id="f3cb0-113">Databasen används för att lagra metadata för registrerings data eller Oozie, eller både och.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-113">The database is used to store metadata for Hive or Oozie, or both.</span></span>

## <span data-ttu-id="f3cb0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3cb0-114">EXAMPLES</span></span>

### <span data-ttu-id="f3cb0-115">Exempel 1: lägga till en metastore</span><span class="sxs-lookup"><span data-stu-id="f3cb0-115">Example 1: Add a metastore</span></span>
```
PS C:\>$Metaconfig = Add-AzureHDInsightMetastore -Config $Config -SqlAzureServerName "ContosoSQLServer" -DatabaseName "DBname" -Credential (Get-Credential) -MetastoreType HiveMetaStore
```

<span data-ttu-id="f3cb0-116">Det här kommandot lägger till en SQL Server-databas med namnet ContosoSQLServer som fungerar som en struktur metastore för ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-116">This command adds a SQL Server database named ContosoSQLServer to serve as a Hive metastore for an HDInsight cluster.</span></span>

### <span data-ttu-id="f3cb0-117">Exempel 2: Konfigurera lagring och Lägg till metastores</span><span class="sxs-lookup"><span data-stu-id="f3cb0-117">Example 2: Configure storage and add metastores</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer"
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="f3cb0-118">I det första kommandot används cmdleten **Get-AzureSubscription** för att hämta aktuellt ABONNEMANGS-ID och det sparas sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="f3cb0-119">I det andra och tredje kommandot används cmdleten **Get-AzureStorageKey** för att hämta primär lagrings nycklar för MyBlobStorage och MySecondBlobStorage, och sedan sparas nycklarna i $Key 1-och $Key 2-variabler.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="f3cb0-120">De fjärde, femte och sjätte kommandona använder cmdleten **Get-Credential** för att få autentiseringsuppgifter för det aktuella abonnemanget och för Oozie och Hive och sedan lagra autentiseringsuppgifterna i variabler.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="f3cb0-121">Det slutliga kommandot utför en sekvens med operationer genom att använda dessa cmdletar:</span><span class="sxs-lookup"><span data-stu-id="f3cb0-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="f3cb0-122">**New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="f3cb0-123">**Set-AzureHDInsightDefaultStorage** för att ange standard lagrings kontot för konfigurationen till MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="f3cb0-124">**Add-AzureHDInsightStorage** om du vill lägga till ett andra lagrings konto med namnet MySecondBlobStorage.blob.Core.Windows.net i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="f3cb0-125">**Add-AzureHDInsightMetastore** om du vill lägga till en metastore för Oozie och en metastore för struktur till konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="f3cb0-126">**New-AzureHDInsightCluster** för att skapa ett HDInsight-kluster med den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="f3cb0-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3cb0-127">PARAMETERS</span></span>

### <span data-ttu-id="f3cb0-128">-Config</span><span class="sxs-lookup"><span data-stu-id="f3cb0-128">-Config</span></span>
<span data-ttu-id="f3cb0-129">Anger ett konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-129">Specifies a configuration object.</span></span>
<span data-ttu-id="f3cb0-130">Denna cmdlet lägger till metastore information i det konfigurations objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-130">This cmdlet adds metastore information to the configuration object that this parameter specifies.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3cb0-131">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="f3cb0-131">-Credential</span></span>
<span data-ttu-id="f3cb0-132">Anger de autentiseringsuppgifter som används för att komma åt en SQL Server-databas.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-132">Specifies the credentials that are used to access a SQL Server database.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cb0-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3cb0-133">-DatabaseName</span></span>
<span data-ttu-id="f3cb0-134">Anger namnet på databasen där registrerings data ska lagras eller Oozie.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-134">Specifies the name of the database to store Hive or Oozie metadata.</span></span>

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

### <span data-ttu-id="f3cb0-135">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="f3cb0-135">-MetastoreType</span></span>
<span data-ttu-id="f3cb0-136">Anger typen av metastore.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-136">Specifies the metastore type.</span></span>
<span data-ttu-id="f3cb0-137">De acceptabla värdena för den här parametern är: HiveMetaStore eller OozieMetaStore.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-137">The acceptable values for this parameter are: HiveMetaStore or OozieMetaStore.</span></span>

```yaml
Type: AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3cb0-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="f3cb0-138">-Profile</span></span>
<span data-ttu-id="f3cb0-139">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f3cb0-140">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f3cb0-141">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="f3cb0-141">-SqlAzureServerName</span></span>
<span data-ttu-id="f3cb0-142">Anger det fullständigt kvalificerade domän namnet (FQDN) för SQL Server som innehåller databasen där metadata lagras.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-142">Specifies the fully qualified domain name (FQDN) of the SQL Server that contains the database to store metadata.</span></span>

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

### <span data-ttu-id="f3cb0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3cb0-143">CommonParameters</span></span>
<span data-ttu-id="f3cb0-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3cb0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3cb0-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3cb0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3cb0-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3cb0-146">INPUTS</span></span>

## <span data-ttu-id="f3cb0-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3cb0-147">OUTPUTS</span></span>

## <span data-ttu-id="f3cb0-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3cb0-148">NOTES</span></span>

## <span data-ttu-id="f3cb0-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3cb0-149">RELATED LINKS</span></span>

[<span data-ttu-id="f3cb0-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="f3cb0-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="f3cb0-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f3cb0-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="f3cb0-152">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="f3cb0-152">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="f3cb0-153">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="f3cb0-153">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
