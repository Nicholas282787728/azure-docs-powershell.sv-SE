---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 96122c68317166f078d40be8cee9d0124c4d713e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755828"
---
# <span data-ttu-id="34532-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="34532-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="34532-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="34532-102">SYNOPSIS</span></span>
<span data-ttu-id="34532-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="34532-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34532-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="34532-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34532-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="34532-105">DESCRIPTION</span></span>
<span data-ttu-id="34532-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="34532-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="34532-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="34532-107">EXAMPLES</span></span>

### <span data-ttu-id="34532-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="34532-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="34532-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="34532-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="34532-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="34532-110">PARAMETERS</span></span>

### <span data-ttu-id="34532-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34532-111">-DefaultProfile</span></span>
<span data-ttu-id="34532-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="34532-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34532-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="34532-113">-Name</span></span>
<span data-ttu-id="34532-114">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="34532-114">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34532-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="34532-115">-RouteFilter</span></span>
<span data-ttu-id="34532-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="34532-116">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34532-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34532-117">CommonParameters</span></span>
<span data-ttu-id="34532-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34532-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34532-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34532-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34532-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="34532-120">INPUTS</span></span>

### <span data-ttu-id="34532-121">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="34532-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="34532-122">Parametrar: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="34532-122">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="34532-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="34532-123">OUTPUTS</span></span>

### <span data-ttu-id="34532-124">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="34532-124">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="34532-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="34532-125">NOTES</span></span>

## <span data-ttu-id="34532-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="34532-126">RELATED LINKS</span></span>
