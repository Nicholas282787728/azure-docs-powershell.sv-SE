---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6E967F9C-949E-4485-9B57-FC4F523D5DC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteConfig.md
ms.openlocfilehash: a86e5346078bd1a8c9be924cdeac3b94fab907dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575963"
---
# <span data-ttu-id="ef927-101">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ef927-101">Set-AzureRmRouteConfig</span></span>

## <span data-ttu-id="ef927-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef927-102">SYNOPSIS</span></span>
<span data-ttu-id="ef927-103">Anger mål tillstånd för ett flöde.</span><span class="sxs-lookup"><span data-stu-id="ef927-103">Sets the goal state for a route.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef927-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef927-104">SYNTAX</span></span>

```
Set-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-AddressPrefix <String>]
 -NextHopType <String> [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef927-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef927-105">DESCRIPTION</span></span>
<span data-ttu-id="ef927-106">Cmdleten **set-AzureRmRouteConfig** anger mål tillståndet för en Azure-väg.</span><span class="sxs-lookup"><span data-stu-id="ef927-106">The **Set-AzureRmRouteConfig** cmdlet sets the goal state for an Azure route.</span></span>

## <span data-ttu-id="ef927-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef927-107">EXAMPLES</span></span>

### <span data-ttu-id="ef927-108">Exempel 1: ändra ett flöde</span><span class="sxs-lookup"><span data-stu-id="ef927-108">Example 1: Modify a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Set-AzureRmRouteConfig -Name "Route02" -AddressPrefix 10.4.0.0/16 -NextHopType VnetLocal | Set-AzureRmRouteTable
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

<span data-ttu-id="ef927-109">Det här kommandot hämtar routningstabellen med namnet RouteTable01 med hjälp av Get-AzureRmRouteTable cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef927-109">This command gets the route table named RouteTable01 by using the Get-AzureRmRouteTable cmdlet.</span></span>
<span data-ttu-id="ef927-110">Kommandot skickar tabellen till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ef927-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef927-111">Den aktuella cmdleten ändrar vägen med namnet Route02 och skickar sedan resultatet till cmdleten **set-AzureRmRouteTable** som uppdaterar tabellen så att den återspeglar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="ef927-111">The current cmdlet modifies the route named Route02, and then passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>

## <span data-ttu-id="ef927-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef927-112">PARAMETERS</span></span>

### <span data-ttu-id="ef927-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ef927-113">-AddressPrefix</span></span>
<span data-ttu-id="ef927-114">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="ef927-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="ef927-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef927-115">-Name</span></span>
<span data-ttu-id="ef927-116">Anger namnet på den väg som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ef927-116">Specifies the name of the route that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ef927-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="ef927-117">-NextHopIpAddress</span></span>
<span data-ttu-id="ef927-118">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="ef927-118">Specifies the IP address of a virtual appliance that you add to your Azure virtual network.</span></span>
<span data-ttu-id="ef927-119">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="ef927-119">This route forwards packets to that address.</span></span>
<span data-ttu-id="ef927-120">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="ef927-120">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="ef927-121">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="ef927-121">-NextHopType</span></span>
<span data-ttu-id="ef927-122">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="ef927-122">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="ef927-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ef927-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef927-124">Internet.</span><span class="sxs-lookup"><span data-stu-id="ef927-124">Internet.</span></span>
<span data-ttu-id="ef927-125">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="ef927-125">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="ef927-126">Ingen.</span><span class="sxs-lookup"><span data-stu-id="ef927-126">None.</span></span>
<span data-ttu-id="ef927-127">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="ef927-127">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="ef927-128">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="ef927-128">VirtualAppliance.</span></span>
<span data-ttu-id="ef927-129">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="ef927-129">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="ef927-130">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="ef927-130">VirtualNetworkGateway.</span></span>
<span data-ttu-id="ef927-131">En Azureserver-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="ef927-131">An Azureserver-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="ef927-132">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="ef927-132">VnetLocal.</span></span>
<span data-ttu-id="ef927-133">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="ef927-133">The local virtual network.</span></span>
<span data-ttu-id="ef927-134">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="ef927-134">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="ef927-135">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="ef927-135">-RouteTable</span></span>
<span data-ttu-id="ef927-136">Anger den routningstabell som den här vägen är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="ef927-136">Specifies the route table with which this route is associated.</span></span>

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

### <span data-ttu-id="ef927-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef927-137">-DefaultProfile</span></span>
<span data-ttu-id="ef927-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef927-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef927-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef927-139">CommonParameters</span></span>
<span data-ttu-id="ef927-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef927-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef927-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef927-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef927-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef927-142">INPUTS</span></span>

### <span data-ttu-id="ef927-143">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ef927-143">PSRouteTable</span></span>
<span data-ttu-id="ef927-144">Parametern ' RouteTable ' godkänner värdet av typen ' PSRouteTable ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ef927-144">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="ef927-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef927-145">OUTPUTS</span></span>

### <span data-ttu-id="ef927-146">Microsoft. Azure. commands. Networks. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="ef927-146">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="ef927-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef927-147">NOTES</span></span>

## <span data-ttu-id="ef927-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef927-148">RELATED LINKS</span></span>

[<span data-ttu-id="ef927-149">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ef927-149">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="ef927-150">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ef927-150">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="ef927-151">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ef927-151">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="ef927-152">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="ef927-152">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)


