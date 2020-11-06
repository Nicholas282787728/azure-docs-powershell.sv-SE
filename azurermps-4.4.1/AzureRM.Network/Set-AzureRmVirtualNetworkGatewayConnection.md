---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 5885f98d66e6226273215dcde856f5fc50d0bd56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575952"
---
# <span data-ttu-id="c954e-101">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-101">Set-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c954e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c954e-102">SYNOPSIS</span></span>
<span data-ttu-id="c954e-103">Konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c954e-103">Configures a virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c954e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c954e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>]
 [-IpsecPolicies <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c954e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c954e-105">DESCRIPTION</span></span>
<span data-ttu-id="c954e-106">Cmdleten **set-AzureRmVirtualNetworkGatewayConnection** konfigurerar en anslutning till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c954e-106">The **Set-AzureRmVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="c954e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c954e-107">EXAMPLES</span></span>

## <span data-ttu-id="c954e-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c954e-108">PARAMETERS</span></span>

### <span data-ttu-id="c954e-109">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="c954e-109">-EnableBgp</span></span>
<span data-ttu-id="c954e-110">Om en BGP-session ska användas över en VPN-tunnel för S2S</span><span class="sxs-lookup"><span data-stu-id="c954e-110">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c954e-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c954e-111">-Force</span></span>
<span data-ttu-id="c954e-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c954e-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c954e-113">-IpsecPolicies</span><span class="sxs-lookup"><span data-stu-id="c954e-113">-IpsecPolicies</span></span>
<span data-ttu-id="c954e-114">En lista över IPSec-principer.</span><span class="sxs-lookup"><span data-stu-id="c954e-114">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="c954e-115">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="c954e-115">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="c954e-116">Om du ska använda principbaserad Traffic Selector för en S2S-anslutning</span><span class="sxs-lookup"><span data-stu-id="c954e-116">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c954e-117">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-117">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="c954e-118">Anger det PSVirtualNetworkGatewayConnection-objekt som denna cmdlet använder för att ändra anslutningen för den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c954e-118">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c954e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c954e-119">-Confirm</span></span>
<span data-ttu-id="c954e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c954e-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c954e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c954e-121">-WhatIf</span></span>
<span data-ttu-id="c954e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c954e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c954e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c954e-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c954e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c954e-124">-DefaultProfile</span></span>
<span data-ttu-id="c954e-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c954e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c954e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c954e-126">CommonParameters</span></span>
<span data-ttu-id="c954e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c954e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c954e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c954e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c954e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c954e-129">INPUTS</span></span>

### <span data-ttu-id="c954e-130">PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-130">PSVirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="c954e-131">Parametern ' VirtualNetworkGatewayConnection ' godkänner värdet av typen ' PSVirtualNetworkGatewayConnection ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c954e-131">Parameter 'VirtualNetworkGatewayConnection' accepts value of type 'PSVirtualNetworkGatewayConnection' from the pipeline</span></span>

## <span data-ttu-id="c954e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c954e-132">OUTPUTS</span></span>

### <span data-ttu-id="c954e-133">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c954e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c954e-134">NOTES</span></span>

## <span data-ttu-id="c954e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c954e-135">RELATED LINKS</span></span>

[<span data-ttu-id="c954e-136">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-136">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c954e-137">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-137">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c954e-138">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c954e-138">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>](./Remove-AzureRmVirtualNetworkGatewayConnection.md)


