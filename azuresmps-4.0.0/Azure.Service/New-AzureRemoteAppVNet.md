---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099224"
---
# <span data-ttu-id="57790-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="57790-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="57790-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57790-102">SYNOPSIS</span></span>
<span data-ttu-id="57790-103">Skapar ett Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="57790-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="57790-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57790-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57790-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57790-105">DESCRIPTION</span></span>
<span data-ttu-id="57790-106">Cmdleten **New-AzureRemoteAppVNet** skapar ett Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="57790-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="57790-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57790-107">EXAMPLES</span></span>

### <span data-ttu-id="57790-108">Exempel 1: skapa ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="57790-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="57790-109">Det här kommandot skapar ett virtuellt nätverk med namnet ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="57790-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="57790-110">Om du vill ta reda på åtgärdens status använder du cmdleten **Get-AzureRemoteAppOperationResult** med det SPÅRNINGS-ID som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="57790-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="57790-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57790-111">PARAMETERS</span></span>

### <span data-ttu-id="57790-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="57790-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="57790-113">Anger en matris i IPv4-adresserna för DNS-servrarna.</span><span class="sxs-lookup"><span data-stu-id="57790-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57790-114">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="57790-114">-GatewayType</span></span>
<span data-ttu-id="57790-115">Anger vilken typ av Gateway-operationsföljd som ska användas.</span><span class="sxs-lookup"><span data-stu-id="57790-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="57790-116">De acceptabla värdena för den här parametern är: StaticRouting eller DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="57790-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57790-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="57790-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="57790-118">Anger en matris med strängar som anger det lokala nätverks adress utrymmet i CIDR-notation (Classless Interdomain Routing).</span><span class="sxs-lookup"><span data-stu-id="57790-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="57790-119">Det här adress utrymmet får inte överlappa det virtuella nätverks adress utrymmet som parametern *VirtualNetworkAddressSpace* anger.</span><span class="sxs-lookup"><span data-stu-id="57790-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57790-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="57790-120">-Location</span></span>
<span data-ttu-id="57790-121">Anger den plats där du vill skapa det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="57790-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57790-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="57790-122">-Profile</span></span>
<span data-ttu-id="57790-123">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="57790-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57790-124">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="57790-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57790-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="57790-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="57790-126">Anger en matris med sträng som anger det virtuella nätverks adress utrymmet i CIDR-notation.</span><span class="sxs-lookup"><span data-stu-id="57790-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="57790-127">Det måste finnas i det privata IP-adressintervallet och får inte överlappa det lokala nätverks adress utrymmet som parametern *LocalNetworkAddressSpace* anger.</span><span class="sxs-lookup"><span data-stu-id="57790-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57790-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="57790-128">-VNetName</span></span>
<span data-ttu-id="57790-129">Anger namnet på det virtuella Azure RemoteApp-nätverket.</span><span class="sxs-lookup"><span data-stu-id="57790-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="57790-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="57790-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="57790-131">Anger adressen för den virtuella privata nätverks enheten (VPN).</span><span class="sxs-lookup"><span data-stu-id="57790-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="57790-132">Det måste vara en offentlig adress.</span><span class="sxs-lookup"><span data-stu-id="57790-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="57790-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57790-133">CommonParameters</span></span>
<span data-ttu-id="57790-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57790-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57790-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57790-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57790-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57790-136">INPUTS</span></span>

## <span data-ttu-id="57790-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57790-137">OUTPUTS</span></span>

## <span data-ttu-id="57790-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57790-138">NOTES</span></span>

## <span data-ttu-id="57790-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57790-139">RELATED LINKS</span></span>

[<span data-ttu-id="57790-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="57790-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="57790-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="57790-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="57790-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="57790-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="57790-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="57790-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


