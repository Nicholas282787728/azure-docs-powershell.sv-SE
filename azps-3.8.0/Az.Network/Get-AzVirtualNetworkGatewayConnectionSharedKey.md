---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090993"
---
# <span data-ttu-id="d0664-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d0664-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="d0664-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0664-102">SYNOPSIS</span></span>
<span data-ttu-id="d0664-103">Visar den delade knappen som används för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d0664-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="d0664-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0664-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0664-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0664-105">DESCRIPTION</span></span>
<span data-ttu-id="d0664-106">Visar den delade knappen som används för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="d0664-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="d0664-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0664-107">EXAMPLES</span></span>

### <span data-ttu-id="d0664-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0664-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="d0664-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0664-109">PARAMETERS</span></span>

### <span data-ttu-id="d0664-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0664-110">-DefaultProfile</span></span>
<span data-ttu-id="d0664-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0664-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0664-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0664-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0664-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0664-113">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0664-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0664-114">CommonParameters</span></span>
<span data-ttu-id="d0664-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0664-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0664-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0664-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0664-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0664-117">INPUTS</span></span>

### <span data-ttu-id="d0664-118">System. String</span><span class="sxs-lookup"><span data-stu-id="d0664-118">System.String</span></span>

## <span data-ttu-id="d0664-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0664-119">OUTPUTS</span></span>

### <span data-ttu-id="d0664-120">System. String</span><span class="sxs-lookup"><span data-stu-id="d0664-120">System.String</span></span>

## <span data-ttu-id="d0664-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0664-121">NOTES</span></span>

## <span data-ttu-id="d0664-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0664-122">RELATED LINKS</span></span>

[<span data-ttu-id="d0664-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d0664-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="d0664-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="d0664-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
