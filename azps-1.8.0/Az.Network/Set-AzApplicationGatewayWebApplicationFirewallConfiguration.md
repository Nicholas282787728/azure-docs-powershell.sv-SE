---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: a5f60588a0db848d0b96aa0611b8647142db2b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747754"
---
# <span data-ttu-id="4fe01-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fe01-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="4fe01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4fe01-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe01-103">Ändrar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4fe01-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="4fe01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4fe01-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4fe01-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe01-106">Cmdleten **set-AzApplicationGatewayWebApplicationFirewallConfiguration** ändrar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="4fe01-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="4fe01-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4fe01-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe01-108">Exempel 1: uppdatera konfigurationen för webb programmet brand vägg för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="4fe01-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="4fe01-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="4fe01-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4fe01-110">Med det andra kommandot aktive ras brand Väggs konfigurationen för programgatewayen som lagras i $AppGw och anger brand Väggs läget för "RuleSetType" och RuleSetVersion till "3,0".</span><span class="sxs-lookup"><span data-stu-id="4fe01-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="4fe01-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4fe01-111">PARAMETERS</span></span>

### <span data-ttu-id="4fe01-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe01-112">-ApplicationGateway</span></span>
<span data-ttu-id="4fe01-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="4fe01-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="4fe01-114">Du kan använda Get-AzApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4fe01-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="4fe01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe01-115">-DefaultProfile</span></span>
<span data-ttu-id="4fe01-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4fe01-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fe01-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="4fe01-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="4fe01-118">De inaktiverade regel grupperna.</span><span class="sxs-lookup"><span data-stu-id="4fe01-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="4fe01-119">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="4fe01-119">-Enabled</span></span>
<span data-ttu-id="4fe01-120">Anger om webb programs brand väggen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4fe01-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="4fe01-121">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="4fe01-121">-Exclusion</span></span>
<span data-ttu-id="4fe01-122">Undantags listorna.</span><span class="sxs-lookup"><span data-stu-id="4fe01-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="4fe01-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="4fe01-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="4fe01-124">Max gränsen för fil uppladdning i MB.</span><span class="sxs-lookup"><span data-stu-id="4fe01-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="4fe01-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="4fe01-125">-FirewallMode</span></span>
<span data-ttu-id="4fe01-126">Anger brand Väggs läget för webb programmet.</span><span class="sxs-lookup"><span data-stu-id="4fe01-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="4fe01-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4fe01-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4fe01-128">Proxyidentifiering</span><span class="sxs-lookup"><span data-stu-id="4fe01-128">Detection</span></span>
- <span data-ttu-id="4fe01-129">Utebliv</span><span class="sxs-lookup"><span data-stu-id="4fe01-129">Prevention</span></span>

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

### <span data-ttu-id="4fe01-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="4fe01-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="4fe01-131">Max storlek för begärantext i KB.</span><span class="sxs-lookup"><span data-stu-id="4fe01-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="4fe01-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="4fe01-132">-RequestBodyCheck</span></span>
<span data-ttu-id="4fe01-133">Om bröd texten är markerad eller inte.</span><span class="sxs-lookup"><span data-stu-id="4fe01-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="4fe01-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="4fe01-134">-RuleSetType</span></span>
<span data-ttu-id="4fe01-135">Typ av brand Väggs regel för webb program.</span><span class="sxs-lookup"><span data-stu-id="4fe01-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="4fe01-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4fe01-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="4fe01-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="4fe01-137">OWASP</span></span>

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

### <span data-ttu-id="4fe01-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="4fe01-138">-RuleSetVersion</span></span>
<span data-ttu-id="4fe01-139">Versionen av regel uppsättnings typen.</span><span class="sxs-lookup"><span data-stu-id="4fe01-139">The version of the rule set type.</span></span>
<span data-ttu-id="4fe01-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4fe01-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="4fe01-141">3,0</span><span class="sxs-lookup"><span data-stu-id="4fe01-141">3.0</span></span>
- <span data-ttu-id="4fe01-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="4fe01-142">2.2.9</span></span>

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

### <span data-ttu-id="4fe01-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4fe01-143">-Confirm</span></span>
<span data-ttu-id="4fe01-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4fe01-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe01-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe01-145">-WhatIf</span></span>
<span data-ttu-id="4fe01-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4fe01-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fe01-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4fe01-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe01-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe01-148">CommonParameters</span></span>
<span data-ttu-id="4fe01-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe01-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe01-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe01-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe01-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4fe01-151">INPUTS</span></span>

### <span data-ttu-id="4fe01-152">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe01-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fe01-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4fe01-153">OUTPUTS</span></span>

### <span data-ttu-id="4fe01-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe01-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fe01-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4fe01-155">NOTES</span></span>

## <span data-ttu-id="4fe01-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4fe01-156">RELATED LINKS</span></span>

[<span data-ttu-id="4fe01-157">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fe01-157">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="4fe01-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fe01-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="4fe01-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fe01-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

