---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9481580e482c709c17b3a1acf36be765ca45e444
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917930"
---
# <span data-ttu-id="2a1ba-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a1ba-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="2a1ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="2a1ba-103">Ändrar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="2a1ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a1ba-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a1ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a1ba-105">DESCRIPTION</span></span>
<span data-ttu-id="2a1ba-106">Cmdleten **set-AzApplicationGatewayWebApplicationFirewallConfiguration** ändrar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="2a1ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a1ba-107">EXAMPLES</span></span>

### <span data-ttu-id="2a1ba-108">Exempel 1: uppdatera konfigurationen för webb programmet brand vägg för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2a1ba-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="2a1ba-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2a1ba-110">Med det andra kommandot aktive ras brand Väggs konfigurationen för programgatewayen som lagras i $AppGw och anger brand Väggs läget för "RuleSetType" och RuleSetVersion till "3,0".</span><span class="sxs-lookup"><span data-stu-id="2a1ba-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="2a1ba-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a1ba-111">PARAMETERS</span></span>

### <span data-ttu-id="2a1ba-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a1ba-112">-ApplicationGateway</span></span>
<span data-ttu-id="2a1ba-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="2a1ba-114">Du kan använda Get-AzApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a1ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a1ba-115">-DefaultProfile</span></span>
<span data-ttu-id="2a1ba-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a1ba-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="2a1ba-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="2a1ba-118">De inaktiverade regel grupperna.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="2a1ba-119">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="2a1ba-119">-Enabled</span></span>
<span data-ttu-id="2a1ba-120">Anger om webb programs brand väggen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="2a1ba-121">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="2a1ba-121">-Exclusion</span></span>
<span data-ttu-id="2a1ba-122">Undantags listorna.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="2a1ba-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="2a1ba-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="2a1ba-124">Max gränsen för fil uppladdning i MB.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="2a1ba-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="2a1ba-125">-FirewallMode</span></span>
<span data-ttu-id="2a1ba-126">Anger brand Väggs läget för webb programmet.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="2a1ba-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2a1ba-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2a1ba-128">Proxyidentifiering</span><span class="sxs-lookup"><span data-stu-id="2a1ba-128">Detection</span></span>
- <span data-ttu-id="2a1ba-129">Utebliv</span><span class="sxs-lookup"><span data-stu-id="2a1ba-129">Prevention</span></span>

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

### <span data-ttu-id="2a1ba-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="2a1ba-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="2a1ba-131">Max storlek för begärantext i KB.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="2a1ba-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="2a1ba-132">-RequestBodyCheck</span></span>
<span data-ttu-id="2a1ba-133">Om bröd texten är markerad eller inte.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="2a1ba-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="2a1ba-134">-RuleSetType</span></span>
<span data-ttu-id="2a1ba-135">Typ av brand Väggs regel för webb program.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="2a1ba-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2a1ba-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="2a1ba-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="2a1ba-137">OWASP</span></span>

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

### <span data-ttu-id="2a1ba-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="2a1ba-138">-RuleSetVersion</span></span>
<span data-ttu-id="2a1ba-139">Versionen av regel uppsättnings typen.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a1ba-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a1ba-140">-Confirm</span></span>
<span data-ttu-id="2a1ba-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a1ba-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a1ba-142">-WhatIf</span></span>
<span data-ttu-id="2a1ba-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a1ba-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a1ba-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1ba-145">CommonParameters</span></span>
<span data-ttu-id="2a1ba-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a1ba-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1ba-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a1ba-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1ba-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a1ba-148">INPUTS</span></span>

### <span data-ttu-id="2a1ba-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a1ba-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a1ba-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a1ba-150">OUTPUTS</span></span>

### <span data-ttu-id="2a1ba-151">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a1ba-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2a1ba-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a1ba-152">NOTES</span></span>

## <span data-ttu-id="2a1ba-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a1ba-153">RELATED LINKS</span></span>

[<span data-ttu-id="2a1ba-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a1ba-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2a1ba-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a1ba-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="2a1ba-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a1ba-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

