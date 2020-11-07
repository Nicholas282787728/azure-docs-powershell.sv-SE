---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientIpsecParameter.md
ms.openlocfilehash: e547389518bce61c3c3654011bdc0107dc5a112f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747973"
---
# <span data-ttu-id="edd50-101">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="edd50-101">New-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="edd50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edd50-102">SYNOPSIS</span></span>
<span data-ttu-id="edd50-103">Med det här kommandot kan användarna skapa IPsec-parametrar-objekt med ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, som ska anges på den befintliga VPN-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="edd50-103">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="edd50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edd50-104">SYNTAX</span></span>

```
New-AzVpnClientIpsecParameter [-SALifeTime <Int32>] [-SADataSize <Int32>] [-IpsecEncryption <String>]
 [-IpsecIntegrity <String>] [-IkeEncryption <String>] [-IkeIntegrity <String>] [-DhGroup <String>]
 [-PfsGroup <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edd50-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edd50-105">DESCRIPTION</span></span>
<span data-ttu-id="edd50-106">Med det här kommandot kan användarna skapa IPsec-parametrar-objekt med ett eller alla värden, till exempel IpsecEncryption, IpsecIntegrity, IkeEncryption, IkeIntegrity, DhGroup, PfsGroup, som ska anges på den befintliga VPN-gatewayen.</span><span class="sxs-lookup"><span data-stu-id="edd50-106">This command allows the users to create the Vpn ipsec parameters object specifying one or all values such as IpsecEncryption,IpsecIntegrity,IkeEncryption,IkeIntegrity,DhGroup,PfsGroup to set on the existing VPN gateway.</span></span>

## <span data-ttu-id="edd50-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edd50-107">EXAMPLES</span></span>

### <span data-ttu-id="edd50-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="edd50-108">Example 1</span></span>
```
PS C:\> $vpnclientipsecparams1 = New-AzVpnClientIpsecParameter -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTime 86473 -SADataSize 429498 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2
PS C:\> $setvpnIpsecParams = Set-AzVpnClientIpsecParameter -VirtualNetworkGatewayName $rname -ResourceGroupName $rgname -VpnClientIPsecParameter $vpnclientipsecparams1
```

<span data-ttu-id="edd50-109">New-AzVpnClientIpsecParameter cmdlet används för att skapa IPsec-parametrar-objektet för att använda en eller alla parametrar-värden som användaren kan ange för en befintlig virtuell nätverksgateway i ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="edd50-109">New-AzVpnClientIpsecParameter cmdlet is used to create the vpn ipsec parameters object of using the passed one or all parameters' values which user can set for any existing Virtual network gateway in ResourceGroup.</span></span>
<span data-ttu-id="edd50-110">Det här skapade VpnClientIPsecParameters-objektet skickas till Set-AzVpnClientIpsecParameter kommandot för att ange den angivna anpassade VPN-principen för IPSec på en virtuell nätverksgateway enligt exemplet ovan.</span><span class="sxs-lookup"><span data-stu-id="edd50-110">This created VpnClientIPsecParameters object is passed to Set-AzVpnClientIpsecParameter command to set the specified Vpn ipsec custom policy on Virtual network gateway as shown in above example.</span></span> <span data-ttu-id="edd50-111">Det här kommandot returnerar ett objekt med VpnClientIPsecParameters som visar inställda parametrar.</span><span class="sxs-lookup"><span data-stu-id="edd50-111">This command returns object of VpnClientIPsecParameters which shows set parameters.</span></span>

## <span data-ttu-id="edd50-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edd50-112">PARAMETERS</span></span>

### <span data-ttu-id="edd50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd50-113">-DefaultProfile</span></span>
<span data-ttu-id="edd50-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edd50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edd50-115">-DhGroup</span><span class="sxs-lookup"><span data-stu-id="edd50-115">-DhGroup</span></span>
<span data-ttu-id="edd50-116">Vpnclient DH-grupper som används i IKE fas 1 för initial SA.</span><span class="sxs-lookup"><span data-stu-id="edd50-116">The Vpnclient DH Groups used in IKE Phase 1 for initial SA.</span></span>

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

### <span data-ttu-id="edd50-117">-IkeEncryption</span><span class="sxs-lookup"><span data-stu-id="edd50-117">-IkeEncryption</span></span>
<span data-ttu-id="edd50-118">Vpnclient IKE-krypteringsalgoritm (IKE fas 2)</span><span class="sxs-lookup"><span data-stu-id="edd50-118">The Vpnclient IKE encryption algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="edd50-119">-IkeIntegrity</span><span class="sxs-lookup"><span data-stu-id="edd50-119">-IkeIntegrity</span></span>
<span data-ttu-id="edd50-120">Vpnclient IKE-integritetsalgoritm (IKE Phase 2)</span><span class="sxs-lookup"><span data-stu-id="edd50-120">The Vpnclient IKE integrity algorithm (IKE Phase 2)</span></span>

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

### <span data-ttu-id="edd50-121">-IpsecEncryption</span><span class="sxs-lookup"><span data-stu-id="edd50-121">-IpsecEncryption</span></span>
<span data-ttu-id="edd50-122">Vpnclient IPSec-krypteringsalgoritm (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="edd50-122">The Vpnclient IPSec encryption algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="edd50-123">-IpsecIntegrity</span><span class="sxs-lookup"><span data-stu-id="edd50-123">-IpsecIntegrity</span></span>
<span data-ttu-id="edd50-124">IPSec-integritetsalgoritmen Vpnclient (IKE-fas 1)</span><span class="sxs-lookup"><span data-stu-id="edd50-124">The Vpnclient IPSec integrity algorithm (IKE Phase 1)</span></span>

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

### <span data-ttu-id="edd50-125">-PfsGroup</span><span class="sxs-lookup"><span data-stu-id="edd50-125">-PfsGroup</span></span>
<span data-ttu-id="edd50-126">Vpnclient PFS-grupper som används i IKE fas 2 för ny underordnad SA</span><span class="sxs-lookup"><span data-stu-id="edd50-126">The Vpnclient PFS Groups used in IKE Phase 2 for new child SA</span></span>

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

### <span data-ttu-id="edd50-127">-SADataSize</span><span class="sxs-lookup"><span data-stu-id="edd50-127">-SADataSize</span></span>
<span data-ttu-id="edd50-128">Vpnclient säkerhets Association för IPSec (kallas även för en nytto Last storlek i KB för snabb läge eller fas 2)</span><span class="sxs-lookup"><span data-stu-id="edd50-128">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) payload size in KB</span></span>

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

### <span data-ttu-id="edd50-129">-SALifeTime</span><span class="sxs-lookup"><span data-stu-id="edd50-129">-SALifeTime</span></span>
<span data-ttu-id="edd50-130">Vpnclient säkerhets Association för IPSec (kallas även för snabb läge eller fas 2 SA) i sekunder</span><span class="sxs-lookup"><span data-stu-id="edd50-130">The Vpnclient IPSec Security Association (also called Quick Mode or Phase 2 SA) lifetime in seconds</span></span>

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

### <span data-ttu-id="edd50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd50-131">CommonParameters</span></span>
<span data-ttu-id="edd50-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd50-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd50-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd50-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edd50-134">INPUTS</span></span>

### <span data-ttu-id="edd50-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="edd50-135">None</span></span>

## <span data-ttu-id="edd50-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edd50-136">OUTPUTS</span></span>

### <span data-ttu-id="edd50-137">Microsoft. Azure. commands. Networks. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="edd50-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="edd50-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edd50-138">NOTES</span></span>

## <span data-ttu-id="edd50-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edd50-139">RELATED LINKS</span></span>

[<span data-ttu-id="edd50-140">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="edd50-140">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="edd50-141">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="edd50-141">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="edd50-142">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="edd50-142">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
