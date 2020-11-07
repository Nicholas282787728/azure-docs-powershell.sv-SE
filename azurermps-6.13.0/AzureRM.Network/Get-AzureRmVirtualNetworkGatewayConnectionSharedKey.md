---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: ECC5C079-C9A0-4159-A039-EE216897D686
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: c2a1a63abb18f5f47ed155f24e8ac73a7bae83ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756155"
---
# <span data-ttu-id="df9d7-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="df9d7-101">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="df9d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="df9d7-103">Visar den delade knappen som används för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="df9d7-103">Displays the shared key used for the connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df9d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df9d7-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df9d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df9d7-105">DESCRIPTION</span></span>
<span data-ttu-id="df9d7-106">Visar den delade knappen som används för anslutningen.</span><span class="sxs-lookup"><span data-stu-id="df9d7-106">Displays the shared key used for the connection.</span></span>

## <span data-ttu-id="df9d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df9d7-107">EXAMPLES</span></span>

### <span data-ttu-id="df9d7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="df9d7-108">Example 1</span></span>
```
Get-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name 1 -ResourceGroupName P2SVPNGateway
xxxxxx
```

## <span data-ttu-id="df9d7-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df9d7-109">PARAMETERS</span></span>

### <span data-ttu-id="df9d7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9d7-110">-DefaultProfile</span></span>
<span data-ttu-id="df9d7-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="df9d7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df9d7-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="df9d7-112">-Name</span></span>
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

### <span data-ttu-id="df9d7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9d7-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="df9d7-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9d7-114">CommonParameters</span></span>
<span data-ttu-id="df9d7-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9d7-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9d7-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df9d7-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9d7-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df9d7-117">INPUTS</span></span>

### <span data-ttu-id="df9d7-118">System. String</span><span class="sxs-lookup"><span data-stu-id="df9d7-118">System.String</span></span>

## <span data-ttu-id="df9d7-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df9d7-119">OUTPUTS</span></span>

### <span data-ttu-id="df9d7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="df9d7-120">System.String</span></span>

## <span data-ttu-id="df9d7-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df9d7-121">NOTES</span></span>

## <span data-ttu-id="df9d7-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df9d7-122">RELATED LINKS</span></span>
