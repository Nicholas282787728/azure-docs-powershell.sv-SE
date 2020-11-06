---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: bb51d5bfb1ccc81aa10c7aecc4d7a255fc0f60d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575994"
---
# <span data-ttu-id="48b4b-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="48b4b-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="48b4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="48b4b-103">Skapar ett flöde för en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="48b4b-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48b4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48b4b-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig -Name <String> [-AddressPrefix <String>] -NextHopType <String>
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48b4b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="48b4b-106">Cmdleten **New-AzureRmRouteConfig** skapar en väg för en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="48b4b-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="48b4b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="48b4b-108">Exempel 1: skapa en väg</span><span class="sxs-lookup"><span data-stu-id="48b4b-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzureRmRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="48b4b-109">Det första kommandot skapar en väg med namnet Route07 och lagrar det sedan i $Route variabel.</span><span class="sxs-lookup"><span data-stu-id="48b4b-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="48b4b-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="48b4b-110">This route forwards packets to the local virtual network.</span></span>

<span data-ttu-id="48b4b-111">Det andra kommandot visar vägens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="48b4b-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="48b4b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48b4b-112">PARAMETERS</span></span>

### <span data-ttu-id="48b4b-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="48b4b-113">-AddressPrefix</span></span>
<span data-ttu-id="48b4b-114">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="48b4b-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="48b4b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="48b4b-115">-Name</span></span>
<span data-ttu-id="48b4b-116">Anger ett namn för vägen.</span><span class="sxs-lookup"><span data-stu-id="48b4b-116">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="48b4b-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="48b4b-117">-NextHopIpAddress</span></span>
<span data-ttu-id="48b4b-118">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azurevirtual-nätverk.</span><span class="sxs-lookup"><span data-stu-id="48b4b-118">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="48b4b-119">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="48b4b-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="48b4b-120">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="48b4b-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="48b4b-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="48b4b-121">-NextHopType</span></span>
<span data-ttu-id="48b4b-122">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="48b4b-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="48b4b-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="48b4b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48b4b-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="48b4b-124">Internet.</span></span>
<span data-ttu-id="48b4b-125">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="48b4b-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="48b4b-126">Ingen.</span><span class="sxs-lookup"><span data-stu-id="48b4b-126">None.</span></span>
<span data-ttu-id="48b4b-127">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="48b4b-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="48b4b-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="48b4b-128">VirtualAppliance.</span></span>
<span data-ttu-id="48b4b-129">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="48b4b-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="48b4b-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="48b4b-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="48b4b-131">En Azure server-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="48b4b-131">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="48b4b-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="48b4b-132">VnetLocal.</span></span>
<span data-ttu-id="48b4b-133">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="48b4b-133">The local virtual network.</span></span>
<span data-ttu-id="48b4b-134">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="48b4b-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, None, VirtualAppliance, VirtualNetworkGateway, VnetLocal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b4b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b4b-135">-DefaultProfile</span></span>
<span data-ttu-id="48b4b-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48b4b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b4b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b4b-137">CommonParameters</span></span>
<span data-ttu-id="48b4b-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b4b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b4b-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b4b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b4b-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48b4b-140">INPUTS</span></span>

## <span data-ttu-id="48b4b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48b4b-141">OUTPUTS</span></span>

### <span data-ttu-id="48b4b-142">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="48b4b-142">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="48b4b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48b4b-143">NOTES</span></span>

## <span data-ttu-id="48b4b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48b4b-144">RELATED LINKS</span></span>

[<span data-ttu-id="48b4b-145">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="48b4b-145">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="48b4b-146">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="48b4b-146">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="48b4b-147">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="48b4b-147">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="48b4b-148">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="48b4b-148">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


