---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 204ecf05f0781649f441399c7a9b6acfbfbd8cdd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927590"
---
# <span data-ttu-id="f706d-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f706d-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="f706d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f706d-102">SYNOPSIS</span></span>
<span data-ttu-id="f706d-103">Lägger till en regel för flödes filter i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="f706d-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="f706d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f706d-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f706d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f706d-105">DESCRIPTION</span></span>
<span data-ttu-id="f706d-106">Add-AzRouteFilterRuleConfig cmdlet lägger till en regel för flödes filter i ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="f706d-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="f706d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f706d-107">EXAMPLES</span></span>

### <span data-ttu-id="f706d-108">Exempel 1: lägga till en rutt filter regel i ett väg filter</span><span class="sxs-lookup"><span data-stu-id="f706d-108">Example 1: Add a route filter rule to a route filter</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="f706d-109">Det första kommandot får ett väg filter med namnet routefilter01 med hjälp av Get-AzRouteFilter cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f706d-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="f706d-110">Kommandot lagrar filtret i $RouteFilter variabel.</span><span class="sxs-lookup"><span data-stu-id="f706d-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="f706d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f706d-111">PARAMETERS</span></span>

### <span data-ttu-id="f706d-112">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="f706d-112">-Access</span></span>
<span data-ttu-id="f706d-113">Anger åtkomst för regeln för flödes filter, giltiga värden är neka eller Tillåt.</span><span class="sxs-lookup"><span data-stu-id="f706d-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="f706d-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="f706d-114">-CommunityList</span></span>
<span data-ttu-id="f706d-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="f706d-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f706d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f706d-116">-DefaultProfile</span></span>
<span data-ttu-id="f706d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f706d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f706d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f706d-118">-Force</span></span>
<span data-ttu-id="f706d-119">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="f706d-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f706d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="f706d-120">-Name</span></span>
<span data-ttu-id="f706d-121">Anger ett namn på den väg filter regel som ska läggas till i väg filtret.</span><span class="sxs-lookup"><span data-stu-id="f706d-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="f706d-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-122">-RouteFilter</span></span>
<span data-ttu-id="f706d-123">Anger det väg filter där denna cmdlet lägger till en regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="f706d-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="f706d-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="f706d-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="f706d-125">Anger regel typen för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="f706d-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="f706d-126">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="f706d-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="f706d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f706d-127">-Confirm</span></span>
<span data-ttu-id="f706d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f706d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f706d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f706d-129">-WhatIf</span></span>
<span data-ttu-id="f706d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f706d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f706d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f706d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f706d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f706d-132">CommonParameters</span></span>
<span data-ttu-id="f706d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f706d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f706d-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f706d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f706d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f706d-135">INPUTS</span></span>

### <span data-ttu-id="f706d-136">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f706d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f706d-137">OUTPUTS</span></span>

### <span data-ttu-id="f706d-138">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f706d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f706d-139">NOTES</span></span>
<span data-ttu-id="f706d-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="f706d-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f706d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f706d-141">RELATED LINKS</span></span>

[<span data-ttu-id="f706d-142">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f706d-142">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f706d-143">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f706d-143">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f706d-144">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f706d-144">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f706d-145">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f706d-145">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f706d-146">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-146">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f706d-147">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-147">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f706d-148">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-148">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="f706d-149">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f706d-149">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
