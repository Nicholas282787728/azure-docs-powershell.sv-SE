---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 68df4cd7dc1149b7bb62a148ff7c649ed2418db8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088741"
---
# <span data-ttu-id="eba15-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="eba15-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="eba15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eba15-102">SYNOPSIS</span></span>
<span data-ttu-id="eba15-103">Skapar ett Azure VpnSiteLink-objekt.</span><span class="sxs-lookup"><span data-stu-id="eba15-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="eba15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eba15-104">SYNTAX</span></span>

### <span data-ttu-id="eba15-105">ByVpnSiteLinkIpAddress</span><span class="sxs-lookup"><span data-stu-id="eba15-105">ByVpnSiteLinkIpAddress</span></span>
```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eba15-106">ByVpnSiteLinkFqdn</span><span class="sxs-lookup"><span data-stu-id="eba15-106">ByVpnSiteLinkFqdn</span></span>
```
New-AzVpnSiteLink -Name <String> -Fqdn <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eba15-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eba15-107">DESCRIPTION</span></span>
<span data-ttu-id="eba15-108">Skapar ett Azure VpnSiteLink-objekt.</span><span class="sxs-lookup"><span data-stu-id="eba15-108">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="eba15-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eba15-109">EXAMPLES</span></span>

### <span data-ttu-id="eba15-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eba15-110">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="eba15-111">Ovanstående skapar en resurs grupp, en virtuell WAN-och en VpnSite med 1 VpnSiteLinks i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="eba15-111">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="eba15-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eba15-112">PARAMETERS</span></span>

### <span data-ttu-id="eba15-113">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="eba15-113">-BGPAsn</span></span>
<span data-ttu-id="eba15-114">BGP ASN för denna VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="eba15-114">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba15-115">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="eba15-115">-BGPPeeringAddress</span></span>
<span data-ttu-id="eba15-116">BGP peering-adressen för denna VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="eba15-116">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="eba15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba15-117">-DefaultProfile</span></span>
<span data-ttu-id="eba15-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eba15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba15-119">-FQDN</span><span class="sxs-lookup"><span data-stu-id="eba15-119">-Fqdn</span></span>
<span data-ttu-id="eba15-120">Nästa hopp-FQDN.</span><span class="sxs-lookup"><span data-stu-id="eba15-120">The Next Hop Fqdn.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkFqdn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba15-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="eba15-121">-IPAddress</span></span>
<span data-ttu-id="eba15-122">Nästa hopp-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="eba15-122">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteLinkIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba15-123">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="eba15-123">-LinkProviderName</span></span>
<span data-ttu-id="eba15-124">Länk leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="eba15-124">Link Provider Name.</span></span>

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

### <span data-ttu-id="eba15-125">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="eba15-125">-LinkSpeedInMbps</span></span>
<span data-ttu-id="eba15-126">Länk hastighet i Mbps.</span><span class="sxs-lookup"><span data-stu-id="eba15-126">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba15-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="eba15-127">-Name</span></span>
<span data-ttu-id="eba15-128">Namn</span><span class="sxs-lookup"><span data-stu-id="eba15-128">Name</span></span>

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

### <span data-ttu-id="eba15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba15-129">CommonParameters</span></span>
<span data-ttu-id="eba15-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba15-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba15-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba15-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eba15-132">INPUTS</span></span>

### <span data-ttu-id="eba15-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="eba15-133">None</span></span>

## <span data-ttu-id="eba15-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eba15-134">OUTPUTS</span></span>

### <span data-ttu-id="eba15-135">Microsoft. Azure. commands. Networks. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="eba15-135">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="eba15-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eba15-136">NOTES</span></span>

## <span data-ttu-id="eba15-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eba15-137">RELATED LINKS</span></span>

[<span data-ttu-id="eba15-138">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="eba15-138">New-AzVpnSite</span></span>](./New-AzVpnSite.md)