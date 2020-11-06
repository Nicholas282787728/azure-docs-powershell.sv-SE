---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/submit-azurermhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Submit-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 866bd8c8189ca727b3893f09370bcca1136e827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585148"
---
# <span data-ttu-id="59d91-101">Submit-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="59d91-101">Submit-AzureRmHDInsightScriptAction</span></span>

## <span data-ttu-id="59d91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59d91-102">SYNOPSIS</span></span>
<span data-ttu-id="59d91-103">Skickar en ny skript åtgärd till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="59d91-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59d91-104">SYNTAX</span></span>

```
Submit-AzureRmHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="59d91-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59d91-105">DESCRIPTION</span></span>
<span data-ttu-id="59d91-106">Cmdleten **Submit-AzureRmHDInsightScriptAction** skickar en ny skript åtgärd till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="59d91-106">The **Submit-AzureRmHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="59d91-107">Använd *PersistOnSuccess* för att köra skript åtgärden varje gång klustret skalas, så länge skript åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="59d91-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="59d91-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59d91-108">EXAMPLES</span></span>

### <span data-ttu-id="59d91-109">Exempel 1: skicka en ny skript åtgärd till ett pågående HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="59d91-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzureRmHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="59d91-110">Det här kommandot skickar en skript åtgärd till ett HDInsight-kluster som körs.</span><span class="sxs-lookup"><span data-stu-id="59d91-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="59d91-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59d91-111">PARAMETERS</span></span>

### <span data-ttu-id="59d91-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="59d91-112">-ApplicationName</span></span>
<span data-ttu-id="59d91-113">Anger programmets namn för skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="59d91-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="59d91-114">När *ApplicationName* är angivet ska *PersistOnSuccess* vara inställt på false, noderna får innehålla högst 1.</span><span class="sxs-lookup"><span data-stu-id="59d91-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="59d91-115">-ClusterName</span></span>
<span data-ttu-id="59d91-116">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="59d91-116">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d91-117">-DefaultProfile</span></span>
<span data-ttu-id="59d91-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="59d91-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59d91-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="59d91-119">-Name</span></span>
<span data-ttu-id="59d91-120">Anger namnet på skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="59d91-120">Specifies the name of the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="59d91-121">-NodeTypes</span></span>
<span data-ttu-id="59d91-122">Anger de nodtyper som skript åtgärden ska köras på.</span><span class="sxs-lookup"><span data-stu-id="59d91-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-123">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="59d91-123">-Parameters</span></span>
<span data-ttu-id="59d91-124">Anger parametrar för skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="59d91-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="59d91-125">-PersistOnSuccess</span></span>
<span data-ttu-id="59d91-126">Anger att skript åtgärden ska köras varje gång klustret skal för änd ras.</span><span class="sxs-lookup"><span data-stu-id="59d91-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="59d91-127">Denna växel parameter ignoreras om skript åtgärden från början Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="59d91-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d91-128">-ResourceGroupName</span></span>
<span data-ttu-id="59d91-129">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="59d91-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="59d91-130">-URI</span><span class="sxs-lookup"><span data-stu-id="59d91-130">-Uri</span></span>
<span data-ttu-id="59d91-131">Anger den offentliga URI: n för skript åtgärden (ett PowerShell-eller bash-skript).</span><span class="sxs-lookup"><span data-stu-id="59d91-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d91-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d91-132">CommonParameters</span></span>
<span data-ttu-id="59d91-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d91-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d91-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d91-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d91-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59d91-135">INPUTS</span></span>

### <span data-ttu-id="59d91-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="59d91-136">None</span></span>
<span data-ttu-id="59d91-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="59d91-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59d91-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59d91-138">OUTPUTS</span></span>

### <span data-ttu-id="59d91-139">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="59d91-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="59d91-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59d91-140">NOTES</span></span>

## <span data-ttu-id="59d91-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59d91-141">RELATED LINKS</span></span>

[<span data-ttu-id="59d91-142">Add-AzureRmHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="59d91-142">Add-AzureRmHDInsightScriptAction</span></span>](./Add-AzureRmHDInsightScriptAction.md)


