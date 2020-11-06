---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: a09da5122403d971d8b5d1abde79c8a9a95c3ecd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584740"
---
# <span data-ttu-id="c515b-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c515b-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="c515b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c515b-102">SYNOPSIS</span></span>
<span data-ttu-id="c515b-103">Tar bort angivet HDInsight-kluster från aktuell prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c515b-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c515b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c515b-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c515b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c515b-105">DESCRIPTION</span></span>
<span data-ttu-id="c515b-106">Cmdleten **Remove-AzureRmHDInsightCluster** tar bort angivet HDInsight-serverkluster från ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c515b-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="c515b-107">Den här åtgärden tar också bort data som lagrats i HDFS (Hadoop Distributed File System) i klustret.</span><span class="sxs-lookup"><span data-stu-id="c515b-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="c515b-108">Data som lagras i det associerade Azure Storage-kontot tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="c515b-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="c515b-109">Data som lagras i externa metastores tas inte bort.</span><span class="sxs-lookup"><span data-stu-id="c515b-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="c515b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c515b-110">EXAMPLES</span></span>

### <span data-ttu-id="c515b-111">Exempel 1: ta bort ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="c515b-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="c515b-112">Det här kommandot tar bort klustret med namnet din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c515b-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c515b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c515b-113">PARAMETERS</span></span>

### <span data-ttu-id="c515b-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="c515b-114">-ClusterName</span></span>
<span data-ttu-id="c515b-115">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="c515b-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="c515b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c515b-116">-ResourceGroupName</span></span>
<span data-ttu-id="c515b-117">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c515b-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c515b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c515b-118">-DefaultProfile</span></span>
<span data-ttu-id="c515b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c515b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c515b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c515b-120">CommonParameters</span></span>
<span data-ttu-id="c515b-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c515b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c515b-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c515b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c515b-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c515b-123">INPUTS</span></span>

## <span data-ttu-id="c515b-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c515b-124">OUTPUTS</span></span>

### <span data-ttu-id="c515b-125">Microsoft. Azure. Management. HDInsight. Models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="c515b-125">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="c515b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c515b-126">NOTES</span></span>

## <span data-ttu-id="c515b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c515b-127">RELATED LINKS</span></span>

[<span data-ttu-id="c515b-128">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c515b-128">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="c515b-129">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c515b-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


