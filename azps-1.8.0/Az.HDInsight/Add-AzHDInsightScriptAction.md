---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: b34fbf01196f5e25cb62ed7d9ecb0ba78aafa17f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916669"
---
# <span data-ttu-id="6aad1-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="6aad1-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="6aad1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6aad1-102">SYNOPSIS</span></span>
<span data-ttu-id="6aad1-103">Lägger till en skript åtgärd i ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="6aad1-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="6aad1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6aad1-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aad1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6aad1-105">DESCRIPTION</span></span>
<span data-ttu-id="6aad1-106">Cmdleten **Add-AzHDInsightScriptAction** lägger till skript åtgärder i HDInsight-konfigurationsobjektet som skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aad1-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="6aad1-107">Skript åtgärder tillhandahåller funktioner som används för att installera ytterligare program vara eller för att ändra konfigurationen för program som körs i ett Hadoop-kluster med hjälp av Windows PowerShell-eller bash-skript (för Windows-eller Linux-kluster).</span><span class="sxs-lookup"><span data-stu-id="6aad1-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="6aad1-108">En skript åtgärd körs på klusternoderna när HDInsight-kluster distribueras och körs efter noder i klustrets fullständiga HDInsight-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="6aad1-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="6aad1-109">Skript åtgärden körs under administratörs behörighet och ger full åtkomst till klusternoderna.</span><span class="sxs-lookup"><span data-stu-id="6aad1-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="6aad1-110">Du kan tillhandahålla varje kluster med en lista med skript åtgärder som ska köras i en viss sekvens.</span><span class="sxs-lookup"><span data-stu-id="6aad1-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="6aad1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6aad1-111">EXAMPLES</span></span>

### <span data-ttu-id="6aad1-112">Exempel 1: lägga till en skript åtgärd i ett kluster konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="6aad1-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="6aad1-113">Det här kommandot lägger till en skript åtgärd för Head-och Worker-noder i ditt-Hadoop-001-kluster och körs när klustret skapas.</span><span class="sxs-lookup"><span data-stu-id="6aad1-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="6aad1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6aad1-114">PARAMETERS</span></span>

### <span data-ttu-id="6aad1-115">-Config</span><span class="sxs-lookup"><span data-stu-id="6aad1-115">-Config</span></span>
<span data-ttu-id="6aad1-116">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6aad1-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="6aad1-117">Det här objektet skapas av cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="6aad1-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6aad1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aad1-118">-DefaultProfile</span></span>
<span data-ttu-id="6aad1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6aad1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6aad1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6aad1-120">-Name</span></span>
<span data-ttu-id="6aad1-121">Anger namnet på skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6aad1-121">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aad1-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6aad1-122">-NodeType</span></span>
<span data-ttu-id="6aad1-123">Anger nodtyp för körning av skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6aad1-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="6aad1-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6aad1-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6aad1-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="6aad1-125">HeadNode</span></span>
- <span data-ttu-id="6aad1-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="6aad1-126">WorkerNode</span></span>
- <span data-ttu-id="6aad1-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="6aad1-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aad1-128">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="6aad1-128">-Parameters</span></span>
<span data-ttu-id="6aad1-129">Anger parametrar för skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6aad1-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aad1-130">-URI</span><span class="sxs-lookup"><span data-stu-id="6aad1-130">-Uri</span></span>
<span data-ttu-id="6aad1-131">Anger den offentliga URI: n för skript åtgärden (ett PowerShell-eller bash-skript).</span><span class="sxs-lookup"><span data-stu-id="6aad1-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aad1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aad1-132">CommonParameters</span></span>
<span data-ttu-id="6aad1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aad1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aad1-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aad1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aad1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6aad1-135">INPUTS</span></span>

### <span data-ttu-id="6aad1-136">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6aad1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6aad1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6aad1-137">OUTPUTS</span></span>

### <span data-ttu-id="6aad1-138">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6aad1-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="6aad1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6aad1-139">NOTES</span></span>

## <span data-ttu-id="6aad1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6aad1-140">RELATED LINKS</span></span>

[<span data-ttu-id="6aad1-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6aad1-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

