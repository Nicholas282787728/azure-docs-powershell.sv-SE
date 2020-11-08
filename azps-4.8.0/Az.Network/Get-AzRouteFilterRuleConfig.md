---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: d55c16f7fa4f45ac3b1249f4e2e8b41dfb529d4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258266"
---
# <span data-ttu-id="4aa43-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4aa43-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4aa43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4aa43-102">SYNOPSIS</span></span>
<span data-ttu-id="4aa43-103">Hämtar en regel för flödes filter i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="4aa43-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="4aa43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4aa43-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aa43-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4aa43-105">DESCRIPTION</span></span>
<span data-ttu-id="4aa43-106">Cmdleten **Get-AzRouteFilterRuleConfig** hämtar en regel för flödes filter eller en lista med flödes filter regler i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="4aa43-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="4aa43-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4aa43-107">EXAMPLES</span></span>

### <span data-ttu-id="4aa43-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4aa43-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="4aa43-109">Det första kommandot får vägen med namnet MyRouteFilter och lagrar det sedan i variabeln $rf.</span><span class="sxs-lookup"><span data-stu-id="4aa43-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="4aa43-110">Det andra kommandot får regel regeln med namnet Rule01 associerat med vägen.</span><span class="sxs-lookup"><span data-stu-id="4aa43-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="4aa43-111">Det tredje kommandot får en lista över regler för flödes filter som är kopplade till det väg filtret.</span><span class="sxs-lookup"><span data-stu-id="4aa43-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="4aa43-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4aa43-112">PARAMETERS</span></span>

### <span data-ttu-id="4aa43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aa43-113">-DefaultProfile</span></span>
<span data-ttu-id="4aa43-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4aa43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aa43-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4aa43-115">-Name</span></span>
<span data-ttu-id="4aa43-116">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="4aa43-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="4aa43-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-117">-RouteFilter</span></span>
<span data-ttu-id="4aa43-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-118">The RouteFilter</span></span>

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

### <span data-ttu-id="4aa43-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aa43-119">CommonParameters</span></span>
<span data-ttu-id="4aa43-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aa43-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aa43-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4aa43-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aa43-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4aa43-122">INPUTS</span></span>

### <span data-ttu-id="4aa43-123">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4aa43-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4aa43-124">OUTPUTS</span></span>

### <span data-ttu-id="4aa43-125">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="4aa43-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="4aa43-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4aa43-126">NOTES</span></span>

## <span data-ttu-id="4aa43-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4aa43-127">RELATED LINKS</span></span>

[<span data-ttu-id="4aa43-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4aa43-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4aa43-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4aa43-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4aa43-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4aa43-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4aa43-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4aa43-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4aa43-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4aa43-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="4aa43-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4aa43-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4aa43-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
