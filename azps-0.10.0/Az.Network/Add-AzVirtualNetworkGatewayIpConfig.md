---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 31790ead292c9146aa73f41c56e79f3bdf51c715
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922377"
---
# <span data-ttu-id="93ffd-101">Add-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="93ffd-101">Add-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="93ffd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="93ffd-103">Lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="93ffd-103">Adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="93ffd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93ffd-104">SYNTAX</span></span>

### <span data-ttu-id="93ffd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="93ffd-105">SetByResourceId</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ffd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="93ffd-106">SetByResource</span></span>
```
Add-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ffd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93ffd-107">DESCRIPTION</span></span>
<span data-ttu-id="93ffd-108">Cmdleten **Add-AzVirtualNetworkGatewayIpConfig** lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="93ffd-108">The **Add-AzVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="93ffd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93ffd-109">EXAMPLES</span></span>

### <span data-ttu-id="93ffd-110">9.1</span><span class="sxs-lookup"><span data-stu-id="93ffd-110">1:</span></span>
```

```

## <span data-ttu-id="93ffd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93ffd-111">PARAMETERS</span></span>

### <span data-ttu-id="93ffd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ffd-112">-DefaultProfile</span></span>
<span data-ttu-id="93ffd-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="93ffd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ffd-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="93ffd-114">-Name</span></span>
<span data-ttu-id="93ffd-115">Anger namnet på gatewayens IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="93ffd-115">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="93ffd-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="93ffd-116">-PrivateIpAddress</span></span>
<span data-ttu-id="93ffd-117">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="93ffd-117">Specifies the private IP address.</span></span>

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

### <span data-ttu-id="93ffd-118">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="93ffd-118">-PublicIpAddress</span></span>
<span data-ttu-id="93ffd-119">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="93ffd-119">Specifies the public IP address.</span></span>

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

### <span data-ttu-id="93ffd-120">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="93ffd-120">-PublicIpAddressId</span></span>
<span data-ttu-id="93ffd-121">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="93ffd-121">Specifies the ID of the public IP address.</span></span>

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

### <span data-ttu-id="93ffd-122">-Undernät</span><span class="sxs-lookup"><span data-stu-id="93ffd-122">-Subnet</span></span>
<span data-ttu-id="93ffd-123">Anger ett **PSSubnet** -objekt.</span><span class="sxs-lookup"><span data-stu-id="93ffd-123">Specifies a **PSSubnet** object.</span></span>

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

### <span data-ttu-id="93ffd-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="93ffd-124">-SubnetId</span></span>
<span data-ttu-id="93ffd-125">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="93ffd-125">Specifies the ID of the subnet.</span></span>

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

### <span data-ttu-id="93ffd-126">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="93ffd-126">-VirtualNetworkGateway</span></span>
<span data-ttu-id="93ffd-127">Anger ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="93ffd-127">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="93ffd-128">Denna cmdlet ändrar det **PSVirtualNetworkGateway** -objekt som du anger.</span><span class="sxs-lookup"><span data-stu-id="93ffd-128">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="93ffd-129">Du kan använda Get-AzVirtualNetworkGateway cmdlet för att hämta ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="93ffd-129">You can use the Get-AzVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

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

### <span data-ttu-id="93ffd-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="93ffd-130">-Confirm</span></span>
<span data-ttu-id="93ffd-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="93ffd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ffd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ffd-132">-WhatIf</span></span>
<span data-ttu-id="93ffd-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="93ffd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ffd-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="93ffd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ffd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ffd-135">CommonParameters</span></span>
<span data-ttu-id="93ffd-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ffd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ffd-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ffd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ffd-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93ffd-138">INPUTS</span></span>

### <span data-ttu-id="93ffd-139">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="93ffd-139">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="93ffd-140">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="93ffd-140">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="93ffd-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93ffd-141">OUTPUTS</span></span>

### <span data-ttu-id="93ffd-142">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="93ffd-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="93ffd-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93ffd-143">NOTES</span></span>

## <span data-ttu-id="93ffd-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93ffd-144">RELATED LINKS</span></span>

[<span data-ttu-id="93ffd-145">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="93ffd-145">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="93ffd-146">New-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="93ffd-146">New-AzVirtualNetworkGatewayIpConfig</span></span>](./New-AzVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="93ffd-147">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="93ffd-147">Remove-AzVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzVirtualNetworkGatewayIpConfig.md)


