---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 356764CF-A860-432A-907A-9058CEB2BF8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermrouteconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteConfig.md
ms.openlocfilehash: ba5a389bd726822c24931fecb631f6c70cf7ce48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576879"
---
# <span data-ttu-id="248e6-101">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="248e6-101">New-AzureRmRouteConfig</span></span>

## <span data-ttu-id="248e6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="248e6-102">SYNOPSIS</span></span>
<span data-ttu-id="248e6-103">Skapar ett flöde för en väg tabell.</span><span class="sxs-lookup"><span data-stu-id="248e6-103">Creates a route for a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="248e6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="248e6-104">SYNTAX</span></span>

```
New-AzureRmRouteConfig [-Name <String>] [-AddressPrefix <String>] [-NextHopType <String>]
 [-NextHopIpAddress <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="248e6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="248e6-105">DESCRIPTION</span></span>
<span data-ttu-id="248e6-106">Cmdleten **New-AzureRmRouteConfig** skapar en väg för en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="248e6-106">The **New-AzureRmRouteConfig** cmdlet creates a route for an Azure route table.</span></span>

## <span data-ttu-id="248e6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="248e6-107">EXAMPLES</span></span>

### <span data-ttu-id="248e6-108">Exempel 1: skapa en väg</span><span class="sxs-lookup"><span data-stu-id="248e6-108">Example 1: Create a route</span></span>
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

<span data-ttu-id="248e6-109">Det första kommandot skapar en väg med namnet Route07 och lagrar det sedan i $Route variabel.</span><span class="sxs-lookup"><span data-stu-id="248e6-109">The first command creates a route named Route07, and then stores it in the $Route variable.</span></span>
<span data-ttu-id="248e6-110">Den här vägen vidarebefordrar paket till det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="248e6-110">This route forwards packets to the local virtual network.</span></span>
<span data-ttu-id="248e6-111">Det andra kommandot visar vägens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="248e6-111">The second command displays the properties of the route.</span></span>

## <span data-ttu-id="248e6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="248e6-112">PARAMETERS</span></span>

### <span data-ttu-id="248e6-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="248e6-113">-AddressPrefix</span></span>
<span data-ttu-id="248e6-114">Anger destinationen, i CIDR-format (Classless Interdomain Routing), som vägen gäller för.</span><span class="sxs-lookup"><span data-stu-id="248e6-114">Specifies the destination, in Classless Interdomain Routing (CIDR) format, to which the route applies.</span></span>

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

### <span data-ttu-id="248e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="248e6-115">-DefaultProfile</span></span>
<span data-ttu-id="248e6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="248e6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="248e6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="248e6-117">-Name</span></span>
<span data-ttu-id="248e6-118">Anger ett namn för vägen.</span><span class="sxs-lookup"><span data-stu-id="248e6-118">Specifies a name for the route.</span></span>

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

### <span data-ttu-id="248e6-119">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="248e6-119">-NextHopIpAddress</span></span>
<span data-ttu-id="248e6-120">Anger IP-adressen för en virtuell apparat som du lägger till i ditt Azurevirtual-nätverk.</span><span class="sxs-lookup"><span data-stu-id="248e6-120">Specifies the IP address of a virtual appliance that you add to your Azurevirtual network.</span></span>
<span data-ttu-id="248e6-121">Den här vägen vidarebefordrar paket till den adressen.</span><span class="sxs-lookup"><span data-stu-id="248e6-121">This route forwards packets to that address.</span></span>
<span data-ttu-id="248e6-122">Ange endast den här parametern om du anger ett värde för VirtualAppliance för parametern *NextHopType* .</span><span class="sxs-lookup"><span data-stu-id="248e6-122">Specify this parameter only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="248e6-123">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="248e6-123">-NextHopType</span></span>
<span data-ttu-id="248e6-124">Anger hur den här vägen vidarebefordrar paket.</span><span class="sxs-lookup"><span data-stu-id="248e6-124">Specifies how this route forwards packets.</span></span>
<span data-ttu-id="248e6-125">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="248e6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="248e6-126">Internet.</span><span class="sxs-lookup"><span data-stu-id="248e6-126">Internet.</span></span>
<span data-ttu-id="248e6-127">Standard Internet Gateway tillhandahålls av Azure.</span><span class="sxs-lookup"><span data-stu-id="248e6-127">The default Internet gateway provided by Azure.</span></span> 
- <span data-ttu-id="248e6-128">Ingen.</span><span class="sxs-lookup"><span data-stu-id="248e6-128">None.</span></span>
<span data-ttu-id="248e6-129">Om du anger det här värdet vidarebefordras inte paket.</span><span class="sxs-lookup"><span data-stu-id="248e6-129">If you specify this value, the route does not forward packets.</span></span> 
- <span data-ttu-id="248e6-130">VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="248e6-130">VirtualAppliance.</span></span>
<span data-ttu-id="248e6-131">En virtuell enhet som du lägger till i ditt Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="248e6-131">A virtual appliance that you add to your Azure virtual network.</span></span> 
- <span data-ttu-id="248e6-132">VirtualNetworkGateway.</span><span class="sxs-lookup"><span data-stu-id="248e6-132">VirtualNetworkGateway.</span></span>
<span data-ttu-id="248e6-133">En Azure server-till-Server-Gateway för virtuella privata nätverk.</span><span class="sxs-lookup"><span data-stu-id="248e6-133">An Azure server-to-server virtual private network gateway.</span></span> 
- <span data-ttu-id="248e6-134">VnetLocal.</span><span class="sxs-lookup"><span data-stu-id="248e6-134">VnetLocal.</span></span>
<span data-ttu-id="248e6-135">Det lokala virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="248e6-135">The local virtual network.</span></span>
<span data-ttu-id="248e6-136">Om du har två undernät, 10.1.0.0/16 och 10.2.0.0/16 i samma virtuella nätverk, väljer du ett värde för VnetLocal för varje undernät att vidarekoppla till det andra under nätet.</span><span class="sxs-lookup"><span data-stu-id="248e6-136">If you have two subnets, 10.1.0.0/16 and 10.2.0.0/16 in the same virtual network, select a value of VnetLocal for each subnet to forward to the other subnet.</span></span>

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

### <span data-ttu-id="248e6-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="248e6-137">-Confirm</span></span>
<span data-ttu-id="248e6-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="248e6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="248e6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="248e6-139">-WhatIf</span></span>
<span data-ttu-id="248e6-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="248e6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="248e6-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="248e6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="248e6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="248e6-142">CommonParameters</span></span>
<span data-ttu-id="248e6-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="248e6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="248e6-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="248e6-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="248e6-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="248e6-145">INPUTS</span></span>

### <span data-ttu-id="248e6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="248e6-146">System.String</span></span>

## <span data-ttu-id="248e6-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="248e6-147">OUTPUTS</span></span>

### <span data-ttu-id="248e6-148">Microsoft. Azure. commands. Networks. Models. PSRoute</span><span class="sxs-lookup"><span data-stu-id="248e6-148">Microsoft.Azure.Commands.Network.Models.PSRoute</span></span>

## <span data-ttu-id="248e6-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="248e6-149">NOTES</span></span>

## <span data-ttu-id="248e6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="248e6-150">RELATED LINKS</span></span>

[<span data-ttu-id="248e6-151">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="248e6-151">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="248e6-152">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="248e6-152">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="248e6-153">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="248e6-153">Remove-AzureRmRouteConfig</span></span>](./Remove-AzureRmRouteConfig.md)

[<span data-ttu-id="248e6-154">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="248e6-154">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


