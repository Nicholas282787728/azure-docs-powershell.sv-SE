---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: d2508b233bc67cb49d0a1c525f7e43ccf07242b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269633"
---
# <span data-ttu-id="64d28-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d28-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="64d28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64d28-102">SYNOPSIS</span></span>
<span data-ttu-id="64d28-103">Skapar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="64d28-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="64d28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64d28-104">SYNTAX</span></span>

### <span data-ttu-id="64d28-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="64d28-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64d28-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="64d28-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64d28-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64d28-107">DESCRIPTION</span></span>
<span data-ttu-id="64d28-108">Cmdleten **New-AzLoadBalancerInboundNatRuleConfig** skapar en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="64d28-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="64d28-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64d28-109">EXAMPLES</span></span>

### <span data-ttu-id="64d28-110">Exempel 1: skapa en inkommande NAT-regel för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="64d28-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="64d28-111">Det första kommandot skapar en offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="64d28-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="64d28-112">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip och lagrar den sedan i $frontend-variabeln.</span><span class="sxs-lookup"><span data-stu-id="64d28-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="64d28-113">Det tredje kommandot skapar en inkommande NAT-regel som heter MyInboundNatRule med hjälp av ett frontend-objekt i $frontend.</span><span class="sxs-lookup"><span data-stu-id="64d28-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="64d28-114">TCP-protokollet anges och front porten är 3389, samma som Server porten i det här fallet.</span><span class="sxs-lookup"><span data-stu-id="64d28-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="64d28-115">Parametrarna *FrontendIpConfiguration* , *Protocol* , *FrontendPort* och *BackendPort* är nödvändiga för att skapa en inkommande konfiguration för NAT-regler.</span><span class="sxs-lookup"><span data-stu-id="64d28-115">The *FrontendIpConfiguration* , *Protocol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="64d28-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64d28-116">PARAMETERS</span></span>

### <span data-ttu-id="64d28-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="64d28-117">-BackendPort</span></span>
<span data-ttu-id="64d28-118">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="64d28-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d28-119">-DefaultProfile</span></span>
<span data-ttu-id="64d28-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64d28-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d28-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="64d28-121">-EnableFloatingIP</span></span>
<span data-ttu-id="64d28-122">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="64d28-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="64d28-123">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="64d28-123">-EnableTcpReset</span></span>
<span data-ttu-id="64d28-124">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="64d28-124">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="64d28-125">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="64d28-125">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="64d28-126">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="64d28-126">-FrontendIpConfiguration</span></span>
<span data-ttu-id="64d28-127">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="64d28-127">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-128">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="64d28-128">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="64d28-129">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="64d28-129">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-130">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="64d28-130">-FrontendPort</span></span>
<span data-ttu-id="64d28-131">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="64d28-131">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="64d28-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="64d28-133">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="64d28-133">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="64d28-134">-Name</span></span>
<span data-ttu-id="64d28-135">Anger namnet på den regel konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="64d28-135">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="64d28-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="64d28-136">-Protocol</span></span>
<span data-ttu-id="64d28-137">Anger ett protokoll.</span><span class="sxs-lookup"><span data-stu-id="64d28-137">Specifies a protocol.</span></span>
<span data-ttu-id="64d28-138">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="64d28-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64d28-139">TCP</span><span class="sxs-lookup"><span data-stu-id="64d28-139">Tcp</span></span>
- <span data-ttu-id="64d28-140">UDP</span><span class="sxs-lookup"><span data-stu-id="64d28-140">Udp</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="64d28-141">-Confirm</span></span>
<span data-ttu-id="64d28-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="64d28-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64d28-143">-WhatIf</span></span>
<span data-ttu-id="64d28-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="64d28-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64d28-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="64d28-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64d28-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d28-146">CommonParameters</span></span>
<span data-ttu-id="64d28-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64d28-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d28-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d28-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d28-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64d28-149">INPUTS</span></span>

### <span data-ttu-id="64d28-150">System. String</span><span class="sxs-lookup"><span data-stu-id="64d28-150">System.String</span></span>

### <span data-ttu-id="64d28-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="64d28-151">System.Int32</span></span>

### <span data-ttu-id="64d28-152">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="64d28-152">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="64d28-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64d28-153">OUTPUTS</span></span>

### <span data-ttu-id="64d28-154">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="64d28-154">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="64d28-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64d28-155">NOTES</span></span>

## <span data-ttu-id="64d28-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64d28-156">RELATED LINKS</span></span>

[<span data-ttu-id="64d28-157">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d28-157">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="64d28-158">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d28-158">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="64d28-159">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="64d28-159">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="64d28-160">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="64d28-160">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="64d28-161">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d28-161">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="64d28-162">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="64d28-162">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


