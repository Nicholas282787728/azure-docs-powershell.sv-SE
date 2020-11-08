---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C868DFA4-8A9D-4108-B88B-ACD7F100A63C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteConfig.md
ms.openlocfilehash: 1afd855be89f83e9591bbd180b1357e1b03952eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922382"
---
# <span data-ttu-id="2a79d-101">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2a79d-101">Add-AzRouteConfig</span></span>

## <span data-ttu-id="2a79d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a79d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a79d-103">Lägger till en väg i en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="2a79d-103">Adds a route to a route table.</span></span>

## <span data-ttu-id="2a79d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a79d-104">SYNTAX</span></span>

```
Add-AzRouteConfig -RouteTable <PSRouteTable> [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a79d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a79d-105">DESCRIPTION</span></span>
<span data-ttu-id="2a79d-106">Cmdleten **Add-AzRouteConfig** lägger till en väg till en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="2a79d-106">The **Add-AzRouteConfig** cmdlet adds a route to an Azure route table.</span></span>

## <span data-ttu-id="2a79d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a79d-107">EXAMPLES</span></span>

### <span data-ttu-id="2a79d-108">Exempel 1: lägga till en väg i en routningstabell</span><span class="sxs-lookup"><span data-stu-id="2a79d-108">Example 1: Add a route to a route table</span></span>
```
PS C:\>$RouteTable = Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01"
PS C:\> Add-AzRouteConfig -Name "Route13" -AddressPrefix 10.3.0.0/16 -NextHopType "VnetLocal" -RouteTable $RouteTable
```

<span data-ttu-id="2a79d-109">Med det första kommandot hämtas en väg tabell med namnet RouteTable01 med hjälp av Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a79d-109">The first command gets a route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="2a79d-110">Kommandot lagrar tabellen i $RouteTable variabel.</span><span class="sxs-lookup"><span data-stu-id="2a79d-110">The command stores the table in the $RouteTable variable.</span></span>

<span data-ttu-id="2a79d-111">Det andra kommandot lägger till en väg med namnet Route13 i routningstabellen som lagras i $RouteTable.</span><span class="sxs-lookup"><span data-stu-id="2a79d-111">The second command adds a route named Route13 to the route table stored in $RouteTable.</span></span>
<span data-ttu-id="2a79d-112">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2a79d-112">This route forwards packets to the local virtual network.</span></span>

### <span data-ttu-id="2a79d-113">Exempel 2: lägga till en väg till en väg tabell med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="2a79d-113">Example 2: Add a route to a route table by using the pipeline</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Add-AzRouteConfig -Name "Route02" -AddressPrefix 10.2.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
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

<span data-ttu-id="2a79d-114">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av **Get-AzRouteTable**.</span><span class="sxs-lookup"><span data-stu-id="2a79d-114">This command gets the route table named RouteTable01 by using **Get-AzRouteTable**.</span></span>
<span data-ttu-id="2a79d-115">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="2a79d-115">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2a79d-116">Den aktuella cmdleten lägger till vägen med namnet Route02 och skickar sedan resultatet till cmdleten **set-AzRouteTable** som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="2a79d-116">The current cmdlet adds the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="2a79d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a79d-117">PARAMETERS</span></span>

### <span data-ttu-id="2a79d-118">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2a79d-118">-AddressPrefix</span></span>
<span data-ttu-id="2a79d-119">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="2a79d-119">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="2a79d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a79d-120">-DefaultProfile</span></span>
<span data-ttu-id="2a79d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a79d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a79d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a79d-122">-Name</span></span>
<span data-ttu-id="2a79d-123">Anger ett namn på den väg som ska läggas till i väg tabellen.</span><span class="sxs-lookup"><span data-stu-id="2a79d-123">Specifies a name of the route to add to the route table.</span></span>

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

### <span data-ttu-id="2a79d-124">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="2a79d-124">-NextHopIpAddress</span></span>
<span data-ttu-id="2a79d-125">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2a79d-125">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="2a79d-126">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="2a79d-126">This route forwards packets to that address.</span></span>
<span data-ttu-id="2a79d-127">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="2a79d-127">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="2a79d-128">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="2a79d-128">-NextHopType</span></span>
<span data-ttu-id="2a79d-129">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="2a79d-129">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="2a79d-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2a79d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2a79d-131">Internet.</span><span class="sxs-lookup"><span data-stu-id="2a79d-131">Internet.</span></span>
<span data-ttu-id="2a79d-132">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="2a79d-132">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="2a79d-133">Ingen.</span><span class="sxs-lookup"><span data-stu-id="2a79d-133">None.</span></span>
<span data-ttu-id="2a79d-134">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="2a79d-134">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="2a79d-135">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="2a79d-135">VirtualAppliance.</span></span>
<span data-ttu-id="2a79d-136">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2a79d-136">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="2a79d-137">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="2a79d-137">VirtualNetworkGateway.</span></span>
<span data-ttu-id="2a79d-138">En Azure server-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="2a79d-138">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="2a79d-139">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="2a79d-139">VnetLocal.</span></span>
<span data-ttu-id="2a79d-140">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2a79d-140">The local virtual network.</span></span>
<span data-ttu-id="2a79d-141">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="2a79d-141">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="2a79d-142">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2a79d-142">-RouteTable</span></span>
<span data-ttu-id="2a79d-143">Anger den routningstabell till vilken denna cmdlet lägger till en väg.</span><span class="sxs-lookup"><span data-stu-id="2a79d-143">Specifies the route table to which this cmdlet adds a route.</span></span>

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

### <span data-ttu-id="2a79d-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a79d-144">-Confirm</span></span>
<span data-ttu-id="2a79d-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a79d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a79d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a79d-146">-WhatIf</span></span>
<span data-ttu-id="2a79d-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a79d-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a79d-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a79d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a79d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a79d-149">CommonParameters</span></span>
<span data-ttu-id="2a79d-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a79d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a79d-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a79d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a79d-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a79d-152">INPUTS</span></span>

### <span data-ttu-id="2a79d-153">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2a79d-153">PSRouteTable</span></span>
<span data-ttu-id="2a79d-154">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2a79d-154">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="2a79d-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a79d-155">OUTPUTS</span></span>

### <span data-ttu-id="2a79d-156">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2a79d-156">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2a79d-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a79d-157">NOTES</span></span>

## <span data-ttu-id="2a79d-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a79d-158">RELATED LINKS</span></span>

[<span data-ttu-id="2a79d-159">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2a79d-159">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="2a79d-160">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2a79d-160">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="2a79d-161">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2a79d-161">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="2a79d-162">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2a79d-162">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="2a79d-163">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2a79d-163">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)

[<span data-ttu-id="2a79d-164">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2a79d-164">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)

