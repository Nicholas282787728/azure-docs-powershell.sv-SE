---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: bcd4ba14a14fdacdcdaa0ea85ec8059d2639bdc6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922221"
---
# <span data-ttu-id="6de0f-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="6de0f-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="6de0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6de0f-102">SYNOPSIS</span></span>
<span data-ttu-id="6de0f-103">Visar tillgängliga slut punkts tjänster för plats.</span><span class="sxs-lookup"><span data-stu-id="6de0f-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="6de0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6de0f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6de0f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6de0f-105">DESCRIPTION</span></span>
<span data-ttu-id="6de0f-106">Get-AzVirtualNetworkAvailableEndpointService visar tillgängliga slut punkts tjänster på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="6de0f-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="6de0f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6de0f-107">EXAMPLES</span></span>

### <span data-ttu-id="6de0f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6de0f-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="6de0f-109">Hämtar tillgängliga slut punkts tjänster i regionen region.</span><span class="sxs-lookup"><span data-stu-id="6de0f-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="6de0f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6de0f-110">PARAMETERS</span></span>

### <span data-ttu-id="6de0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de0f-111">-DefaultProfile</span></span>
<span data-ttu-id="6de0f-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6de0f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de0f-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="6de0f-113">-Location</span></span>
<span data-ttu-id="6de0f-114">Den plats där slut punkts tjänsterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="6de0f-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="6de0f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de0f-115">CommonParameters</span></span>
<span data-ttu-id="6de0f-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de0f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de0f-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de0f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de0f-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6de0f-118">INPUTS</span></span>

### <span data-ttu-id="6de0f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="6de0f-119">System.String</span></span>

## <span data-ttu-id="6de0f-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6de0f-120">OUTPUTS</span></span>

### <span data-ttu-id="6de0f-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. commands. Network, version = 4.2.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6de0f-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6de0f-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6de0f-122">NOTES</span></span>

## <span data-ttu-id="6de0f-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6de0f-123">RELATED LINKS</span></span>

