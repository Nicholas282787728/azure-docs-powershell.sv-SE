---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756522"
---
# <span data-ttu-id="51ee4-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="51ee4-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="51ee4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="51ee4-103">Skapar en ny Analysis Services Firewall-konfiguration</span><span class="sxs-lookup"><span data-stu-id="51ee4-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51ee4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51ee4-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## <span data-ttu-id="51ee4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="51ee4-106">New-AzureRmAnalysisServicesFirewallConfig skapar ett nytt brand Väggs konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="51ee4-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="51ee4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="51ee4-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51ee4-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

<span data-ttu-id="51ee4-109">Skapar en brand Väggs regel konfiguration utan att aktivera Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="51ee4-109">Creates a firewall rule config without enabling power bi service.</span></span>

## <span data-ttu-id="51ee4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="51ee4-111">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="51ee4-111">-EnablePowerBIService</span></span>
<span data-ttu-id="51ee4-112">En flagga som anger om aktivera PowerBI-tjänsten</span><span class="sxs-lookup"><span data-stu-id="51ee4-112">A flag to indicate if enable PowerBI service</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51ee4-113">-FirewallRules</span><span class="sxs-lookup"><span data-stu-id="51ee4-113">-FirewallRules</span></span>
<span data-ttu-id="51ee4-114">En lista med brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="51ee4-114">A list of firewall rules</span></span>

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="51ee4-115">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51ee4-115">INPUTS</span></span>

## <span data-ttu-id="51ee4-116">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51ee4-116">OUTPUTS</span></span>

### <span data-ttu-id="51ee4-117">Microsoft. Azure. commands. AnalysisServices. Models. AzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="51ee4-117">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="51ee4-118">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51ee4-118">RELATED LINKS</span></span>

[<span data-ttu-id="51ee4-119">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="51ee4-119">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
