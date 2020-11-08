---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsCluster.md
ms.openlocfilehash: aaa3522afb3bf021f2bf5fbff5ec6c3d9e14928f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259216"
---
# <span data-ttu-id="fda6e-101">Get-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="fda6e-101">Get-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="fda6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fda6e-102">SYNOPSIS</span></span>
<span data-ttu-id="fda6e-103">Skaffa eller lista kluster</span><span class="sxs-lookup"><span data-stu-id="fda6e-103">Get or list clusters</span></span>

## <span data-ttu-id="fda6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fda6e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fda6e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fda6e-105">DESCRIPTION</span></span>
<span data-ttu-id="fda6e-106">Hämta eller lista kluster, lista kluster under resurs grupp när "-kluster namn" inte angavs angavs lista kluster under prenumerationen när "-kluster namn" och "ResourceGroupName" inte tillhandahölls.</span><span class="sxs-lookup"><span data-stu-id="fda6e-106">Get or list clusters, list clusters under resource group when "-ClusterName" was not provided, list clusters under subscription when "-ClusterName" and "ResourceGroupName" were not provided.</span></span>

## <span data-ttu-id="fda6e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fda6e-107">EXAMPLES</span></span>

### <span data-ttu-id="fda6e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fda6e-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Succeeded
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="fda6e-109">Skaffa kluster</span><span class="sxs-lookup"><span data-stu-id="fda6e-109">Get cluster</span></span>

## <span data-ttu-id="fda6e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fda6e-110">PARAMETERS</span></span>

### <span data-ttu-id="fda6e-111">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="fda6e-111">-ClusterName</span></span>
<span data-ttu-id="fda6e-112">Kluster namnet.</span><span class="sxs-lookup"><span data-stu-id="fda6e-112">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda6e-113">-DefaultProfile</span></span>
<span data-ttu-id="fda6e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fda6e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda6e-115">-ResourceGroupName</span></span>
<span data-ttu-id="fda6e-116">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="fda6e-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda6e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda6e-117">CommonParameters</span></span>
<span data-ttu-id="fda6e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fda6e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda6e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fda6e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda6e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fda6e-120">INPUTS</span></span>

### <span data-ttu-id="fda6e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fda6e-121">System.String</span></span>

## <span data-ttu-id="fda6e-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fda6e-122">OUTPUTS</span></span>

### <span data-ttu-id="fda6e-123">Microsoft. Azure. commands. OperationalInsights. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fda6e-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="fda6e-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fda6e-124">NOTES</span></span>

## <span data-ttu-id="fda6e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fda6e-125">RELATED LINKS</span></span>
