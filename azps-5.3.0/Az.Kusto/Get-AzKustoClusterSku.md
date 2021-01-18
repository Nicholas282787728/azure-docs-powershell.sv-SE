---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 42fed776d1f77211c7967dd6313d0ddd1e04b65a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521231"
---
# <span data-ttu-id="71714-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="71714-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="71714-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71714-102">SYNOPSIS</span></span>
<span data-ttu-id="71714-103">Visar en lista med stödberättigade SKU: er för Kusto.</span><span class="sxs-lookup"><span data-stu-id="71714-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="71714-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71714-104">SYNTAX</span></span>

### <span data-ttu-id="71714-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="71714-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71714-106">List1</span><span class="sxs-lookup"><span data-stu-id="71714-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="71714-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71714-107">DESCRIPTION</span></span>
<span data-ttu-id="71714-108">Visar en lista med stödberättigade SKU: er för Kusto.</span><span class="sxs-lookup"><span data-stu-id="71714-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="71714-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71714-109">EXAMPLES</span></span>

### <span data-ttu-id="71714-110">Exempel 1: här visas giltiga SKU: er</span><span class="sxs-lookup"><span data-stu-id="71714-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="71714-111">Kommandot ovan visar kvalificerade SKU: er.</span><span class="sxs-lookup"><span data-stu-id="71714-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="71714-112">Exempel 2: listar giltiga SKU: er för specifika kluster</span><span class="sxs-lookup"><span data-stu-id="71714-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="71714-113">Kommandot ovan visar kvalificerade SKU: er för specifika kluster</span><span class="sxs-lookup"><span data-stu-id="71714-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="71714-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71714-114">PARAMETERS</span></span>

### <span data-ttu-id="71714-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="71714-115">-ClusterName</span></span>
<span data-ttu-id="71714-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="71714-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71714-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71714-117">-DefaultProfile</span></span>
<span data-ttu-id="71714-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71714-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71714-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71714-119">-ResourceGroupName</span></span>
<span data-ttu-id="71714-120">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="71714-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71714-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71714-121">-SubscriptionId</span></span>
<span data-ttu-id="71714-122">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="71714-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="71714-123">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="71714-123">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71714-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71714-124">CommonParameters</span></span>
<span data-ttu-id="71714-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71714-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71714-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71714-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71714-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71714-127">INPUTS</span></span>

## <span data-ttu-id="71714-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71714-128">OUTPUTS</span></span>

### <span data-ttu-id="71714-129">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="71714-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAzureResourceSku</span></span>

### <span data-ttu-id="71714-130">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="71714-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ISkuDescription</span></span>

## <span data-ttu-id="71714-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71714-131">NOTES</span></span>

<span data-ttu-id="71714-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="71714-132">ALIASES</span></span>

## <span data-ttu-id="71714-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71714-133">RELATED LINKS</span></span>

