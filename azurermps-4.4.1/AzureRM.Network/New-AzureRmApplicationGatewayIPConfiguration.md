---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 076965d0f63a8c28742cf9853068b9e020403a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583251"
---
# <span data-ttu-id="85799-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85799-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="85799-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="85799-102">SYNOPSIS</span></span>
<span data-ttu-id="85799-103">Skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="85799-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85799-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="85799-104">SYNTAX</span></span>

### <span data-ttu-id="85799-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85799-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85799-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85799-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85799-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="85799-107">DESCRIPTION</span></span>
<span data-ttu-id="85799-108">Cmdleten **New-AzureRmApplicationGatewayIPConfiguration** skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="85799-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="85799-109">IP-konfigurationen innehåller det undernät då Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="85799-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="85799-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="85799-110">EXAMPLES</span></span>

### <span data-ttu-id="85799-111">Exempel 1: skapa en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="85799-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="85799-112">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="85799-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="85799-113">Det andra kommandot får under nätets konfiguration för det undernät som det virtuella nätverket i föregående kommando tillhör och lagrar det i $Subnet variabeln.</span><span class="sxs-lookup"><span data-stu-id="85799-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="85799-114">Det tredje kommandot skapar IP-konfigurationen med $Subnet.</span><span class="sxs-lookup"><span data-stu-id="85799-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="85799-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="85799-115">PARAMETERS</span></span>

### <span data-ttu-id="85799-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="85799-116">-Name</span></span>
<span data-ttu-id="85799-117">Anger namnet på den IP-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="85799-117">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="85799-118">-Undernät</span><span class="sxs-lookup"><span data-stu-id="85799-118">-Subnet</span></span>
<span data-ttu-id="85799-119">Anger ett under näts objekt.</span><span class="sxs-lookup"><span data-stu-id="85799-119">Specifies the subnet object.</span></span>
<span data-ttu-id="85799-120">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="85799-120">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="85799-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="85799-121">-SubnetId</span></span>
<span data-ttu-id="85799-122">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="85799-122">Specifies the subnet ID.</span></span>
<span data-ttu-id="85799-123">Det här är det undernät där programgatewayen distribueras.</span><span class="sxs-lookup"><span data-stu-id="85799-123">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="85799-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85799-124">-DefaultProfile</span></span>
<span data-ttu-id="85799-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="85799-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85799-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85799-126">CommonParameters</span></span>
<span data-ttu-id="85799-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85799-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85799-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85799-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85799-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="85799-129">INPUTS</span></span>

### <span data-ttu-id="85799-130">System. String</span><span class="sxs-lookup"><span data-stu-id="85799-130">System.String</span></span>

## <span data-ttu-id="85799-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="85799-131">OUTPUTS</span></span>

### <span data-ttu-id="85799-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85799-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="85799-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="85799-133">NOTES</span></span>

## <span data-ttu-id="85799-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="85799-134">RELATED LINKS</span></span>

[<span data-ttu-id="85799-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85799-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85799-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85799-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85799-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85799-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="85799-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85799-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


