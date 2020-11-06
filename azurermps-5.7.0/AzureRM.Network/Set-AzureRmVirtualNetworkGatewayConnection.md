---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 218ef3115a4bc8325bc4dda37ae0a5e5820afae2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575607"
---
# <span data-ttu-id="d983b-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d983b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d983b-102">SYNOPSIS</span></span>
<span data-ttu-id="d983b-103">Konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="d983b-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d983b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d983b-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d983b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d983b-105">DESCRIPTION</span></span>
<span data-ttu-id="d983b-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnection** konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="d983b-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="d983b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d983b-107">EXAMPLES</span></span>

## <span data-ttu-id="d983b-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d983b-108">PARAMETERS</span></span>

### <span data-ttu-id="d983b-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d983b-109">-AsJob</span></span>
<span data-ttu-id="d983b-110">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d983b-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d983b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d983b-111">-DefaultProfile</span></span>
<span data-ttu-id="d983b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d983b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d983b-113">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="d983b-113">-EnableBgp</span></span>
<span data-ttu-id="d983b-114">Om en BGP-session ska användas över en VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="d983b-114">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="d983b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d983b-115">-Force</span></span>
<span data-ttu-id="d983b-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d983b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d983b-117">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="d983b-117">-IpsecPolicies</span></span>
<span data-ttu-id="d983b-118">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="d983b-118">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="d983b-119">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="d983b-119">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="d983b-120">Om du ska använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="d983b-120">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="d983b-121">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-121">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="d983b-122">Anger det PSVirtualNetworkGatewayConnection-objekt som denna cmdlet använder för att ändra anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="d983b-122">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="d983b-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d983b-123">-Confirm</span></span>
<span data-ttu-id="d983b-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d983b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d983b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d983b-125">-WhatIf</span></span>
<span data-ttu-id="d983b-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d983b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d983b-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d983b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d983b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d983b-128">CommonParameters</span></span>
<span data-ttu-id="d983b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d983b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d983b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d983b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d983b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d983b-131">INPUTS</span></span>

### <span data-ttu-id="d983b-132">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-132">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="d983b-133">Parametern ' VirtualNetworkGatewayConnection ' godkänner värdet av typen ' PSVirtualNetworkGatewayConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d983b-133">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="d983b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d983b-134">OUTPUTS</span></span>

### <span data-ttu-id="d983b-135">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="d983b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d983b-136">NOTES</span></span>

## <span data-ttu-id="d983b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d983b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d983b-138">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-138">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d983b-139">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-139">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="d983b-140">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="d983b-140">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


