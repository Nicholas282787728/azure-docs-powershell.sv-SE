---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVpnClientIpsecParameter.md
ms.openlocfilehash: 658a242b724c57092bd155be69743f2080c07732
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523810"
---
# <span data-ttu-id="3d658-101">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d658-101">Set-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="3d658-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d658-102">SYNOPSIS</span></span>
<span data-ttu-id="3d658-103">Ställer in IPSec-parametrarna för VPN för befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d658-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

## <span data-ttu-id="3d658-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d658-104">SYNTAX</span></span>

### <span data-ttu-id="3d658-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3d658-105">ByFactoryName (Default)</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d658-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3d658-106">ByFactoryObject</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d658-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d658-107">ByResourceId</span></span>
```
Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d658-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d658-108">DESCRIPTION</span></span>
<span data-ttu-id="3d658-109">Cmdleten **set-AzVpnClientIpsecParameter** anger VPN-parametrarna för IPSec för befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d658-109">The **Set-AzVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="3d658-110">När en virtuell nätverksgateway skapas anger den uppsättningen med standard-IPSec-principer för VPN för gateway.</span><span class="sxs-lookup"><span data-stu-id="3d658-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="3d658-111">Om du till exempel vill använda en anpassad IPsec-princip för att ansluta till en VPN-gateway måste användaren ange IPSec-principen först.</span><span class="sxs-lookup"><span data-stu-id="3d658-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="3d658-112">**Set-AzVpnClientIpsecParameter** ger dig ett sätt att göra det.</span><span class="sxs-lookup"><span data-stu-id="3d658-112">**Set-AzVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="3d658-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d658-113">EXAMPLES</span></span>

### <span data-ttu-id="3d658-114">Exempel 1: anger en anpassad IPsec-princip för VPN till befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="3d658-114">Example 1: Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="3d658-115">I det här exemplet anges en anpassad VPN-princip till en befintlig virtuell nätverksgateway som heter ContosoVirtualGateway från resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d658-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="3d658-116">New-AzVpnClientIpsecParameter cmdlet används för att skapa IPsec-parametrar-objektet för att använda en eller alla parametrar-värden som användaren kan ange för en befintlig virtuell nätverksgateway i ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d658-116">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="3d658-117">Det här skapade VpnClientIPsecParameters-objektet skickas till Set-AzVpnClientIpsecParameter kommandot för att ange den angivna anpassade VPN-principen för IPSec på en virtuell nätverksgateway enligt exemplet ovan.</span><span class="sxs-lookup"><span data-stu-id="3d658-117">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="3d658-118">Det här kommandot returnerar ett objekt med VpnClientIPsecParameters som visar inställda parametrar.</span><span class="sxs-lookup"><span data-stu-id="3d658-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="3d658-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d658-119">PARAMETERS</span></span>

### <span data-ttu-id="3d658-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d658-120">-DefaultProfile</span></span>
<span data-ttu-id="3d658-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3d658-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d658-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d658-122">-InputObject</span></span>
<span data-ttu-id="3d658-123">Objektet virtuellt nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="3d658-123">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d658-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d658-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d658-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3d658-125">The resource group name.</span></span>

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

### <span data-ttu-id="3d658-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d658-126">-ResourceId</span></span>
<span data-ttu-id="3d658-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="3d658-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d658-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3d658-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3d658-129">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="3d658-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="3d658-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d658-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="3d658-131">IPsec-parametrar för VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="3d658-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="3d658-132">Det här parametervärdet kan konstrueras med hjälp av PS-kommando: ny-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d658-132">This parameter value can be constructed using PS command let:New-AzVpnClientIpsecParameter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d658-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d658-133">-Confirm</span></span>
<span data-ttu-id="3d658-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d658-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d658-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d658-135">-WhatIf</span></span>
<span data-ttu-id="3d658-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d658-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d658-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d658-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d658-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d658-138">CommonParameters</span></span>
<span data-ttu-id="3d658-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d658-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d658-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d658-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d658-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d658-141">INPUTS</span></span>

### <span data-ttu-id="3d658-142">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3d658-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

### <span data-ttu-id="3d658-143">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="3d658-143">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="3d658-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3d658-144">System.String</span></span>

## <span data-ttu-id="3d658-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d658-145">OUTPUTS</span></span>

### <span data-ttu-id="3d658-146">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="3d658-146">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="3d658-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d658-147">NOTES</span></span>

## <span data-ttu-id="3d658-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d658-148">RELATED LINKS</span></span>

[<span data-ttu-id="3d658-149">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d658-149">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="3d658-150">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d658-150">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="3d658-151">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="3d658-151">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)
