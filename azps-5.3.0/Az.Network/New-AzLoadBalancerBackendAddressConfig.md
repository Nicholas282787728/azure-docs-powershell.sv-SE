---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523244"
---
# <span data-ttu-id="df4b1-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="df4b1-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="df4b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df4b1-102">SYNOPSIS</span></span>
<span data-ttu-id="df4b1-103">Returnerar en server för belastnings Utjämnings adresser.</span><span class="sxs-lookup"><span data-stu-id="df4b1-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="df4b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df4b1-104">SYNTAX</span></span>

### <span data-ttu-id="df4b1-105">SetByResourcePublicIpAddress (standard)</span><span class="sxs-lookup"><span data-stu-id="df4b1-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df4b1-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="df4b1-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df4b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df4b1-107">DESCRIPTION</span></span>
<span data-ttu-id="df4b1-108">Returnerar en server för belastnings Utjämnings adresser.</span><span class="sxs-lookup"><span data-stu-id="df4b1-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="df4b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df4b1-109">EXAMPLES</span></span>

### <span data-ttu-id="df4b1-110">Exempel 1: ny Loadbalancer-adress konfiguration med virtuell nätverks referens</span><span class="sxs-lookup"><span data-stu-id="df4b1-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="df4b1-111">Exempel 2: ny Loadbalancer-adress config med IP-konfiguration Reference för klient delen</span><span class="sxs-lookup"><span data-stu-id="df4b1-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="df4b1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df4b1-112">PARAMETERS</span></span>

### <span data-ttu-id="df4b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4b1-113">-DefaultProfile</span></span>
<span data-ttu-id="df4b1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df4b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4b1-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="df4b1-115">-IpAddress</span></span>
<span data-ttu-id="df4b1-116">Den IP-adress som ska läggas till i backend-poolen</span><span class="sxs-lookup"><span data-stu-id="df4b1-116">The IPAddress to add to the backend pool</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b1-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="df4b1-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="df4b1-118">Belastningsutjämnarens IP-konfiguration för belastningsutjämnare med Server dels adress konfiguration</span><span class="sxs-lookup"><span data-stu-id="df4b1-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceFrontendIPConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b1-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="df4b1-119">-Name</span></span>
<span data-ttu-id="df4b1-120">Namnet på Server delens konfiguration</span><span class="sxs-lookup"><span data-stu-id="df4b1-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="df4b1-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="df4b1-121">-VirtualNetworkId</span></span>
<span data-ttu-id="df4b1-122">Det virtuella nätverk som är kopplat till Server dels adress konfiguration</span><span class="sxs-lookup"><span data-stu-id="df4b1-122">The virtual network associated with Backend Address config</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4b1-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="df4b1-123">-Confirm</span></span>
<span data-ttu-id="df4b1-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="df4b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df4b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df4b1-125">-WhatIf</span></span>
<span data-ttu-id="df4b1-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="df4b1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df4b1-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="df4b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df4b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4b1-128">CommonParameters</span></span>
<span data-ttu-id="df4b1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4b1-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df4b1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4b1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df4b1-131">INPUTS</span></span>

### <span data-ttu-id="df4b1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="df4b1-132">System.String</span></span>

### <span data-ttu-id="df4b1-133">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df4b1-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df4b1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df4b1-134">OUTPUTS</span></span>

### <span data-ttu-id="df4b1-135">Microsoft. Azure. commands. Networks. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="df4b1-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="df4b1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df4b1-136">NOTES</span></span>

## <span data-ttu-id="df4b1-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df4b1-137">RELATED LINKS</span></span>
