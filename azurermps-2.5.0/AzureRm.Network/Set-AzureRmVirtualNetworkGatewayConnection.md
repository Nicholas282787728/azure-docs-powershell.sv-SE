---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
ms.openlocfilehash: bb098e23f6e55cc28fcae02b7094a953c5179308
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930510"
---
# <span data-ttu-id="5fabe-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5fabe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fabe-102">SYNOPSIS</span></span>
<span data-ttu-id="5fabe-103">Konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5fabe-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fabe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fabe-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fabe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fabe-105">DESCRIPTION</span></span>
<span data-ttu-id="5fabe-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnection** konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5fabe-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="5fabe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fabe-107">EXAMPLES</span></span>

### <span data-ttu-id="5fabe-108">9.1</span><span class="sxs-lookup"><span data-stu-id="5fabe-108">1:</span></span>
```

```

## <span data-ttu-id="5fabe-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fabe-109">PARAMETERS</span></span>

### <span data-ttu-id="5fabe-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fabe-110">-AsJob</span></span>
<span data-ttu-id="5fabe-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5fabe-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fabe-112">-DefaultProfile</span></span>
<span data-ttu-id="5fabe-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5fabe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="5fabe-114">-EnableBgp</span></span>
<span data-ttu-id="5fabe-115">Om en BGP-session ska användas över en VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="5fabe-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5fabe-116">-Force</span></span>
<span data-ttu-id="5fabe-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5fabe-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="5fabe-118">-IpsecPolicies</span></span>
<span data-ttu-id="5fabe-119">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="5fabe-119">A list of IPSec policies.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="5fabe-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="5fabe-121">Om du ska använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="5fabe-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="5fabe-123">Anger det PSVirtualNetworkGatewayConnection-objekt som denna cmdlet använder för att ändra anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="5fabe-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5fabe-124">-Confirm</span></span>
<span data-ttu-id="5fabe-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5fabe-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fabe-126">-WhatIf</span></span>
<span data-ttu-id="5fabe-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5fabe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fabe-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5fabe-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fabe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fabe-129">CommonParameters</span></span>
<span data-ttu-id="5fabe-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fabe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fabe-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fabe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fabe-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fabe-132">INPUTS</span></span>

### <span data-ttu-id="5fabe-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="5fabe-134">Parametern ' VirtualNetworkGatewayConnection ' godkänner värdet av typen ' PSVirtualNetworkGatewayConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5fabe-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="5fabe-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fabe-135">OUTPUTS</span></span>

### <span data-ttu-id="5fabe-136">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="5fabe-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fabe-137">NOTES</span></span>

## <span data-ttu-id="5fabe-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fabe-138">RELATED LINKS</span></span>

[<span data-ttu-id="5fabe-139">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-139">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5fabe-140">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-140">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="5fabe-141">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5fabe-141">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


