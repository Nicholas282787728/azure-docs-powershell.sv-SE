---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringdirectconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringDirectConnectionObject.md
ms.openlocfilehash: 0b72cd501f9e003e39fc3dd4f4e90bbd85331180
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322195"
---
# <span data-ttu-id="205de-101">Set-AzPeeringDirectConnectionObject</span><span class="sxs-lookup"><span data-stu-id="205de-101">Set-AzPeeringDirectConnectionObject</span></span>

## <span data-ttu-id="205de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="205de-102">SYNOPSIS</span></span>
<span data-ttu-id="205de-103">Anger eller uppdaterar direkt anslutnings information.</span><span class="sxs-lookup"><span data-stu-id="205de-103">Sets or updates the Direct Connection information.</span></span> 

## <span data-ttu-id="205de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="205de-104">SYNTAX</span></span>

### <span data-ttu-id="205de-105">Bandbredd (standard)</span><span class="sxs-lookup"><span data-stu-id="205de-105">Bandwidth (Default)</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -BandwidthInMbps <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="205de-106">IPv4Prefix</span><span class="sxs-lookup"><span data-stu-id="205de-106">IPv4Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV4 <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="205de-107">IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="205de-107">IPv6Prefix</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -SessionPrefixV6 <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="205de-108">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="205de-108">Md5Authentication</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="205de-109">ParameterSetNameUseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="205de-109">ParameterSetNameUseForPeeringService</span></span>
```
Set-AzPeeringDirectConnectionObject -InputObject <PSDirectConnection> -UseForPeeringService <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="205de-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="205de-110">DESCRIPTION</span></span>
<span data-ttu-id="205de-111">Den används tillsammans med Update-AzPeering, men detta är en i minnet och kommer bara att bevaras `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="205de-111">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="205de-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="205de-112">EXAMPLES</span></span>

### <span data-ttu-id="205de-113">Uppgradera bandbredd</span><span class="sxs-lookup"><span data-stu-id="205de-113">Upgrade Bandwidth</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -BandwidthInMbps 30000
```

<span data-ttu-id="205de-114">Uppgraderar bandbredden för den första anslutningen i peering-objektet i minnet.</span><span class="sxs-lookup"><span data-stu-id="205de-114">Upgrades the bandwidth for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="205de-115">Uppdatera BGP-sessionens adress</span><span class="sxs-lookup"><span data-stu-id="205de-115">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -SessionPrefixV4 "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="205de-116">Uppdaterar peering Address för den första anslutningen i peering-objektet i minnet.</span><span class="sxs-lookup"><span data-stu-id="205de-116">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="205de-117">Uppdaterings användning för peering-tjänsten</span><span class="sxs-lookup"><span data-stu-id="205de-117">Update Use for peering service</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringDirectConnectionObject -UseForPeeringService $true

PeeringDBFacilityId    : 99999
UseForPeeringService   : True
SessionAddressProvider : Microsoft
ConnectionIdentifier   : 16c24fd5-89aa-48d7-a101-38ca68a4ce6d
BandwidthInMbps        : 30000
```

<span data-ttu-id="205de-118">Uppdaterar anslutningen för användning med peering service</span><span class="sxs-lookup"><span data-stu-id="205de-118">Updates the connection for use with peering service</span></span>

## <span data-ttu-id="205de-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="205de-119">PARAMETERS</span></span>

### <span data-ttu-id="205de-120">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="205de-120">-BandwidthInMbps</span></span>
<span data-ttu-id="205de-121">Bandbredden som erbjuds på den här platsen i Mbps.</span><span class="sxs-lookup"><span data-stu-id="205de-121">The Bandwidth offered at this location in Mbps.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Bandwidth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205de-122">-DefaultProfile</span></span>
<span data-ttu-id="205de-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="205de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="205de-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="205de-124">-InputObject</span></span>
<span data-ttu-id="205de-125">Direkt anslutnings objekt</span><span class="sxs-lookup"><span data-stu-id="205de-125">The direct connection Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205de-126">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="205de-126">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="205de-127">Maximalt annonserad IPv4</span><span class="sxs-lookup"><span data-stu-id="205de-127">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-128">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="205de-128">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="205de-129">Det högsta antalet annonserade IPv6</span><span class="sxs-lookup"><span data-stu-id="205de-129">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Prefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-130">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="205de-130">-MD5AuthenticationKey</span></span>
<span data-ttu-id="205de-131">MD5-autentiseringsprocessen för session.</span><span class="sxs-lookup"><span data-stu-id="205de-131">The MD5 authentication key for session.</span></span>

```yaml
Type: System.String
Parameter Sets: Md5Authentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-132">-SessionPrefixV4</span><span class="sxs-lookup"><span data-stu-id="205de-132">-SessionPrefixV4</span></span>
<span data-ttu-id="205de-133">IPv4-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="205de-133">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-134">-SessionPrefixV6</span><span class="sxs-lookup"><span data-stu-id="205de-134">-SessionPrefixV6</span></span>
<span data-ttu-id="205de-135">IPv6-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="205de-135">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Prefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-136">-UseForPeeringService</span><span class="sxs-lookup"><span data-stu-id="205de-136">-UseForPeeringService</span></span>
<span data-ttu-id="205de-137">Aktivera för användning med Microsoft peering service (MPS).</span><span class="sxs-lookup"><span data-stu-id="205de-137">Enable for use with Microsoft Peering Service (MPS).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: ParameterSetNameUseForPeeringService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="205de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205de-138">CommonParameters</span></span>
<span data-ttu-id="205de-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205de-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="205de-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205de-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="205de-141">INPUTS</span></span>

### <span data-ttu-id="205de-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="205de-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="205de-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="205de-143">OUTPUTS</span></span>

### <span data-ttu-id="205de-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span><span class="sxs-lookup"><span data-stu-id="205de-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSDirectConnection</span></span>

## <span data-ttu-id="205de-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="205de-145">NOTES</span></span>

## <span data-ttu-id="205de-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="205de-146">RELATED LINKS</span></span>
