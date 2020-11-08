---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 625f293e669c8e4209aeed957aaa669954ff8c7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091000"
---
# <span data-ttu-id="ecafa-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="ecafa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecafa-102">SYNOPSIS</span></span>
<span data-ttu-id="ecafa-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="ecafa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecafa-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecafa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecafa-105">DESCRIPTION</span></span>
<span data-ttu-id="ecafa-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="ecafa-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="ecafa-107">Cmdleten **Get-AzVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="ecafa-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="ecafa-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecafa-108">EXAMPLES</span></span>

### <span data-ttu-id="ecafa-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="ecafa-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "myGateway1" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="ecafa-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="ecafa-111">2: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-111">2: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="ecafa-112">Returnerar alla virtuella nätverksgateway som börjar med "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="ecafa-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="ecafa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecafa-113">PARAMETERS</span></span>

### <span data-ttu-id="ecafa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecafa-114">-DefaultProfile</span></span>
<span data-ttu-id="ecafa-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecafa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecafa-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="ecafa-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ecafa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecafa-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="ecafa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecafa-118">CommonParameters</span></span>
<span data-ttu-id="ecafa-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecafa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecafa-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecafa-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecafa-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecafa-121">INPUTS</span></span>

### <span data-ttu-id="ecafa-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ecafa-122">System.String</span></span>

## <span data-ttu-id="ecafa-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecafa-123">OUTPUTS</span></span>

### <span data-ttu-id="ecafa-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="ecafa-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecafa-125">NOTES</span></span>

## <span data-ttu-id="ecafa-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecafa-126">RELATED LINKS</span></span>

[<span data-ttu-id="ecafa-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ecafa-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ecafa-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ecafa-130">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="ecafa-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ecafa-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
