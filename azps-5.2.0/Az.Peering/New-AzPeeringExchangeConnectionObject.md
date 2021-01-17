---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: d3522a2916944c3ab14535a3b7957babd5f4a6ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388482"
---
# <span data-ttu-id="b06cb-101">New-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b06cb-101">New-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="b06cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b06cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b06cb-103">Skapar en i Memory PSObject som ska användas för att skapa eller ändra en peering.</span><span class="sxs-lookup"><span data-stu-id="b06cb-103">Creates a in memory PSObject to be used for creating or modifying a Peering.</span></span>

## <span data-ttu-id="b06cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b06cb-104">SYNTAX</span></span>

### <span data-ttu-id="b06cb-105">IPv4Address (standard)</span><span class="sxs-lookup"><span data-stu-id="b06cb-105">IPv4Address (Default)</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06cb-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="b06cb-106">IPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-MD5AuthenticationKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06cb-107">IPv4AddressIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b06cb-107">IPv4AddressIPv6Address</span></span>
```
New-AzPeeringExchangeConnectionObject [-PeeringDBFacilityId] <Int32> -PeerSessionIPv4Address <String>
 -PeerSessionIPv6Address <String> [-MaxPrefixesAdvertisedIPv4 <Int32>] [-MaxPrefixesAdvertisedIPv6 <Int32>]
 [-MD5AuthenticationKey <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b06cb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b06cb-108">DESCRIPTION</span></span>
<span data-ttu-id="b06cb-109">Skapar en i minnet PSObject</span><span class="sxs-lookup"><span data-stu-id="b06cb-109">Creates an in memory PSObject</span></span> 

## <span data-ttu-id="b06cb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b06cb-110">EXAMPLES</span></span>

### <span data-ttu-id="b06cb-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b06cb-111">Example 1</span></span>
```powershell
PS C:> $exconnection = New-AzPeeringExchangeConnectionObject -PeeringDBFacilityId 99999 -PeerSessionIPv4Address 10.3.151.99 -MaxPrefixesAdvertisedIPv4 20000 -MD5AuthenticationKey 25234523452123411fd234qdwfas3234

PeeringDBFacilityId     : 99999
PeerSessionIPv4Address  : 10.3.151.99
MaxPrefixesAdvertisedV4 : 20000
Md5AuthenticationKey    : 25234523452123411fd234qdwfas3234
```

<span data-ttu-id="b06cb-112">Lokalt anslutnings objekt</span><span class="sxs-lookup"><span data-stu-id="b06cb-112">Local connection object</span></span>

## <span data-ttu-id="b06cb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b06cb-113">PARAMETERS</span></span>

### <span data-ttu-id="b06cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06cb-114">-DefaultProfile</span></span>
<span data-ttu-id="b06cb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b06cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b06cb-116">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="b06cb-116">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="b06cb-117">Maximalt annonserad IPv4</span><span class="sxs-lookup"><span data-stu-id="b06cb-117">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06cb-118">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="b06cb-118">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="b06cb-119">Det högsta antalet annonserade IPv6</span><span class="sxs-lookup"><span data-stu-id="b06cb-119">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06cb-120">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="b06cb-120">-MD5AuthenticationKey</span></span>
<span data-ttu-id="b06cb-121">MD5-autentiseringsprocessen för session.</span><span class="sxs-lookup"><span data-stu-id="b06cb-121">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="b06cb-122">-PeeringDBFacilityId</span><span class="sxs-lookup"><span data-stu-id="b06cb-122">-PeeringDBFacilityId</span></span>
<span data-ttu-id="b06cb-123">ID för peering-funktion på https://peeringdb.com</span><span class="sxs-lookup"><span data-stu-id="b06cb-123">The peering facility Id found on https://peeringdb.com</span></span>

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

### <span data-ttu-id="b06cb-124">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="b06cb-124">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="b06cb-125">IPv4-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="b06cb-125">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06cb-126">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="b06cb-126">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="b06cb-127">IPv6-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="b06cb-127">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address, IPv4AddressIPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b06cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06cb-128">CommonParameters</span></span>
<span data-ttu-id="b06cb-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b06cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06cb-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b06cb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06cb-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b06cb-131">INPUTS</span></span>

### <span data-ttu-id="b06cb-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="b06cb-132">None</span></span>

## <span data-ttu-id="b06cb-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b06cb-133">OUTPUTS</span></span>

### <span data-ttu-id="b06cb-134">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="b06cb-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="b06cb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b06cb-135">NOTES</span></span>

## <span data-ttu-id="b06cb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b06cb-136">RELATED LINKS</span></span>
