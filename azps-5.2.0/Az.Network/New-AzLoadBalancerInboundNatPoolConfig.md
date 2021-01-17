---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401256"
---
# <span data-ttu-id="d06d1-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d06d1-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="d06d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d06d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d06d1-103">Skapar en inkommande konfiguration för NAT-pool för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="d06d1-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="d06d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d06d1-104">SYNTAX</span></span>

### <span data-ttu-id="d06d1-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d06d1-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d06d1-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d06d1-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d06d1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d06d1-107">DESCRIPTION</span></span>
<span data-ttu-id="d06d1-108">Cmdleten **New-AzLoadBalancerInboundNatPoolConfig** skapar en inkommande konfiguration för NAT-pool för en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="d06d1-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="d06d1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d06d1-109">EXAMPLES</span></span>

### <span data-ttu-id="d06d1-110">Exempel 1: ny</span><span class="sxs-lookup"><span data-stu-id="d06d1-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="d06d1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d06d1-111">PARAMETERS</span></span>

### <span data-ttu-id="d06d1-112">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="d06d1-112">-BackendPort</span></span>
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

### <span data-ttu-id="d06d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06d1-113">-DefaultProfile</span></span>
<span data-ttu-id="d06d1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d06d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06d1-115">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="d06d1-115">-EnableFloatingIP</span></span>
<span data-ttu-id="d06d1-116">Konfigurerar en virtuell dators slut punkt för den flytande IP-kapaciteten som krävs för att konfigurera en SQL AlwaysOn-tillgänglighetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="d06d1-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="d06d1-117">Den här inställningen krävs vid användning av SQL AlwaysOn-tillgänglighetsgruppen i SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d06d1-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="d06d1-118">Den här inställningen kan inte ändras när du har skapat slut punkten.</span><span class="sxs-lookup"><span data-stu-id="d06d1-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="d06d1-119">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="d06d1-119">-EnableTcpReset</span></span>
<span data-ttu-id="d06d1-120">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="d06d1-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="d06d1-121">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="d06d1-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d06d1-122">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d06d1-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="d06d1-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d06d1-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="d06d1-124">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="d06d1-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="d06d1-125">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="d06d1-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="d06d1-126">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="d06d1-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="d06d1-127">Timeout för TCP-inaktiv anslutning.</span><span class="sxs-lookup"><span data-stu-id="d06d1-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="d06d1-128">Värdet kan anges mellan 4 och 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="d06d1-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="d06d1-129">Standardvärdet är 4 minuter.</span><span class="sxs-lookup"><span data-stu-id="d06d1-129">The default value is 4 minutes.</span></span> <span data-ttu-id="d06d1-130">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="d06d1-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="d06d1-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="d06d1-131">-Name</span></span>
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

### <span data-ttu-id="d06d1-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d06d1-132">-Protocol</span></span>
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

### <span data-ttu-id="d06d1-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d06d1-133">-Confirm</span></span>
<span data-ttu-id="d06d1-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d06d1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06d1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06d1-135">-WhatIf</span></span>
<span data-ttu-id="d06d1-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d06d1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d06d1-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d06d1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06d1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06d1-138">CommonParameters</span></span>
<span data-ttu-id="d06d1-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06d1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06d1-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06d1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06d1-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d06d1-141">INPUTS</span></span>

### <span data-ttu-id="d06d1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d06d1-142">System.String</span></span>

### <span data-ttu-id="d06d1-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d06d1-143">System.Int32</span></span>

### <span data-ttu-id="d06d1-144">Microsoft. Azure. commands. Networks. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d06d1-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="d06d1-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d06d1-145">OUTPUTS</span></span>

### <span data-ttu-id="d06d1-146">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="d06d1-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="d06d1-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d06d1-147">NOTES</span></span>

## <span data-ttu-id="d06d1-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d06d1-148">RELATED LINKS</span></span>

[<span data-ttu-id="d06d1-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d06d1-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d06d1-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d06d1-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d06d1-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d06d1-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="d06d1-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d06d1-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
