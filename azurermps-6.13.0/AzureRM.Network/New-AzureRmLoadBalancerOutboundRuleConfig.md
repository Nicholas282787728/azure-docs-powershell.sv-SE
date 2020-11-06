---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: dd2c0064b92ff96fedd9e06c32b2f2f0f5a2c65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584920"
---
# <span data-ttu-id="51c57-101">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="51c57-101">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="51c57-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51c57-102">SYNOPSIS</span></span>
<span data-ttu-id="51c57-103">Skapar en konfiguration för utgående regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="51c57-103">Creates an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51c57-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51c57-104">SYNTAX</span></span>

### <span data-ttu-id="51c57-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="51c57-105">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51c57-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51c57-106">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerOutboundRuleConfig -Name <String> [-AllocatedOutboundPort <Int32>] -Protocol <String>
 [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51c57-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51c57-107">DESCRIPTION</span></span>
<span data-ttu-id="51c57-108">Cmdleten **New-AzureRmLoadBalancerOutboundRuleConfig** skapar en konfiguration för utgående regel för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="51c57-108">The **New-AzureRmLoadBalancerOutboundRuleConfig** cmdlet creates an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="51c57-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51c57-109">EXAMPLES</span></span>

### <span data-ttu-id="51c57-110">Exempel 1: skapa en konfiguration för utgående regel för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="51c57-110">Example 1: Create an outbound rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\>$frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\>$backend = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool01"
PS C:\>New-AzureRmLoadBalancerOutboundRuleConfig -Name "MyOutboundRule" -Protocol "Tcp" -FrontendIPConfiguration $frontend -BackendAddressPool $backend
```

<span data-ttu-id="51c57-111">Det första kommandot skapar en offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="51c57-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="51c57-112">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip och lagrar den sedan i $frontend-variabeln.</span><span class="sxs-lookup"><span data-stu-id="51c57-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>
<span data-ttu-id="51c57-113">Det tredje kommandot skapar en konfiguration för backend-adresspoolen med namnet BackendAddressPool01 och lagrar den sedan i $backend variabel.</span><span class="sxs-lookup"><span data-stu-id="51c57-113">The third command creates a back-end address pool configuration named BackendAddressPool01, and then stores it in the $backend variable.</span></span>
<span data-ttu-id="51c57-114">Det fjärde kommandot skapar en konfiguration för utgående regel som heter MyOutboundRule med hjälp av front-och backend-objekt i $frontend och $backend.</span><span class="sxs-lookup"><span data-stu-id="51c57-114">The fourth command creates an outbound rule configuration named MyOutboundRule using the front-end and back-end objects in $frontend and $backend.</span></span>
<span data-ttu-id="51c57-115">Parametrarna *Protocol* , *FrontendIPConfiguration* och *BackendAddressPool* krävs för att skapa en regel för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="51c57-115">The *Protocol* , *FrontendIPConfiguration* , and *BackendAddressPool* parameters are all required to create an outbound rule configuration.</span></span>

## <span data-ttu-id="51c57-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51c57-116">PARAMETERS</span></span>

### <span data-ttu-id="51c57-117">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="51c57-117">-AllocatedOutboundPort</span></span>
<span data-ttu-id="51c57-118">Antalet utgående portar som ska användas för NAT.</span><span class="sxs-lookup"><span data-stu-id="51c57-118">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="51c57-119">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="51c57-119">-BackendAddressPool</span></span>
<span data-ttu-id="51c57-120">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="51c57-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="51c57-121">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="51c57-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="51c57-122">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="51c57-122">-BackendAddressPoolId</span></span>
<span data-ttu-id="51c57-123">En referens till en pool med DIP.</span><span class="sxs-lookup"><span data-stu-id="51c57-123">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="51c57-124">Utgående trafik bal anse ras slumpmässigt för IP i Server delen.</span><span class="sxs-lookup"><span data-stu-id="51c57-124">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="51c57-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51c57-125">-DefaultProfile</span></span>
<span data-ttu-id="51c57-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51c57-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51c57-127">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="51c57-127">-EnableTcpReset</span></span>
<span data-ttu-id="51c57-128">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="51c57-128">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="51c57-129">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="51c57-129">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="51c57-130">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="51c57-130">-FrontendIpConfiguration</span></span>
<span data-ttu-id="51c57-131">Belastnings utjämningens IP-adresser för klient delen.</span><span class="sxs-lookup"><span data-stu-id="51c57-131">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51c57-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="51c57-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="51c57-133">Timeout för TCP-inaktiv anslutning</span><span class="sxs-lookup"><span data-stu-id="51c57-133">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="51c57-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="51c57-134">-Name</span></span>
<span data-ttu-id="51c57-135">Namn på regeln för utgående trafik.</span><span class="sxs-lookup"><span data-stu-id="51c57-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="51c57-136">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="51c57-136">-Protocol</span></span>
<span data-ttu-id="51c57-137">Protokoll – TCP, UDP eller alla</span><span class="sxs-lookup"><span data-stu-id="51c57-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="51c57-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51c57-138">-Confirm</span></span>
<span data-ttu-id="51c57-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51c57-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51c57-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51c57-140">-WhatIf</span></span>
<span data-ttu-id="51c57-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51c57-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51c57-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51c57-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51c57-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51c57-143">CommonParameters</span></span>
<span data-ttu-id="51c57-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51c57-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51c57-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51c57-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51c57-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51c57-146">INPUTS</span></span>

### <span data-ttu-id="51c57-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="51c57-147">System.Int32</span></span>
<span data-ttu-id="51c57-148">System. String system. Collections. Genered. list \` 1 [[Microsoft. Azure. commands. Network. Models. PSResourceId, Microsoft. Azure. commands. Network, version = 6.5.0.0, Culture = neutralt, PublicKeyToken = null]] Microsoft. Azure. commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="51c57-148">System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="51c57-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51c57-149">OUTPUTS</span></span>

### <span data-ttu-id="51c57-150">Microsoft. Azure. commands. Networks. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="51c57-150">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="51c57-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51c57-151">NOTES</span></span>

## <span data-ttu-id="51c57-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51c57-152">RELATED LINKS</span></span>
