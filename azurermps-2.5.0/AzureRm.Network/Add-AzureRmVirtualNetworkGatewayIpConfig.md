---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: 340baa4b7a7d0afaf0e0523cb8c2f14f8270bf7c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931365"
---
# <span data-ttu-id="c1573-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1573-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="c1573-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1573-102">SYNOPSIS</span></span>
<span data-ttu-id="c1573-103">Lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c1573-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1573-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1573-104">SYNTAX</span></span>

### <span data-ttu-id="c1573-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1573-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1573-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1573-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1573-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1573-107">DESCRIPTION</span></span>
<span data-ttu-id="c1573-108">Cmdleten **Add-AzureRmVirtualNetworkGatewayIpConfig** lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="c1573-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="c1573-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1573-109">EXAMPLES</span></span>

### <span data-ttu-id="c1573-110">9.1</span><span class="sxs-lookup"><span data-stu-id="c1573-110">1:</span></span>
```

```

## <span data-ttu-id="c1573-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1573-111">PARAMETERS</span></span>

### <span data-ttu-id="c1573-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1573-112">-DefaultProfile</span></span>
<span data-ttu-id="c1573-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1573-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1573-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1573-114">-Name</span></span>
<span data-ttu-id="c1573-115">Anger namnet på gatewayens IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="c1573-115">Specifies the name of the gateway IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1573-116">-PrivateIpAddress</span></span>
<span data-ttu-id="c1573-117">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="c1573-117">Specifies the private IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1573-118">-PublicIpAddress</span></span>
<span data-ttu-id="c1573-119">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="c1573-119">Specifies the public IP address.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="c1573-120">-PublicIpAddressId</span></span>
<span data-ttu-id="c1573-121">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="c1573-121">Specifies the ID of the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-122">-Undernät</span><span class="sxs-lookup"><span data-stu-id="c1573-122">-Subnet</span></span>
<span data-ttu-id="c1573-123">Anger ett **PSSubnet** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c1573-123">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c1573-124">-SubnetId</span></span>
<span data-ttu-id="c1573-125">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="c1573-125">Specifies the ID of the subnet.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1573-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="c1573-127">Anger ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c1573-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="c1573-128">Denna cmdlet ändrar det **PSVirtualNetworkGateway** -objekt som du anger.</span><span class="sxs-lookup"><span data-stu-id="c1573-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="c1573-129">Du kan använda Get-AzureRmVirtualNetworkGateway cmdlet för att hämta ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c1573-129">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1573-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1573-130">-Confirm</span></span>
<span data-ttu-id="c1573-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1573-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1573-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1573-132">-WhatIf</span></span>
<span data-ttu-id="c1573-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1573-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1573-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1573-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1573-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1573-135">CommonParameters</span></span>
<span data-ttu-id="c1573-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1573-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1573-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1573-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1573-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1573-138">INPUTS</span></span>

### <span data-ttu-id="c1573-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1573-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="c1573-140">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c1573-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="c1573-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1573-141">OUTPUTS</span></span>

### <span data-ttu-id="c1573-142">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1573-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="c1573-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1573-143">NOTES</span></span>

## <span data-ttu-id="c1573-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1573-144">RELATED LINKS</span></span>

[<span data-ttu-id="c1573-145">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c1573-145">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="c1573-146">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1573-146">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="c1573-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c1573-147">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


