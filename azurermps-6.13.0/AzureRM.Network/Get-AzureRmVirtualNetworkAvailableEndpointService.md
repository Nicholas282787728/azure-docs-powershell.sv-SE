---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 7499c96ec887673faaf93cf2901e4705b63604b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586324"
---
# <span data-ttu-id="6000f-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="6000f-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="6000f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6000f-102">SYNOPSIS</span></span>
<span data-ttu-id="6000f-103">Visar tillgängliga slut punkts tjänster för plats.</span><span class="sxs-lookup"><span data-stu-id="6000f-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6000f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6000f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6000f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6000f-105">DESCRIPTION</span></span>
<span data-ttu-id="6000f-106">Get-AzureRmVirtualNetworkAvailableEndpointService visar tillgängliga slut punkts tjänster på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="6000f-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="6000f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6000f-107">EXAMPLES</span></span>

### <span data-ttu-id="6000f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6000f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="6000f-109">Hämtar tillgängliga slut punkts tjänster i regionen region.</span><span class="sxs-lookup"><span data-stu-id="6000f-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="6000f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6000f-110">PARAMETERS</span></span>

### <span data-ttu-id="6000f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6000f-111">-DefaultProfile</span></span>
<span data-ttu-id="6000f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6000f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6000f-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="6000f-113">-Location</span></span>
<span data-ttu-id="6000f-114">Den plats där slut punkts tjänsterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="6000f-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="6000f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6000f-115">CommonParameters</span></span>
<span data-ttu-id="6000f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6000f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6000f-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6000f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6000f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6000f-118">INPUTS</span></span>

### <span data-ttu-id="6000f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="6000f-119">System.String</span></span>

## <span data-ttu-id="6000f-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6000f-120">OUTPUTS</span></span>

### <span data-ttu-id="6000f-121">Microsoft. Azure. commands. Networks. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="6000f-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="6000f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6000f-122">NOTES</span></span>

## <span data-ttu-id="6000f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6000f-123">RELATED LINKS</span></span>
