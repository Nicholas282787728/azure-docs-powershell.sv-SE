---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926642"
---
# <span data-ttu-id="ae52d-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="ae52d-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="ae52d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae52d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae52d-103">Anger antalet arbets tagare i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="ae52d-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="ae52d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae52d-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae52d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae52d-105">DESCRIPTION</span></span>
<span data-ttu-id="ae52d-106">Cmdleten **set-AzHDInsightClusterSize** anger antalet Worker-noder i ett angivet Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="ae52d-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="ae52d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae52d-107">EXAMPLES</span></span>

### <span data-ttu-id="ae52d-108">Exempel 1: Ange storleken på ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="ae52d-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="ae52d-109">Det här kommandot anger storleken på det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="ae52d-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ae52d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae52d-110">PARAMETERS</span></span>

### <span data-ttu-id="ae52d-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="ae52d-111">-ClusterName</span></span>
<span data-ttu-id="ae52d-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="ae52d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ae52d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae52d-113">-DefaultProfile</span></span>
<span data-ttu-id="ae52d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ae52d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae52d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae52d-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae52d-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ae52d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ae52d-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="ae52d-117">-TargetInstanceCount</span></span>
<span data-ttu-id="ae52d-118">Anger önskat antal arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="ae52d-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae52d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae52d-119">CommonParameters</span></span>
<span data-ttu-id="ae52d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae52d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae52d-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae52d-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae52d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae52d-122">INPUTS</span></span>

### <span data-ttu-id="ae52d-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="ae52d-123">None</span></span>

## <span data-ttu-id="ae52d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae52d-124">OUTPUTS</span></span>

### <span data-ttu-id="ae52d-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="ae52d-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="ae52d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae52d-126">NOTES</span></span>

## <span data-ttu-id="ae52d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae52d-127">RELATED LINKS</span></span>