---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayipconfiguration
schema: 2.0.0
ms.openlocfilehash: 09986be8ccc8dce8eaec522c501fe3f98ff03c56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931330"
---
# <span data-ttu-id="b2125-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b2125-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2125-102">SYNOPSIS</span></span>
<span data-ttu-id="b2125-103">Hämtar IP-konfigurationen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b2125-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2125-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2125-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2125-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2125-105">DESCRIPTION</span></span>
<span data-ttu-id="b2125-106">Cmdleten **Get-AzureRmApplicationGatewayIPConfiguration** hämtar IP-konfigurationen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b2125-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="b2125-107">IP-konfigurationen innehåller det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="b2125-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="b2125-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2125-108">EXAMPLES</span></span>

### <span data-ttu-id="b2125-109">Exempel 1: skaffa en specifik IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b2125-110">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln. Det andra kommandot får en IP-konfiguration med namnet GateSubnet01 från den gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b2125-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="b2125-111">Exempel 2: Hämta en lista med IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="b2125-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="b2125-112">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln. Det andra kommandot får en lista över alla IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="b2125-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="b2125-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2125-113">PARAMETERS</span></span>

### <span data-ttu-id="b2125-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b2125-114">-ApplicationGateway</span></span>
<span data-ttu-id="b2125-115">Anger det Application Gateway-objekt som innehåller IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2125-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="b2125-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2125-116">-DefaultProfile</span></span>
<span data-ttu-id="b2125-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2125-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2125-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2125-118">-Name</span></span>
<span data-ttu-id="b2125-119">Anger namnet på den IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="b2125-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2125-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2125-120">CommonParameters</span></span>
<span data-ttu-id="b2125-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2125-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2125-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2125-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2125-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2125-123">INPUTS</span></span>

### <span data-ttu-id="b2125-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b2125-124">System.String</span></span>

## <span data-ttu-id="b2125-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2125-125">OUTPUTS</span></span>

### <span data-ttu-id="b2125-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b2125-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2125-127">NOTES</span></span>

## <span data-ttu-id="b2125-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2125-128">RELATED LINKS</span></span>

[<span data-ttu-id="b2125-129">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b2125-130">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b2125-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b2125-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b2125-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


