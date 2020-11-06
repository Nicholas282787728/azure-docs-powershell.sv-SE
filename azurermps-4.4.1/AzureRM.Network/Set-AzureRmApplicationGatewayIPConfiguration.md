---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4D5F469D-FF1F-4D49-AC42-26E6DECFAA26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: feeed9709833f56c42d4f3134794b96dda800ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585407"
---
# <span data-ttu-id="1f277-101">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-101">Set-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="1f277-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f277-102">SYNOPSIS</span></span>
<span data-ttu-id="1f277-103">Ändrar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="1f277-103">Modifies an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f277-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f277-104">SYNTAX</span></span>

### <span data-ttu-id="1f277-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f277-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f277-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1f277-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f277-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f277-107">DESCRIPTION</span></span>
<span data-ttu-id="1f277-108">Cmdleten **set-AzureRmApplicationGatewayIPConfiguration** ändrar en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1f277-108">The **Set-AzureRmApplicationGatewayIPConfiguration** cmdlet modifies an IP configuration.</span></span>
<span data-ttu-id="1f277-109">En IP-konfiguration innehåller det undernät där en Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="1f277-109">An IP configuration contains the subnet in which an application gateway is deployed.</span></span>

## <span data-ttu-id="1f277-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f277-110">EXAMPLES</span></span>

### <span data-ttu-id="1f277-111">Exempel 1: Ange mål tillstånd för en IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-111">Example 1: Set the goal state of an IP configuration</span></span>
```
PS C:\>$VNet = Get-AzureRmVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "AppgwSubnet01" -Subnet $Subnets
```

<span data-ttu-id="1f277-112">Det första kommandot hämtar det virtuella nätverk som heter VNet01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar det i $VNet variabeln.</span><span class="sxs-lookup"><span data-stu-id="1f277-112">The first command gets the virtual network named VNet01 that belongs to the resource group named ResourceGroup01 and stores it in the $VNet variable.</span></span>

<span data-ttu-id="1f277-113">Med det andra kommandot får du en under näts konfiguration som heter Subnet01 med $VNet och lagrar den i $Subnet-variabeln.</span><span class="sxs-lookup"><span data-stu-id="1f277-113">The second command gets the subnet configuration named Subnet01 using $VNet and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="1f277-114">Det tredje kommandot får en Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="1f277-114">The third command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1f277-115">Kommandot tillbaka anger IP-konfigurationen för den Programgateway som lagras i $AppGw till den under näts konfiguration som lagras i $Subnet.</span><span class="sxs-lookup"><span data-stu-id="1f277-115">The forth command sets the IP configuration of the application gateway stored in $AppGw to the subnet configuration stored in $Subnet.</span></span>

## <span data-ttu-id="1f277-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f277-116">PARAMETERS</span></span>

### <span data-ttu-id="1f277-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f277-117">-ApplicationGateway</span></span>
<span data-ttu-id="1f277-118">Anger ett Application Gateway-objekt som denna cmdlet associerar en IP-konfiguration med.</span><span class="sxs-lookup"><span data-stu-id="1f277-118">Specifies an application gateway object with which this cmdlet associates an IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f277-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f277-119">-Name</span></span>
<span data-ttu-id="1f277-120">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="1f277-120">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="1f277-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="1f277-121">-Subnet</span></span>
<span data-ttu-id="1f277-122">Anger under nätet.</span><span class="sxs-lookup"><span data-stu-id="1f277-122">Specifies the subnet.</span></span>
<span data-ttu-id="1f277-123">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="1f277-123">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f277-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1f277-124">-SubnetId</span></span>
<span data-ttu-id="1f277-125">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="1f277-125">Specifies the subnet ID.</span></span>
<span data-ttu-id="1f277-126">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="1f277-126">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f277-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f277-127">-DefaultProfile</span></span>
<span data-ttu-id="1f277-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f277-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f277-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f277-129">CommonParameters</span></span>
<span data-ttu-id="1f277-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f277-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f277-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f277-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f277-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f277-132">INPUTS</span></span>

### <span data-ttu-id="1f277-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f277-133">System.String</span></span>

## <span data-ttu-id="1f277-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f277-134">OUTPUTS</span></span>

### <span data-ttu-id="1f277-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1f277-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1f277-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f277-136">NOTES</span></span>

## <span data-ttu-id="1f277-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f277-137">RELATED LINKS</span></span>

[<span data-ttu-id="1f277-138">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-138">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1f277-139">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-139">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1f277-140">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-140">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1f277-141">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-141">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="1f277-142">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f277-142">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)


