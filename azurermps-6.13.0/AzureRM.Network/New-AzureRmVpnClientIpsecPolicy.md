---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientipsecpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientIpsecPolicy.md
ms.openlocfilehash: 98ea39141614c800b7b71d2f0c75519762bb87b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584908"
---
# <span data-ttu-id="52861-101">New-AzureRmVpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="52861-101">New-AzureRmVpnClientIpsecPolicy</span></span>

## <span data-ttu-id="52861-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52861-102">SYNOPSIS</span></span>
<span data-ttu-id="52861-103">Med det här kommandot kan användarna skapa IPSec-principobjektet för VPN och ange ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup för VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="52861-103">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="52861-104">Med det här kommandot kan output-objekt användas för att ställa in IPSec-principer för VPN för både nya/befintliga Gateway.</span><span class="sxs-lookup"><span data-stu-id="52861-104">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52861-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52861-105">SYNTAX</span></span>

```
New-AzureRmVpnClientIpsecPolicy [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52861-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52861-106">DESCRIPTION</span></span>
<span data-ttu-id="52861-107">Med det här kommandot kan användarna skapa IPSec-principobjektet för VPN och ange ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup för VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="52861-107">This command allows the users to create the Vpn ipsec policy object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the VPN gateway.</span></span> <span data-ttu-id="52861-108">Med det här kommandot kan output-objekt användas för att ställa in IPSec-principer för VPN för både nya/befintliga Gateway.</span><span class="sxs-lookup"><span data-stu-id="52861-108">This command let output object is used to set vpn ipsec policy for both new / exisitng gateway.</span></span>

## <span data-ttu-id="52861-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52861-109">EXAMPLES</span></span>

### <span data-ttu-id="52861-110">Definiera principobjektet för VPN-IPSec:</span><span class="sxs-lookup"><span data-stu-id="52861-110">Define vpn ipsec policy object:</span></span>
```
PS C:\>$vpnclientipsecpolicy = New-AzureRmVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86472 -SADataSize 429497 -IkeEncryption AES256 -IkeIntegrity SHA256 -DhGroup DHGroup2 -PfsGroup None
```

<span data-ttu-id="52861-111">Den här cmdleten används för att skapa IPSec-principobjektet för VPN med den överförda en eller alla parametrar-värden som användaren kan skicka till parametrar: VpnClientIpsecPolicy of PS-kommando: New-AzureRmVirtualNetworkGateway (ny VPN-gateway skapas)/Set-AzureRmVirtualNetworkGateway (befintlig VPN gateway-uppdatering) i ResourceGroup:</span><span class="sxs-lookup"><span data-stu-id="52861-111">This cmdlet is used to create the vpn ipsec policy object using the passed one or all parameters' values which user can pass to param:VpnClientIpsecPolicy of PS command let: New-AzureRmVirtualNetworkGateway (New VPN Gateway creation) / Set-AzureRmVirtualNetworkGateway (existing VPN Gateway update) in ResourceGroup :</span></span>

### <span data-ttu-id="52861-112">Skapa en ny virtuell nätverksgateway med att ange en anpassad IPsec-princip:</span><span class="sxs-lookup"><span data-stu-id="52861-112">Create new virtual network gateway with setting vpn custom ipsec policy:</span></span>
```
PS C:\> $vnetGateway = New-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -GatewaySku VpnGw1 -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="52861-113">Denna cmdlet returnerar objektet virtuellt nätverksgateway när det har skapats.</span><span class="sxs-lookup"><span data-stu-id="52861-113">This cmdlet returns virtual network gateway object after creation.</span></span> 

### <span data-ttu-id="52861-114">Konfigurera en anpassad IPsec-princip på en befintlig virtuell nätverksgateway:</span><span class="sxs-lookup"><span data-stu-id="52861-114">Set vpn custom ipsec policy on existing virtual network gateway:</span></span>
```
PS C:\> $vnetGateway = Set-AzureRmVirtualNetworkGateway -VirtualNetworkGateway $gateway -VpnClientIpsecPolicy $vpnclientipsecpolicy
```

