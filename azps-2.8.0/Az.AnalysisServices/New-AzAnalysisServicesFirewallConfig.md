---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: f3c84b22a9ea8c913cb520ae913fff89ae9470ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745893"
---
# <span data-ttu-id="19885-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="19885-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="19885-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19885-102">SYNOPSIS</span></span>
<span data-ttu-id="19885-103">Skapar en ny Analysis Services Firewall-konfiguration</span><span class="sxs-lookup"><span data-stu-id="19885-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="19885-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19885-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19885-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19885-105">DESCRIPTION</span></span>
<span data-ttu-id="19885-106">New-AzAnalysisServicesFirewallConfig skapar ett nytt brand Väggs konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="19885-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="19885-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19885-107">EXAMPLES</span></span>

### <span data-ttu-id="19885-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19885-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="19885-109">Skapar ett brand Väggs konfigurations objekt med två regler samtidigt som du aktiverar åtkomst från Power BI-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="19885-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="19885-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19885-110">PARAMETERS</span></span>

### <span data-ttu-id="19885-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19885-111">-DefaultProfile</span></span>
<span data-ttu-id="19885-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19885-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19885-113">-EnablePowerBIService</span><span class="sxs-lookup"><span data-stu-id="19885-113">-EnablePowerBIService</span></span>
<span data-ttu-id="19885-114">En flagga som anger om brand väggen tillåter åtkomst från Power BI</span><span class="sxs-lookup"><span data-stu-id="19885-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="19885-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="19885-115">-FirewallRule</span></span>
<span data-ttu-id="19885-116">En lista med brand Väggs regler</span><span class="sxs-lookup"><span data-stu-id="19885-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="19885-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19885-117">CommonParameters</span></span>
<span data-ttu-id="19885-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19885-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19885-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19885-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19885-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19885-120">INPUTS</span></span>

### <span data-ttu-id="19885-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. cmdletar. AnalysisServices, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="19885-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="19885-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19885-122">OUTPUTS</span></span>

### <span data-ttu-id="19885-123">Microsoft. Azure. commands. AnalysisServices. Models. PsAzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="19885-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="19885-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19885-124">NOTES</span></span>

## <span data-ttu-id="19885-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19885-125">RELATED LINKS</span></span>

[<span data-ttu-id="19885-126">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="19885-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)