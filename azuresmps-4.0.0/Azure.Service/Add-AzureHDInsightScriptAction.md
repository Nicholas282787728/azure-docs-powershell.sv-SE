---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093446"
---
# <span data-ttu-id="d9ec4-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="d9ec4-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="d9ec4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9ec4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ec4-103">Lägger till en HDInsight-skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="d9ec4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9ec4-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9ec4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9ec4-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ec4-106">Den här versionen av Azure PowerShell HDInsight är inaktuell.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="d9ec4-107">Dessa cmdletar tas bort den 1 januari 2017.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="d9ec4-108">Använd den nyare versionen av Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="d9ec4-109">Information om hur du använder nya HDInsight för att skapa ett kluster finns i [skapa Linux-baserade kluster i HDInsight med Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="d9ec4-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="d9ec4-110">Information om hur du skickar jobb med Azure PowerShell och andra metoder finns i [Skicka Hadoop-jobb i HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="d9ec4-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="d9ec4-111">Referensinformation om Azure PowerShell HDInsight finns i [Azure HDInsight cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d9ec4-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="d9ec4-112">Cmdleten **Add-AzureHDInsightScriptAction** tillhandahåller Azure HDInsight-funktioner som används för att installera ytterligare program vara eller för att ändra konfigurationen för program som körs i ett Hadoop-kluster med hjälp av Windows PowerShell-skript.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="d9ec4-113">En skript åtgärd körs på klusternoderna när HDInsight-kluster distribueras och körs efter noder i klustrets fullständiga HDInsight-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="d9ec4-114">Skript åtgärden körs under administratörs behörighet och ger full åtkomst till klusternoderna.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="d9ec4-115">Du kan tillhandahålla varje kluster med en lista med skript åtgärder som ska köras i en viss sekvens.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="d9ec4-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9ec4-116">EXAMPLES</span></span>

### <span data-ttu-id="d9ec4-117">Exempel 1: lägga till en skript åtgärd i ett kluster</span><span class="sxs-lookup"><span data-stu-id="d9ec4-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="d9ec4-118">I det första kommandot används cmdleten **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration och sedan lagras den i $config variabel.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="d9ec4-119">Med det andra kommandot används cmdleten **Add-AzureHDInsightScriptAction** för att lägga till skript åtgärden med namnet TestScriptAction i $config.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="d9ec4-120">I det sista kommandot används cmdleten **New-AzureHDInsightCluster** för att skapa ett nytt HDInsight-kluster som kör skript åtgärden som lagras i $config.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="d9ec4-121">Exempel 2: lägga till flera skript åtgärder i ett kluster</span><span class="sxs-lookup"><span data-stu-id="d9ec4-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="d9ec4-122">I det första kommandot används cmdleten **New-AzureHDInsightClusterConfig** för att skapa en HDInsight-kluster konfiguration och sedan lagras den i $config variabel.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="d9ec4-123">Med det andra kommandot används cmdleten **Add-AzureHDInsightScriptAction** för att lägga till den angivna skript åtgärden i $config och sedan används pipeline-operatorn för att skicka $config till **AzureHDInsightScriptAction** en andra gång för att lägga till en andra skript åtgärd för $config.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="d9ec4-124">Det sista kommandot använder cmdleten **New-AzureHDInsightCluster** för att skapa ett kluster som kör skript åtgärderna i $config.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="d9ec4-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9ec4-125">PARAMETERS</span></span>

### <span data-ttu-id="d9ec4-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="d9ec4-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="d9ec4-127">Anger de noder som du vill köra ett skript för.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="d9ec4-128">De acceptabla värdena för den här parametern är: HeadNode eller DataNode.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="d9ec4-129">Du kan ange ett eller båda värden.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ec4-130">-Config</span><span class="sxs-lookup"><span data-stu-id="d9ec4-130">-Config</span></span>
<span data-ttu-id="d9ec4-131">Anger ett konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-131">Specifies a configuration object.</span></span>
<span data-ttu-id="d9ec4-132">Denna cmdlet lägger till skript åtgärds information till det objekt som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9ec4-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9ec4-133">-Name</span></span>
<span data-ttu-id="d9ec4-134">Anger namnet på en skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-134">Specifies the name of a script action.</span></span>

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

### <span data-ttu-id="d9ec4-135">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="d9ec4-135">-Parameters</span></span>
<span data-ttu-id="d9ec4-136">Anger de parametrar som krävs för en skript åtgärd.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="d9ec4-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="d9ec4-137">-Profile</span></span>
<span data-ttu-id="d9ec4-138">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9ec4-139">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9ec4-140">-URI</span><span class="sxs-lookup"><span data-stu-id="d9ec4-140">-Uri</span></span>
<span data-ttu-id="d9ec4-141">Anger URI-platsen för ett skript som ska köras.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ec4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ec4-142">CommonParameters</span></span>
<span data-ttu-id="d9ec4-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ec4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ec4-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9ec4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ec4-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9ec4-145">INPUTS</span></span>

## <span data-ttu-id="d9ec4-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9ec4-146">OUTPUTS</span></span>

## <span data-ttu-id="d9ec4-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9ec4-147">NOTES</span></span>

## <span data-ttu-id="d9ec4-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9ec4-148">RELATED LINKS</span></span>

[<span data-ttu-id="d9ec4-149">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d9ec4-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="d9ec4-150">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d9ec4-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