<span data-ttu-id="52861-115">Denna cmdlet returnerar objektet virtuellt nätverk för gateway efter att du har angett den anpassade IPSec-principen.</span><span class="sxs-lookup"><span data-stu-id="52861-115">This cmdlet returns virtual network gateway object after setting vpn custom ipsec policy.</span></span>

### <span data-ttu-id="52861-116">Skaffa virtuell nätverksgateway för att se om den anpassade VPN-principen är korrekt:</span><span class="sxs-lookup"><span data-stu-id="52861-116">Get virtual network gateway to see if vpn custom policy is set correctly:</span></span>
```
PS C:\> $gateway = Get-AzureRmVirtualNetworkGateway -ResourceGroupName vnet-gateway -name myNGW
```

<span data-ttu-id="52861-117">Denna cmdlet returnerar objektet virtuellt nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="52861-117">This cmdlet returns virtual network gateway object.</span></span>

## <span data-ttu-id="52861-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52861-118">PARAMETERS</span></span>

### <span data-ttu-id="52861-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52861-119">-DefaultProfile</span></span>
<span data-ttu-id="52861-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52861-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52861-121">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="52861-121">-DhGroup</span></span>
<span data-ttu-id="52861-122">Vpnclient DH-grupper som används i IKE fas 1 för inledande SA</span><span class="sxs-lookup"><span data-stu-id="52861-122">The Vpnclient DH Groups used in IKE Phase 1 for initial SA</span></span>

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

### <span data-ttu-id="52861-123">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="52861-123">-IkeEncryption</span></span>
<span data-ttu-id="52861-124">Vpnclient IKE-krypteringsalgoritm (IKE fas 2)</span><span class="sxs-lookup"><span data-stu-id="52861-124">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="52861-125">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="52861-125">-IkeIntegrity</span></span>
<span data-ttu-id="52861-126">Vpnclient IKE-integritetsalgoritm (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="52861-126">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="52861-127">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="52861-127">-IpsecEncryption</span></span>
<span data-ttu-id="52861-128">Vpnclient IPSec-krypteringsalgoritm (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="52861-128">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="52861-129">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="52861-129">-IpsecIntegrity</span></span>
<span data-ttu-id="52861-130">IPSec-integritetsalgoritmen Vpnclient (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="52861-130">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="52861-131">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="52861-131">-PfsGroup</span></span>
<span data-ttu-id="52861-132">Vpnclient PFS-grupper som används i IKE fas 2 för ny underordnad SA</span><span class="sxs-lookup"><span data-stu-id="52861-132">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="52861-133">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="52861-133">-SADataSize</span></span>
<span data-ttu-id="52861-134">Vpnclient säkerhets Association för IPSec (kallas även för en nytto Last storlek i KB för snabb läge eller fas 2)</span><span class="sxs-lookup"><span data-stu-id="52861-134">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="52861-135">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="52861-135">-SALifeTime</span></span>
<span data-ttu-id="52861-136">Vpnclient säkerhets Association för IPSec (kallas även för snabb läge eller fas 2 SA) i sekunder</span><span class="sxs-lookup"><span data-stu-id="52861-136">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="52861-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52861-137">CommonParameters</span></span>
<span data-ttu-id="52861-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52861-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52861-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52861-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52861-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52861-140">INPUTS</span></span>

### <span data-ttu-id="52861-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="52861-141">None</span></span>

## <span data-ttu-id="52861-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52861-142">OUTPUTS</span></span>

### <span data-ttu-id="52861-143">Microsoft. Azure. commands. Networks. Models. PSIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="52861-143">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy</span></span>

## <span data-ttu-id="52861-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52861-144">NOTES</span></span>

## <span data-ttu-id="52861-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52861-145">RELATED LINKS</span></span>
