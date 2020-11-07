---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c7912f1a5d0539a0c81aff930cd94cb944e45bb7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922321"
---
# <span data-ttu-id="408f1-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="408f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="408f1-102">SYNOPSIS</span></span>
<span data-ttu-id="408f1-103">Hämtar IP-konfigurationen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="408f1-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="408f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="408f1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="408f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="408f1-105">DESCRIPTION</span></span>
<span data-ttu-id="408f1-106">Cmdleten **Get-AzApplicationGatewayIPConfiguration** hämtar IP-konfigurationen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="408f1-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="408f1-107">IP-konfigurationen innehåller det undernät där Application Gateway distribueras.</span><span class="sxs-lookup"><span data-stu-id="408f1-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="408f1-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="408f1-108">EXAMPLES</span></span>

### <span data-ttu-id="408f1-109">Exempel 1: skaffa en specifik IP-konfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="408f1-110">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln. Det andra kommandot får en IP-konfiguration med namnet GateSubnet01 från den gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="408f1-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="408f1-111">Exempel 2: Hämta en lista med IP-konfigurationer</span><span class="sxs-lookup"><span data-stu-id="408f1-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="408f1-112">Det första kommandot får en Programgateway och lagrar den i $AppGw variabeln. Det andra kommandot får en lista över alla IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="408f1-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="408f1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="408f1-113">PARAMETERS</span></span>

### <span data-ttu-id="408f1-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="408f1-114">-ApplicationGateway</span></span>
<span data-ttu-id="408f1-115">Anger det Application Gateway-objekt som innehåller IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="408f1-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="408f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408f1-116">-DefaultProfile</span></span>
<span data-ttu-id="408f1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="408f1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="408f1-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="408f1-118">-Name</span></span>
<span data-ttu-id="408f1-119">Anger namnet på den IP-konfiguration som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="408f1-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="408f1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408f1-120">CommonParameters</span></span>
<span data-ttu-id="408f1-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408f1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408f1-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408f1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408f1-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="408f1-123">INPUTS</span></span>

### <span data-ttu-id="408f1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="408f1-124">System.String</span></span>

## <span data-ttu-id="408f1-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="408f1-125">OUTPUTS</span></span>

### <span data-ttu-id="408f1-126">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="408f1-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="408f1-127">NOTES</span></span>

## <span data-ttu-id="408f1-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="408f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="408f1-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="408f1-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="408f1-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="408f1-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="408f1-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


