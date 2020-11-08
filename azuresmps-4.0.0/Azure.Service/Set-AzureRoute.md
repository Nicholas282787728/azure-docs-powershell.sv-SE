---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099053"
---
# <span data-ttu-id="20710-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="20710-101">Set-AzureRoute</span></span>

## <span data-ttu-id="20710-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20710-102">SYNOPSIS</span></span>
<span data-ttu-id="20710-103">Skapar en väg i en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="20710-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="20710-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20710-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="20710-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20710-105">DESCRIPTION</span></span>
<span data-ttu-id="20710-106">Cmdleten **set-AzureRoute** skapar en väg i en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="20710-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="20710-107">Den nya vägen börjar gälla nästan omedelbart på de virtuella datorerna som är kopplade till väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="20710-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="20710-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20710-108">EXAMPLES</span></span>

### <span data-ttu-id="20710-109">Exempel 1: lägga till en virtuell enhet nästa hopp väg</span><span class="sxs-lookup"><span data-stu-id="20710-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="20710-110">Det här kommandot skapar en routningstabell som heter ApplianceRouteTable på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="20710-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="20710-111">Kommandot skickar den väg tabellen till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20710-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="20710-112">Den aktuella cmdleten lägger till en väg med namnet ApplianceRoute03, som är en VirtualAppliance nästa hopp typ.</span><span class="sxs-lookup"><span data-stu-id="20710-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="20710-113">Kommandot anger nästa hopp-IP-adress och adressprefixet för vägen.</span><span class="sxs-lookup"><span data-stu-id="20710-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="20710-114">Exempel 2: lägga till en Internet-routning nästa hopp</span><span class="sxs-lookup"><span data-stu-id="20710-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="20710-115">Det här kommandot får en routningstabell med namnet ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="20710-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="20710-116">Kommandot skickar den väg tabellen till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20710-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="20710-117">Den aktuella cmdleten lägger till en väg som heter InternetRoute, som är en typ av Internet hopp.</span><span class="sxs-lookup"><span data-stu-id="20710-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="20710-118">Kommandot anger adressprefixet för vägen.</span><span class="sxs-lookup"><span data-stu-id="20710-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="20710-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20710-119">PARAMETERS</span></span>

### <span data-ttu-id="20710-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="20710-120">-AddressPrefix</span></span>
<span data-ttu-id="20710-121">Anger ett adressprefix för den nya vägen.</span><span class="sxs-lookup"><span data-stu-id="20710-121">Specifies an address prefix for the new route.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20710-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="20710-122">-NextHopIpAddress</span></span>
<span data-ttu-id="20710-123">Anger IP-adressen för den enhet som är nästa hopp för trafik som använder vägen.</span><span class="sxs-lookup"><span data-stu-id="20710-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="20710-124">Ange bara det här värdet om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="20710-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20710-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="20710-125">-NextHopType</span></span>
<span data-ttu-id="20710-126">Anger nästa hopp typ för trafik som använder vägen.</span><span class="sxs-lookup"><span data-stu-id="20710-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="20710-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="20710-127">Valid values are:</span></span> 

- <span data-ttu-id="20710-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="20710-128">VPNGateway</span></span>
- <span data-ttu-id="20710-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="20710-129">VNETLocal</span></span>
- <span data-ttu-id="20710-130">Internet</span><span class="sxs-lookup"><span data-stu-id="20710-130">Internet</span></span>
- <span data-ttu-id="20710-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="20710-131">VirtualAppliance</span></span>
- <span data-ttu-id="20710-132">Kan</span><span class="sxs-lookup"><span data-stu-id="20710-132">Null</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20710-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="20710-133">-Profile</span></span>
<span data-ttu-id="20710-134">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="20710-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="20710-135">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="20710-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="20710-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="20710-136">-RouteName</span></span>
<span data-ttu-id="20710-137">Anger ett namn för den nya vägen som läggs till av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20710-137">Specifies a name for the new route that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20710-138">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="20710-138">-RouteTable</span></span>
<span data-ttu-id="20710-139">Anger den routningstabell till vilken denna cmdlet lägger till det nya flödet.</span><span class="sxs-lookup"><span data-stu-id="20710-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20710-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20710-140">CommonParameters</span></span>
<span data-ttu-id="20710-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20710-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20710-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20710-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20710-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20710-143">INPUTS</span></span>

## <span data-ttu-id="20710-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20710-144">OUTPUTS</span></span>

## <span data-ttu-id="20710-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20710-145">NOTES</span></span>

## <span data-ttu-id="20710-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20710-146">RELATED LINKS</span></span>

[<span data-ttu-id="20710-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="20710-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


