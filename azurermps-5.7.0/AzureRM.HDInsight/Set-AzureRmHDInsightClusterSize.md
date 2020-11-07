---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: eda9032cde317f418132e28917f7543d60ea0bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756509"
---
# <span data-ttu-id="7cc9b-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="7cc9b-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="7cc9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cc9b-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc9b-103">Anger antalet arbets tagare i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cc9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cc9b-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cc9b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cc9b-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc9b-106">Cmdleten **set-AzureRmHDInsightClusterSize** anger antalet Worker-noder i ett angivet Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="7cc9b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cc9b-107">EXAMPLES</span></span>

### <span data-ttu-id="7cc9b-108">Exempel 1: Ange storleken på ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="7cc9b-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="7cc9b-109">Det här kommandot anger storleken på det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="7cc9b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cc9b-110">PARAMETERS</span></span>

### <span data-ttu-id="7cc9b-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="7cc9b-111">-ClusterName</span></span>
<span data-ttu-id="7cc9b-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="7cc9b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc9b-113">-DefaultProfile</span></span>
<span data-ttu-id="7cc9b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7cc9b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc9b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc9b-115">-ResourceGroupName</span></span>
<span data-ttu-id="7cc9b-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7cc9b-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="7cc9b-117">-TargetInstanceCount</span></span>
<span data-ttu-id="7cc9b-118">Anger önskat antal arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc9b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc9b-119">CommonParameters</span></span>
<span data-ttu-id="7cc9b-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc9b-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc9b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc9b-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cc9b-122">INPUTS</span></span>

### <span data-ttu-id="7cc9b-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="7cc9b-123">None</span></span>
<span data-ttu-id="7cc9b-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7cc9b-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7cc9b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cc9b-125">OUTPUTS</span></span>

### <span data-ttu-id="7cc9b-126">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="7cc9b-126">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="7cc9b-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cc9b-127">NOTES</span></span>

## <span data-ttu-id="7cc9b-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cc9b-128">RELATED LINKS</span></span>

