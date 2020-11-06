---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bcc40b77208506712a319d7f43d74f8928e18927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574899"
---
# <span data-ttu-id="21711-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21711-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="21711-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21711-102">SYNOPSIS</span></span>
<span data-ttu-id="21711-103">Skapar en WAF-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="21711-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21711-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21711-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21711-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21711-105">DESCRIPTION</span></span>
<span data-ttu-id="21711-106">Cmdleten **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** skapar en WAF-konfiguration (Web Application Firewall) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="21711-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="21711-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21711-107">EXAMPLES</span></span>

### <span data-ttu-id="21711-108">Exempel 1: skapa en brand Väggs konfiguration för webb program för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="21711-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="21711-109">Det första kommandot skapar en ny inaktive rad konfiguration för regel grupp för regel gruppen med namnet "REQUEST-942-APPLICATION-SQLI" med regel 942130 och regel 942140 inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="21711-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="21711-110">Det andra kommandot skapar en annan inaktive rad konfiguration för regel grupp för en regel grupp med namnet "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="21711-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="21711-111">Inga regler skickades och därför kommer alla regler i regel gruppen att avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="21711-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="21711-112">Det senaste kommandot skapar då en WAF-konfiguration med brand Väggs regler som är inaktiverade som konfigurerade i $disabledRuleGroup 1 och $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="21711-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="21711-113">Den nya WAF-konfigurationen lagras i variabeln $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="21711-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="21711-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21711-114">PARAMETERS</span></span>

### <span data-ttu-id="21711-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21711-115">-DefaultProfile</span></span>
<span data-ttu-id="21711-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21711-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21711-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="21711-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="21711-118">De inaktiverade regel grupperna.</span><span class="sxs-lookup"><span data-stu-id="21711-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-119">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="21711-119">-Enabled</span></span>
<span data-ttu-id="21711-120">Anger om WAF är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="21711-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="21711-121">-FirewallMode</span></span>
<span data-ttu-id="21711-122">Anger brand Väggs läget för webb programmet.</span><span class="sxs-lookup"><span data-stu-id="21711-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="21711-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21711-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="21711-124">Proxyidentifiering</span><span class="sxs-lookup"><span data-stu-id="21711-124">Detection</span></span>
- <span data-ttu-id="21711-125">Utebliv</span><span class="sxs-lookup"><span data-stu-id="21711-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="21711-126">-RuleSetType</span></span>
<span data-ttu-id="21711-127">Typ av brand Väggs regel för webb program.</span><span class="sxs-lookup"><span data-stu-id="21711-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="21711-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21711-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="21711-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="21711-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="21711-130">-RuleSetVersion</span></span>
<span data-ttu-id="21711-131">Versionen av regel uppsättnings typen.</span><span class="sxs-lookup"><span data-stu-id="21711-131">The version of the rule set type.</span></span>
<span data-ttu-id="21711-132">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="21711-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="21711-133">3,0</span><span class="sxs-lookup"><span data-stu-id="21711-133">3.0</span></span>
- <span data-ttu-id="21711-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="21711-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21711-135">-Confirm</span></span>
<span data-ttu-id="21711-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21711-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21711-137">-WhatIf</span></span>
<span data-ttu-id="21711-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21711-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="21711-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21711-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21711-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21711-140">CommonParameters</span></span>
<span data-ttu-id="21711-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21711-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21711-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21711-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21711-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21711-143">INPUTS</span></span>

### <span data-ttu-id="21711-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="21711-144">None</span></span>
<span data-ttu-id="21711-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="21711-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21711-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21711-146">OUTPUTS</span></span>

### <span data-ttu-id="21711-147">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21711-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="21711-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21711-148">NOTES</span></span>

## <span data-ttu-id="21711-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21711-149">RELATED LINKS</span></span>

[<span data-ttu-id="21711-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21711-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="21711-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21711-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


