---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVpnClientIpsecParameter.md
ms.openlocfilehash: 38dcfdb1188a810b0f154dfed31f8a1ef3206247
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578868"
---
# <span data-ttu-id="0d0a2-101">Set-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="0d0a2-101">Set-AzureRmVpnClientIpsecParameter</span></span>

## <span data-ttu-id="0d0a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0a2-103">Ställer in IPSec-parametrarna för VPN för befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-103">Sets the vpn ipsec parameters for existing virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d0a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d0a2-104">SYNTAX</span></span>

### <span data-ttu-id="0d0a2-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="0d0a2-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0a2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0d0a2-106">ByFactoryObject</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0a2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0d0a2-107">ByResourceId</span></span>
```
Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -VpnClientIPsecParameter <PSVpnClientIPsecParameters> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d0a2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d0a2-108">DESCRIPTION</span></span>
<span data-ttu-id="0d0a2-109">Cmdleten **set-AzureRmVpnClientIpsecParameter** anger VPN-parametrarna för IPSec för befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-109">The **Set-AzureRmVpnClientIpsecParameter** cmdlet sets the vpn ipsec parameters for existing virtual network gateway.</span></span>
<span data-ttu-id="0d0a2-110">När en virtuell nätverksgateway skapas anger den uppsättningen med standard-IPSec-principer för VPN för gateway.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-110">When Virtual network gateway is created, it sets the set of default vpn ipsec policies on Gateway.</span></span> <span data-ttu-id="0d0a2-111">Om du till exempel vill använda en anpassad IPsec-princip för att ansluta till en VPN-gateway måste användaren ange IPSec-principen först.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-111">In case, Point to site user wants to use certain custom ipsec policy to connect to VPN Gateway, user has to set that ipsec policy on VPN Gateway first.</span></span> <span data-ttu-id="0d0a2-112">**Set-AzureRmVpnClientIpsecParameter** ger dig ett sätt att göra det.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-112">**Set-AzureRmVpnClientIpsecParameter** provides a way to do that.</span></span>

## <span data-ttu-id="0d0a2-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d0a2-113">EXAMPLES</span></span>

### <span data-ttu-id="0d0a2-114">Exempel 1: anger en anpassad IPsec-princip för VPN till befintlig virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-114">Example 1 : Sets a custom vpn ipsec policy to existing virtual network gateway.</span></span>
```powershell
PS C:\>$vpnclientipsecparams = New-AzureRmVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzureRmVpnClientIpsecParameter -VirtualNetworkGatewayName "ContosoLocalGateway" -ResourceGroupName "ContosoResourceGroup" -VpnClientIPsecParameter $vpnclientipsecparams
```

<span data-ttu-id="0d0a2-115">I det här exemplet anges en anpassad VPN-princip till en befintlig virtuell nätverksgateway som heter ContosoVirtualGateway från resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-115">This example sets custom vpn ipsec policy to existing virtual network gateway named ContosoVirtualGateway from Resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="0d0a2-116">New-AzureRmVpnClientIpsecParameter cmdlet används för att skapa IPsec-parametrar-objektet för att använda en eller alla parametrar-värden som användaren kan ange för en befintlig virtuell nätverksgateway i ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-116">New-AzureRmVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="0d0a2-117">Det här skapade VpnClientIPsecParameters-objektet skickas till Set-AzureRmVpnClientIpsecParameter kommandot för att ange den angivna anpassade VPN-principen för IPSec på en virtuell nätverksgateway enligt exemplet ovan.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-117">This created VpnClientIPsecParameters object is passed to Set-AzureRmVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="0d0a2-118">Det här kommandot returnerar ett objekt med VpnClientIPsecParameters som visar inställda parametrar.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-118">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="0d0a2-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d0a2-119">PARAMETERS</span></span>

### <span data-ttu-id="0d0a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0a2-120">-DefaultProfile</span></span>
<span data-ttu-id="0d0a2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d0a2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d0a2-122">-InputObject</span></span>
<span data-ttu-id="0d0a2-123">Objektet Gateaway virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="0d0a2-123">The virtual network gateaway object</span></span>

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

### <span data-ttu-id="0d0a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d0a2-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-125">The resource group name.</span></span>

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

### <span data-ttu-id="0d0a2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d0a2-126">-ResourceId</span></span>
<span data-ttu-id="0d0a2-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0d0a2-128">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0d0a2-128">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0d0a2-129">Namnet på den virtuella Nätverksgatewayen.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-129">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="0d0a2-130">-VpnClientIPsecParameter</span><span class="sxs-lookup"><span data-stu-id="0d0a2-130">-VpnClientIPsecParameter</span></span>
<span data-ttu-id="0d0a2-131">IPsec-parametrar för VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-131">Vpn client ipsec parameters.</span></span> <span data-ttu-id="0d0a2-132">Det här parametervärdet kan konstrueras med hjälp av PS-kommando: ny-AzureRmVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="0d0a2-132">This parameter value can be constructed using PS command let:New-AzureRmVpnClientIpsecParameter</span></span>

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

### <span data-ttu-id="0d0a2-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d0a2-133">-Confirm</span></span>
<span data-ttu-id="0d0a2-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d0a2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d0a2-135">-WhatIf</span></span>
<span data-ttu-id="0d0a2-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d0a2-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d0a2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0a2-138">CommonParameters</span></span>
<span data-ttu-id="0d0a2-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d0a2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0a2-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d0a2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0a2-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d0a2-141">INPUTS</span></span>

### <span data-ttu-id="0d0a2-142">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0d0a2-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>
<span data-ttu-id="0d0a2-143">Parametrar: VpnClientIPsecParameter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d0a2-143">Parameters: VpnClientIPsecParameter (ByValue)</span></span>

### <span data-ttu-id="0d0a2-144">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="0d0a2-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="0d0a2-145">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d0a2-145">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0d0a2-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0d0a2-146">System.String</span></span>

## <span data-ttu-id="0d0a2-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d0a2-147">OUTPUTS</span></span>

### <span data-ttu-id="0d0a2-148">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0d0a2-148">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="0d0a2-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d0a2-149">NOTES</span></span>

## <span data-ttu-id="0d0a2-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d0a2-150">RELATED LINKS</span></span>

[<span data-ttu-id="0d0a2-151">New-AzureRmVpnClientIpsecParameters</span><span class="sxs-lookup"><span data-stu-id="0d0a2-151">New-AzureRmVpnClientIpsecParameters</span></span>](./New-AzureRmVpnClientIpsecParameters.md)
