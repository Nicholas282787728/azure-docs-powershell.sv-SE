---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: d3a309d99dff493e2440618d87c20b1a543e2ed9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929278"
---
# <span data-ttu-id="505b2-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="505b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="505b2-102">SYNOPSIS</span></span>
<span data-ttu-id="505b2-103">Ändrar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="505b2-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="505b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="505b2-104">SYNTAX</span></span>

### <span data-ttu-id="505b2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="505b2-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="505b2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="505b2-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="505b2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="505b2-107">DESCRIPTION</span></span>
<span data-ttu-id="505b2-108">Cmdleten **set-AzureRmApplicationGatewayIPConfiguration** ändrar en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="505b2-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="505b2-109">En IP-konfiguration innehåller det undernät där en Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="505b2-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="505b2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="505b2-110">EXAMPLES</span></span>

### <span data-ttu-id="505b2-111">Exempel 1: Ange mål tillstånd för en IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="505b2-112">Det första kommandot hämtar det virtuella nätverk som heter VNet01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="505b2-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="505b2-113">Med det andra kommandot får du en under näts konfiguration som heter Subnet01 med $VNet och lagrar den i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="505b2-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="505b2-114">Det tredje kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="505b2-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="505b2-115">Kommandot tillbaka anger IP-konfigurationen för den Programgateway som lagras i $AppGw till den under näts konfiguration som lagras i $Subnet.</span><span class="sxs-lookup"><span data-stu-id="505b2-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="505b2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="505b2-116">PARAMETERS</span></span>

### <span data-ttu-id="505b2-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505b2-117">-ApplicationGateway</span></span>
<span data-ttu-id="505b2-118">Anger ett Application Gateway-objekt som denna cmdlet associerar en IP-konfiguration med.</span><span class="sxs-lookup"><span data-stu-id="505b2-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="505b2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505b2-119">-DefaultProfile</span></span>
<span data-ttu-id="505b2-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="505b2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="505b2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="505b2-121">-Name</span></span>
<span data-ttu-id="505b2-122">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="505b2-122">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="505b2-123">-Undernät</span><span class="sxs-lookup"><span data-stu-id="505b2-123">-Subnet</span></span>
<span data-ttu-id="505b2-124">Anger under nätet.</span><span class="sxs-lookup"><span data-stu-id="505b2-124">Specifies the subnet.</span></span>
<span data-ttu-id="505b2-125">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="505b2-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505b2-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="505b2-126">-SubnetId</span></span>
<span data-ttu-id="505b2-127">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="505b2-127">Specifies the subnet ID.</span></span>
<span data-ttu-id="505b2-128">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="505b2-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505b2-129">CommonParameters</span></span>
<span data-ttu-id="505b2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="505b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505b2-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="505b2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505b2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="505b2-132">INPUTS</span></span>

### <span data-ttu-id="505b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="505b2-133">System.String</span></span>

## <span data-ttu-id="505b2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="505b2-134">OUTPUTS</span></span>

### <span data-ttu-id="505b2-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="505b2-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="505b2-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="505b2-136">NOTES</span></span>

## <span data-ttu-id="505b2-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="505b2-137">RELATED LINKS</span></span>

[<span data-ttu-id="505b2-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="505b2-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="505b2-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="505b2-141">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="505b2-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="505b2-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

