---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 15C5D659-472B-41DD-806A-A0A175434EE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/submit-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Submit-AzHDInsightScriptAction.md
ms.openlocfilehash: dfae83e6bd540a83475f02ed95382bebff2ec7a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259944"
---
# <span data-ttu-id="fc635-101">Submit-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="fc635-101">Submit-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="fc635-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc635-102">SYNOPSIS</span></span>
<span data-ttu-id="fc635-103">Skickar en ny skript åtgärd till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="fc635-103">Submits a new script action to an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fc635-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc635-104">SYNTAX</span></span>

```
Submit-AzHDInsightScriptAction [-ClusterName] <String> [-Name] <String> [-Uri] <Uri>
 [-NodeTypes] <RuntimeScriptActionClusterNodeType[]> [[-Parameters] <String>] [[-ApplicationName] <String>]
 [-PersistOnSuccess] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc635-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc635-105">DESCRIPTION</span></span>
<span data-ttu-id="fc635-106">Cmdleten **Submit-AzHDInsightScriptAction** skickar en ny skript åtgärd till ett Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="fc635-106">The **Submit-AzHDInsightScriptAction** cmdlet submits a new script action to an Azure HDInsight cluster.</span></span>
<span data-ttu-id="fc635-107">Använd *PersistOnSuccess* för att köra skript åtgärden varje gång klustret skalas, så länge skript åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="fc635-107">Use *PersistOnSuccess* to have the script action run each time the cluster is scaled up, as long as the script action initially succeeds.</span></span>

## <span data-ttu-id="fc635-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc635-108">EXAMPLES</span></span>

### <span data-ttu-id="fc635-109">Exempel 1: skicka en ny skript åtgärd till ett pågående HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="fc635-109">Example 1: Submit a new script action to a running HDInsight cluster</span></span>
```
PS C:\>Submit-AzHDInsightScriptAction `
            -ClusterName "your-hadoop-001" `
            -Name "scriptaction" `
            -Uri "<script action URI>" `
            -NodeTypes Worker -PersistOnSuccess
```

<span data-ttu-id="fc635-110">Det här kommandot skickar en skript åtgärd till ett HDInsight-kluster som körs.</span><span class="sxs-lookup"><span data-stu-id="fc635-110">This command submits a script action to a running HDInsight cluster.</span></span>

## <span data-ttu-id="fc635-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc635-111">PARAMETERS</span></span>

### <span data-ttu-id="fc635-112">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="fc635-112">-ApplicationName</span></span>
<span data-ttu-id="fc635-113">Anger programmets namn för skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fc635-113">Specifies the application name for the script action.</span></span>
<span data-ttu-id="fc635-114">När *ApplicationName* är angivet ska *PersistOnSuccess* vara inställt på false, noderna får innehålla högst 1.</span><span class="sxs-lookup"><span data-stu-id="fc635-114">When *ApplicationName* is specified, *PersistOnSuccess* should be set to False, nodes must contain only edgenode, and script action count should equal 1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="fc635-115">-ClusterName</span></span>
<span data-ttu-id="fc635-116">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="fc635-116">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc635-117">-DefaultProfile</span></span>
<span data-ttu-id="fc635-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fc635-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc635-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc635-119">-Name</span></span>
<span data-ttu-id="fc635-120">Anger namnet på skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fc635-120">Specifies the name of the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-121">-NodeTypes</span><span class="sxs-lookup"><span data-stu-id="fc635-121">-NodeTypes</span></span>
<span data-ttu-id="fc635-122">Anger de nodtyper som skript åtgärden ska köras på.</span><span class="sxs-lookup"><span data-stu-id="fc635-122">Specifies the node types on which to run the script action.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-123">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="fc635-123">-Parameters</span></span>
<span data-ttu-id="fc635-124">Anger parametrar för skript åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fc635-124">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-125">-PersistOnSuccess</span><span class="sxs-lookup"><span data-stu-id="fc635-125">-PersistOnSuccess</span></span>
<span data-ttu-id="fc635-126">Anger att skript åtgärden ska köras varje gång klustret skal för änd ras.</span><span class="sxs-lookup"><span data-stu-id="fc635-126">Indicates that the script action should run each time the cluster is scaled up.</span></span>
<span data-ttu-id="fc635-127">Denna växel parameter ignoreras om skript åtgärden från början Miss lyckas.</span><span class="sxs-lookup"><span data-stu-id="fc635-127">This switch parameter is ignored if the script action initially fails.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc635-128">-ResourceGroupName</span></span>
<span data-ttu-id="fc635-129">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fc635-129">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fc635-130">-URI</span><span class="sxs-lookup"><span data-stu-id="fc635-130">-Uri</span></span>
<span data-ttu-id="fc635-131">Anger den offentliga URI: n för skript åtgärden (ett PowerShell-eller bash-skript).</span><span class="sxs-lookup"><span data-stu-id="fc635-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc635-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc635-132">CommonParameters</span></span>
<span data-ttu-id="fc635-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc635-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc635-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc635-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc635-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc635-135">INPUTS</span></span>

### <span data-ttu-id="fc635-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fc635-136">System.String</span></span>

### <span data-ttu-id="fc635-137">System. URI</span><span class="sxs-lookup"><span data-stu-id="fc635-137">System.Uri</span></span>

### <span data-ttu-id="fc635-138">Microsoft. Azure. commands. HDInsight. Models. Management. RuntimeScriptActionClusterNodeType []</span><span class="sxs-lookup"><span data-stu-id="fc635-138">Microsoft.Azure.Commands.HDInsight.Models.Management.RuntimeScriptActionClusterNodeType[]</span></span>

## <span data-ttu-id="fc635-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc635-139">OUTPUTS</span></span>

### <span data-ttu-id="fc635-140">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightRuntimeScriptActionOperationResource</span><span class="sxs-lookup"><span data-stu-id="fc635-140">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightRuntimeScriptActionOperationResource</span></span>

## <span data-ttu-id="fc635-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc635-141">NOTES</span></span>

## <span data-ttu-id="fc635-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc635-142">RELATED LINKS</span></span>

[<span data-ttu-id="fc635-143">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="fc635-143">Add-AzHDInsightScriptAction</span></span>](./Add-AzHDInsightScriptAction.md)

