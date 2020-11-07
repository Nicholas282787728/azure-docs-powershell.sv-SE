---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: c447d8dbfb7ed0b1fb4cf2ac3ad4c63aa4666ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758077"
---
# <span data-ttu-id="f3383-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f3383-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="f3383-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3383-102">SYNOPSIS</span></span>
<span data-ttu-id="f3383-103">Ger åtkomst till klustret via HTTP.</span><span class="sxs-lookup"><span data-stu-id="f3383-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3383-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3383-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3383-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3383-105">DESCRIPTION</span></span>
<span data-ttu-id="f3383-106">**Grant-AzureRmHDInsightHttpServicesAccess** cmdlet beviljar http-åtkomst till ett Azure HDInsight-kluster med ODBC, Ambari, Oozie och webb tjänster.</span><span class="sxs-lookup"><span data-stu-id="f3383-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="f3383-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3383-107">EXAMPLES</span></span>

### <span data-ttu-id="f3383-108">Exempel 1: bevilja HTTP-åtkomst till ett Azure HDInsight-kluster</span><span class="sxs-lookup"><span data-stu-id="f3383-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="f3383-109">Det här kommandot beviljar HTTP-åtkomst till det kluster som heter din-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="f3383-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="f3383-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3383-110">PARAMETERS</span></span>

### <span data-ttu-id="f3383-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="f3383-111">-ClusterName</span></span>
<span data-ttu-id="f3383-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="f3383-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="f3383-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="f3383-113">-HttpCredential</span></span>
<span data-ttu-id="f3383-114">Anger klustrets inloggnings uppgifter (HTTP).</span><span class="sxs-lookup"><span data-stu-id="f3383-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3383-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3383-115">-ResourceGroupName</span></span>
<span data-ttu-id="f3383-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f3383-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f3383-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3383-117">-DefaultProfile</span></span>
<span data-ttu-id="f3383-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3383-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3383-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3383-119">CommonParameters</span></span>
<span data-ttu-id="f3383-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3383-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3383-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3383-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3383-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3383-122">INPUTS</span></span>

## <span data-ttu-id="f3383-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3383-123">OUTPUTS</span></span>

### <span data-ttu-id="f3383-124">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="f3383-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="f3383-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3383-125">NOTES</span></span>

## <span data-ttu-id="f3383-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3383-126">RELATED LINKS</span></span>

[<span data-ttu-id="f3383-127">Återkalla-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="f3383-127">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


