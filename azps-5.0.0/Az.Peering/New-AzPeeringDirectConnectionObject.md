---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 3d58834dbd80549aed52104e84099544a427fa1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323130"
---
# <span data-ttu-id="2e815-101">New-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="2e815-101">New-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="2e815-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e815-102">SYNOPSIS</span></span>
<span data-ttu-id="2e815-103">Skapar en i Memory PSObject som ska användas för att skapa eller ändra en peering.</span><span class="sxs-lookup"><span data-stu-id="2e815-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="2e815-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e815-104">SYNTAX</span></span>

### <span data-ttu-id="2e815-105">IPv4PrefixIPv6Prefix (standard)</span><span class="sxs-lookup"><span data-stu-id="2e815-105">IPv4PrefixIPv6Prefix (Default)</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-SessionPrefixV4 <String>]
 [-SessionPrefixV6 <String>] -BandwidthInMbps <Int32> [-UseForPeeringService]
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e815-106">ParameterSetNameMicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2e815-106">ParameterSetNameMicrosoftProvidedIPAddress</span></span>
```
New-AzPeeringDirectConnectionObject [-PeeringDBFacilityId] <Int32> [-MicrosoftProvidedIPAddress]
 -BandwidthInMbps <Int32> [-UseForPeeringService] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e815-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e815-107">DESCRIPTION</span></span>
<span data-ttu-id="2e815-108">Skapar en i minnet PSObject</span><span class="sxs-lookup"><span data-stu-id="2e815-108">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="2e815-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e815-109">EXAMPLES</span></span>

### <span data-ttu-id="2e815-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2e815-110">Example 1</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -MaxPrefixesAdvertisedIPv4 20000 -MaxPrefixesAdvertisedIPv6 2000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 6d771cef-7169-4b0a-b028-c7270054bd31
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
Md5AuthenticationKey   : 25234523452123411fd234qdwfas3234
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="2e815-111">Ny lokal anslutning</span><span class="sxs-lookup"><span data-stu-id="2e815-111">New local connection</span></span>

### <span data-ttu-id="2e815-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2e815-112">Example 2</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -MicrosoftProvidedIPAddress -BandwidthInMbps 30000 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 1de364bf-74ea-4088-ad17-bb79c16cfa81
BandwidthInMbps        : 30000
```

<span data-ttu-id="2e815-113">Skapa direkt peering-anslutning med användning för peering-tjänsten aktive rad och Microsofts IP-adresser</span><span class="sxs-lookup"><span data-stu-id="2e815-113">Create direct peering connection with use for peering service enabled and Microsoft provided IP addresses</span></span>

### <span data-ttu-id="2e815-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="2e815-114">Example 3</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000 -SessionPrefixV4 192.168.1.0/31 -SessionPrefixV6 fe01::0/127 -UseForPeeringService

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Peer
SessionPrefixV4        : 192.168.1.0/31
ConnectionIdentifier   : 74ea6eab-5625-4170-a642-822e85d97566
SessionPrefixV6        : fe01::0/127
BandwidthInMbps        : 30000
SessionStateV4         :
SessionStateV6         :
```

<span data-ttu-id="2e815-115">Skapa direkt peering-anslutning med användning för peering-tjänsten aktive rad och peer-tillhandahållna IP-adresser</span><span class="sxs-lookup"><span data-stu-id="2e815-115">Create direct peering connection with use for peering service enabled and peer provided IP Addresses</span></span>

### <span data-ttu-id="2e815-116">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="2e815-116">Example 4</span></span>
```powershell
PS C:>New-AzPeeringDirectConnectionObject -PeeringDBFacilityId 99999 -BandwidthInMbps 30000

PeeringDBFacilityId    : 99999
UseForPeeringService   : False
SessionAddressProvider : Peer
ConnectionIdentifier   : 920f128a-c9d8-4514-a2e0-c533ab1a550c
BandwidthInMbps        : 30000
```

<span data-ttu-id="2e815-117">Skapa direkt peering-anslutning utan BGP-sessionens IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="2e815-117">Create direct peering connection without bgp session IP addresses.</span></span> <span data-ttu-id="2e815-118">Motparten måste ange IP-adresserna innan BGP-sessionen kan konfigureras.</span><span class="sxs-lookup"><span data-stu-id="2e815-118">The peer will have to set the IP addresses before the bgp session can be configured.</span></span>

## <span data-ttu-id="2e815-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e815-119">PARAMETERS</span></span>

### <span data-ttu-id="2e815-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="2e815-120">-BandwidthInMbps</span></span>
<span data-ttu-id="2e815-121">Bandbredden som erbjuds på den här platsen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="2e815-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e815-122">-DefaultProfile</span></span>
<span data-ttu-id="2e815-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e815-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e815-124">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="2e815-124">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="2e815-125">Maximalt annonserad IPv4</span><span class="sxs-lookup"><span data-stu-id="2e815-125">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-126">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="2e815-126">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="2e815-127">Det högsta antalet annonserade IPv6</span><span class="sxs-lookup"><span data-stu-id="2e815-127">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-128">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="2e815-128">-MD5AuthenticationKey</span></span>
<span data-ttu-id="2e815-129">MD5-autentiseringsprocessen för session.</span><span class="sxs-lookup"><span data-stu-id="2e815-129">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-130">-MicrosoftProvidedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2e815-130">-MicrosoftProvidedIPAddress</span></span>
<span data-ttu-id="2e815-131">Aktivera flagga som anger att Microsoft ska tillhandahålla BGP-sessionens adresser.</span><span class="sxs-lookup"><span data-stu-id="2e815-131">Enable flag that tells Microsoft to provide the BGP session addresses.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ParameterSetNameMicrosoftProvidedIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-132">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="2e815-132">-PeeringDBFacilityId</span></span>
<span data-ttu-id="2e815-133">ID för peering-funktion på https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="2e815-133">The peering facility Id found on https://peeringdb.com</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-134">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="2e815-134">-SessionPrefixV4</span></span>
<span data-ttu-id="2e815-135">IPv4-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="2e815-135">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-136">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="2e815-136">-SessionPrefixV6</span></span>
<span data-ttu-id="2e815-137">IPv6-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="2e815-137">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4PrefixIPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-138">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="2e815-138">-UseForPeeringService</span></span>
<span data-ttu-id="2e815-139">Aktivera för användning med Microsoft peering service (MPS).</span><span class="sxs-lookup"><span data-stu-id="2e815-139">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e815-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e815-140">CommonParameters</span></span>
<span data-ttu-id="2e815-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e815-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e815-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e815-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e815-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e815-143">INPUTS</span></span>

### <span data-ttu-id="2e815-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="2e815-144">None</span></span>

## <span data-ttu-id="2e815-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e815-145">OUTPUTS</span></span>

### <span data-ttu-id="2e815-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="2e815-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="2e815-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e815-147">NOTES</span></span>

## <span data-ttu-id="2e815-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e815-148">RELATED LINKS</span></span>
