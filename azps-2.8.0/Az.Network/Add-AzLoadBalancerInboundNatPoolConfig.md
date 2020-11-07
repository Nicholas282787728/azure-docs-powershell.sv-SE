---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 672829daffa2117265e8f43b30f504adc702f3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918831"
---
# <span data-ttu-id="fbd2b-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fbd2b-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="fbd2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbd2b-102">SYNOPSIS</span></span>
<span data-ttu-id="fbd2b-103">Lägger till en inkommande NAT-pool till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="fbd2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbd2b-104">SYNTAX</span></span>

### <span data-ttu-id="fbd2b-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="fbd2b-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbd2b-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbd2b-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbd2b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbd2b-107">DESCRIPTION</span></span>
<span data-ttu-id="fbd2b-108">Cmdleten **Add-AzLoadBalancerInboundNatPoolConfig** lägger till en inkommande NAT-pool till en belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="fbd2b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbd2b-109">EXAMPLES</span></span>

### <span data-ttu-id="fbd2b-110">1: lägga till</span><span class="sxs-lookup"><span data-stu-id="fbd2b-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="fbd2b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbd2b-111">PARAMETERS</span></span>

### <span data-ttu-id="fbd2b-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fbd2b-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbd2b-113">-DefaultProfile</span></span>
<span data-ttu-id="fbd2b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbd2b-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="fbd2b-115">-EnableFloatingIP</span></span>
<span data-ttu-id="fbd2b-116">Konfigurerar en virtuell dators slut punkt för den flytande IP-kapaciteten som krävs för att konfigurera en SQL AlwaysOn-tillgänglighetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="fbd2b-117">Den här inställningen krävs vid användning av SQL AlwaysOn-tillgänglighetsgruppen i SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="fbd2b-118">Den här inställningen kan inte ändras när du har skapat slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="fbd2b-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="fbd2b-119">-EnableTcpReset</span></span>
<span data-ttu-id="fbd2b-120">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="fbd2b-121">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="fbd2b-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbd2b-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="fbd2b-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="fbd2b-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="fbd2b-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="fbd2b-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2b-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="fbd2b-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2b-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="fbd2b-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="fbd2b-127">Timeout för TCP-inaktiv anslutning.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="fbd2b-128">Värdet kan anges mellan 4 och 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="fbd2b-129">Standardvärdet är 4 minuter.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-129">The default value is 4 minutes.</span></span> <span data-ttu-id="fbd2b-130">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="fbd2b-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbd2b-131">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2b-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbd2b-132">-Name</span></span>
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

### <span data-ttu-id="fbd2b-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="fbd2b-133">-Protocol</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbd2b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fbd2b-134">-Confirm</span></span>
<span data-ttu-id="fbd2b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbd2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbd2b-136">-WhatIf</span></span>
<span data-ttu-id="fbd2b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbd2b-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbd2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbd2b-139">CommonParameters</span></span>
<span data-ttu-id="fbd2b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbd2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbd2b-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbd2b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbd2b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbd2b-142">INPUTS</span></span>

### <span data-ttu-id="fbd2b-143">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbd2b-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="fbd2b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fbd2b-144">System.String</span></span>

### <span data-ttu-id="fbd2b-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fbd2b-145">System.Int32</span></span>

### <span data-ttu-id="fbd2b-146">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fbd2b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="fbd2b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbd2b-147">OUTPUTS</span></span>

### <span data-ttu-id="fbd2b-148">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="fbd2b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="fbd2b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbd2b-149">NOTES</span></span>

## <span data-ttu-id="fbd2b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbd2b-150">RELATED LINKS</span></span>

[<span data-ttu-id="fbd2b-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fbd2b-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="fbd2b-152">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fbd2b-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="fbd2b-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fbd2b-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="fbd2b-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="fbd2b-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
