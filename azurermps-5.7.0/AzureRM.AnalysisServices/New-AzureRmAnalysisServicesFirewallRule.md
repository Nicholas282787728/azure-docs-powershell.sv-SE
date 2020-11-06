---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581228"
---
# <span data-ttu-id="8f771-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f771-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="8f771-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f771-102">SYNOPSIS</span></span>
<span data-ttu-id="8f771-103">Skapar en ny regel för Analysis Services-brandväggen</span><span class="sxs-lookup"><span data-stu-id="8f771-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f771-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f771-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="8f771-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f771-105">DESCRIPTION</span></span>
<span data-ttu-id="8f771-106">New-AzureRmAnalysisServicesFirewallRule skapar ett nytt brand Väggs regel objekt.</span><span class="sxs-lookup"><span data-stu-id="8f771-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="8f771-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f771-107">EXAMPLES</span></span>

### <span data-ttu-id="8f771-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8f771-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="8f771-109">Skapar en brand Väggs regel med namnet rule1 med startintervallet 0.0.0.0 och slut intervall 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="8f771-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="8f771-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f771-110">PARAMETERS</span></span>

### <span data-ttu-id="8f771-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="8f771-111">-FirewallRuleName</span></span>
<span data-ttu-id="8f771-112">Namn på brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="8f771-112">Name of firewall rule</span></span>

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

### <span data-ttu-id="8f771-113">-Rang</span><span class="sxs-lookup"><span data-stu-id="8f771-113">-RangeStart</span></span>
<span data-ttu-id="8f771-114">Intervallet början av en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="8f771-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f771-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="8f771-115">-RangeEnd</span></span>
<span data-ttu-id="8f771-116">Intervallet för en brand Väggs regel</span><span class="sxs-lookup"><span data-stu-id="8f771-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="8f771-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f771-117">INPUTS</span></span>

## <span data-ttu-id="8f771-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f771-118">OUTPUTS</span></span>

### <span data-ttu-id="8f771-119">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f771-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="8f771-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f771-120">RELATED LINKS</span></span>

[<span data-ttu-id="8f771-121">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="8f771-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
