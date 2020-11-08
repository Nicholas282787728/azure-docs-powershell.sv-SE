---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: a7414690e1d0e1f5a6d8242af7b1d27490dcde93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918991"
---
# <span data-ttu-id="8dd33-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8dd33-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8dd33-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8dd33-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd33-103">Tar bort en regel för flödes filter från ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="8dd33-103">Removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="8dd33-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8dd33-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd33-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8dd33-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd33-106">Cmdleten **Remove-AzRouteFilterRuleConfig** tar bort en regel för flödes filter från ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="8dd33-106">The **Remove-AzRouteFilterRuleConfig** cmdlet removes a route filter rule from a route filter.</span></span>

## <span data-ttu-id="8dd33-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8dd33-107">EXAMPLES</span></span>

### <span data-ttu-id="8dd33-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8dd33-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
```

<span data-ttu-id="8dd33-109">Det första kommandot får ett väg filter med namnet RouteFilter01 som tillhör resurs gruppen som heter ResourceGroup01 och lagrar det i $rf variabeln.</span><span class="sxs-lookup"><span data-stu-id="8dd33-109">The first command gets a route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01 and stores it in the $rf variable.</span></span>
<span data-ttu-id="8dd33-110">Det andra kommandot tar bort regel regeln med namnet Rule01 från det väg filter som lagras i $rf.</span><span class="sxs-lookup"><span data-stu-id="8dd33-110">The second command removes the route filter rule named Rule01 from the route filter stored in $rf.</span></span>

## <span data-ttu-id="8dd33-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8dd33-111">PARAMETERS</span></span>

### <span data-ttu-id="8dd33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd33-112">-DefaultProfile</span></span>
<span data-ttu-id="8dd33-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd33-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dd33-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8dd33-114">-Force</span></span>
<span data-ttu-id="8dd33-115">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="8dd33-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8dd33-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8dd33-116">-Name</span></span>
<span data-ttu-id="8dd33-117">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="8dd33-117">The name of the route filter rule</span></span>

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

### <span data-ttu-id="8dd33-118">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-118">-RouteFilter</span></span>
<span data-ttu-id="8dd33-119">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-119">The RouteFilter</span></span>

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

### <span data-ttu-id="8dd33-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8dd33-120">-Confirm</span></span>
<span data-ttu-id="8dd33-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8dd33-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd33-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd33-122">-WhatIf</span></span>
<span data-ttu-id="8dd33-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8dd33-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dd33-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8dd33-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd33-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd33-125">CommonParameters</span></span>
<span data-ttu-id="8dd33-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd33-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd33-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd33-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd33-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8dd33-128">INPUTS</span></span>

### <span data-ttu-id="8dd33-129">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8dd33-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8dd33-130">OUTPUTS</span></span>

### <span data-ttu-id="8dd33-131">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8dd33-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8dd33-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8dd33-132">NOTES</span></span>

## <span data-ttu-id="8dd33-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8dd33-133">RELATED LINKS</span></span>

[<span data-ttu-id="8dd33-134">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8dd33-134">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8dd33-135">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8dd33-135">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8dd33-136">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8dd33-136">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8dd33-137">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8dd33-137">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="8dd33-138">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-138">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="8dd33-139">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-139">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="8dd33-140">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-140">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="8dd33-141">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8dd33-141">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)