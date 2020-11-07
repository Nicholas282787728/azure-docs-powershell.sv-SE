---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758064"
---
# <span data-ttu-id="4e844-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4e844-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="4e844-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e844-102">SYNOPSIS</span></span>
<span data-ttu-id="4e844-103">Väljer ett kluster som ska användas med Invoke-RmAzureHDInsightHiveJob cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e844-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e844-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e844-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e844-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e844-105">DESCRIPTION</span></span>
<span data-ttu-id="4e844-106">Cmdleten **use-AzureRmHDInsightCluster** väljer Azure HDInsight-klustret för den Invoke-AzureRmHDInsightHiveJob cmdlet som ska användas för att skicka struktur jobb.</span><span class="sxs-lookup"><span data-stu-id="4e844-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="4e844-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e844-107">EXAMPLES</span></span>

### <span data-ttu-id="4e844-108">Exempel 1: Välj ett kluster för överföring av registrerings data fil</span><span class="sxs-lookup"><span data-stu-id="4e844-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="4e844-109">Det här kommandot väljer ett kluster för överföring av registrerings data fil.</span><span class="sxs-lookup"><span data-stu-id="4e844-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="4e844-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e844-110">PARAMETERS</span></span>

### <span data-ttu-id="4e844-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="4e844-111">-ClusterName</span></span>
<span data-ttu-id="4e844-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="4e844-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4e844-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4e844-113">-HttpCredential</span></span>
<span data-ttu-id="4e844-114">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="4e844-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4e844-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e844-115">-ResourceGroupName</span></span>
<span data-ttu-id="4e844-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4e844-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4e844-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e844-117">-DefaultProfile</span></span>
<span data-ttu-id="4e844-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e844-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e844-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e844-119">CommonParameters</span></span>
<span data-ttu-id="4e844-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e844-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e844-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e844-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e844-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e844-122">INPUTS</span></span>

## <span data-ttu-id="4e844-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e844-123">OUTPUTS</span></span>

### <span data-ttu-id="4e844-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4e844-124">System.String</span></span>

## <span data-ttu-id="4e844-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e844-125">NOTES</span></span>

## <span data-ttu-id="4e844-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e844-126">RELATED LINKS</span></span>

[<span data-ttu-id="4e844-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4e844-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="4e844-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4e844-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


