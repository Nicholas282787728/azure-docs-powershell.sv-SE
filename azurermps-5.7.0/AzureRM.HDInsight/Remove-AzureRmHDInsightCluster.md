---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/remove-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: 1029871a2125668c732f7ff541582f06dbd790c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756285"
---
# <span data-ttu-id="423f0-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="423f0-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="423f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="423f0-102">SYNOPSIS</span></span>
<span data-ttu-id="423f0-103">Tar bort angivet HDInsight-kluster från aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="423f0-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="423f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="423f0-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423f0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="423f0-105">DESCRIPTION</span></span>
<span data-ttu-id="423f0-106">Cmdleten **Remove-AzureRmHDInsightCluster** tar bort angivet HDInsight-serverkluster från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="423f0-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="423f0-107">Den här åtgärden tar också bort data som lagrats i HDFS (Hadoop Distributed File System) i klustret.</span><span class="sxs-lookup"><span data-stu-id="423f0-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="423f0-108">Data som lagras i det associerade Azure Storage-kontot tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="423f0-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="423f0-109">Data som lagras i externa metastores tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="423f0-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="423f0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="423f0-110">EXAMPLES</span></span>

### <span data-ttu-id="423f0-111">Exempel 1: ta bort ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="423f0-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="423f0-112">Det här kommandot tar bort klustret med namnet din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="423f0-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="423f0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="423f0-113">PARAMETERS</span></span>

### <span data-ttu-id="423f0-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="423f0-114">-ClusterName</span></span>
<span data-ttu-id="423f0-115">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="423f0-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="423f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423f0-116">-DefaultProfile</span></span>
<span data-ttu-id="423f0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="423f0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="423f0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="423f0-118">-ResourceGroupName</span></span>
<span data-ttu-id="423f0-119">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="423f0-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="423f0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423f0-120">CommonParameters</span></span>
<span data-ttu-id="423f0-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="423f0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423f0-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="423f0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423f0-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="423f0-123">INPUTS</span></span>

### <span data-ttu-id="423f0-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="423f0-124">None</span></span>
<span data-ttu-id="423f0-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="423f0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="423f0-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="423f0-126">OUTPUTS</span></span>

### <span data-ttu-id="423f0-127">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="423f0-127">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="423f0-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="423f0-128">NOTES</span></span>

## <span data-ttu-id="423f0-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="423f0-129">RELATED LINKS</span></span>

[<span data-ttu-id="423f0-130">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="423f0-130">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="423f0-131">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="423f0-131">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


