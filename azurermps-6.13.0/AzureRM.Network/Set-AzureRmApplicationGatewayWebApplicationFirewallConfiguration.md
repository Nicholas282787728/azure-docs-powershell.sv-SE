---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 3b2de5d139c8addb448ac76609e13becf2e0153c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755191"
---
# <span data-ttu-id="b9f81-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9f81-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="b9f81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9f81-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f81-103">Ändrar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b9f81-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9f81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9f81-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-RequestBodyCheck <Boolean>] [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9f81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9f81-105">DESCRIPTION</span></span>
<span data-ttu-id="b9f81-106">Cmdleten **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** ändrar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b9f81-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="b9f81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9f81-107">EXAMPLES</span></span>

### <span data-ttu-id="b9f81-108">Exempel 1: uppdatera konfigurationen för webb programmet brand vägg för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="b9f81-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="b9f81-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="b9f81-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9f81-110">Med det andra kommandot aktive ras brand Väggs konfigurationen för programgatewayen som lagras i $AppGw och anger brand Väggs läget för "RuleSetType" och RuleSetVersion till "3,0".</span><span class="sxs-lookup"><span data-stu-id="b9f81-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="b9f81-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9f81-111">PARAMETERS</span></span>

### <span data-ttu-id="b9f81-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9f81-112">-ApplicationGateway</span></span>
<span data-ttu-id="b9f81-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="b9f81-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="b9f81-114">Du kan använda Get-AzureRmApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9f81-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="b9f81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f81-115">-DefaultProfile</span></span>
<span data-ttu-id="b9f81-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9f81-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="b9f81-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="b9f81-118">De inaktiverade regel grupperna.</span><span class="sxs-lookup"><span data-stu-id="b9f81-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f81-119">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="b9f81-119">-Enabled</span></span>
<span data-ttu-id="b9f81-120">Anger om webb programs brand väggen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="b9f81-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="b9f81-121">-Uteslutning</span><span class="sxs-lookup"><span data-stu-id="b9f81-121">-Exclusion</span></span>
<span data-ttu-id="b9f81-122">Undantags listorna.</span><span class="sxs-lookup"><span data-stu-id="b9f81-122">The exclusion lists.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f81-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="b9f81-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="b9f81-124">Max gränsen för fil uppladdning i MB.</span><span class="sxs-lookup"><span data-stu-id="b9f81-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="b9f81-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="b9f81-125">-FirewallMode</span></span>
<span data-ttu-id="b9f81-126">Anger brand Väggs läget för webb programmet.</span><span class="sxs-lookup"><span data-stu-id="b9f81-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="b9f81-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b9f81-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b9f81-128">Proxyidentifiering</span><span class="sxs-lookup"><span data-stu-id="b9f81-128">Detection</span></span>
- <span data-ttu-id="b9f81-129">Utebliv</span><span class="sxs-lookup"><span data-stu-id="b9f81-129">Prevention</span></span>

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

### <span data-ttu-id="b9f81-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="b9f81-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="b9f81-131">Max storlek för begärantext i KB.</span><span class="sxs-lookup"><span data-stu-id="b9f81-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="b9f81-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="b9f81-132">-RequestBodyCheck</span></span>
<span data-ttu-id="b9f81-133">Om bröd texten är markerad eller inte.</span><span class="sxs-lookup"><span data-stu-id="b9f81-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="b9f81-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="b9f81-134">-RuleSetType</span></span>
<span data-ttu-id="b9f81-135">Typ av brand Väggs regel för webb program.</span><span class="sxs-lookup"><span data-stu-id="b9f81-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="b9f81-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b9f81-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="b9f81-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="b9f81-137">OWASP</span></span>

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

### <span data-ttu-id="b9f81-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="b9f81-138">-RuleSetVersion</span></span>
<span data-ttu-id="b9f81-139">Versionen av regel uppsättnings typen.</span><span class="sxs-lookup"><span data-stu-id="b9f81-139">The version of the rule set type.</span></span>
<span data-ttu-id="b9f81-140">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b9f81-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="b9f81-141">3,0</span><span class="sxs-lookup"><span data-stu-id="b9f81-141">3.0</span></span>
- <span data-ttu-id="b9f81-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="b9f81-142">2.2.9</span></span>

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

### <span data-ttu-id="b9f81-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b9f81-143">-Confirm</span></span>
<span data-ttu-id="b9f81-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b9f81-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9f81-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f81-145">-WhatIf</span></span>
<span data-ttu-id="b9f81-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b9f81-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9f81-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b9f81-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9f81-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f81-148">CommonParameters</span></span>
<span data-ttu-id="b9f81-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f81-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f81-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9f81-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f81-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9f81-151">INPUTS</span></span>

### <span data-ttu-id="b9f81-152">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9f81-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="b9f81-153">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b9f81-153">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="b9f81-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9f81-154">OUTPUTS</span></span>

### <span data-ttu-id="b9f81-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9f81-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9f81-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9f81-156">NOTES</span></span>

## <span data-ttu-id="b9f81-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9f81-157">RELATED LINKS</span></span>

[<span data-ttu-id="b9f81-158">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9f81-158">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="b9f81-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9f81-159">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="b9f81-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9f81-160">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


