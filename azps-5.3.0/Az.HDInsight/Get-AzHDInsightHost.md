---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 430c2aa7f38e6246c13ef6045f52346b580d20fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520639"
---
# <span data-ttu-id="9827a-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="9827a-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="9827a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9827a-102">SYNOPSIS</span></span>
<span data-ttu-id="9827a-103">Visar värderna för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9827a-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="9827a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9827a-104">SYNTAX</span></span>

### <span data-ttu-id="9827a-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9827a-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9827a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9827a-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9827a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9827a-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9827a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9827a-108">DESCRIPTION</span></span>
<span data-ttu-id="9827a-109">Cmdleten **Get-AzHDInsightHost** visar värdarna för HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="9827a-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="9827a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9827a-110">EXAMPLES</span></span>

### <span data-ttu-id="9827a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9827a-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="9827a-112">Det här kommandot visar klustrets värdar med kluster namn.</span><span class="sxs-lookup"><span data-stu-id="9827a-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="9827a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9827a-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="9827a-114">Det här kommandot visar klustrets värdar med pipelines.</span><span class="sxs-lookup"><span data-stu-id="9827a-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="9827a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9827a-115">PARAMETERS</span></span>

### <span data-ttu-id="9827a-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="9827a-116">-ClusterName</span></span>
<span data-ttu-id="9827a-117">Hämtar eller anger klustrets namn.</span><span class="sxs-lookup"><span data-stu-id="9827a-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9827a-118">-DefaultProfile</span></span>
<span data-ttu-id="9827a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9827a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9827a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9827a-120">-InputObject</span></span>
<span data-ttu-id="9827a-121">Hämtar eller anger indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="9827a-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9827a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9827a-123">Hämtar eller anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9827a-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9827a-124">-ResourceId</span></span>
<span data-ttu-id="9827a-125">Hämtar eller anger resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="9827a-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9827a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9827a-126">CommonParameters</span></span>
<span data-ttu-id="9827a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9827a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9827a-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9827a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9827a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9827a-129">INPUTS</span></span>

### <span data-ttu-id="9827a-130">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9827a-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="9827a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9827a-131">OUTPUTS</span></span>

### <span data-ttu-id="9827a-132">Microsoft. Azure. commands. HDInsight. Models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="9827a-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="9827a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9827a-133">NOTES</span></span>

## <span data-ttu-id="9827a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9827a-134">RELATED LINKS</span></span>
