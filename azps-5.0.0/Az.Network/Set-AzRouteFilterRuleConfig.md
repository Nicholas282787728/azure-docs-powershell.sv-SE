---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilterRuleConfig.md
ms.openlocfilehash: eb8de50aac1b68928d5cebe8118665b9a24e8fbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271523"
---
# <span data-ttu-id="cebb5-101">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cebb5-101">Set-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="cebb5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cebb5-102">SYNOPSIS</span></span>
<span data-ttu-id="cebb5-103">Ändrar regeln för väg filter för ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="cebb5-103">Modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="cebb5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cebb5-104">SYNTAX</span></span>

```
Set-AzRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cebb5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cebb5-105">DESCRIPTION</span></span>
<span data-ttu-id="cebb5-106">Cmdleten **set-AzRouteFilterRuleConfig** ändrar regeln för väg filter för ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="cebb5-106">The **Set-AzRouteFilterRuleConfig** cmdlet modifies the route filter rule of a route filter.</span></span>

## <span data-ttu-id="cebb5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cebb5-107">EXAMPLES</span></span>

### <span data-ttu-id="cebb5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cebb5-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> $rf = Set-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01" -Access Deny -RouteFilterRuleType Community -CommunityList "12076:5010","12076:5040"
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="cebb5-109">Det första kommandot får vägen med namnet RouteFilter01 och lagrar det i $rf variabeln.</span><span class="sxs-lookup"><span data-stu-id="cebb5-109">The first command gets the route filter named RouteFilter01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="cebb5-110">Det andra kommandot ändrar regeln för väg filter med namnet Rule01 och lagrar ett uppdaterat väg filter i $rf variabel.</span><span class="sxs-lookup"><span data-stu-id="cebb5-110">The second command modifies the route filter rule named Rule01 and stores updated route filter in the $rf variable.</span></span>
<span data-ttu-id="cebb5-111">Det tredje kommandot sparar det uppdaterade väg filtret.</span><span class="sxs-lookup"><span data-stu-id="cebb5-111">The third command saves updated route filter.</span></span>

## <span data-ttu-id="cebb5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cebb5-112">PARAMETERS</span></span>

### <span data-ttu-id="cebb5-113">-Åtkomst</span><span class="sxs-lookup"><span data-stu-id="cebb5-113">-Access</span></span>
<span data-ttu-id="cebb5-114">Åtkomst typen för regeln.</span><span class="sxs-lookup"><span data-stu-id="cebb5-114">The access type of the rule.</span></span>
<span data-ttu-id="cebb5-115">Möjliga värden är: ' Allow ', ' neka '</span><span class="sxs-lookup"><span data-stu-id="cebb5-115">Possible values are: 'Allow', 'Deny'</span></span>

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

### <span data-ttu-id="cebb5-116">-CommunityList</span><span class="sxs-lookup"><span data-stu-id="cebb5-116">-CommunityList</span></span>
<span data-ttu-id="cebb5-117">Listan över community-värden som routing filter filtrerar efter</span><span class="sxs-lookup"><span data-stu-id="cebb5-117">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="cebb5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebb5-118">-DefaultProfile</span></span>
<span data-ttu-id="cebb5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cebb5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cebb5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cebb5-120">-Force</span></span>
<span data-ttu-id="cebb5-121">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="cebb5-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cebb5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="cebb5-122">-Name</span></span>
<span data-ttu-id="cebb5-123">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="cebb5-123">The name of the route filter rule</span></span>

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

### <span data-ttu-id="cebb5-124">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-124">-RouteFilter</span></span>
<span data-ttu-id="cebb5-125">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-125">The RouteFilter</span></span>

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

### <span data-ttu-id="cebb5-126">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="cebb5-126">-RouteFilterRuleType</span></span>
<span data-ttu-id="cebb5-127">Regel typen för flödes filter regeln.</span><span class="sxs-lookup"><span data-stu-id="cebb5-127">The route filter rule type of the rule.</span></span>
<span data-ttu-id="cebb5-128">Möjliga värden är: ' community '</span><span class="sxs-lookup"><span data-stu-id="cebb5-128">Possible values are: 'Community'</span></span>

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

### <span data-ttu-id="cebb5-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cebb5-129">-Confirm</span></span>
<span data-ttu-id="cebb5-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cebb5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cebb5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cebb5-131">-WhatIf</span></span>
<span data-ttu-id="cebb5-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cebb5-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cebb5-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cebb5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cebb5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebb5-134">CommonParameters</span></span>
<span data-ttu-id="cebb5-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebb5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebb5-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cebb5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebb5-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cebb5-137">INPUTS</span></span>

### <span data-ttu-id="cebb5-138">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cebb5-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cebb5-139">OUTPUTS</span></span>

### <span data-ttu-id="cebb5-140">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-140">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cebb5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cebb5-141">NOTES</span></span>

## <span data-ttu-id="cebb5-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cebb5-142">RELATED LINKS</span></span>

[<span data-ttu-id="cebb5-143">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cebb5-143">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cebb5-144">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cebb5-144">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cebb5-145">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cebb5-145">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cebb5-146">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cebb5-146">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="cebb5-147">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-147">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="cebb5-148">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-148">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="cebb5-149">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-149">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="cebb5-150">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cebb5-150">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
