---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: c555ce87f746d7f976add4fc49fb14b661a276d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585943"
---
# <span data-ttu-id="c8c92-101">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c92-101">Add-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="c8c92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8c92-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c92-103">Lägger till en regel för flödes filter i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="c8c92-103">Adds a route filter rule to a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8c92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8c92-104">SYNTAX</span></span>

```
Add-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c92-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8c92-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c92-106">Add-AzureRmRouteFilterRuleConfig cmdlet lägger till en regel för flödes filter i ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="c8c92-106">The Add-AzureRmRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="c8c92-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8c92-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c92-108">Exempel 1: lägga till en rutt filter regel i ett väg filter</span><span class="sxs-lookup"><span data-stu-id="c8c92-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzureRmRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzureRmRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="c8c92-109">Det första kommandot får ett väg filter med namnet routefilter01 med hjälp av Get-AzureRmRouteFilter cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c92-109">The first command gets a route filter named routefilter01 by using the Get-AzureRmRouteFilter cmdlet.</span></span>
<span data-ttu-id="c8c92-110">Kommandot lagrar filtret i $RouteFilter variabel.</span><span class="sxs-lookup"><span data-stu-id="c8c92-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="c8c92-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8c92-111">PARAMETERS</span></span>

### <span data-ttu-id="c8c92-112">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="c8c92-112">-Access</span></span>
<span data-ttu-id="c8c92-113">Anger åtkomst för regeln för flödes filter, giltiga värden är neka eller Tillåt.</span><span class="sxs-lookup"><span data-stu-id="c8c92-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c92-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="c8c92-114">-CommunityList</span></span>
<span data-ttu-id="c8c92-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="c8c92-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="c8c92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c92-116">-DefaultProfile</span></span>
<span data-ttu-id="c8c92-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c92-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8c92-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c8c92-118">-Force</span></span>
<span data-ttu-id="c8c92-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="c8c92-119">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c92-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8c92-120">-Name</span></span>
<span data-ttu-id="c8c92-121">Anger ett namn på den väg filter regel som ska läggas till i väg filtret.</span><span class="sxs-lookup"><span data-stu-id="c8c92-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c92-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="c8c92-122">-RouteFilter</span></span>
<span data-ttu-id="c8c92-123">Anger det väg filter där denna cmdlet lägger till en regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="c8c92-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="c8c92-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="c8c92-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="c8c92-125">Anger regel typen för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="c8c92-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="c8c92-126">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="c8c92-126">Valid values are: Community</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c92-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8c92-127">-Confirm</span></span>
<span data-ttu-id="c8c92-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8c92-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c92-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c92-129">-WhatIf</span></span>
<span data-ttu-id="c8c92-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8c92-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8c92-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8c92-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8c92-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c92-132">CommonParameters</span></span>
<span data-ttu-id="c8c92-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c92-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c92-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c92-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c92-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8c92-135">INPUTS</span></span>

### <span data-ttu-id="c8c92-136">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c8c92-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="c8c92-137">Parametrar: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8c92-137">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="c8c92-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8c92-138">OUTPUTS</span></span>

### <span data-ttu-id="c8c92-139">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c8c92-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="c8c92-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8c92-140">NOTES</span></span>
<span data-ttu-id="c8c92-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="c8c92-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c8c92-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8c92-142">RELATED LINKS</span></span>

[<span data-ttu-id="c8c92-143">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c8c92-143">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="c8c92-144">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c8c92-144">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="c8c92-145">New-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="c8c92-145">New-AzureRmRouteFilterRuleConfigConfig</span></span>](./New-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="c8c92-146">Remove-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="c8c92-146">Remove-AzureRmRouteFilterRuleConfigConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="c8c92-147">Set-AzureRmRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="c8c92-147">Set-AzureRmRouteFilterRuleConfigConfig</span></span>](./Set-AzureRmRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="c8c92-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="c8c92-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)

