---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 5d83678d26804c97a0e21da4dcbff3f5af75d409
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748227"
---
# <span data-ttu-id="0eab9-101">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eab9-101">Get-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="0eab9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0eab9-102">SYNOPSIS</span></span>
<span data-ttu-id="0eab9-103">Hämtar en regel för flödes filter i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="0eab9-103">Gets a route filter rule in a route filter.</span></span>

## <span data-ttu-id="0eab9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0eab9-104">SYNTAX</span></span>

```
Get-AzRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eab9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0eab9-105">DESCRIPTION</span></span>
<span data-ttu-id="0eab9-106">Cmdleten **Get-AzRouteFilterRuleConfig** hämtar en regel för flödes filter eller en lista med flödes filter regler i ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="0eab9-106">The **Get-AzRouteFilterRuleConfig** cmdlet gets a route filter rule or a list of route filter rules in a route filter.</span></span>

## <span data-ttu-id="0eab9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0eab9-107">EXAMPLES</span></span>

### <span data-ttu-id="0eab9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0eab9-108">Example 1</span></span>
```powershell
PS C:\> $rf = Get-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf -Name "Rule01"
PS C:\> Get-AzRouteFilterRuleConfig -RouteFilter $rf
```

<span data-ttu-id="0eab9-109">Det första kommandot får vägen med namnet MyRouteFilter och lagrar det sedan i variabeln $rf.</span><span class="sxs-lookup"><span data-stu-id="0eab9-109">The first command gets the route filter named MyRouteFilter, and then stores it in the variable $rf.</span></span>
<span data-ttu-id="0eab9-110">Det andra kommandot får regel regeln med namnet Rule01 associerat med vägen.</span><span class="sxs-lookup"><span data-stu-id="0eab9-110">The second command gets the route filter rule named Rule01 associated with that route filter.</span></span>
<span data-ttu-id="0eab9-111">Det tredje kommandot får en lista över regler för flödes filter som är kopplade till det väg filtret.</span><span class="sxs-lookup"><span data-stu-id="0eab9-111">The third command gets a list of route filter rules associated with that route filter.</span></span>

## <span data-ttu-id="0eab9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0eab9-112">PARAMETERS</span></span>

### <span data-ttu-id="0eab9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eab9-113">-DefaultProfile</span></span>
<span data-ttu-id="0eab9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0eab9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eab9-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0eab9-115">-Name</span></span>
<span data-ttu-id="0eab9-116">Namnet på regeln för flödes filter</span><span class="sxs-lookup"><span data-stu-id="0eab9-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="0eab9-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-117">-RouteFilter</span></span>
<span data-ttu-id="0eab9-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-118">The RouteFilter</span></span>

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

### <span data-ttu-id="0eab9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eab9-119">CommonParameters</span></span>
<span data-ttu-id="0eab9-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eab9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eab9-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0eab9-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eab9-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0eab9-122">INPUTS</span></span>

### <span data-ttu-id="0eab9-123">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0eab9-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0eab9-124">OUTPUTS</span></span>

### <span data-ttu-id="0eab9-125">Microsoft. Azure. commands. Networks. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="0eab9-125">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="0eab9-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0eab9-126">NOTES</span></span>

## <span data-ttu-id="0eab9-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0eab9-127">RELATED LINKS</span></span>

[<span data-ttu-id="0eab9-128">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eab9-128">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0eab9-129">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eab9-129">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0eab9-130">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eab9-130">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0eab9-131">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0eab9-131">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="0eab9-132">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-132">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="0eab9-133">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-133">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="0eab9-134">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-134">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="0eab9-135">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0eab9-135">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
