---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c0dad1f63f8a203a9f1b8aaeb75a2be13bfc61f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918669"
---
# <span data-ttu-id="20f02-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f02-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="20f02-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20f02-102">SYNOPSIS</span></span>
<span data-ttu-id="20f02-103">Skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="20f02-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="20f02-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20f02-104">SYNTAX</span></span>

### <span data-ttu-id="20f02-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="20f02-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20f02-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="20f02-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20f02-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20f02-107">DESCRIPTION</span></span>
<span data-ttu-id="20f02-108">Cmdleten **New-AzApplicationGatewayIPConfiguration** skapar en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="20f02-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="20f02-109">IP-konfigurationen innehåller det undernät då Programgateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="20f02-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="20f02-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20f02-110">EXAMPLES</span></span>

### <span data-ttu-id="20f02-111">Exempel 1: skapa en IP-konfiguration för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="20f02-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="20f02-112">Det första kommandot får ett virtuellt nätverk som heter VNet01 som tillhör resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="20f02-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="20f02-113">Det andra kommandot får under nätets konfiguration för det undernät som det virtuella nätverket i föregående kommando tillhör och lagrar det i $Subnet variabeln.</span><span class="sxs-lookup"><span data-stu-id="20f02-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="20f02-114">Det tredje kommandot skapar IP-konfigurationen med $Subnet.</span><span class="sxs-lookup"><span data-stu-id="20f02-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="20f02-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20f02-115">PARAMETERS</span></span>

### <span data-ttu-id="20f02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f02-116">-DefaultProfile</span></span>
<span data-ttu-id="20f02-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20f02-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f02-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="20f02-118">-Name</span></span>
<span data-ttu-id="20f02-119">Anger namnet på den IP-konfiguration som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="20f02-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="20f02-120">-Undernät</span><span class="sxs-lookup"><span data-stu-id="20f02-120">-Subnet</span></span>
<span data-ttu-id="20f02-121">Anger ett under näts objekt.</span><span class="sxs-lookup"><span data-stu-id="20f02-121">Specifies the subnet object.</span></span>
<span data-ttu-id="20f02-122">Det här är det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="20f02-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="20f02-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="20f02-123">-SubnetId</span></span>
<span data-ttu-id="20f02-124">Anger nät-ID.</span><span class="sxs-lookup"><span data-stu-id="20f02-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="20f02-125">Det här är det undernät där programgatewayen distribueras.</span><span class="sxs-lookup"><span data-stu-id="20f02-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="20f02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f02-126">CommonParameters</span></span>
<span data-ttu-id="20f02-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f02-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f02-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f02-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20f02-129">INPUTS</span></span>

### <span data-ttu-id="20f02-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="20f02-130">None</span></span>

## <span data-ttu-id="20f02-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20f02-131">OUTPUTS</span></span>

### <span data-ttu-id="20f02-132">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f02-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="20f02-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20f02-133">NOTES</span></span>

## <span data-ttu-id="20f02-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20f02-134">RELATED LINKS</span></span>

[<span data-ttu-id="20f02-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f02-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="20f02-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f02-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="20f02-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f02-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="20f02-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="20f02-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)

