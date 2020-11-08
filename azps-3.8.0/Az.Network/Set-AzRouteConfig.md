---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteConfig.md
ms.openlocfilehash: d96f65586162eac330aa6309476dd00aea152920
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090812"
---
# <span data-ttu-id="2f07e-101">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2f07e-101">Set-AzRouteConfig</span></span>

## <span data-ttu-id="2f07e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f07e-102">SYNOPSIS</span></span>
<span data-ttu-id="2f07e-103">Uppdaterar en flödes konfiguration för en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="2f07e-103">Updates a route configuration for a route table.</span></span>

## <span data-ttu-id="2f07e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f07e-104">SYNTAX</span></span>

```
Set-AzRouteConfig -RouteTable <PSRouteTable> [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f07e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f07e-105">DESCRIPTION</span></span>
<span data-ttu-id="2f07e-106">Cmdleten **set-AzRouteConfig** uppdaterar en vägkälla för en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="2f07e-106">The **Set-AzRouteConfig** cmdlet updates a route configuration for a route table.</span></span>

## <span data-ttu-id="2f07e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f07e-107">EXAMPLES</span></span>

### <span data-ttu-id="2f07e-108">Exempel 1: ändra ett flöde</span><span class="sxs-lookup"><span data-stu-id="2f07e-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzRouteTable
Name              : Routetable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"58c2922e-9efe-4554-a457-956ef44bc718"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/Routetable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      },
                      {
                        "Name": "route02",
                        "Etag": "W/\"58c2922e-9efe-4554-a457-956ef44bc718\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/routetable01/routes/route02",
                        "AddressPrefix": "10.4.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="2f07e-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av Get-AzRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f07e-109">This command gets the route table named RouteTable01 by using the Get-AzRouteTable cmdlet.</span></span>
<span data-ttu-id="2f07e-110">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="2f07e-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2f07e-111">Den aktuella cmdleten ändrar vägen med namnet Route02 och skickar sedan resultatet till cmdleten **set-AzRouteTable** som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="2f07e-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="2f07e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f07e-112">PARAMETERS</span></span>

### <span data-ttu-id="2f07e-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2f07e-113">-AddressPrefix</span></span>
<span data-ttu-id="2f07e-114">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="2f07e-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f07e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f07e-115">-DefaultProfile</span></span>
<span data-ttu-id="2f07e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f07e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f07e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f07e-117">-Name</span></span>
<span data-ttu-id="2f07e-118">Anger namnet på den väg som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="2f07e-118">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2f07e-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="2f07e-119">-NextHopIpAddress</span></span>
<span data-ttu-id="2f07e-120">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2f07e-120">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="2f07e-121">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="2f07e-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="2f07e-122">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="2f07e-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f07e-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="2f07e-123">-NextHopType</span></span>
<span data-ttu-id="2f07e-124">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="2f07e-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="2f07e-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2f07e-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f07e-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="2f07e-126">Internet.</span></span>
<span data-ttu-id="2f07e-127">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="2f07e-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="2f07e-128">Ingen.</span><span class="sxs-lookup"><span data-stu-id="2f07e-128">None.</span></span>
<span data-ttu-id="2f07e-129">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="2f07e-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="2f07e-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="2f07e-130">VirtualAppliance.</span></span>
<span data-ttu-id="2f07e-131">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="2f07e-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="2f07e-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="2f07e-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="2f07e-133">En Azureserver-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="2f07e-133">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="2f07e-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="2f07e-134">VnetLocal.</span></span>
<span data-ttu-id="2f07e-135">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2f07e-135">The local virtual network.</span></span>
<span data-ttu-id="2f07e-136">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="2f07e-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f07e-137">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="2f07e-137">-RouteTable</span></span>
<span data-ttu-id="2f07e-138">Anger den routningstabell som den här vägen är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="2f07e-138">Specifies the route table with which this route is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f07e-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f07e-139">-Confirm</span></span>
<span data-ttu-id="2f07e-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f07e-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f07e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f07e-141">-WhatIf</span></span>
<span data-ttu-id="2f07e-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f07e-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f07e-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f07e-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f07e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f07e-144">CommonParameters</span></span>
<span data-ttu-id="2f07e-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f07e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f07e-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f07e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f07e-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f07e-147">INPUTS</span></span>

### <span data-ttu-id="2f07e-148">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f07e-148">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

### <span data-ttu-id="2f07e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="2f07e-149">System.String</span></span>

## <span data-ttu-id="2f07e-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f07e-150">OUTPUTS</span></span>

### <span data-ttu-id="2f07e-151">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="2f07e-151">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="2f07e-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f07e-152">NOTES</span></span>

## <span data-ttu-id="2f07e-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f07e-153">RELATED LINKS</span></span>

[<span data-ttu-id="2f07e-154">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2f07e-154">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="2f07e-155">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2f07e-155">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="2f07e-156">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2f07e-156">New-AzRouteConfig</span></span>](./New-AzRouteConfig.md)

[<span data-ttu-id="2f07e-157">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="2f07e-157">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)


