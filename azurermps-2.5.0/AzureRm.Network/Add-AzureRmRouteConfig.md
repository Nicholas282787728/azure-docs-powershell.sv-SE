---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermrouteconfig
schema: 2.0.0
ms.openlocfilehash: aa5f8f71765118a2fb95117709a7fcfc83b1edcb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928753"
---
# <span data-ttu-id="803b8-101">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="803b8-101">Add-AzureRmRouteConfig</span></span>

## <span data-ttu-id="803b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="803b8-102">SYNOPSIS</span></span>
<span data-ttu-id="803b8-103">Lägger till en väg i en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="803b8-103">Adds a route to a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="803b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="803b8-104">SYNTAX</span></span>

```
Add-AzureRmRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="803b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="803b8-105">DESCRIPTION</span></span>
<span data-ttu-id="803b8-106">Cmdleten **Add-AzureRmRouteConfig** lägger till en väg till en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="803b8-106">The **Add-AzureRmRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="803b8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="803b8-107">EXAMPLES</span></span>

### <span data-ttu-id="803b8-108">Exempel 1: lägga till en väg i en routningstabell</span><span class="sxs-lookup"><span data-stu-id="803b8-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzureRmRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="803b8-109">Med det första kommandot hämtas en väg tabell med namnet RouteTable01 med hjälp av Get-AzureRmRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="803b8-109">The first command gets a route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="803b8-110">Kommandot lagrar tabellen i $RouteTable variabel.</span><span class="sxs-lookup"><span data-stu-id="803b8-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="803b8-111">Det andra kommandot lägger till en väg med namnet Route13 i routningstabellen som lagras i $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="803b8-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="803b8-112">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="803b8-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="803b8-113">Exempel 2: lägga till en väg till en väg tabell med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="803b8-113">Example 2: Add a route to a route table by using the pipeline</span></span>
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

<span data-ttu-id="803b8-114">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av **Get-AzureRmRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="803b8-114">This command gets the route table named RouteTable01 by using **Get-AzureRmRouteTable**.</span></span>
<span data-ttu-id="803b8-115">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="803b8-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="803b8-116">Den aktuella cmdleten lägger till vägen med namnet Route02 och skickar sedan resultatet till cmdleten **set-AzureRmRouteTable** som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="803b8-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="803b8-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="803b8-117">PARAMETERS</span></span>

### <span data-ttu-id="803b8-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="803b8-118">-AddressPrefix</span></span>
<span data-ttu-id="803b8-119">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="803b8-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803b8-120">-DefaultProfile</span></span>
<span data-ttu-id="803b8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="803b8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="803b8-122">-Name</span></span>
<span data-ttu-id="803b8-123">Anger ett namn på den väg som ska läggas till i väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="803b8-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="803b8-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="803b8-124">-NextHopIpAddress</span></span>
<span data-ttu-id="803b8-125">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="803b8-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="803b8-126">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="803b8-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="803b8-127">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="803b8-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="803b8-128">-NextHopType</span></span>
<span data-ttu-id="803b8-129">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="803b8-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="803b8-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="803b8-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="803b8-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="803b8-131">Internet.</span></span>
<span data-ttu-id="803b8-132">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="803b8-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="803b8-133">Ingen.</span><span class="sxs-lookup"><span data-stu-id="803b8-133">None.</span></span>
<span data-ttu-id="803b8-134">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="803b8-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="803b8-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="803b8-135">VirtualAppliance.</span></span>
<span data-ttu-id="803b8-136">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="803b8-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="803b8-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="803b8-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="803b8-138">En Azure server-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="803b8-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="803b8-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="803b8-139">VnetLocal.</span></span>
<span data-ttu-id="803b8-140">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="803b8-140">The local virtual network.</span></span>
<span data-ttu-id="803b8-141">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="803b8-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="803b8-142">-RouteTable</span></span>
<span data-ttu-id="803b8-143">Anger den routningstabell till vilken denna cmdlet lägger till en väg.</span><span class="sxs-lookup"><span data-stu-id="803b8-143">Specifies the route table to which this cmdlet adds a route.</span></span>

```yaml
Type: PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="803b8-144">-Confirm</span></span>
<span data-ttu-id="803b8-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="803b8-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="803b8-146">-WhatIf</span></span>
<span data-ttu-id="803b8-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="803b8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="803b8-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="803b8-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="803b8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803b8-149">CommonParameters</span></span>
<span data-ttu-id="803b8-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="803b8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803b8-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="803b8-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803b8-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="803b8-152">INPUTS</span></span>

### <span data-ttu-id="803b8-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="803b8-153">PSRouteTable</span></span>
<span data-ttu-id="803b8-154">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="803b8-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="803b8-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="803b8-155">OUTPUTS</span></span>

### <span data-ttu-id="803b8-156">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="803b8-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="803b8-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="803b8-157">NOTES</span></span>

## <span data-ttu-id="803b8-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="803b8-158">RELATED LINKS</span></span>

[<span data-ttu-id="803b8-159">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="803b8-159">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="803b8-160">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="803b8-160">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="803b8-161">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="803b8-161">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="803b8-162">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="803b8-162">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="803b8-163">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="803b8-163">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)

[<span data-ttu-id="803b8-164">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="803b8-164">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


