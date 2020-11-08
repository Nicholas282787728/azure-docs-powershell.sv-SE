---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecPolicy.md
ms.openlocfilehash: 028c33db36df5debb6f951f11e27f0586e7a21dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262536"
---
# <span data-ttu-id="21aea-101">New-AzVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="21aea-101">New-AzVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="21aea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21aea-102">SYNOPSIS</span></span>
<span data-ttu-id="21aea-103">Med det här kommandot kan användarna skapa IPSec-principobjektet för VPN och ange ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup för VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="21aea-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="21aea-104">Med det här kommandot kan output-objekt användas för att ställa in IPSec-principer för både ny/befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="21aea-104">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="21aea-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21aea-105">SYNTAX</span></span>

```
New-AzVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21aea-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21aea-106">DESCRIPTION</span></span>
<span data-ttu-id="21aea-107">Med det här kommandot kan användarna skapa IPSec-principobjektet för VPN och ange ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup för VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="21aea-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="21aea-108">Med det här kommandot kan output-objekt användas för att ställa in IPSec-principer för både ny/befintlig gateway.</span><span class="sxs-lookup"><span data-stu-id="21aea-108">This command let output object is used to set vpn ipsec policy for both new / existing gateway.</span></span>

## <span data-ttu-id="21aea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21aea-109">EXAMPLES</span></span>

### <span data-ttu-id="21aea-110">Exempel 1: definiera principobjektet för IPSec-principer:</span><span class="sxs-lookup"><span data-stu-id="21aea-110">Example 1: Define vpn ipsec policy object:</span></span>
```powershell
PS C:\>$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="21aea-111">Den här cmdleten används för att skapa IPSec-principobjektet för VPN med den överförda en eller alla parametrar-värden som användaren kan skicka till parametrar: VpnClientIpsecPolicy of PS-kommando: New-AzVirtualNetworkGateway (ny VPN-gateway skapas)/Set-AzVirtualNetworkGateway (befintlig VPN gateway-uppdatering) i ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="21aea-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzVirtualNetworkGateway (New VPN Gateway creation) / Set-AzVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="21aea-112">Exempel 2: skapa ny virtuell nätverksgateway med inställningar för anpassad IPsec-princip:</span><span class="sxs-lookup"><span data-stu-id="21aea-112">Example 2: Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```powershell
PS C:\> $vnetGateway = New-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="21aea-113">Denna cmdlet returnerar objektet virtuellt nätverksgateway när det har skapats.</span><span class="sxs-lookup"><span data-stu-id="21aea-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="21aea-114">Exempel 3: ange anpassad IPsec-princip på en befintlig virtuell nätverksgateway:</span><span class="sxs-lookup"><span data-stu-id="21aea-114">Example 3: Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```powershell
PS C:\> $vnetGateway = Set-AzVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="21aea-115">Denna cmdlet returnerar objektet virtuellt nätverk för gateway efter att du har angett den anpassade IPSec-principen.</span><span class="sxs-lookup"><span data-stu-id="21aea-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="21aea-116">Exempel 4: skaffa virtuell nätverksgateway för att se om den anpassade VPN-principen är korrekt:</span><span class="sxs-lookup"><span data-stu-id="21aea-116">Example 4: Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```powershell
PS C:\> $gateway = Get-AzVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="21aea-117">Denna cmdlet returnerar objektet virtuellt nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="21aea-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="21aea-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21aea-118">PARAMETERS</span></span>

### <span data-ttu-id="21aea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21aea-119">-DefaultProfile</span></span>
<span data-ttu-id="21aea-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21aea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21aea-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="21aea-121">-DhGroup</span></span>
<span data-ttu-id="21aea-122">VpnClient DH-grupper som används i IKE fas 1 för inledande SA</span><span class="sxs-lookup"><span data-stu-id="21aea-122">The VpnClient DH Groups used in IKE Phase 1 for initial SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DHGroup24, ECP384, ECP256, DHGroup14, DHGroup2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="21aea-123">-IkeEncryption</span></span>
<span data-ttu-id="21aea-124">VpnClient IKE-krypteringsalgoritm (IKE fas 2)</span><span class="sxs-lookup"><span data-stu-id="21aea-124">The VpnClient IKE encryption algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="21aea-125">-IkeIntegrity</span></span>
<span data-ttu-id="21aea-126">VpnClient IKE-integritetsalgoritm (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="21aea-126">The VpnClient IKE integrity algorithm (IKE Phase 2)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SHA384, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="21aea-127">-IpsecEncryption</span></span>
<span data-ttu-id="21aea-128">VpnClient IPSec-krypteringsalgoritm (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="21aea-128">The VpnClient IPSec encryption algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, AES256, AES128

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="21aea-129">-IpsecIntegrity</span></span>
<span data-ttu-id="21aea-130">IPSec-integritetsalgoritmen VpnClient (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="21aea-130">The VpnClient IPSec integrity algorithm (IKE Phase 1)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GCMAES256, GCMAES128, SHA256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="21aea-131">-PfsGroup</span></span>
<span data-ttu-id="21aea-132">VpnClient PFS-grupper som används i IKE fas 2 för ny underordnad SA</span><span class="sxs-lookup"><span data-stu-id="21aea-132">The VpnClient PFS Groups used in IKE Phase 2 for new child SA</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PFS24, PFSMM, ECP384, ECP256, PFS14, PFS2, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="21aea-133">-SADataSize</span></span>
<span data-ttu-id="21aea-134">VpnClient säkerhets Association för IPSec (kallas även för en nytto Last storlek i KB för snabb läge eller fas 2)</span><span class="sxs-lookup"><span data-stu-id="21aea-134">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="21aea-135">-SALifeTime</span></span>
<span data-ttu-id="21aea-136">VpnClient säkerhets Association för IPSec (kallas även för snabb läge eller fas 2 SA) i sekunder</span><span class="sxs-lookup"><span data-stu-id="21aea-136">The VpnClient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21aea-137">CommonParameters</span></span>
<span data-ttu-id="21aea-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21aea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21aea-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21aea-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21aea-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21aea-140">INPUTS</span></span>

### <span data-ttu-id="21aea-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="21aea-141">None</span></span>

## <span data-ttu-id="21aea-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21aea-142">OUTPUTS</span></span>

### <span data-ttu-id="21aea-143">Microsoft. Azure. commands. Networks. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="21aea-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="21aea-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21aea-144">NOTES</span></span>

## <span data-ttu-id="21aea-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21aea-145">RELATED LINKS</span></span>
