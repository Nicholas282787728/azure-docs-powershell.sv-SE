---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520604"
---
# <span data-ttu-id="6abb8-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6abb8-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="6abb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6abb8-102">SYNOPSIS</span></span>
<span data-ttu-id="6abb8-103">Tar bort angivet HDInsight-kluster från aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="6abb8-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="6abb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6abb8-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6abb8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6abb8-105">DESCRIPTION</span></span>
<span data-ttu-id="6abb8-106">Cmdleten **Remove-AzHDInsightCluster** tar bort angivet HDInsight-serverkluster från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6abb8-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="6abb8-107">Den här åtgärden tar också bort data som lagrats i HDFS (Hadoop Distributed File System) i klustret.</span><span class="sxs-lookup"><span data-stu-id="6abb8-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="6abb8-108">Data som lagras i det associerade Azure Storage-kontot tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="6abb8-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="6abb8-109">Data som lagras i externa metastores tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="6abb8-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="6abb8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6abb8-110">EXAMPLES</span></span>

### <span data-ttu-id="6abb8-111">Exempel 1: ta bort ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="6abb8-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="6abb8-112">Det här kommandot tar bort klustret med namnet din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="6abb8-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6abb8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6abb8-113">PARAMETERS</span></span>

### <span data-ttu-id="6abb8-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="6abb8-114">-ClusterName</span></span>
<span data-ttu-id="6abb8-115">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="6abb8-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6abb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6abb8-116">-DefaultProfile</span></span>
<span data-ttu-id="6abb8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6abb8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6abb8-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6abb8-118">-PassThru</span></span>
<span data-ttu-id="6abb8-119">Om det finns en PassThru visas resultatet</span><span class="sxs-lookup"><span data-stu-id="6abb8-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6abb8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6abb8-120">-ResourceGroupName</span></span>
<span data-ttu-id="6abb8-121">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6abb8-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6abb8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6abb8-122">CommonParameters</span></span>
<span data-ttu-id="6abb8-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6abb8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6abb8-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6abb8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6abb8-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6abb8-125">INPUTS</span></span>

### <span data-ttu-id="6abb8-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="6abb8-126">None</span></span>
## <span data-ttu-id="6abb8-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6abb8-127">OUTPUTS</span></span>

### <span data-ttu-id="6abb8-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6abb8-128">System.Boolean</span></span>
## <span data-ttu-id="6abb8-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6abb8-129">NOTES</span></span>

## <span data-ttu-id="6abb8-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6abb8-130">RELATED LINKS</span></span>

[<span data-ttu-id="6abb8-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6abb8-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="6abb8-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6abb8-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


