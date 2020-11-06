---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteConfig.md
ms.openlocfilehash: 7b28c50cfc53fee03d5715697a88e9356ea7664b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582339"
---
# <span data-ttu-id="67327-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="67327-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="67327-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67327-102">SYNOPSIS</span></span>
<span data-ttu-id="67327-103">Lägger till en väg i en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="67327-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67327-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67327-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67327-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67327-105">DESCRIPTION</span></span>
<span data-ttu-id="67327-106">Cmdleten **Add-AzureRmRouteConfig** lägger till en väg till en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="67327-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="67327-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67327-107">EXAMPLES</span></span>

### <span data-ttu-id="67327-108">Exempel 1: lägga till en väg i en routningstabell</span><span class="sxs-lookup"><span data-stu-id="67327-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="67327-109">Med det första kommandot hämtas en väg tabell med namnet RouteTable01 med hjälp av Get-AzureRmRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67327-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="67327-110">Kommandot lagrar tabellen i $RouteTable variabel.</span><span class="sxs-lookup"><span data-stu-id="67327-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="67327-111">Det andra kommandot lägger till en väg med namnet Route13 i routningstabellen som lagras i $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="67327-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="67327-112">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="67327-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="67327-113">Exempel 2: lägga till en väg till en väg tabell med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="67327-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
Name              : routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/routetable01
Etag              : W/"f13e1bc8-d41f-44d0-882d-b8b5a1134f59"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "route07",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"f13e1bc8-d41f-44d0-882d-b8b5a1134f59\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.2.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route13",
                        "Etag": null, 
                        "Id": null, 
                        "AddressPrefix": "10.3.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": null
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="67327-114">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="67327-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="67327-115">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="67327-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="67327-116">Den aktuella cmdleten lägger till vägen med namnet Route02 och skickar sedan resultatet till cmdleten **set-AzureRmRouteTable** som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="67327-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="67327-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67327-117">PARAMETERS</span></span>

### <span data-ttu-id="67327-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="67327-118">-AddressPrefix</span></span>
<span data-ttu-id="67327-119">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="67327-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="67327-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="67327-120">-Name</span></span>
<span data-ttu-id="67327-121">Anger ett namn på den väg som ska läggas till i väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="67327-121">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="67327-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="67327-122">-NextHopIpAddress</span></span>
<span data-ttu-id="67327-123">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="67327-123">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="67327-124">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="67327-124">This route forwards packets to that address.</span></span>
<span data-ttu-id="67327-125">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="67327-125">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="67327-126">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="67327-126">-NextHopType</span></span>
<span data-ttu-id="67327-127">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="67327-127">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="67327-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="67327-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67327-129">Internet.</span><span class="sxs-lookup"><span data-stu-id="67327-129">Internet.</span></span>
<span data-ttu-id="67327-130">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="67327-130">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="67327-131">Ingen.</span><span class="sxs-lookup"><span data-stu-id="67327-131">None.</span></span>
<span data-ttu-id="67327-132">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="67327-132">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="67327-133">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="67327-133">VirtualAppliance.</span></span>
<span data-ttu-id="67327-134">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="67327-134">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="67327-135">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="67327-135">VirtualNetworkGateway.</span></span>
<span data-ttu-id="67327-136">En Azure server-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="67327-136">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="67327-137">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="67327-137">VnetLocal.</span></span>
<span data-ttu-id="67327-138">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="67327-138">The local virtual network.</span></span>
<span data-ttu-id="67327-139">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="67327-139">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="67327-140">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="67327-140">-RouteTable</span></span>
<span data-ttu-id="67327-141">Anger den routningstabell till vilken denna cmdlet lägger till en väg.</span><span class="sxs-lookup"><span data-stu-id="67327-141">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67327-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67327-142">-DefaultProfile</span></span>
<span data-ttu-id="67327-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67327-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67327-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67327-144">CommonParameters</span></span>
<span data-ttu-id="67327-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67327-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67327-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67327-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67327-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67327-147">INPUTS</span></span>

### <span data-ttu-id="67327-148">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="67327-148">PSRouteTable</span></span>
<span data-ttu-id="67327-149">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="67327-149">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="67327-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67327-150">OUTPUTS</span></span>

### <span data-ttu-id="67327-151">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="67327-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="67327-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67327-152">NOTES</span></span>

## <span data-ttu-id="67327-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67327-153">RELATED LINKS</span></span>

[<span data-ttu-id="67327-154">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="67327-154">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="67327-155">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="67327-155">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="67327-156">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="67327-156">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="67327-157">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="67327-157">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="67327-158">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="67327-158">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="67327-159">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="67327-159">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


