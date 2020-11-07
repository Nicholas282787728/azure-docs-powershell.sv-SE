---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: b38ef9d212ceeb519e29d99391b17099177236a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924150"
---
# <span data-ttu-id="564fd-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="564fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="564fd-102">SYNOPSIS</span></span>
<span data-ttu-id="564fd-103">Konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="564fd-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="564fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="564fd-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="564fd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="564fd-105">DESCRIPTION</span></span>
<span data-ttu-id="564fd-106">Cmdleten **set-AzVirtualNetworkGatewayConnection** konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="564fd-106">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="564fd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="564fd-107">EXAMPLES</span></span>

### <span data-ttu-id="564fd-108">9.1</span><span class="sxs-lookup"><span data-stu-id="564fd-108">1:</span></span>
```

```

## <span data-ttu-id="564fd-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="564fd-109">PARAMETERS</span></span>

### <span data-ttu-id="564fd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="564fd-110">-AsJob</span></span>
<span data-ttu-id="564fd-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="564fd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="564fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564fd-112">-DefaultProfile</span></span>
<span data-ttu-id="564fd-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="564fd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="564fd-114">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="564fd-114">-EnableBgp</span></span>
<span data-ttu-id="564fd-115">Om en BGP-session ska användas över en VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="564fd-115">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="564fd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="564fd-116">-Force</span></span>
<span data-ttu-id="564fd-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="564fd-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="564fd-118">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="564fd-118">-IpsecPolicies</span></span>
<span data-ttu-id="564fd-119">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="564fd-119">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="564fd-120">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="564fd-120">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="564fd-121">Om du ska använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="564fd-121">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="564fd-122">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-122">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="564fd-123">Anger det PSVirtualNetworkGatewayConnection-objekt som denna cmdlet använder för att ändra anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="564fd-123">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="564fd-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="564fd-124">-Confirm</span></span>
<span data-ttu-id="564fd-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="564fd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="564fd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="564fd-126">-WhatIf</span></span>
<span data-ttu-id="564fd-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="564fd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="564fd-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="564fd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="564fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564fd-129">CommonParameters</span></span>
<span data-ttu-id="564fd-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="564fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564fd-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="564fd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564fd-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="564fd-132">INPUTS</span></span>

### <span data-ttu-id="564fd-133">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-133">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="564fd-134">Parametern ' VirtualNetworkGatewayConnection ' godkänner värdet av typen ' PSVirtualNetworkGatewayConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="564fd-134">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="564fd-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="564fd-135">OUTPUTS</span></span>

### <span data-ttu-id="564fd-136">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="564fd-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="564fd-137">NOTES</span></span>

## <span data-ttu-id="564fd-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="564fd-138">RELATED LINKS</span></span>

[<span data-ttu-id="564fd-139">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-139">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="564fd-140">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-140">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="564fd-141">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="564fd-141">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


