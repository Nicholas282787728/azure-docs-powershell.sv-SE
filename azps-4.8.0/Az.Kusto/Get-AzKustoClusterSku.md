---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103196"
---
# <span data-ttu-id="33f41-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="33f41-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="33f41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33f41-102">SYNOPSIS</span></span>
<span data-ttu-id="33f41-103">Visar en lista med stödberättigade SKU: er för Kusto.</span><span class="sxs-lookup"><span data-stu-id="33f41-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="33f41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33f41-104">SYNTAX</span></span>

### <span data-ttu-id="33f41-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="33f41-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="33f41-106">List1</span><span class="sxs-lookup"><span data-stu-id="33f41-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="33f41-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33f41-107">DESCRIPTION</span></span>
<span data-ttu-id="33f41-108">Visar en lista med stödberättigade SKU: er för Kusto.</span><span class="sxs-lookup"><span data-stu-id="33f41-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="33f41-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33f41-109">EXAMPLES</span></span>

### <span data-ttu-id="33f41-110">Exempel 1: här visas giltiga SKU: er</span><span class="sxs-lookup"><span data-stu-id="33f41-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="33f41-111">Kommandot ovan visar kvalificerade SKU: er.</span><span class="sxs-lookup"><span data-stu-id="33f41-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="33f41-112">Exempel 2: listar giltiga SKU: er för specifika kluster</span><span class="sxs-lookup"><span data-stu-id="33f41-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="33f41-113">Kommandot ovan visar kvalificerade SKU: er för specifika kluster</span><span class="sxs-lookup"><span data-stu-id="33f41-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="33f41-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33f41-114">PARAMETERS</span></span>

### <span data-ttu-id="33f41-115">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="33f41-115">-ClusterName</span></span>
<span data-ttu-id="33f41-116">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="33f41-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="33f41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33f41-117">-DefaultProfile</span></span>
<span data-ttu-id="33f41-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="33f41-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33f41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33f41-119">-ResourceGroupName</span></span>
<span data-ttu-id="33f41-120">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="33f41-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="33f41-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33f41-121">-SubscriptionId</span></span>
<span data-ttu-id="33f41-122">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="33f41-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="33f41-123">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="33f41-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="33f41-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33f41-124">CommonParameters</span></span>
<span data-ttu-id="33f41-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33f41-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33f41-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33f41-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33f41-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33f41-127">INPUTS</span></span>

## <span data-ttu-id="33f41-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33f41-128">OUTPUTS</span></span>

### <span data-ttu-id="33f41-129">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="33f41-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="33f41-130">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ISkuDescription</span><span class="sxs-lookup"><span data-stu-id="33f41-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="33f41-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33f41-131">NOTES</span></span>

<span data-ttu-id="33f41-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33f41-132">ALIASES</span></span>

## <span data-ttu-id="33f41-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33f41-133">RELATED LINKS</span></span>

