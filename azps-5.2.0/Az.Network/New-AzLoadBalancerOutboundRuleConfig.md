---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 9bc4c582956b30a8298b9579d92b2cd4fe0e31a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412192"
---
# <span data-ttu-id="e8e3f-101">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8e3f-101">New-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="e8e3f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e3f-103">Skapar en konfiguration för utgående regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-103">Creates an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e8e3f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8e3f-104">SYNTAX</span></span>

### <span data-ttu-id="e8e3f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="e8e3f-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e3f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e3f-106">SetByResourceId</span></span>
```
New-AzLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>] -FrontendIpConfiguration <PSResourceId[]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8e3f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8e3f-107">DESCRIPTION</span></span>
<span data-ttu-id="e8e3f-108">Cmdleten **New-AzLoadBalancerOutboundRuleConfig** skapar en konfiguration för utgående regel för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-108">The **New-AzLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e8e3f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8e3f-109">EXAMPLES</span></span>

### <span data-ttu-id="e8e3f-110">Exempel 1: skapa en konfiguration för utgående regel för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="e8e3f-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```powershell
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic" -Sku "Standard"
PS C:\>$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="e8e3f-111">Det första kommandot skapar en offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="e8e3f-112">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip och lagrar den sedan i $frontend-variabeln.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="e8e3f-113">Det tredje kommandot skapar en konfiguration för backend-adresspoolen med namnet BackendAddressPool01 och lagrar den sedan i $backend variabel.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="e8e3f-114">Det fjärde kommandot skapar en konfiguration för utgående regel som heter MyOutboundRule med hjälp av front-och backend-objekt i $frontend och $backend.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="e8e3f-115">Parametrarna *Protocol*, *FrontendIPConfiguration* och *BackendAddressPool* krävs för att skapa en regel för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-115">The *Protocol*, *FrontendIPConfiguration*, and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

### <span data-ttu-id="e8e3f-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e8e3f-116">Example 2</span></span>

<span data-ttu-id="e8e3f-117">Skapar en konfiguration för utgående regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-117">Creates an outbound rule configuration for a load balancer.</span></span> <span data-ttu-id="e8e3f-118">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="e8e3f-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzLoadBalancerOutboundRuleConfig -BackendAddressPool <PSBackendAddressPool> -EnableTcpReset -FrontendIpConfiguration <PSResourceId[]> -Name 'MyOutboundRule' -Protocol 'Tcp'
```

## <span data-ttu-id="e8e3f-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8e3f-119">PARAMETERS</span></span>

### <span data-ttu-id="e8e3f-120">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="e8e3f-120">-AllocatedOutboundPort</span></span>
<span data-ttu-id="e8e3f-121">Antalet utgående portar som ska användas för NAT.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-121">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="e8e3f-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8e3f-122">-BackendAddressPool</span></span>
<span data-ttu-id="e8e3f-123">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e8e3f-124">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e3f-125">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e8e3f-125">-BackendAddressPoolId</span></span>
<span data-ttu-id="e8e3f-126">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-126">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="e8e3f-127">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-127">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e3f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e3f-128">-DefaultProfile</span></span>
<span data-ttu-id="e8e3f-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e3f-130">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="e8e3f-130">-EnableTcpReset</span></span>
<span data-ttu-id="e8e3f-131">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-131">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="e8e3f-132">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-132">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="e8e3f-133">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8e3f-133">-FrontendIpConfiguration</span></span>
<span data-ttu-id="e8e3f-134">Belastnings utjämningens IP-adresser för klient delen.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-134">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8e3f-135">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="e8e3f-135">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="e8e3f-136">Timeout för TCP-inaktiv anslutning</span><span class="sxs-lookup"><span data-stu-id="e8e3f-136">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="e8e3f-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="e8e3f-137">-Name</span></span>
<span data-ttu-id="e8e3f-138">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-138">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="e8e3f-139">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e8e3f-139">-Protocol</span></span>
<span data-ttu-id="e8e3f-140">Protokoll – TCP, UDP eller alla</span><span class="sxs-lookup"><span data-stu-id="e8e3f-140">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="e8e3f-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8e3f-141">-Confirm</span></span>
<span data-ttu-id="e8e3f-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e3f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e3f-143">-WhatIf</span></span>
<span data-ttu-id="e8e3f-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8e3f-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8e3f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e3f-146">CommonParameters</span></span>
<span data-ttu-id="e8e3f-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e3f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e3f-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8e3f-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e3f-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8e3f-149">INPUTS</span></span>

### <span data-ttu-id="e8e3f-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e8e3f-150">System.Int32</span></span>

### <span data-ttu-id="e8e3f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e8e3f-151">System.String</span></span>

### <span data-ttu-id="e8e3f-152">Microsoft. Azure. commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="e8e3f-152">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="e8e3f-153">Microsoft. Azure. commands. Networks. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e8e3f-153">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e8e3f-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8e3f-154">OUTPUTS</span></span>

### <span data-ttu-id="e8e3f-155">Microsoft. Azure. commands. Networks. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="e8e3f-155">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="e8e3f-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8e3f-156">NOTES</span></span>

## <span data-ttu-id="e8e3f-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8e3f-157">RELATED LINKS</span></span>

[<span data-ttu-id="e8e3f-158">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8e3f-158">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e8e3f-159">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8e3f-159">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e8e3f-160">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8e3f-160">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="e8e3f-161">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e8e3f-161">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
