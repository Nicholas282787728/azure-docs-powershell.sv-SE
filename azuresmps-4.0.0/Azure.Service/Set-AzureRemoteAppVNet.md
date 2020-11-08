---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099282"
---
# <span data-ttu-id="a7d6f-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a7d6f-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="a7d6f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a7d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d6f-103">Anger egenskaperna för ett virtuellt Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="a7d6f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a7d6f-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a7d6f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a7d6f-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d6f-106">Cmdleten **set-AzureRemoteAppVNet** anger egenskaperna för ett Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="a7d6f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a7d6f-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d6f-108">Exempel 1: Ange egenskaper för ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="a7d6f-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="a7d6f-109">Det här kommandot anger egenskaperna för ett virtuellt nätverk med namnet ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="a7d6f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a7d6f-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d6f-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7d6f-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="a7d6f-112">Anger IPv4-adresser för DNS-servrarna.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d6f-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="a7d6f-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="a7d6f-114">Anger det lokala nätverks adress utrymmet i CIDR-notation (classes Inter-Domain routing).</span><span class="sxs-lookup"><span data-stu-id="a7d6f-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="a7d6f-115">Det får inte överlappa det virtuella nätverkets adress utrymme.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d6f-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="a7d6f-116">-Profile</span></span>
<span data-ttu-id="a7d6f-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a7d6f-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7d6f-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="a7d6f-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="a7d6f-120">Anger det virtuella nätverks adress utrymmet i CIDR-notation.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="a7d6f-121">Det måste finnas i det privata IP-adressintervallet och får inte överlappa det lokala nätverks adress utrymmet.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d6f-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a7d6f-122">-VNetName</span></span>
<span data-ttu-id="a7d6f-123">Anger namnet på det virtuella Azure RemoteApp-nätverket.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d6f-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7d6f-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="a7d6f-125">Anger adressen för den virtuella privata nätverks enheten (VPN).</span><span class="sxs-lookup"><span data-stu-id="a7d6f-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="a7d6f-126">Det måste vara en offentlig adress.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d6f-127">CommonParameters</span></span>
<span data-ttu-id="a7d6f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d6f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7d6f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d6f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a7d6f-130">INPUTS</span></span>

## <span data-ttu-id="a7d6f-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a7d6f-131">OUTPUTS</span></span>

## <span data-ttu-id="a7d6f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a7d6f-132">NOTES</span></span>

## <span data-ttu-id="a7d6f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a7d6f-133">RELATED LINKS</span></span>

[<span data-ttu-id="a7d6f-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="a7d6f-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


