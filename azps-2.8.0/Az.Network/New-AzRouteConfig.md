---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteConfig.md
ms.openlocfilehash: 07b7d0decd196fba9cbf0a813af4d252d01dfc8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918210"
---
# <span data-ttu-id="b004d-101">New-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b004d-101">New-AzRouteConfig</span></span>

## <span data-ttu-id="b004d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b004d-102">SYNOPSIS</span></span>
<span data-ttu-id="b004d-103">Skapar ett flöde för en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="b004d-103">Creates a route for a route table.</span></span>

## <span data-ttu-id="b004d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b004d-104">SYNTAX</span></span>

```
New-AzRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b004d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b004d-105">DESCRIPTION</span></span>
<span data-ttu-id="b004d-106">Cmdleten **New-AzRouteConfig** skapar en väg för en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="b004d-106">The **New-AzRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="b004d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b004d-107">EXAMPLES</span></span>

### <span data-ttu-id="b004d-108">Exempel 1: skapa en väg</span><span class="sxs-lookup"><span data-stu-id="b004d-108">Example 1: Create a route</span></span>
```
PS C:\>$Route = New-AzRouteConfig -Name "Route07" -AddressPrefix 10.1.0.0/16 -NextHopType "VnetLocal"
PS C:\> $Route
Name              : Route07
Id                : 
Etag              : 
ProvisioningState : 
AddressPrefix     : 10.1.0.0/16
NextHopType       : VnetLocal
NextHopIpAddress  :
```

<span data-ttu-id="b004d-109">Det första kommandot skapar en väg med namnet Route07 och lagrar det sedan i $Route variabel.</span><span class="sxs-lookup"><span data-stu-id="b004d-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="b004d-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="b004d-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="b004d-111">Det andra kommandot visar vägens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="b004d-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="b004d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b004d-112">PARAMETERS</span></span>

### <span data-ttu-id="b004d-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b004d-113">-AddressPrefix</span></span>
<span data-ttu-id="b004d-114">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="b004d-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="b004d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b004d-115">-DefaultProfile</span></span>
<span data-ttu-id="b004d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b004d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b004d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b004d-117">-Name</span></span>
<span data-ttu-id="b004d-118">Anger ett namn för vägen.</span><span class="sxs-lookup"><span data-stu-id="b004d-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="b004d-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="b004d-119">-NextHopIpAddress</span></span>
<span data-ttu-id="b004d-120">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azurevirtual-nätverk.</span><span class="sxs-lookup"><span data-stu-id="b004d-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="b004d-121">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="b004d-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="b004d-122">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="b004d-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="b004d-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="b004d-123">-NextHopType</span></span>
<span data-ttu-id="b004d-124">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="b004d-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="b004d-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="b004d-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b004d-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="b004d-126">Internet.</span></span>
<span data-ttu-id="b004d-127">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="b004d-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="b004d-128">Ingen.</span><span class="sxs-lookup"><span data-stu-id="b004d-128">None.</span></span>
<span data-ttu-id="b004d-129">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="b004d-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="b004d-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="b004d-130">VirtualAppliance.</span></span>
<span data-ttu-id="b004d-131">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="b004d-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="b004d-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="b004d-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="b004d-133">En Azure server-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="b004d-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="b004d-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="b004d-134">VnetLocal.</span></span>
<span data-ttu-id="b004d-135">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="b004d-135">The local virtual network.</span></span>
<span data-ttu-id="b004d-136">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="b004d-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="b004d-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b004d-137">-Confirm</span></span>
<span data-ttu-id="b004d-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b004d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b004d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b004d-139">-WhatIf</span></span>
<span data-ttu-id="b004d-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b004d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b004d-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b004d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b004d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b004d-142">CommonParameters</span></span>
<span data-ttu-id="b004d-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b004d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b004d-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b004d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b004d-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b004d-145">INPUTS</span></span>

### <span data-ttu-id="b004d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b004d-146">System.String</span></span>

## <span data-ttu-id="b004d-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b004d-147">OUTPUTS</span></span>

### <span data-ttu-id="b004d-148">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="b004d-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="b004d-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b004d-149">NOTES</span></span>

## <span data-ttu-id="b004d-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b004d-150">RELATED LINKS</span></span>

[<span data-ttu-id="b004d-151">Add-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b004d-151">Add-AzRouteConfig</span></span>](./Add-AzRouteConfig.md)

[<span data-ttu-id="b004d-152">Get-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b004d-152">Get-AzRouteConfig</span></span>](./Get-AzRouteConfig.md)

[<span data-ttu-id="b004d-153">Remove-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b004d-153">Remove-AzRouteConfig</span></span>](./Remove-AzRouteConfig.md)

[<span data-ttu-id="b004d-154">Set-AzRouteConfig</span><span class="sxs-lookup"><span data-stu-id="b004d-154">Set-AzRouteConfig</span></span>](./Set-AzRouteConfig.md)


