---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 4c2d5c4e3c46c79caa4bd8b47fdc178da4fd6450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748210"
---
# <span data-ttu-id="52d17-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="52d17-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52d17-102">SYNOPSIS</span></span>
<span data-ttu-id="52d17-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="52d17-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="52d17-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52d17-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52d17-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52d17-105">DESCRIPTION</span></span>
<span data-ttu-id="52d17-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="52d17-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="52d17-107">Cmdleten **Get-AzVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="52d17-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="52d17-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52d17-108">EXAMPLES</span></span>

### <span data-ttu-id="52d17-109">1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="52d17-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="52d17-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "myGateway1" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="52d17-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="52d17-111">2: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="52d17-111">2: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="52d17-112">Returnerar alla virtuella nätverksgateway som börjar med "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="52d17-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="52d17-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52d17-113">PARAMETERS</span></span>

### <span data-ttu-id="52d17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d17-114">-DefaultProfile</span></span>
<span data-ttu-id="52d17-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52d17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52d17-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="52d17-116">-Name</span></span>
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

### <span data-ttu-id="52d17-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52d17-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="52d17-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d17-118">CommonParameters</span></span>
<span data-ttu-id="52d17-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52d17-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d17-120">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52d17-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d17-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52d17-121">INPUTS</span></span>

### <span data-ttu-id="52d17-122">System. String</span><span class="sxs-lookup"><span data-stu-id="52d17-122">System.String</span></span>

## <span data-ttu-id="52d17-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52d17-123">OUTPUTS</span></span>

### <span data-ttu-id="52d17-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="52d17-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52d17-125">NOTES</span></span>

## <span data-ttu-id="52d17-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52d17-126">RELATED LINKS</span></span>

[<span data-ttu-id="52d17-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="52d17-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="52d17-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="52d17-130">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="52d17-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52d17-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
