---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319564"
---
# <span data-ttu-id="66dd9-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66dd9-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="66dd9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="66dd9-103">Tar bort angivet HDInsight-kluster från aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="66dd9-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="66dd9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66dd9-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66dd9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66dd9-105">DESCRIPTION</span></span>
<span data-ttu-id="66dd9-106">Cmdleten **Remove-AzHDInsightCluster** tar bort angivet HDInsight-serverkluster från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="66dd9-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="66dd9-107">Den här åtgärden tar också bort data som lagrats i HDFS (Hadoop Distributed File System) i klustret.</span><span class="sxs-lookup"><span data-stu-id="66dd9-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="66dd9-108">Data som lagras i det associerade Azure Storage-kontot tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="66dd9-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="66dd9-109">Data som lagras i externa metastores tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="66dd9-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="66dd9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66dd9-110">EXAMPLES</span></span>

### <span data-ttu-id="66dd9-111">Exempel 1: ta bort ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="66dd9-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="66dd9-112">Det här kommandot tar bort klustret med namnet din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="66dd9-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="66dd9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66dd9-113">PARAMETERS</span></span>

### <span data-ttu-id="66dd9-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="66dd9-114">-ClusterName</span></span>
<span data-ttu-id="66dd9-115">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="66dd9-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="66dd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66dd9-116">-DefaultProfile</span></span>
<span data-ttu-id="66dd9-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66dd9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66dd9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66dd9-118">-ResourceGroupName</span></span>
<span data-ttu-id="66dd9-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="66dd9-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="66dd9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66dd9-120">-PassThru</span></span>
<span data-ttu-id="66dd9-121">Om det finns en PassThru visas resultatet</span><span class="sxs-lookup"><span data-stu-id="66dd9-121">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="66dd9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66dd9-122">CommonParameters</span></span>
<span data-ttu-id="66dd9-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66dd9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66dd9-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66dd9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66dd9-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66dd9-125">INPUTS</span></span>

### <span data-ttu-id="66dd9-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="66dd9-126">None</span></span>
## <span data-ttu-id="66dd9-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66dd9-127">OUTPUTS</span></span>

### <span data-ttu-id="66dd9-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66dd9-128">System.Boolean</span></span>
## <span data-ttu-id="66dd9-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66dd9-129">NOTES</span></span>

## <span data-ttu-id="66dd9-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66dd9-130">RELATED LINKS</span></span>

[<span data-ttu-id="66dd9-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66dd9-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="66dd9-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="66dd9-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


