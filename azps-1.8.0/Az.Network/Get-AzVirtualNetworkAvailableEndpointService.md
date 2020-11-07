---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 2de970201456f941d8b35d40c569c41e114468c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748211"
---
# <span data-ttu-id="ca5dd-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="ca5dd-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="ca5dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca5dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5dd-103">Visar tillgängliga slut punkts tjänster för plats.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="ca5dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca5dd-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca5dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca5dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ca5dd-106">Get-AzVirtualNetworkAvailableEndpointService visar tillgängliga slut punkts tjänster på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="ca5dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca5dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ca5dd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ca5dd-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="ca5dd-109">Hämtar tillgängliga slut punkts tjänster i regionen region.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="ca5dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca5dd-110">PARAMETERS</span></span>

### <span data-ttu-id="ca5dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5dd-111">-DefaultProfile</span></span>
<span data-ttu-id="ca5dd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca5dd-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="ca5dd-113">-Location</span></span>
<span data-ttu-id="ca5dd-114">Den plats där slut punkts tjänsterna hämtas från.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="ca5dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5dd-115">CommonParameters</span></span>
<span data-ttu-id="ca5dd-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5dd-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca5dd-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5dd-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca5dd-118">INPUTS</span></span>

### <span data-ttu-id="ca5dd-119">System. String</span><span class="sxs-lookup"><span data-stu-id="ca5dd-119">System.String</span></span>

## <span data-ttu-id="ca5dd-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca5dd-120">OUTPUTS</span></span>

### <span data-ttu-id="ca5dd-121">Microsoft. Azure. commands. Networks. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="ca5dd-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="ca5dd-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca5dd-122">NOTES</span></span>

## <span data-ttu-id="ca5dd-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca5dd-123">RELATED LINKS</span></span>
