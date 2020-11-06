---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 780e231f2ca512b5becf0ee068c004dd815cea89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577134"
---
# <span data-ttu-id="dd3c9-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="dd3c9-101">New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="dd3c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd3c9-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3c9-103">Skapar en ny inaktive rad konfiguration för regel grupp.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-103">Creates a new disabled rule group configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd3c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd3c9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd3c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd3c9-105">DESCRIPTION</span></span>
<span data-ttu-id="dd3c9-106">Cmdleten **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** skapar en ny inaktive rad konfiguration för regel grupp.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-106">The **New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="dd3c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd3c9-107">EXAMPLES</span></span>

### <span data-ttu-id="dd3c9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd3c9-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="dd3c9-109">Kommandot skapar en ny inaktive rad konfiguration för regel grupp för regel gruppen med namnet "REQUEST-942-APPLICATION-SQLI" med regel 942130 och regel 942140 inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="dd3c9-110">Den nya gruppen för regel grupp för inaktive rad sparas i $disabledRuleGroup 1.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="dd3c9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd3c9-111">PARAMETERS</span></span>

### <span data-ttu-id="dd3c9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3c9-112">-DefaultProfile</span></span>
<span data-ttu-id="dd3c9-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd3c9-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3c9-114">-RuleGroupName</span></span>
<span data-ttu-id="dd3c9-115">Namnet på regel gruppen som kommer att avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3c9-116">-Regler</span><span class="sxs-lookup"><span data-stu-id="dd3c9-116">-Rules</span></span>
<span data-ttu-id="dd3c9-117">Listan över regler som kommer att inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="dd3c9-118">Om det är null är alla regler för regel gruppen inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3c9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3c9-119">CommonParameters</span></span>
<span data-ttu-id="dd3c9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd3c9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3c9-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd3c9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3c9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd3c9-122">INPUTS</span></span>

### <span data-ttu-id="dd3c9-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="dd3c9-123">None</span></span>

## <span data-ttu-id="dd3c9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd3c9-124">OUTPUTS</span></span>

### <span data-ttu-id="dd3c9-125">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="dd3c9-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="dd3c9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd3c9-126">NOTES</span></span>

## <span data-ttu-id="dd3c9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd3c9-127">RELATED LINKS</span></span>

[<span data-ttu-id="dd3c9-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3c9-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="dd3c9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd3c9-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

