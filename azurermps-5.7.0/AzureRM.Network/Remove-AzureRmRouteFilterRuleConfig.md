---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 59a8ff1467bf70cea2eafe2117850d3423236f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757402"
---
# <span data-ttu-id="bd84d-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bd84d-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="bd84d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd84d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd84d-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="bd84d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd84d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd84d-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd84d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd84d-105">DESCRIPTION</span></span>
<span data-ttu-id="bd84d-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="bd84d-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="bd84d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd84d-107">EXAMPLES</span></span>

### <span data-ttu-id="bd84d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd84d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bd84d-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="bd84d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bd84d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd84d-110">PARAMETERS</span></span>

### <span data-ttu-id="bd84d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd84d-111">-DefaultProfile</span></span>
<span data-ttu-id="bd84d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd84d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd84d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bd84d-113">-Force</span></span>
<span data-ttu-id="bd84d-114">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="bd84d-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd84d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd84d-115">-Name</span></span>
<span data-ttu-id="bd84d-116">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="bd84d-116">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd84d-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd84d-117">-RouteFilter</span></span>
<span data-ttu-id="bd84d-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd84d-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd84d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd84d-119">-Confirm</span></span>
<span data-ttu-id="bd84d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd84d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd84d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd84d-121">-WhatIf</span></span>
<span data-ttu-id="bd84d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd84d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd84d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd84d-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd84d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd84d-124">CommonParameters</span></span>
<span data-ttu-id="bd84d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd84d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd84d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd84d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd84d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd84d-127">INPUTS</span></span>

### <span data-ttu-id="bd84d-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="bd84d-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="bd84d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd84d-129">OUTPUTS</span></span>

### <span data-ttu-id="bd84d-130">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="bd84d-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="bd84d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd84d-131">NOTES</span></span>

## <span data-ttu-id="bd84d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd84d-132">RELATED LINKS</span></span>

