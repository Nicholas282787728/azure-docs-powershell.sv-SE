---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddressconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressConfig.md
ms.openlocfilehash: 3c3cc0e5da1cc8afbc6160acf13c3ef94eb02e34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398680"
---
# <span data-ttu-id="45b0b-101">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="45b0b-101">New-AzLoadBalancerBackendAddressConfig</span></span>

## <span data-ttu-id="45b0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45b0b-102">SYNOPSIS</span></span>
<span data-ttu-id="45b0b-103">Returnerar en server för belastnings Utjämnings adresser.</span><span class="sxs-lookup"><span data-stu-id="45b0b-103">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="45b0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45b0b-104">SYNTAX</span></span>

### <span data-ttu-id="45b0b-105">SetByResourcePublicIpAddress (standard)</span><span class="sxs-lookup"><span data-stu-id="45b0b-105">SetByResourcePublicIpAddress (Default)</span></span>
```
New-AzLoadBalancerBackendAddressConfig -IpAddress <String> -Name <String> -VirtualNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45b0b-106">SetByResourceFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="45b0b-106">SetByResourceFrontendIPConfiguration</span></span>
```
New-AzLoadBalancerBackendAddressConfig -Name <String> -LoadBalancerFrontendIPConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b0b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45b0b-107">DESCRIPTION</span></span>
<span data-ttu-id="45b0b-108">Returnerar en server för belastnings Utjämnings adresser.</span><span class="sxs-lookup"><span data-stu-id="45b0b-108">Returns a load balancer backend address config.</span></span> 

## <span data-ttu-id="45b0b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45b0b-109">EXAMPLES</span></span>

### <span data-ttu-id="45b0b-110">Exempel 1: ny Loadbalancer-adress konfiguration med virtuell nätverks referens</span><span class="sxs-lookup"><span data-stu-id="45b0b-110">Example 1: New loadbalancer address config with virtual network reference</span></span>
```powershell
PS C:\> $virtualNetwork = Get-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroup
New-AzLoadBalancerBackendAddressConfig -IpAddress "10.0.0.5" -Name "TestVNetRef" -VirtualNetworkId $virtualNetwork.Id
```

### <span data-ttu-id="45b0b-111">Exempel 2: ny Loadbalancer-adress config med IP-konfiguration Reference för klient delen</span><span class="sxs-lookup"><span data-stu-id="45b0b-111">Example 2: New loadbalancer address config with loadbalancer frontend ip configuration reference</span></span>
```powershell
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name $frontendName -PublicIpAddress $publicip
New-AzLoadBalancerBackendAddressConfig -LoadBalancerFrontendIPConfigurationId $frontend.Id -Name "TestLBFERef"
```

## <span data-ttu-id="45b0b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45b0b-112">PARAMETERS</span></span>

### <span data-ttu-id="45b0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b0b-113">-DefaultProfile</span></span>
<span data-ttu-id="45b0b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45b0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45b0b-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="45b0b-115">-IpAddress</span></span>
<span data-ttu-id="45b0b-116">Den IP-adress som ska läggas till i backend-poolen</span><span class="sxs-lookup"><span data-stu-id="45b0b-116">The IPAddress to add to the backend pool</span></span>

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

### <span data-ttu-id="45b0b-117">-LoadBalancerFrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="45b0b-117">-LoadBalancerFrontendIPConfigurationId</span></span>
<span data-ttu-id="45b0b-118">Belastningsutjämnarens IP-konfiguration för belastningsutjämnare med Server dels adress konfiguration</span><span class="sxs-lookup"><span data-stu-id="45b0b-118">The load balancer frontend ip configuration associated with Backend Address config</span></span>

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

### <span data-ttu-id="45b0b-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="45b0b-119">-Name</span></span>
<span data-ttu-id="45b0b-120">Namnet på Server delens konfiguration</span><span class="sxs-lookup"><span data-stu-id="45b0b-120">The name of the Backend Address config</span></span>

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

### <span data-ttu-id="45b0b-121">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="45b0b-121">-VirtualNetworkId</span></span>
<span data-ttu-id="45b0b-122">Det virtuella nätverk som är kopplat till Server dels adress konfiguration</span><span class="sxs-lookup"><span data-stu-id="45b0b-122">The virtual network associated with Backend Address config</span></span>

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

### <span data-ttu-id="45b0b-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45b0b-123">-Confirm</span></span>
<span data-ttu-id="45b0b-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45b0b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b0b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b0b-125">-WhatIf</span></span>
<span data-ttu-id="45b0b-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45b0b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45b0b-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45b0b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b0b-128">CommonParameters</span></span>
<span data-ttu-id="45b0b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45b0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b0b-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45b0b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b0b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45b0b-131">INPUTS</span></span>

### <span data-ttu-id="45b0b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="45b0b-132">System.String</span></span>

### <span data-ttu-id="45b0b-133">Microsoft. Azure. commands. Networks. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="45b0b-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="45b0b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45b0b-134">OUTPUTS</span></span>

### <span data-ttu-id="45b0b-135">Microsoft. Azure. commands. Networks. Models. PSLoadBalancerBackendAddress</span><span class="sxs-lookup"><span data-stu-id="45b0b-135">Microsoft.Azure.Commands.Network.Models.PSLoadBalancerBackendAddress</span></span>

## <span data-ttu-id="45b0b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45b0b-136">NOTES</span></span>

## <span data-ttu-id="45b0b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45b0b-137">RELATED LINKS</span></span>
