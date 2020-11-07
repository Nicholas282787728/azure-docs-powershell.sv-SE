---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 1cb180d96b99a7dc2286c45a1d3f81a03a9cb212
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931366"
---
# <span data-ttu-id="0aea8-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0aea8-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0aea8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0aea8-102">SYNOPSIS</span></span>
<span data-ttu-id="0aea8-103">Lägger till en regel för flödes filter i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="0aea8-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aea8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0aea8-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aea8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0aea8-105">DESCRIPTION</span></span>
<span data-ttu-id="0aea8-106">Add-AzureRmRouteFilterRuleConfig cmdlet lägger till en regel för flödes filter i ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="0aea8-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="0aea8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0aea8-107">EXAMPLES</span></span>

### <span data-ttu-id="0aea8-108">--------------------------Exempel 1: lägga till en rutt filter regel i ett väg filter--------------------------</span><span class="sxs-lookup"><span data-stu-id="0aea8-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="0aea8-109">Det första kommandot får ett väg filter med namnet routefilter01 med hjälp av Get-AzureRmRouteFilter cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aea8-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="0aea8-110">Kommandot lagrar filtret i $RouteFilter variabel.</span><span class="sxs-lookup"><span data-stu-id="0aea8-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="0aea8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0aea8-111">PARAMETERS</span></span>

### <span data-ttu-id="0aea8-112">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="0aea8-112">-Access</span></span>
<span data-ttu-id="0aea8-113">Anger åtkomst för regeln för flödes filter, giltiga värden är neka eller Tillåt.</span><span class="sxs-lookup"><span data-stu-id="0aea8-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="0aea8-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="0aea8-114">-CommunityList</span></span>
<span data-ttu-id="0aea8-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="0aea8-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="0aea8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aea8-116">-DefaultProfile</span></span>
<span data-ttu-id="0aea8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0aea8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0aea8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0aea8-118">-Force</span></span>
<span data-ttu-id="0aea8-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="0aea8-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="0aea8-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="0aea8-120">-Name</span></span>
<span data-ttu-id="0aea8-121">Anger ett namn på den väg filter regel som ska läggas till i väg filtret.</span><span class="sxs-lookup"><span data-stu-id="0aea8-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="0aea8-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0aea8-122">-RouteFilter</span></span>
<span data-ttu-id="0aea8-123">Anger det väg filter där denna cmdlet lägger till en regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="0aea8-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="0aea8-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="0aea8-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="0aea8-125">Anger regel typen för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="0aea8-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="0aea8-126">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="0aea8-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="0aea8-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0aea8-127">-Confirm</span></span>
<span data-ttu-id="0aea8-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0aea8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aea8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aea8-129">-WhatIf</span></span>
<span data-ttu-id="0aea8-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0aea8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0aea8-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0aea8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aea8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aea8-132">CommonParameters</span></span>
<span data-ttu-id="0aea8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aea8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aea8-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aea8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aea8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0aea8-135">INPUTS</span></span>

### <span data-ttu-id="0aea8-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0aea8-136">PSRouteFilter</span></span>
<span data-ttu-id="0aea8-137">Parametern ' RouteFilter ' godkänner värdet av typen ' PSRouteFilter ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0aea8-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="0aea8-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0aea8-138">OUTPUTS</span></span>

### <span data-ttu-id="0aea8-139">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0aea8-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0aea8-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0aea8-140">NOTES</span></span>
<span data-ttu-id="0aea8-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="0aea8-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0aea8-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0aea8-142">RELATED LINKS</span></span>

[<span data-ttu-id="0aea8-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0aea8-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="0aea8-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0aea8-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)







[<span data-ttu-id="0aea8-145">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0aea8-145">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

