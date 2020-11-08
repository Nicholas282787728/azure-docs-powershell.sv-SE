---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916561"
---
# <span data-ttu-id="d7b0d-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d7b0d-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="d7b0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b0d-103">Inaktiverar HTTP-åtkomst till klustret.</span><span class="sxs-lookup"><span data-stu-id="d7b0d-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="d7b0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7b0d-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7b0d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="d7b0d-106">Med cmdleten **REVOKE-AzHDInsightHttpServicesAccess** inaktive ras http-åtkomst till ett Azure HDInsight-kluster för ODBC-, Ambari-, Oozie-och webHCatalog-webbtjänster.</span><span class="sxs-lookup"><span data-stu-id="d7b0d-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="d7b0d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="d7b0d-108">Exempel 1: Inaktivera HTTP-åtkomst till ett kluster</span><span class="sxs-lookup"><span data-stu-id="d7b0d-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="d7b0d-109">Med det här kommandot återkallas HTTP-åtkomst till det kluster som heter hadoop_001.</span><span class="sxs-lookup"><span data-stu-id="d7b0d-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="d7b0d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7b0d-110">PARAMETERS</span></span>

### <span data-ttu-id="d7b0d-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d7b0d-111">-ClusterName</span></span>
<span data-ttu-id="d7b0d-112">Anger namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="d7b0d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="d7b0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b0d-113">-DefaultProfile</span></span>
<span data-ttu-id="d7b0d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d7b0d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7b0d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b0d-115">-ResourceGroupName</span></span>
<span data-ttu-id="d7b0d-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d7b0d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d7b0d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b0d-117">CommonParameters</span></span>
<span data-ttu-id="d7b0d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b0d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b0d-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b0d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b0d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7b0d-120">INPUTS</span></span>

### <span data-ttu-id="d7b0d-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="d7b0d-121">None</span></span>

## <span data-ttu-id="d7b0d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7b0d-122">OUTPUTS</span></span>

### <span data-ttu-id="d7b0d-123">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="d7b0d-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="d7b0d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7b0d-124">NOTES</span></span>

## <span data-ttu-id="d7b0d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7b0d-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7b0d-126">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="d7b0d-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)

