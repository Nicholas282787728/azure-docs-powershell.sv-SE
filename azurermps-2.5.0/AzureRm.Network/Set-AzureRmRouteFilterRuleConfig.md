---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 0cf13aa5aa1fb558e72a4896bc810859409b5ae1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928981"
---
# <span data-ttu-id="366bf-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="366bf-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="366bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="366bf-102">SYNOPSIS</span></span>
<span data-ttu-id="366bf-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="366bf-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="366bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="366bf-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="366bf-105">DESCRIPTION</span></span>
<span data-ttu-id="366bf-106">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="366bf-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="366bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="366bf-107">EXAMPLES</span></span>

### <span data-ttu-id="366bf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="366bf-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="366bf-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="366bf-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="366bf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="366bf-110">PARAMETERS</span></span>

### <span data-ttu-id="366bf-111">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="366bf-111">-Access</span></span>
<span data-ttu-id="366bf-112">Åtkomst typen för regeln.</span><span class="sxs-lookup"><span data-stu-id="366bf-112">The access type of the rule.</span></span>
<span data-ttu-id="366bf-113">Möjliga värden är: ' Allow ', ' neka '</span><span class="sxs-lookup"><span data-stu-id="366bf-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366bf-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="366bf-114">-CommunityList</span></span>
<span data-ttu-id="366bf-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="366bf-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366bf-116">-DefaultProfile</span></span>
<span data-ttu-id="366bf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="366bf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="366bf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="366bf-118">-Force</span></span>
<span data-ttu-id="366bf-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="366bf-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="366bf-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="366bf-120">-Name</span></span>
<span data-ttu-id="366bf-121">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="366bf-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="366bf-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="366bf-122">-RouteFilter</span></span>
<span data-ttu-id="366bf-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="366bf-123">The RouteFilter</span></span>

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

### <span data-ttu-id="366bf-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="366bf-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="366bf-125">Regel typen för flödes filter regeln.</span><span class="sxs-lookup"><span data-stu-id="366bf-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="366bf-126">Möjliga värden är: ' community '</span><span class="sxs-lookup"><span data-stu-id="366bf-126">Possible values are: 'Community'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="366bf-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="366bf-127">-Confirm</span></span>
<span data-ttu-id="366bf-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="366bf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366bf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="366bf-129">-WhatIf</span></span>
<span data-ttu-id="366bf-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="366bf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="366bf-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="366bf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366bf-132">CommonParameters</span></span>
<span data-ttu-id="366bf-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366bf-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="366bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366bf-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="366bf-135">INPUTS</span></span>

### <span data-ttu-id="366bf-136">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="366bf-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="366bf-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="366bf-137">OUTPUTS</span></span>

### <span data-ttu-id="366bf-138">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="366bf-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="366bf-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="366bf-139">NOTES</span></span>

## <span data-ttu-id="366bf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="366bf-140">RELATED LINKS</span></span>

