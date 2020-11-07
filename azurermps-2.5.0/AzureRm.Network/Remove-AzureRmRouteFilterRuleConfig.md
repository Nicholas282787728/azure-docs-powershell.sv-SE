---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930138"
---
# <span data-ttu-id="54477-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54477-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="54477-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54477-102">SYNOPSIS</span></span>
<span data-ttu-id="54477-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="54477-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54477-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54477-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54477-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54477-105">DESCRIPTION</span></span>
<span data-ttu-id="54477-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="54477-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="54477-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54477-107">EXAMPLES</span></span>

### <span data-ttu-id="54477-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="54477-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="54477-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="54477-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="54477-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54477-110">PARAMETERS</span></span>

### <span data-ttu-id="54477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54477-111">-DefaultProfile</span></span>
<span data-ttu-id="54477-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54477-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54477-113">-Force</span><span class="sxs-lookup"><span data-stu-id="54477-113">-Force</span></span>
<span data-ttu-id="54477-114">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="54477-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="54477-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="54477-115">-Name</span></span>
<span data-ttu-id="54477-116">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="54477-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="54477-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="54477-117">-RouteFilter</span></span>
<span data-ttu-id="54477-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="54477-118">The RouteFilter</span></span>

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

### <span data-ttu-id="54477-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54477-119">-Confirm</span></span>
<span data-ttu-id="54477-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54477-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54477-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54477-121">-WhatIf</span></span>
<span data-ttu-id="54477-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54477-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54477-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54477-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54477-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54477-124">CommonParameters</span></span>
<span data-ttu-id="54477-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54477-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54477-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54477-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54477-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54477-127">INPUTS</span></span>

### <span data-ttu-id="54477-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="54477-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="54477-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54477-129">OUTPUTS</span></span>

### <span data-ttu-id="54477-130">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="54477-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="54477-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54477-131">NOTES</span></span>

## <span data-ttu-id="54477-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54477-132">RELATED LINKS</span></span>

