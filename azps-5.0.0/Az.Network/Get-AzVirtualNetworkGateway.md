---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271570"
---
# <span data-ttu-id="47722-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="47722-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47722-102">SYNOPSIS</span></span>
<span data-ttu-id="47722-103">Hämtar en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="47722-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="47722-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47722-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47722-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47722-105">DESCRIPTION</span></span>
<span data-ttu-id="47722-106">Den virtuella Nätverksgatewayen är det objekt som representerar din gateway i Azure.</span><span class="sxs-lookup"><span data-stu-id="47722-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="47722-107">Cmdleten **Get-AzVirtualNetworkGateway** returnerar gatewayens objekt i Azure baserat på namn-och resurs grupp namn.</span><span class="sxs-lookup"><span data-stu-id="47722-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="47722-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47722-108">EXAMPLES</span></span>

### <span data-ttu-id="47722-109">Exempel 1: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="47722-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="47722-110">Returnerar objektet för den virtuella Nätverksgatewayen med namnet "myGateway1" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="47722-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="47722-111">Exempel 2: skaffa en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="47722-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="47722-112">Returnerar alla virtuella nätverksgateway som börjar med "Gateway" i resurs gruppen "myRG"</span><span class="sxs-lookup"><span data-stu-id="47722-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="47722-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47722-113">PARAMETERS</span></span>

### <span data-ttu-id="47722-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47722-114">-DefaultProfile</span></span>
<span data-ttu-id="47722-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47722-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47722-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="47722-116">-Name</span></span>
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

### <span data-ttu-id="47722-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47722-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="47722-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47722-118">CommonParameters</span></span>
<span data-ttu-id="47722-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47722-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47722-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47722-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47722-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47722-121">INPUTS</span></span>

### <span data-ttu-id="47722-122">System. String</span><span class="sxs-lookup"><span data-stu-id="47722-122">System.String</span></span>

## <span data-ttu-id="47722-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47722-123">OUTPUTS</span></span>

### <span data-ttu-id="47722-124">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="47722-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47722-125">NOTES</span></span>

## <span data-ttu-id="47722-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47722-126">RELATED LINKS</span></span>

[<span data-ttu-id="47722-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="47722-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="47722-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="47722-130">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="47722-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="47722-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
