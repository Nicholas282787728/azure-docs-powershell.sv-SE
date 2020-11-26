---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: d1e05a13ee0f8b31f92c78cd71c5a8dd5e94153c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258754"
---
# <span data-ttu-id="ac3b2-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ac3b2-101">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="ac3b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3b2-103">Visar den delade knappen som används för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="ac3b2-103">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="ac3b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac3b2-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac3b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac3b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ac3b2-106">Visar den delade knappen som används för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="ac3b2-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="ac3b2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac3b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ac3b2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ac3b2-108">Example 1</span></span>
```
Get-AzVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="ac3b2-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac3b2-109">PARAMETERS</span></span>

### <span data-ttu-id="ac3b2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3b2-110">-DefaultProfile</span></span>
<span data-ttu-id="ac3b2-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac3b2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac3b2-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac3b2-112">-Name</span></span>
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

### <span data-ttu-id="ac3b2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac3b2-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ac3b2-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3b2-114">CommonParameters</span></span>
<span data-ttu-id="ac3b2-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac3b2-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3b2-116">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac3b2-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3b2-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac3b2-117">INPUTS</span></span>

### <span data-ttu-id="ac3b2-118">System. String</span><span class="sxs-lookup"><span data-stu-id="ac3b2-118">System.String</span></span>

## <span data-ttu-id="ac3b2-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac3b2-119">OUTPUTS</span></span>

### <span data-ttu-id="ac3b2-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ac3b2-120">System.String</span></span>

## <span data-ttu-id="ac3b2-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac3b2-121">NOTES</span></span>

## <span data-ttu-id="ac3b2-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac3b2-122">RELATED LINKS</span></span>

[<span data-ttu-id="ac3b2-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ac3b2-123">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="ac3b2-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="ac3b2-124">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)