---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 529eedf9cd8ae782d08af7d349d4e11885a8a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574946"
---
# <span data-ttu-id="899d9-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="899d9-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="899d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="899d9-102">SYNOPSIS</span></span>
<span data-ttu-id="899d9-103">Ger åtkomst till klustret via HTTP.</span><span class="sxs-lookup"><span data-stu-id="899d9-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="899d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="899d9-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="899d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="899d9-105">DESCRIPTION</span></span>
<span data-ttu-id="899d9-106">**Grant-AzureRmHDInsightHttpServicesAccess** cmdlet beviljar http-åtkomst till ett Azure HDInsight-kluster med ODBC, Ambari, Oozie och webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="899d9-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="899d9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="899d9-107">EXAMPLES</span></span>

### <span data-ttu-id="899d9-108">Exempel 1: bevilja HTTP-åtkomst till ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="899d9-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="899d9-109">Det här kommandot beviljar HTTP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="899d9-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="899d9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="899d9-110">PARAMETERS</span></span>

### <span data-ttu-id="899d9-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="899d9-111">-ClusterName</span></span>
<span data-ttu-id="899d9-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="899d9-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="899d9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="899d9-113">-DefaultProfile</span></span>
<span data-ttu-id="899d9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="899d9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="899d9-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="899d9-115">-HttpCredential</span></span>
<span data-ttu-id="899d9-116">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="899d9-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="899d9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="899d9-117">-ResourceGroupName</span></span>
<span data-ttu-id="899d9-118">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="899d9-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="899d9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="899d9-119">CommonParameters</span></span>
<span data-ttu-id="899d9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="899d9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="899d9-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="899d9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="899d9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="899d9-122">INPUTS</span></span>

### <span data-ttu-id="899d9-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="899d9-123">None</span></span>
<span data-ttu-id="899d9-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="899d9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="899d9-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="899d9-125">OUTPUTS</span></span>

### <span data-ttu-id="899d9-126">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="899d9-126">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="899d9-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="899d9-127">NOTES</span></span>

## <span data-ttu-id="899d9-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="899d9-128">RELATED LINKS</span></span>

[<span data-ttu-id="899d9-129">Återkalla-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="899d9-129">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


