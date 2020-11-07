---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 03acee0ee1e15ffe0be605753d166ff4a956c274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757493"
---
# <span data-ttu-id="34a07-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="34a07-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="34a07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34a07-102">SYNOPSIS</span></span>
<span data-ttu-id="34a07-103">Ändrar WAF konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="34a07-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34a07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34a07-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34a07-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34a07-105">DESCRIPTION</span></span>
<span data-ttu-id="34a07-106">Cmdleten **set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** ändrar webb program brand väggen (WAF) för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="34a07-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="34a07-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34a07-107">EXAMPLES</span></span>

### <span data-ttu-id="34a07-108">Exempel 1: uppdatera konfigurationen för webb programmet brand vägg för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="34a07-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="34a07-109">Det första kommandot hämtar programgatewayen med namnet ApplicationGateway01 och lagrar den sedan i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="34a07-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="34a07-110">Med det andra kommandot aktive ras brand Väggs konfigurationen för programgatewayen som lagras i $AppGw och anger brand Väggs läget för "RuleSetType" och RuleSetVersion till "3,0".</span><span class="sxs-lookup"><span data-stu-id="34a07-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="34a07-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34a07-111">PARAMETERS</span></span>

### <span data-ttu-id="34a07-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34a07-112">-ApplicationGateway</span></span>
<span data-ttu-id="34a07-113">Anger ett Application Gateway-objekt.</span><span class="sxs-lookup"><span data-stu-id="34a07-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="34a07-114">Du kan använda Get-AzureRmApplicationGateway cmdlet för att hämta ett objekt för Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="34a07-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="34a07-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="34a07-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="34a07-116">De inaktiverade regel grupperna.</span><span class="sxs-lookup"><span data-stu-id="34a07-116">The disabled rule groups.</span></span>

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

### <span data-ttu-id="34a07-117">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="34a07-117">-Enabled</span></span>
<span data-ttu-id="34a07-118">Anger om webb programs brand väggen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="34a07-118">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="34a07-119">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="34a07-119">-FirewallMode</span></span>
<span data-ttu-id="34a07-120">Anger brand Väggs läget för webb programmet.</span><span class="sxs-lookup"><span data-stu-id="34a07-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="34a07-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="34a07-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="34a07-122">Proxyidentifiering</span><span class="sxs-lookup"><span data-stu-id="34a07-122">Detection</span></span>
- <span data-ttu-id="34a07-123">Utebliv</span><span class="sxs-lookup"><span data-stu-id="34a07-123">Prevention</span></span>

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

### <span data-ttu-id="34a07-124">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="34a07-124">-RuleSetType</span></span>
<span data-ttu-id="34a07-125">Typ av brand Väggs regel för webb program.</span><span class="sxs-lookup"><span data-stu-id="34a07-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="34a07-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="34a07-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="34a07-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="34a07-127">OWASP</span></span>

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

### <span data-ttu-id="34a07-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="34a07-128">-RuleSetVersion</span></span>
<span data-ttu-id="34a07-129">Versionen av regel uppsättnings typen.</span><span class="sxs-lookup"><span data-stu-id="34a07-129">The version of the rule set type.</span></span>
<span data-ttu-id="34a07-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="34a07-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="34a07-131">3,0</span><span class="sxs-lookup"><span data-stu-id="34a07-131">3.0</span></span>
- <span data-ttu-id="34a07-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="34a07-132">2.2.9</span></span>

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

### <span data-ttu-id="34a07-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="34a07-133">-Confirm</span></span>
<span data-ttu-id="34a07-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="34a07-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34a07-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34a07-135">-WhatIf</span></span>
<span data-ttu-id="34a07-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="34a07-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34a07-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="34a07-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34a07-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34a07-138">-DefaultProfile</span></span>
<span data-ttu-id="34a07-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34a07-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34a07-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34a07-140">CommonParameters</span></span>
<span data-ttu-id="34a07-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34a07-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34a07-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34a07-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34a07-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34a07-143">INPUTS</span></span>

### <span data-ttu-id="34a07-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34a07-144">PSApplicationGateway</span></span>
<span data-ttu-id="34a07-145">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="34a07-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="34a07-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34a07-146">OUTPUTS</span></span>

### <span data-ttu-id="34a07-147">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34a07-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="34a07-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34a07-148">NOTES</span></span>

## <span data-ttu-id="34a07-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34a07-149">RELATED LINKS</span></span>

[<span data-ttu-id="34a07-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="34a07-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="34a07-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="34a07-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="34a07-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="34a07-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


