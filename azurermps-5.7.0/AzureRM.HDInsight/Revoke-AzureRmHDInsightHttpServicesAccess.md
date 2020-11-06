---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 388e339ba7545bc2e4d00166a6f365a19cb44f28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580424"
---
# <span data-ttu-id="5537a-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5537a-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="5537a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5537a-102">SYNOPSIS</span></span>
<span data-ttu-id="5537a-103">Inaktiverar HTTP-åtkomst till klustret.</span><span class="sxs-lookup"><span data-stu-id="5537a-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5537a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5537a-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5537a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5537a-105">DESCRIPTION</span></span>
<span data-ttu-id="5537a-106">Med cmdleten **REVOKE-AzureRmHDInsightHttpServicesAccess** inaktive ras http-åtkomst till ett Azure HDInsight-kluster för ODBC-, Ambari-, Oozie-och webHCatalog-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="5537a-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="5537a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5537a-107">EXAMPLES</span></span>

### <span data-ttu-id="5537a-108">Exempel 1: Inaktivera HTTP-åtkomst till ett kluster</span><span class="sxs-lookup"><span data-stu-id="5537a-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="5537a-109">Med det här kommandot återkallas HTTP-åtkomst till det kluster som heter hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="5537a-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="5537a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5537a-110">PARAMETERS</span></span>

### <span data-ttu-id="5537a-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="5537a-111">-ClusterName</span></span>
<span data-ttu-id="5537a-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="5537a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="5537a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5537a-113">-DefaultProfile</span></span>
<span data-ttu-id="5537a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5537a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5537a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5537a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5537a-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5537a-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5537a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5537a-117">CommonParameters</span></span>
<span data-ttu-id="5537a-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5537a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5537a-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5537a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5537a-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5537a-120">INPUTS</span></span>

### <span data-ttu-id="5537a-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="5537a-121">None</span></span>
<span data-ttu-id="5537a-122">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5537a-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5537a-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5537a-123">OUTPUTS</span></span>

### <span data-ttu-id="5537a-124">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="5537a-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="5537a-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5537a-125">NOTES</span></span>

## <span data-ttu-id="5537a-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5537a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5537a-127">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="5537a-127">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


