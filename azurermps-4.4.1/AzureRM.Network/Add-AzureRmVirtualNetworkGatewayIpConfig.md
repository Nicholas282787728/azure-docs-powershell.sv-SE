---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BCB64535-FF37-46EF-85AF-7286BB67787B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 08dc5728e13423fdd9e05c5d5b5d843b963c4aa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582331"
---
# <span data-ttu-id="4a61a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a61a-101">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="4a61a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a61a-102">SYNOPSIS</span></span>
<span data-ttu-id="4a61a-103">Lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="4a61a-103">Adds an IP configuration to a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a61a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a61a-104">SYNTAX</span></span>

### <span data-ttu-id="4a61a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a61a-105">SetByResourceId</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a61a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4a61a-106">SetByResource</span></span>
```
Add-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-PrivateIpAddress <String>] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a61a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a61a-107">DESCRIPTION</span></span>
<span data-ttu-id="4a61a-108">Cmdleten **Add-AzureRmVirtualNetworkGatewayIpConfig** lägger till en IP-konfiguration till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="4a61a-108">The **Add-AzureRmVirtualNetworkGatewayIpConfig** cmdlet adds an IP configuration to a virtual network gateway.</span></span>

## <span data-ttu-id="4a61a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a61a-109">EXAMPLES</span></span>

## <span data-ttu-id="4a61a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a61a-110">PARAMETERS</span></span>

### <span data-ttu-id="4a61a-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a61a-111">-Name</span></span>
<span data-ttu-id="4a61a-112">Anger namnet på gatewayens IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="4a61a-112">Specifies the name of the gateway IP configuration to add.</span></span>

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

### <span data-ttu-id="4a61a-113">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a61a-113">-PrivateIpAddress</span></span>
<span data-ttu-id="4a61a-114">Anger den privata IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="4a61a-114">Specifies the private IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a61a-115">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4a61a-115">-PublicIpAddress</span></span>
<span data-ttu-id="4a61a-116">Anger den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="4a61a-116">Specifies the public IP address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a61a-117">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4a61a-117">-PublicIpAddressId</span></span>
<span data-ttu-id="4a61a-118">Anger ID för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="4a61a-118">Specifies the ID of the public IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a61a-119">-Undernät</span><span class="sxs-lookup"><span data-stu-id="4a61a-119">-Subnet</span></span>
<span data-ttu-id="4a61a-120">Anger ett **PSSubnet** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4a61a-120">Specifies a **PSSubnet** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a61a-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4a61a-121">-SubnetId</span></span>
<span data-ttu-id="4a61a-122">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="4a61a-122">Specifies the ID of the subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a61a-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a61a-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="4a61a-124">Anger ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4a61a-124">Specifies a **PSVirtualNetworkGateway** object.</span></span>
<span data-ttu-id="4a61a-125">Denna cmdlet ändrar det **PSVirtualNetworkGateway** -objekt som du anger.</span><span class="sxs-lookup"><span data-stu-id="4a61a-125">This cmdlet modifies the **PSVirtualNetworkGateway** object that you specify.</span></span>
<span data-ttu-id="4a61a-126">Du kan använda Get-AzureRmVirtualNetworkGateway cmdlet för att hämta ett **PSVirtualNetworkGateway** -objekt.</span><span class="sxs-lookup"><span data-stu-id="4a61a-126">You can use the Get-AzureRmVirtualNetworkGateway cmdlet to retrieve a **PSVirtualNetworkGateway** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a61a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a61a-127">-Confirm</span></span>
<span data-ttu-id="4a61a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a61a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a61a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a61a-129">-WhatIf</span></span>
<span data-ttu-id="4a61a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a61a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a61a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a61a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a61a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a61a-132">-DefaultProfile</span></span>
<span data-ttu-id="4a61a-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a61a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a61a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a61a-134">CommonParameters</span></span>
<span data-ttu-id="4a61a-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a61a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a61a-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a61a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a61a-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a61a-137">INPUTS</span></span>

### <span data-ttu-id="4a61a-138">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a61a-138">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="4a61a-139">Parametern ' VirtualNetworkGateway ' godkänner värdet av typen ' PSVirtualNetworkGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4a61a-139">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="4a61a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a61a-140">OUTPUTS</span></span>

### <span data-ttu-id="4a61a-141">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a61a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="4a61a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a61a-142">NOTES</span></span>

## <span data-ttu-id="4a61a-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a61a-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a61a-144">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4a61a-144">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="4a61a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a61a-145">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./New-AzureRmVirtualNetworkGatewayIpConfig.md)

[<span data-ttu-id="4a61a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a61a-146">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>](./Remove-AzureRmVirtualNetworkGatewayIpConfig.md)


