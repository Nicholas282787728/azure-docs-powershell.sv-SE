---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 910b432382eb24f6c5eaf77d3e0c7fe3dc547413
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922374"
---
# <span data-ttu-id="86a14-101">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86a14-101">Add-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="86a14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86a14-102">SYNOPSIS</span></span>
<span data-ttu-id="86a14-103">Lägger till en regel för flödes filter i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="86a14-103">Adds a route filter rule to a route filter.</span></span>

## <span data-ttu-id="86a14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86a14-104">SYNTAX</span></span>

```
Add-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86a14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86a14-105">DESCRIPTION</span></span>
<span data-ttu-id="86a14-106">Add-AzRouteFilterRuleConfig cmdlet lägger till en regel för flödes filter i ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="86a14-106">The Add-AzRouteFilterRuleConfig cmdlet adds a route filter rule to an Azure route filter.</span></span>

## <span data-ttu-id="86a14-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86a14-107">EXAMPLES</span></span>

### <span data-ttu-id="86a14-108">--------------------------Exempel 1: lägga till en rutt filter regel i ett väg filter--------------------------</span><span class="sxs-lookup"><span data-stu-id="86a14-108">--------------------------  Example 1: Add a route filter rule to a route filter  --------------------------</span></span>
```
PS C:\>$RouteFilter = Get-AzRouteFilter -ResourceGroupName "ResourceGroup11" -Name "routefilter01"
                      PS C:\> Add-AzRouteFilterRuleConfig -Name "rule13" -Access Allow -RouteFilterRuleType Community -RouteFilter $RouteFilter
```

<span data-ttu-id="86a14-109">Det första kommandot får ett väg filter med namnet routefilter01 med hjälp av Get-AzRouteFilter cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86a14-109">The first command gets a route filter named routefilter01 by using the Get-AzRouteFilter cmdlet.</span></span>
<span data-ttu-id="86a14-110">Kommandot lagrar filtret i $RouteFilter variabel.</span><span class="sxs-lookup"><span data-stu-id="86a14-110">The command stores the filter in the $RouteFilter variable.</span></span>

## <span data-ttu-id="86a14-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86a14-111">PARAMETERS</span></span>

### <span data-ttu-id="86a14-112">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="86a14-112">-Access</span></span>
<span data-ttu-id="86a14-113">Anger åtkomst för regeln för flödes filter, giltiga värden är neka eller Tillåt.</span><span class="sxs-lookup"><span data-stu-id="86a14-113">Specifies the access of the route filter rule, Valid values are Deny or Allow.</span></span>

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

### <span data-ttu-id="86a14-114">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="86a14-114">-CommunityList</span></span>
<span data-ttu-id="86a14-115">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="86a14-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="86a14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a14-116">-DefaultProfile</span></span>
<span data-ttu-id="86a14-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86a14-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86a14-118">-Force</span><span class="sxs-lookup"><span data-stu-id="86a14-118">-Force</span></span>
<span data-ttu-id="86a14-119">Fråga inte efter bekräftelse om du vill overrite en resurs</span><span class="sxs-lookup"><span data-stu-id="86a14-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="86a14-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="86a14-120">-Name</span></span>
<span data-ttu-id="86a14-121">Anger ett namn på den väg filter regel som ska läggas till i väg filtret.</span><span class="sxs-lookup"><span data-stu-id="86a14-121">Specifies a name of the route filter rule to add to the route filter.</span></span>

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

### <span data-ttu-id="86a14-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="86a14-122">-RouteFilter</span></span>
<span data-ttu-id="86a14-123">Anger det väg filter där denna cmdlet lägger till en regel för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="86a14-123">Specifies the route filter to which this cmdlet adds a route filter rule.</span></span>

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

### <span data-ttu-id="86a14-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="86a14-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="86a14-125">Anger regel typen för flödes filter.</span><span class="sxs-lookup"><span data-stu-id="86a14-125">Specifies the route filter rule type.</span></span>
<span data-ttu-id="86a14-126">Giltiga värden är: community</span><span class="sxs-lookup"><span data-stu-id="86a14-126">Valid values are: Community</span></span>

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

### <span data-ttu-id="86a14-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86a14-127">-Confirm</span></span>
<span data-ttu-id="86a14-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86a14-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86a14-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86a14-129">-WhatIf</span></span>
<span data-ttu-id="86a14-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86a14-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86a14-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86a14-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86a14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a14-132">CommonParameters</span></span>
<span data-ttu-id="86a14-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a14-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a14-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a14-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86a14-135">INPUTS</span></span>

### <span data-ttu-id="86a14-136">PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86a14-136">PSRouteFilter</span></span>
<span data-ttu-id="86a14-137">Parametern ' RouteFilter ' godkänner värdet av typen ' PSRouteFilter ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="86a14-137">Parameter 'RouteFilter' accepts value of type 'PSRouteFilter' from the pipeline</span></span>

## <span data-ttu-id="86a14-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86a14-138">OUTPUTS</span></span>

### <span data-ttu-id="86a14-139">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86a14-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="86a14-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86a14-140">NOTES</span></span>
<span data-ttu-id="86a14-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="86a14-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="86a14-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86a14-142">RELATED LINKS</span></span>

[<span data-ttu-id="86a14-143">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="86a14-143">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="86a14-144">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86a14-144">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="86a14-145">New-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="86a14-145">New-AzRouteFilterRuleConfigConfig</span></span>](./New-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="86a14-146">Remove-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="86a14-146">Remove-AzRouteFilterRuleConfigConfig</span></span>](./Remove-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="86a14-147">Set-AzRouteFilterRuleConfigConfig</span><span class="sxs-lookup"><span data-stu-id="86a14-147">Set-AzRouteFilterRuleConfigConfig</span></span>](./Set-AzRouteFilterRuleConfigConfig.md)

[<span data-ttu-id="86a14-148">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="86a14-148">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

