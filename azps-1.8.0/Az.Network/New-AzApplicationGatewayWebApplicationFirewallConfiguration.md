---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 689dbeef5dd51b525ae5858129c448ba52faab43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748096"
---
# <span data-ttu-id="a5134-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5134-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a5134-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5134-102">SYNOPSIS</span></span>
<span data-ttu-id="a5134-103">Skapar en WAF-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="a5134-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="a5134-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5134-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5134-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5134-105">DESCRIPTION</span></span>
<span data-ttu-id="a5134-106">Cmdleten **New-AzApplicationGatewayWebApplicationFirewallConfiguration** skapar en WAF-konfiguration (Web Application Firewall) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a5134-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a5134-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5134-107">EXAMPLES</span></span>

### <span data-ttu-id="a5134-108">Exempel 1: skapa en brand Väggs konfiguration för webb program för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="a5134-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="a5134-109">Det första kommandot skapar en ny inaktive rad konfiguration för regel grupp för regel gruppen med namnet "REQUEST-942-APPLICATION-SQLI" med regel 942130 och regel 942140 inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="a5134-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="a5134-110">Det andra kommandot skapar en annan inaktive rad konfiguration för regel grupp för en regel grupp med namnet "REQUEST-921-PROTOCOL-ATTACK".</span><span class="sxs-lookup"><span data-stu-id="a5134-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="a5134-111">Inga regler skickades och därför kommer alla regler i regel gruppen att avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="a5134-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="a5134-112">Det senaste kommandot skapar då en WAF-konfiguration med brand Väggs regler som är inaktiverade som konfigurerade i $disabledRuleGroup 1 och $disabledRuleGroup 2.</span><span class="sxs-lookup"><span data-stu-id="a5134-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="a5134-113">Den nya WAF-konfigurationen lagras i variabeln $firewallConfig.</span><span class="sxs-lookup"><span data-stu-id="a5134-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="a5134-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5134-114">PARAMETERS</span></span>

### <span data-ttu-id="a5134-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5134-115">-DefaultProfile</span></span>
<span data-ttu-id="a5134-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5134-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5134-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="a5134-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="a5134-118">De inaktiverade regel grupperna.</span><span class="sxs-lookup"><span data-stu-id="a5134-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-119">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="a5134-119">-Enabled</span></span>
<span data-ttu-id="a5134-120">Anger om WAF är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="a5134-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-121">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="a5134-121">-Exclusion</span></span>
<span data-ttu-id="a5134-122">Undantags listorna.</span><span class="sxs-lookup"><span data-stu-id="a5134-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="a5134-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="a5134-124">Max gränsen för fil uppladdning i MB.</span><span class="sxs-lookup"><span data-stu-id="a5134-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="a5134-125">-FirewallMode</span></span>
<span data-ttu-id="a5134-126">Anger brand Väggs läget för webb programmet.</span><span class="sxs-lookup"><span data-stu-id="a5134-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="a5134-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a5134-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a5134-128">Proxyidentifiering</span><span class="sxs-lookup"><span data-stu-id="a5134-128">Detection</span></span>
- <span data-ttu-id="a5134-129">Utebliv</span><span class="sxs-lookup"><span data-stu-id="a5134-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="a5134-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="a5134-131">Max storlek för begärantext i KB.</span><span class="sxs-lookup"><span data-stu-id="a5134-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="a5134-132">-RequestBodyCheck</span></span>
<span data-ttu-id="a5134-133">Om bröd texten är markerad eller inte.</span><span class="sxs-lookup"><span data-stu-id="a5134-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="a5134-134">-RuleSetType</span></span>
<span data-ttu-id="a5134-135">Typ av brand Väggs regel för webb program.</span><span class="sxs-lookup"><span data-stu-id="a5134-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="a5134-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a5134-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="a5134-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="a5134-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a5134-138">-RuleSetVersion</span></span>
<span data-ttu-id="a5134-139">Versionen av regel uppsättnings typen.</span><span class="sxs-lookup"><span data-stu-id="a5134-139">The version of the rule set type.</span></span>
<span data-ttu-id="a5134-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a5134-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="a5134-141">3,0</span><span class="sxs-lookup"><span data-stu-id="a5134-141">3.0</span></span>
- <span data-ttu-id="a5134-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="a5134-142">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5134-143">-Confirm</span></span>
<span data-ttu-id="a5134-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5134-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5134-145">-WhatIf</span></span>
<span data-ttu-id="a5134-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5134-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5134-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5134-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5134-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5134-148">CommonParameters</span></span>
<span data-ttu-id="a5134-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5134-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5134-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5134-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5134-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5134-151">INPUTS</span></span>

### <span data-ttu-id="a5134-152">Ingen</span><span class="sxs-lookup"><span data-stu-id="a5134-152">None</span></span>

## <span data-ttu-id="a5134-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5134-153">OUTPUTS</span></span>

### <span data-ttu-id="a5134-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5134-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a5134-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5134-155">NOTES</span></span>

## <span data-ttu-id="a5134-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5134-156">RELATED LINKS</span></span>

[<span data-ttu-id="a5134-157">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5134-157">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a5134-158">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5134-158">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


