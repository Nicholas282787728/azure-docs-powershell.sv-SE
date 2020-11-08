---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 1B6AC121-1AA0-4D28-B1EA-C96147FDD168
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02435c28ca17666a3b19389fde039353f3d779a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093442"
---
# <span data-ttu-id="6bd93-101">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="6bd93-101">Add-AzureHDInsightStorage</span></span>

## <span data-ttu-id="6bd93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6bd93-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd93-103">Lägger till en post för en BLOB-lagringsenhet i en HDInsight-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6bd93-103">Adds a blob storage account entry to an HDInsight configuration.</span></span>

## <span data-ttu-id="6bd93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6bd93-104">SYNTAX</span></span>

```
Add-AzureHDInsightStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6bd93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6bd93-105">DESCRIPTION</span></span>
<span data-ttu-id="6bd93-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="6bd93-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6bd93-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="6bd93-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6bd93-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6bd93-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6bd93-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="6bd93-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6bd93-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="6bd93-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6bd93-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6bd93-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6bd93-112">Cmdleten **Add-AzureHDInsightStorage** lägger till en post för BLOB-lagringsenhet i en Azure HDInsight-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6bd93-112">The **Add-AzureHDInsightStorage** cmdlet adds a blob storage account entry to an Azure HDInsight configuration.</span></span>

## <span data-ttu-id="6bd93-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6bd93-113">EXAMPLES</span></span>

### <span data-ttu-id="6bd93-114">Exempel 1: lägga till ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="6bd93-114">Example 1: Add a storage account</span></span>
```
PS C:\>$StoreConfig = Add-AzureHDInsightStorage -Config $Config -StorageAccountName "MyStorage" -StorageAccountKey "Key"
```

<span data-ttu-id="6bd93-115">Det här kommandot lägger till ett lagrings konto med namnet min lagring i det konfigurationsfiler som lagras i $Config och lagrar sedan konfigurationen i $StoreConfig-variabeln.</span><span class="sxs-lookup"><span data-stu-id="6bd93-115">This command adds a storage account named MyStorage to the configuration object stored in $Config, and then stores the configuration in the $StoreConfig variable.</span></span>

### <span data-ttu-id="6bd93-116">Exempel 2: Konfigurera flera lagrings konton</span><span class="sxs-lookup"><span data-stu-id="6bd93-116">Example 2: Configure multiple storage accounts</span></span>
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
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "Sqlserver01.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="6bd93-117">I det första kommandot används cmdleten **Get-AzureSubscription** för att hämta aktuellt ABONNEMANGS-ID och det sparas sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="6bd93-117">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="6bd93-118">I det andra och tredje kommandot används cmdleten **Get-AzureStorageKey** för att hämta primär lagrings nycklar för MyBlobStorage och MySecondBlobStorage, och sedan sparas nycklarna i $Key 1-och $Key 2-variabler.</span><span class="sxs-lookup"><span data-stu-id="6bd93-118">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="6bd93-119">De fjärde, femte och sjätte kommandona hämtar autentiseringsuppgifter för det aktuella abonnemanget och för Oozie och Hive och lagrar sedan autentiseringsuppgifterna i variabler.</span><span class="sxs-lookup"><span data-stu-id="6bd93-119">The fourth, fifth, and sixth commands get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="6bd93-120">Det slutliga kommandot utför en sekvens med operationer genom att använda dessa cmdletar:</span><span class="sxs-lookup"><span data-stu-id="6bd93-120">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="6bd93-121">**New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration</span><span class="sxs-lookup"><span data-stu-id="6bd93-121">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration</span></span>
- <span data-ttu-id="6bd93-122">**Set-AzureHDInsightDefaultStorage** om du vill ange standard lagrings kontot för konfigurationen till MyBlobStorage.blob.Core.Windows.net</span><span class="sxs-lookup"><span data-stu-id="6bd93-122">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net</span></span>
- <span data-ttu-id="6bd93-123">**Add-AzureHDInsightStorage** om du vill lägga till ett andra lagrings konto med MySecondBlobStorage.blob.Core.Windows.net i konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6bd93-123">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration</span></span>
- <span data-ttu-id="6bd93-124">**Add-AzureHDInsightStorage** om du vill lägga till en metastore för Oozie och en metastore för struktur i konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6bd93-124">**Add-AzureHDInsightStorage** to add a metastore for Oozie and a metastore for Hive to the configuration</span></span>
- <span data-ttu-id="6bd93-125">**New-AzureHDInsightCluster** för att skapa ett HDInsight-kluster med den nya konfigurationen</span><span class="sxs-lookup"><span data-stu-id="6bd93-125">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration</span></span>

## <span data-ttu-id="6bd93-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6bd93-126">PARAMETERS</span></span>

### <span data-ttu-id="6bd93-127">-Config</span><span class="sxs-lookup"><span data-stu-id="6bd93-127">-Config</span></span>
<span data-ttu-id="6bd93-128">Anger ett konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="6bd93-128">Specifies a configuration object.</span></span>
<span data-ttu-id="6bd93-129">Denna cmdlet lägger till information om lagrings konto i det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="6bd93-129">This cmdlet adds storage account information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="6bd93-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="6bd93-130">-Profile</span></span>
<span data-ttu-id="6bd93-131">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6bd93-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6bd93-132">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6bd93-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bd93-133">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6bd93-133">-StorageAccountKey</span></span>
<span data-ttu-id="6bd93-134">Anger den lagrings konto plats som används för att komma åt ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6bd93-134">Specifies the storage account key that is used to access a storage account.</span></span>

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

### <span data-ttu-id="6bd93-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6bd93-135">-StorageAccountName</span></span>
<span data-ttu-id="6bd93-136">Anger namnet på det Azure Storage-konto som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6bd93-136">Specifies the name of the Azure storage account to add.</span></span>

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

### <span data-ttu-id="6bd93-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd93-137">CommonParameters</span></span>
<span data-ttu-id="6bd93-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bd93-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd93-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd93-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd93-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6bd93-140">INPUTS</span></span>

## <span data-ttu-id="6bd93-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6bd93-141">OUTPUTS</span></span>

## <span data-ttu-id="6bd93-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6bd93-142">NOTES</span></span>

## <span data-ttu-id="6bd93-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6bd93-143">RELATED LINKS</span></span>

[<span data-ttu-id="6bd93-144">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6bd93-144">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="6bd93-145">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6bd93-145">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="6bd93-146">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="6bd93-146">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


