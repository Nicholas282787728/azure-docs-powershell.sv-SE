---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 1616714879a260dea3611809b5f7028b4a203d34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916557"
---
# <span data-ttu-id="d25d8-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="d25d8-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="d25d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d25d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d25d8-103">Anger antalet arbets tagare i ett angivet kluster.</span><span class="sxs-lookup"><span data-stu-id="d25d8-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="d25d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d25d8-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d25d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d25d8-105">DESCRIPTION</span></span>
<span data-ttu-id="d25d8-106">Cmdleten **set-AzHDInsightClusterSize** anger antalet Worker-noder i ett angivet Azure HDInsight-kluster.</span><span class="sxs-lookup"><span data-stu-id="d25d8-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="d25d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d25d8-107">EXAMPLES</span></span>

### <span data-ttu-id="d25d8-108">Exempel 1: Ange storleken på ett angivet kluster</span><span class="sxs-lookup"><span data-stu-id="d25d8-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="d25d8-109">Det här kommandot anger storleken på det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d25d8-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d25d8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d25d8-110">PARAMETERS</span></span>

### <span data-ttu-id="d25d8-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d25d8-111">-ClusterName</span></span>
<span data-ttu-id="d25d8-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="d25d8-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d25d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25d8-113">-DefaultProfile</span></span>
<span data-ttu-id="d25d8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d25d8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d25d8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25d8-115">-ResourceGroupName</span></span>
<span data-ttu-id="d25d8-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d25d8-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d25d8-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="d25d8-117">-TargetInstanceCount</span></span>
<span data-ttu-id="d25d8-118">Anger önskat antal arbets tagare i klustret.</span><span class="sxs-lookup"><span data-stu-id="d25d8-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="d25d8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25d8-119">CommonParameters</span></span>
<span data-ttu-id="d25d8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25d8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25d8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d25d8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25d8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d25d8-122">INPUTS</span></span>

### <span data-ttu-id="d25d8-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="d25d8-123">None</span></span>

## <span data-ttu-id="d25d8-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d25d8-124">OUTPUTS</span></span>

### <span data-ttu-id="d25d8-125">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="d25d8-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="d25d8-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d25d8-126">NOTES</span></span>

## <span data-ttu-id="d25d8-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d25d8-127">RELATED LINKS</span></span>
