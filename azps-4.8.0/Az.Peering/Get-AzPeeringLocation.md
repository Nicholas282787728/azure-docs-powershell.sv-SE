---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringLocation.md
ms.openlocfilehash: 233cf87eed682919df8ca0ae38fefaec5964942c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259205"
---
# <span data-ttu-id="62e96-101">Get-AzPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="62e96-101">Get-AzPeeringLocation</span></span>

## <span data-ttu-id="62e96-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62e96-102">SYNOPSIS</span></span>
<span data-ttu-id="62e96-103">Får peering-platserna som tillhandahålls av Microsoft</span><span class="sxs-lookup"><span data-stu-id="62e96-103">Gets the Peering locations offered by Microsoft</span></span>

## <span data-ttu-id="62e96-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62e96-104">SYNTAX</span></span>

### <span data-ttu-id="62e96-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="62e96-105">Default (Default)</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62e96-106">LocationByFacilityId</span><span class="sxs-lookup"><span data-stu-id="62e96-106">LocationByFacilityId</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringDbFacilityId <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e96-107">LocationByDirectType</span><span class="sxs-lookup"><span data-stu-id="62e96-107">LocationByDirectType</span></span>
```
Get-AzPeeringLocation [-Kind] <String> [-PeeringLocation <String>] [-DirectPeeringType <String>]
 [-PeeringDbFacilityId <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e96-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62e96-108">DESCRIPTION</span></span>
<span data-ttu-id="62e96-109">Får peering-funktionerna där användarna kan ansluta med ARM.</span><span class="sxs-lookup"><span data-stu-id="62e96-109">Gets the Peering Facilities where users can connect with ARM.</span></span>

## <span data-ttu-id="62e96-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62e96-110">EXAMPLES</span></span>

### <span data-ttu-id="62e96-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="62e96-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Direct

#...More above
PeeringLocation       : Dublin
Address               : Unit 2, North West Business Park
Country               : IE
PeeringDBFacilityId   : 1065
PeeringDBFacilityLink : https://www.peeringdb.com/fac/1065
BandwidthOffers       : {10Gbps, 100Gbps}

PeeringLocation       : Frankfurt
Address               : Hanauer Landstrasse 298
Country               : DE
PeeringDBFacilityId   : 58
PeeringDBFacilityLink : https://www.peeringdb.com/fac/58
BandwidthOffers       : {10Gbps, 100Gbps}
#...More below
```

<span data-ttu-id="62e96-112">En lång lista med platser.</span><span class="sxs-lookup"><span data-stu-id="62e96-112">Its a long list of locations.</span></span> <span data-ttu-id="62e96-113">Hämtar alla funktioner för direkt peering.</span><span class="sxs-lookup"><span data-stu-id="62e96-113">Gets the all the Direct Peering Facilities.</span></span>

### <span data-ttu-id="62e96-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="62e96-114">Example 2</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringLocation "Honolulu" 

ExchangeName          : DRF IX
PeeringLocation       : Honolulu
Country               : US
PeeringDBFacilityId   : 267
PeeringDBFacilityLink : https://www.peeringdb.com/ix/267
MicrosoftIPv4Address  : 206.197.210.37
MicrosoftIPv6Address  : 2606:7c80:3375:50::37
FacilityIPv4Prefix    : 206.197.210.0/24
FacilityIPv6Prefix    : 2606:7c80:3375:50::/64
```

<span data-ttu-id="62e96-115">Hämtar Exchange peering-platsen för Honolulu.</span><span class="sxs-lookup"><span data-stu-id="62e96-115">Gets the exchange peering location for Honolulu.</span></span> 

### <span data-ttu-id="62e96-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="62e96-116">Example 3</span></span>
```powershell
PS C:> Get-AzPeeringLocation -Kind Exchange -PeeringDbFacilityId 71 

ExchangeName          : NIX.CZ
PeeringLocation       : Prague
Country               : CZ
PeeringDBFacilityId   : 71
PeeringDBFacilityLink : https://www.peeringdb.com/ix/71
MicrosoftIPv4Address  : 91.210.16.115
MicrosoftIPv6Address  : 2001:7f8:14::6b:1
FacilityIPv4Prefix    : 91.210.16.0/22
FacilityIPv6Prefix    : 2001:7f8:14::/64
```

<span data-ttu-id="62e96-117">Hämtar Exchange peering-platsen för peering Facility ID 71.</span><span class="sxs-lookup"><span data-stu-id="62e96-117">Gets the exchange peering location for peering facility id 71.</span></span> 

## <span data-ttu-id="62e96-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62e96-118">PARAMETERS</span></span>

### <span data-ttu-id="62e96-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e96-119">-DefaultProfile</span></span>
<span data-ttu-id="62e96-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62e96-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62e96-121">-DirectPeeringType</span><span class="sxs-lookup"><span data-stu-id="62e96-121">-DirectPeeringType</span></span>
<span data-ttu-id="62e96-122">Välj "Edge", "CDN" och "transitering".</span><span class="sxs-lookup"><span data-stu-id="62e96-122">Select 'Edge', 'CDN', and 'Transit'.</span></span>

```yaml
Type: System.String
Parameter Sets: LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e96-123">-Sort</span><span class="sxs-lookup"><span data-stu-id="62e96-123">-Kind</span></span>
<span data-ttu-id="62e96-124">Visar alla peering-resurser av typen.</span><span class="sxs-lookup"><span data-stu-id="62e96-124">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e96-125">-PeeringDbFacilityId</span><span class="sxs-lookup"><span data-stu-id="62e96-125">-PeeringDbFacilityId</span></span>
<span data-ttu-id="62e96-126">PeeringDB.com Facility-ID</span><span class="sxs-lookup"><span data-stu-id="62e96-126">The PeeringDB.com Facility ID</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LocationByFacilityId, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e96-127">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="62e96-127">-PeeringLocation</span></span>
<span data-ttu-id="62e96-128">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="62e96-128">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, LocationByDirectType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62e96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e96-129">CommonParameters</span></span>
<span data-ttu-id="62e96-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62e96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e96-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62e96-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e96-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62e96-132">INPUTS</span></span>

### <span data-ttu-id="62e96-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="62e96-133">None</span></span>

## <span data-ttu-id="62e96-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62e96-134">OUTPUTS</span></span>

### <span data-ttu-id="62e96-135">Microsoft. Azure. PowerShell. cmdletar. peering. Models. PSPeeringLocation</span><span class="sxs-lookup"><span data-stu-id="62e96-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringLocation</span></span>

## <span data-ttu-id="62e96-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62e96-136">NOTES</span></span>

## <span data-ttu-id="62e96-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62e96-137">RELATED LINKS</span></span>
