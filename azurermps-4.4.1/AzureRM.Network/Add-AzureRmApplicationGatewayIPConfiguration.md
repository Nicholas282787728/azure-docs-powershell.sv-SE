---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 98e2249c3577d49a140d31b4287507e0e46185f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582351"
---
# <span data-ttu-id="65a6c-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a6c-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="65a6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="65a6c-103">Lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="65a6c-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65a6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65a6c-104">SYNTAX</span></span>

### <span data-ttu-id="65a6c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="65a6c-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65a6c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="65a6c-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65a6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65a6c-107">DESCRIPTION</span></span>
<span data-ttu-id="65a6c-108">Cmdleten **Add-AzureRmApplicationGatewayIPConfiguration** lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="65a6c-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="65a6c-109">IP-konfigurationer innehåller det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="65a6c-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="65a6c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65a6c-110">EXAMPLES</span></span>

### <span data-ttu-id="65a6c-111">Exempel 1: lägga till en virtuell nätverks konfiguration i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="65a6c-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="65a6c-112">Det första kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="65a6c-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="65a6c-113">Det andra kommandot skapar ett undernät med det skapade virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="65a6c-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="65a6c-114">Det tredje kommandot får programgatewayen och lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="65a6c-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="65a6c-115">Med kommandot fouth lägger du till IP-konfigurationen till den Programgateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="65a6c-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="65a6c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65a6c-116">PARAMETERS</span></span>

### <span data-ttu-id="65a6c-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65a6c-117">-ApplicationGateway</span></span>
<span data-ttu-id="65a6c-118">Anger den Programgateway som denna cmdlet lägger till en IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="65a6c-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="65a6c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="65a6c-119">-Name</span></span>
<span data-ttu-id="65a6c-120">Anger namnet på den IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="65a6c-120">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="65a6c-121">-Undernät</span><span class="sxs-lookup"><span data-stu-id="65a6c-121">-Subnet</span></span>
<span data-ttu-id="65a6c-122">Anger ett undernät.</span><span class="sxs-lookup"><span data-stu-id="65a6c-122">Specifies a subnet.</span></span>
<span data-ttu-id="65a6c-123">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="65a6c-123">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="65a6c-124">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="65a6c-124">-SubnetId</span></span>
<span data-ttu-id="65a6c-125">Anger ett nät-ID.</span><span class="sxs-lookup"><span data-stu-id="65a6c-125">Specifies a subnet ID.</span></span>
<span data-ttu-id="65a6c-126">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="65a6c-126">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="65a6c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a6c-127">-DefaultProfile</span></span>
<span data-ttu-id="65a6c-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65a6c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65a6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a6c-129">CommonParameters</span></span>
<span data-ttu-id="65a6c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a6c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a6c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a6c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65a6c-132">INPUTS</span></span>

### <span data-ttu-id="65a6c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65a6c-133">System.String</span></span>

## <span data-ttu-id="65a6c-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65a6c-134">OUTPUTS</span></span>

### <span data-ttu-id="65a6c-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65a6c-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65a6c-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65a6c-136">NOTES</span></span>

## <span data-ttu-id="65a6c-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65a6c-137">RELATED LINKS</span></span>

[<span data-ttu-id="65a6c-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a6c-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="65a6c-139">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a6c-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="65a6c-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a6c-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="65a6c-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="65a6c-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


