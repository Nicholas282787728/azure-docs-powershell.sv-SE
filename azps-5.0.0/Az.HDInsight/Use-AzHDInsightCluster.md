---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271058"
---
# <span data-ttu-id="a6cfa-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a6cfa-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="a6cfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="a6cfa-103">Väljer ett kluster som ska användas med Invoke-RmAzureHDInsightHiveJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="a6cfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6cfa-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6cfa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6cfa-105">DESCRIPTION</span></span>
<span data-ttu-id="a6cfa-106">Cmdleten **use-AzHDInsightCluster** väljer Azure HDInsight-klustret för den Invoke-AzHDInsightHiveJob cmdlet som ska användas för att skicka struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="a6cfa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6cfa-107">EXAMPLES</span></span>

### <span data-ttu-id="a6cfa-108">Exempel 1: Välj ett kluster för överföring av registrerings data fil</span><span class="sxs-lookup"><span data-stu-id="a6cfa-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="a6cfa-109">Det här kommandot väljer ett kluster för överföring av registrerings data fil.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="a6cfa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6cfa-110">PARAMETERS</span></span>

### <span data-ttu-id="a6cfa-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a6cfa-111">-ClusterName</span></span>
<span data-ttu-id="a6cfa-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a6cfa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6cfa-113">-DefaultProfile</span></span>
<span data-ttu-id="a6cfa-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a6cfa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6cfa-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="a6cfa-115">-HttpCredential</span></span>
<span data-ttu-id="a6cfa-116">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="a6cfa-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cfa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6cfa-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6cfa-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a6cfa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6cfa-119">CommonParameters</span></span>
<span data-ttu-id="a6cfa-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6cfa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6cfa-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6cfa-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6cfa-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6cfa-122">INPUTS</span></span>

### <span data-ttu-id="a6cfa-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="a6cfa-123">None</span></span>

## <span data-ttu-id="a6cfa-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6cfa-124">OUTPUTS</span></span>

### <span data-ttu-id="a6cfa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a6cfa-125">System.String</span></span>

## <span data-ttu-id="a6cfa-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6cfa-126">NOTES</span></span>

## <span data-ttu-id="a6cfa-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6cfa-127">RELATED LINKS</span></span>

[<span data-ttu-id="a6cfa-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a6cfa-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="a6cfa-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a6cfa-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


