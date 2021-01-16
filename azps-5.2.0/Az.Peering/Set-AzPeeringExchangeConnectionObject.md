---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringexchangeconnectionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringExchangeConnectionObject.md
ms.openlocfilehash: 9f4ceb2ac0bc84198e7fcfb71114c12e48a5616e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394347"
---
# <span data-ttu-id="05207-101">Set-AzPeeringExchangeConnectionObject</span><span class="sxs-lookup"><span data-stu-id="05207-101">Set-AzPeeringExchangeConnectionObject</span></span>

## <span data-ttu-id="05207-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05207-102">SYNOPSIS</span></span>
<span data-ttu-id="05207-103">Anger eller uppdaterar anslutnings informationen för Exchange.</span><span class="sxs-lookup"><span data-stu-id="05207-103">Sets or updates the Exchange Connection information.</span></span> 

## <span data-ttu-id="05207-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05207-104">SYNTAX</span></span>

### <span data-ttu-id="05207-105">IPv4Address (standard)</span><span class="sxs-lookup"><span data-stu-id="05207-105">IPv4Address (Default)</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv4Address <String>
 [-MaxPrefixesAdvertisedIPv4 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05207-106">IPv6</span><span class="sxs-lookup"><span data-stu-id="05207-106">IPv6Address</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -PeerSessionIPv6Address <String>
 [-MaxPrefixesAdvertisedIPv6 <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05207-107">Md5Authentication</span><span class="sxs-lookup"><span data-stu-id="05207-107">Md5Authentication</span></span>
```
Set-AzPeeringExchangeConnectionObject -InputObject <PSExchangeConnection> -MD5AuthenticationKey <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05207-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05207-108">DESCRIPTION</span></span>
<span data-ttu-id="05207-109">Den används tillsammans med Update-AzPeering, men detta är en i minnet och kommer bara att bevaras `Update-AzPeering` .</span><span class="sxs-lookup"><span data-stu-id="05207-109">Used in conjunction with Update-AzPeering, this is an in memory operation and will only persist with `Update-AzPeering`.</span></span> 

## <span data-ttu-id="05207-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05207-110">EXAMPLES</span></span>

### <span data-ttu-id="05207-111">Uppdatera Md5-hash</span><span class="sxs-lookup"><span data-stu-id="05207-111">Update Md5 Hash</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -MD5AuthenticationKey $hash
```

<span data-ttu-id="05207-112">Uppdaterar Md5-hashvärdet för den första anslutningen i peering-objektet i minnet.</span><span class="sxs-lookup"><span data-stu-id="05207-112">Updates the Md5 Hash for the first connection in the Peering object in memory.</span></span> 

### <span data-ttu-id="05207-113">Uppdatera BGP-sessionens adress</span><span class="sxs-lookup"><span data-stu-id="05207-113">Update Bgp Session Address</span></span>
```powershell
PS C:> $update = Get-AzPeering -PeerName "ContosoPeering" -ResourceGroupName rg1 | Set-AzPeeringExchangeConnectionObject -PeerSessionIPv4Address "192.168.0.1" -MaxPrefixesAdvertisedIPv4 20000
```

<span data-ttu-id="05207-114">Uppdaterar peering Address för den första anslutningen i peering-objektet i minnet.</span><span class="sxs-lookup"><span data-stu-id="05207-114">Updates the Peering Address for the first connection in the Peering object in memory.</span></span> 

## <span data-ttu-id="05207-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05207-115">PARAMETERS</span></span>

### <span data-ttu-id="05207-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05207-116">-DefaultProfile</span></span>
<span data-ttu-id="05207-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05207-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05207-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05207-118">-InputObject</span></span>
<span data-ttu-id="05207-119">Exchange Connection-objekt</span><span class="sxs-lookup"><span data-stu-id="05207-119">The exchange connection object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05207-120">-MaxPrefixesAdvertisedIPv4</span><span class="sxs-lookup"><span data-stu-id="05207-120">-MaxPrefixesAdvertisedIPv4</span></span>
<span data-ttu-id="05207-121">Maximalt annonserad IPv4</span><span class="sxs-lookup"><span data-stu-id="05207-121">The maximum advertised IPv4</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv4Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05207-122">-MaxPrefixesAdvertisedIPv6</span><span class="sxs-lookup"><span data-stu-id="05207-122">-MaxPrefixesAdvertisedIPv6</span></span>
<span data-ttu-id="05207-123">Det högsta antalet annonserade IPv6</span><span class="sxs-lookup"><span data-stu-id="05207-123">The maximum advertised IPv6</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: IPv6Address
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05207-124">-MD5AuthenticationKey</span><span class="sxs-lookup"><span data-stu-id="05207-124">-MD5AuthenticationKey</span></span>
<span data-ttu-id="05207-125">MD5-autentiseringsprocessen för session.</span><span class="sxs-lookup"><span data-stu-id="05207-125">The MD5 authentication key for session.</span></span>

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

### <span data-ttu-id="05207-126">-PeerSessionIPv4Address</span><span class="sxs-lookup"><span data-stu-id="05207-126">-PeerSessionIPv4Address</span></span>
<span data-ttu-id="05207-127">IPv4-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="05207-127">The peer session IPv4 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv4Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05207-128">-PeerSessionIPv6Address</span><span class="sxs-lookup"><span data-stu-id="05207-128">-PeerSessionIPv6Address</span></span>
<span data-ttu-id="05207-129">IPv6-adress för peer-session</span><span class="sxs-lookup"><span data-stu-id="05207-129">The peer session IPv6 address</span></span>

```yaml
Type: System.String
Parameter Sets: IPv6Address
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05207-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05207-130">CommonParameters</span></span>
<span data-ttu-id="05207-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05207-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05207-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05207-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05207-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05207-133">INPUTS</span></span>

### <span data-ttu-id="05207-134">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="05207-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="05207-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05207-135">OUTPUTS</span></span>

### <span data-ttu-id="05207-136">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSExchangeConnection</span><span class="sxs-lookup"><span data-stu-id="05207-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSExchangeConnection</span></span>

## <span data-ttu-id="05207-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05207-137">NOTES</span></span>

## <span data-ttu-id="05207-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05207-138">RELATED LINKS</span></span>
