---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918146"
---
# <span data-ttu-id="669ae-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="669ae-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="669ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="669ae-102">SYNOPSIS</span></span>
<span data-ttu-id="669ae-103">Skapar ett Azure VpnSiteLink-objekt.</span><span class="sxs-lookup"><span data-stu-id="669ae-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="669ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="669ae-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="669ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="669ae-105">DESCRIPTION</span></span>
<span data-ttu-id="669ae-106">Skapar ett Azure VpnSiteLink-objekt.</span><span class="sxs-lookup"><span data-stu-id="669ae-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="669ae-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="669ae-107">EXAMPLES</span></span>

### <span data-ttu-id="669ae-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="669ae-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="669ae-109">Ovanstående skapar en resurs grupp, en virtuell WAN-och en VpnSite med 1 VpnSiteLinks i västra USA i resurs gruppen "testRG" i Azure.</span><span class="sxs-lookup"><span data-stu-id="669ae-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="669ae-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="669ae-110">PARAMETERS</span></span>

### <span data-ttu-id="669ae-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="669ae-111">-BGPAsn</span></span>
<span data-ttu-id="669ae-112">BGP ASN för denna VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="669ae-112">The BGP ASN for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="669ae-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="669ae-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="669ae-114">BGP peering-adressen för denna VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="669ae-114">The BGP Peering Address for this VpnSiteLink.</span></span>

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

### <span data-ttu-id="669ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669ae-115">-DefaultProfile</span></span>
<span data-ttu-id="669ae-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="669ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="669ae-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="669ae-117">-IPAddress</span></span>
<span data-ttu-id="669ae-118">Nästa hopp-IP-adress.</span><span class="sxs-lookup"><span data-stu-id="669ae-118">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="669ae-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="669ae-119">-LinkProviderName</span></span>
<span data-ttu-id="669ae-120">Länk leverantörens namn.</span><span class="sxs-lookup"><span data-stu-id="669ae-120">Link Provider Name.</span></span>

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

### <span data-ttu-id="669ae-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="669ae-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="669ae-122">Länk hastighet i Mbps.</span><span class="sxs-lookup"><span data-stu-id="669ae-122">Link Speed In Mbps.</span></span>

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

### <span data-ttu-id="669ae-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="669ae-123">-Name</span></span>
<span data-ttu-id="669ae-124">Namn</span><span class="sxs-lookup"><span data-stu-id="669ae-124">Name</span></span>

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

### <span data-ttu-id="669ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669ae-125">CommonParameters</span></span>
<span data-ttu-id="669ae-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="669ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669ae-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="669ae-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669ae-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="669ae-128">INPUTS</span></span>

### <span data-ttu-id="669ae-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="669ae-129">None</span></span>

## <span data-ttu-id="669ae-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="669ae-130">OUTPUTS</span></span>

### <span data-ttu-id="669ae-131">Microsoft. Azure. commands. Networks. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="669ae-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="669ae-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="669ae-132">NOTES</span></span>

## <span data-ttu-id="669ae-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="669ae-133">RELATED LINKS</span></span>

[<span data-ttu-id="669ae-134">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="669ae-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)