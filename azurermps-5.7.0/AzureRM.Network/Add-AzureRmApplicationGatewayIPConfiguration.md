---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: cc84daecf4c98a48bb37ff0edd38f1136960a273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581115"
---
# <span data-ttu-id="d9168-101">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9168-101">Add-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d9168-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9168-102">SYNOPSIS</span></span>
<span data-ttu-id="d9168-103">Lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d9168-103">Adds an IP configuration to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9168-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9168-104">SYNTAX</span></span>

### <span data-ttu-id="d9168-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9168-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9168-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d9168-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9168-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9168-107">DESCRIPTION</span></span>
<span data-ttu-id="d9168-108">Cmdleten **Add-AzureRmApplicationGatewayIPConfiguration** lägger till en IP-konfiguration till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d9168-108">The **Add-AzureRmApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="d9168-109">IP-konfigurationer innehåller det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="d9168-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="d9168-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9168-110">EXAMPLES</span></span>

### <span data-ttu-id="d9168-111">Exempel 1: lägga till en virtuell nätverks konfiguration i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="d9168-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzureRmVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="d9168-112">Det första kommandot skapar ett virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="d9168-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="d9168-113">Det andra kommandot skapar ett undernät med det skapade virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="d9168-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="d9168-114">Det tredje kommandot får programgatewayen och lagras i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="d9168-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d9168-115">Med kommandot fouth lägger du till IP-konfigurationen till den Programgateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d9168-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d9168-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9168-116">PARAMETERS</span></span>

### <span data-ttu-id="d9168-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9168-117">-ApplicationGateway</span></span>
<span data-ttu-id="d9168-118">Anger den Programgateway som denna cmdlet lägger till en IP-konfiguration för.</span><span class="sxs-lookup"><span data-stu-id="d9168-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="d9168-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9168-119">-DefaultProfile</span></span>
<span data-ttu-id="d9168-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9168-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9168-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9168-121">-Name</span></span>
<span data-ttu-id="d9168-122">Anger namnet på den IP-konfiguration som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="d9168-122">Specifies the name of the IP configuration to add.</span></span>

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

### <span data-ttu-id="d9168-123">-Undernät</span><span class="sxs-lookup"><span data-stu-id="d9168-123">-Subnet</span></span>
<span data-ttu-id="d9168-124">Anger ett undernät.</span><span class="sxs-lookup"><span data-stu-id="d9168-124">Specifies a subnet.</span></span>
<span data-ttu-id="d9168-125">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="d9168-125">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="d9168-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d9168-126">-SubnetId</span></span>
<span data-ttu-id="d9168-127">Anger ett nät-ID.</span><span class="sxs-lookup"><span data-stu-id="d9168-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="d9168-128">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="d9168-128">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="d9168-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9168-129">CommonParameters</span></span>
<span data-ttu-id="d9168-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9168-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9168-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9168-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9168-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9168-132">INPUTS</span></span>

### <span data-ttu-id="d9168-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d9168-133">System.String</span></span>

## <span data-ttu-id="d9168-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9168-134">OUTPUTS</span></span>

### <span data-ttu-id="d9168-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d9168-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d9168-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9168-136">NOTES</span></span>

## <span data-ttu-id="d9168-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9168-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9168-138">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9168-138">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d9168-139">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9168-139">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d9168-140">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9168-140">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d9168-141">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9168-141">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


