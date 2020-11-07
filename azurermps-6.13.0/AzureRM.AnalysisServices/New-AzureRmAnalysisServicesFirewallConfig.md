---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755730"
---
# <span data-ttu-id="b61cf-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b61cf-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="b61cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b61cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b61cf-103">Skapar en ny Analysis Services Firewall-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b61cf-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b61cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b61cf-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b61cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b61cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b61cf-106">New-AzureRmAnalysisServicesFirewallConfig skapar ett nytt brand Väggs konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="b61cf-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="b61cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b61cf-107">EXAMPLES</span></span>

### <span data-ttu-id="b61cf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b61cf-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="b61cf-109">Skapar ett brand Väggs konfigurations objekt med två regler samtidigt som du aktiverar åtkomst från Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b61cf-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="b61cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b61cf-110">PARAMETERS</span></span>

### <span data-ttu-id="b61cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61cf-111">-DefaultProfile</span></span>
<span data-ttu-id="b61cf-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b61cf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b61cf-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="b61cf-113">-EnablePowerBIService</span></span>
<span data-ttu-id="b61cf-114">En flagga som anger om brand väggen tillåter åtkomst från Power BI</span><span class="sxs-lookup"><span data-stu-id="b61cf-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61cf-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="b61cf-115">-FirewallRule</span></span>
<span data-ttu-id="b61cf-116">En lista med brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="b61cf-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61cf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61cf-117">CommonParameters</span></span>
<span data-ttu-id="b61cf-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61cf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61cf-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61cf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61cf-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b61cf-120">INPUTS</span></span>

### <span data-ttu-id="b61cf-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. commands. AnalysisServices, version = 0.6.11.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b61cf-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b61cf-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b61cf-122">OUTPUTS</span></span>

### <span data-ttu-id="b61cf-123">Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="b61cf-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="b61cf-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b61cf-124">NOTES</span></span>

## <span data-ttu-id="b61cf-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b61cf-125">RELATED LINKS</span></span>

[<span data-ttu-id="b61cf-126">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b61cf-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
