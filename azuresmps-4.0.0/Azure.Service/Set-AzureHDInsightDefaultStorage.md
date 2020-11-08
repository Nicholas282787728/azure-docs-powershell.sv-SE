---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF41DDBA-6D4B-47A5-BCFF-3D0BB1D375C5
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2b6aaf5e8564b3eea675a57176b8f7118d2c7a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099190"
---
# <span data-ttu-id="47013-101">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="47013-101">Set-AzureHDInsightDefaultStorage</span></span>

## <span data-ttu-id="47013-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47013-102">SYNOPSIS</span></span>
<span data-ttu-id="47013-103">Anger standard lagrings konto för ett HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="47013-103">Sets the default storage account for an HDInsight cluster.</span></span>

## <span data-ttu-id="47013-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47013-104">SYNTAX</span></span>

```
Set-AzureHDInsightDefaultStorage -Config <AzureHDInsightConfig> -StorageAccountKey <String>
 -StorageAccountName <String> -StorageContainerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47013-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47013-105">DESCRIPTION</span></span>
<span data-ttu-id="47013-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="47013-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="47013-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="47013-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="47013-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="47013-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="47013-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="47013-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="47013-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="47013-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="47013-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="47013-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="47013-112">Cmdleten **set-AzureHDInsightDefaultStorage** anger standard lagrings kontot för en HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="47013-112">The **Set-AzureHDInsightDefaultStorage** cmdlet sets the default storage account for an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="47013-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47013-113">EXAMPLES</span></span>

### <span data-ttu-id="47013-114">Exempel 1: Ange standard lagrings konto</span><span class="sxs-lookup"><span data-stu-id="47013-114">Example 1: Set the default storage account</span></span>
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

<span data-ttu-id="47013-115">I det första kommandot används cmdleten **Get-AzureSubscription** för att hämta aktuellt ABONNEMANGS-ID och det sparas sedan i $SubId variabel.</span><span class="sxs-lookup"><span data-stu-id="47013-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="47013-116">I det andra och tredje kommandot används cmdleten **Get-AzureStorageKey** för att hämta primär lagrings nycklar för MyBlobStorage och MySecondBlobStorage, och sedan sparas nycklarna i $Key 1-och $Key 2-variabler.</span><span class="sxs-lookup"><span data-stu-id="47013-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="47013-117">De fjärde, femte och sjätte kommandona använder cmdleten **Get-Credential** för att få autentiseringsuppgifter för det aktuella abonnemanget och lagrar sedan autentiseringsuppgifterna i $Creds, $OozieCreds och $HiveCreds variabler.</span><span class="sxs-lookup"><span data-stu-id="47013-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription, and then stores the credentials in the $Creds, $OozieCreds, and $HiveCreds variables.</span></span>

<span data-ttu-id="47013-118">Det slutliga kommandot utför en sekvens med operationer genom att använda dessa cmdletar:</span><span class="sxs-lookup"><span data-stu-id="47013-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="47013-119">**New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration.</span><span class="sxs-lookup"><span data-stu-id="47013-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="47013-120">**Set-AzureHDInsightDefaultStorage** för att ange standard lagrings kontot för konfigurationen till MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="47013-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="47013-121">**Add-AzureHDInsightStorage** om du vill lägga till ett andra lagrings konto med namnet MySecondBlobStorage.blob.Core.Windows.net i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="47013-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="47013-122">**Add-AzureHDInsightMetastore** om du vill lägga till en metastore för Oozie och en metastore för struktur till konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="47013-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="47013-123">**New-AzureHDInsightCluster** för att skapa ett HDInsight-kluster med den nya konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="47013-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="47013-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47013-124">PARAMETERS</span></span>

### <span data-ttu-id="47013-125">-Config</span><span class="sxs-lookup"><span data-stu-id="47013-125">-Config</span></span>
<span data-ttu-id="47013-126">Anger ett konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="47013-126">Specifies a configuration object.</span></span>
<span data-ttu-id="47013-127">Denna cmdlet anger standard lagrings kontot för det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="47013-127">This cmdlet sets the default storage account for the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="47013-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="47013-128">-Profile</span></span>
<span data-ttu-id="47013-129">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="47013-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="47013-130">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="47013-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47013-131">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="47013-131">-StorageAccountKey</span></span>
<span data-ttu-id="47013-132">Anger den lagrings konto plats som används för att komma åt standard lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="47013-132">Specifies the storage account key that is used to access the default storage account.</span></span>

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

### <span data-ttu-id="47013-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47013-133">-StorageAccountName</span></span>
<span data-ttu-id="47013-134">Anger namnet på ett standard lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="47013-134">Specifies the name of a default storage account.</span></span>

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

### <span data-ttu-id="47013-135">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="47013-135">-StorageContainerName</span></span>
<span data-ttu-id="47013-136">Anger namnet på standard lagrings behållaren för ett kluster.</span><span class="sxs-lookup"><span data-stu-id="47013-136">Specifies the name of the default storage container for a cluster.</span></span>

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

### <span data-ttu-id="47013-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47013-137">CommonParameters</span></span>
<span data-ttu-id="47013-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47013-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47013-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47013-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47013-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47013-140">INPUTS</span></span>

## <span data-ttu-id="47013-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47013-141">OUTPUTS</span></span>

## <span data-ttu-id="47013-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47013-142">NOTES</span></span>

## <span data-ttu-id="47013-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47013-143">RELATED LINKS</span></span>

[<span data-ttu-id="47013-144">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="47013-144">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="47013-145">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="47013-145">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="47013-146">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="47013-146">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="47013-147">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="47013-147">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


