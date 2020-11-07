---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
ms.openlocfilehash: ed33d1a683e10e0e39d0b722dec92b7f7ba11254
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929353"
---
# <span data-ttu-id="fe108-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="fe108-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="fe108-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fe108-102">SYNOPSIS</span></span>
<span data-ttu-id="fe108-103">Visar tillgängliga slut punkts tjänster för plats.</span><span class="sxs-lookup"><span data-stu-id="fe108-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe108-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fe108-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe108-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fe108-105">DESCRIPTION</span></span>
<span data-ttu-id="fe108-106">Get-AzureRmVirtualNetworkAvailableEndpointService visar tillgängliga slut punkts tjänster på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="fe108-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="fe108-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fe108-107">EXAMPLES</span></span>

### <span data-ttu-id="fe108-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fe108-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="fe108-109">Hämtar tillgängliga slut punkts tjänster i regionen region.</span><span class="sxs-lookup"><span data-stu-id="fe108-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="fe108-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fe108-110">PARAMETERS</span></span>

### <span data-ttu-id="fe108-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe108-111">-DefaultProfile</span></span>
<span data-ttu-id="fe108-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fe108-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe108-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="fe108-113">-Location</span></span>
<span data-ttu-id="fe108-114">Den plats där slut punkts tjänsterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="fe108-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe108-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe108-115">CommonParameters</span></span>
<span data-ttu-id="fe108-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe108-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe108-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe108-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe108-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fe108-118">INPUTS</span></span>

### <span data-ttu-id="fe108-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fe108-119">System.String</span></span>

## <span data-ttu-id="fe108-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fe108-120">OUTPUTS</span></span>

### <span data-ttu-id="fe108-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. commands. Network, version = 4.2.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fe108-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fe108-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fe108-122">NOTES</span></span>

## <span data-ttu-id="fe108-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fe108-123">RELATED LINKS</span></span>

