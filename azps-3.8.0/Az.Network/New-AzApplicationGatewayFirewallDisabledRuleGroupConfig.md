---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092559"
---
# <span data-ttu-id="f93e6-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="f93e6-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="f93e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f93e6-102">SYNOPSIS</span></span>
<span data-ttu-id="f93e6-103">Skapar en ny inaktive rad konfiguration för regel grupp.</span><span class="sxs-lookup"><span data-stu-id="f93e6-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f93e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f93e6-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f93e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f93e6-105">DESCRIPTION</span></span>
<span data-ttu-id="f93e6-106">Cmdleten **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** skapar en ny inaktive rad konfiguration för regel grupp.</span><span class="sxs-lookup"><span data-stu-id="f93e6-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="f93e6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f93e6-107">EXAMPLES</span></span>

### <span data-ttu-id="f93e6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f93e6-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="f93e6-109">Kommandot skapar en ny inaktive rad konfiguration för regel grupp för regel gruppen med namnet "REQUEST-942-APPLICATION-SQLI" med regel 942130 och regel 942140 inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="f93e6-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="f93e6-110">Den nya gruppen för regel grupp för inaktive rad sparas i $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="f93e6-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="f93e6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f93e6-111">PARAMETERS</span></span>

### <span data-ttu-id="f93e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f93e6-112">-DefaultProfile</span></span>
<span data-ttu-id="f93e6-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f93e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f93e6-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="f93e6-114">-RuleGroupName</span></span>
<span data-ttu-id="f93e6-115">Namnet på regel gruppen som kommer att avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="f93e6-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e6-116">-Regler</span><span class="sxs-lookup"><span data-stu-id="f93e6-116">-Rules</span></span>
<span data-ttu-id="f93e6-117">Listan över regler som kommer att inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="f93e6-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="f93e6-118">Om det är null är alla regler för regel gruppen inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="f93e6-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f93e6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f93e6-119">CommonParameters</span></span>
<span data-ttu-id="f93e6-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f93e6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f93e6-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f93e6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f93e6-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f93e6-122">INPUTS</span></span>

### <span data-ttu-id="f93e6-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="f93e6-123">None</span></span>

## <span data-ttu-id="f93e6-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f93e6-124">OUTPUTS</span></span>

### <span data-ttu-id="f93e6-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="f93e6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="f93e6-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f93e6-126">NOTES</span></span>

## <span data-ttu-id="f93e6-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f93e6-127">RELATED LINKS</span></span>

[<span data-ttu-id="f93e6-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f93e6-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f93e6-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f93e6-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

