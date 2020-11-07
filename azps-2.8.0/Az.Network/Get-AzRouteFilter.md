---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 26fb3e9a7b4b097e79fdb328d79a82fc423ac675
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918714"
---
# <span data-ttu-id="16874-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16874-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="16874-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16874-102">SYNOPSIS</span></span>
<span data-ttu-id="16874-103">Hämtar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="16874-103">Gets a route filter.</span></span>

## <span data-ttu-id="16874-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16874-104">SYNTAX</span></span>

### <span data-ttu-id="16874-105">Noexpandering</span><span class="sxs-lookup"><span data-stu-id="16874-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="16874-106">Byggnad</span><span class="sxs-lookup"><span data-stu-id="16874-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16874-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16874-107">DESCRIPTION</span></span>
<span data-ttu-id="16874-108">Cmdleten **Get-AzRouteFilter** får ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="16874-108">The **Get-AzRouteFilter** cmdlet gets a route filter.</span></span>

## <span data-ttu-id="16874-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16874-109">EXAMPLES</span></span>

### <span data-ttu-id="16874-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16874-110">Example 1</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="16874-111">Det här kommandot hämtar det väg filter som heter RouteFilter01 som tillhör resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="16874-111">This command gets the route filter named RouteFilter01 that belongs to the resource group named ResourceGroup01.</span></span>

### <span data-ttu-id="16874-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="16874-112">Example 2</span></span>
```powershell
PS C:\> Get-AzRouteFilter -Name "RouteFilter*"

Name              : RouteFilter01
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter01
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []

Name              : RouteFilter02
ResourceGroupName : ResourceGroup01
Location          : westus
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsof
                    t.Network/routeFilters/RouteFilter02
Etag              : W/"00000000-0000-0000-0000-000000000000"
ProvisioningState : Succeeded
Tags              :
Rules             : []
Peerings          : []
```

<span data-ttu-id="16874-113">Det här kommandot får alla väg filter som börjar med "RouteFilter".</span><span class="sxs-lookup"><span data-stu-id="16874-113">This command gets all route filters that start with "RouteFilter".</span></span>

## <span data-ttu-id="16874-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16874-114">PARAMETERS</span></span>

### <span data-ttu-id="16874-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16874-115">-DefaultProfile</span></span>
<span data-ttu-id="16874-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16874-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16874-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="16874-117">-ExpandResource</span></span>
<span data-ttu-id="16874-118">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="16874-118">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16874-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="16874-119">-Name</span></span>
<span data-ttu-id="16874-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="16874-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="16874-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16874-121">-ResourceGroupName</span></span>
<span data-ttu-id="16874-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="16874-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="16874-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16874-123">CommonParameters</span></span>
<span data-ttu-id="16874-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16874-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16874-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16874-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16874-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16874-126">INPUTS</span></span>

### <span data-ttu-id="16874-127">System. String</span><span class="sxs-lookup"><span data-stu-id="16874-127">System.String</span></span>

## <span data-ttu-id="16874-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16874-128">OUTPUTS</span></span>

### <span data-ttu-id="16874-129">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16874-129">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="16874-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16874-130">NOTES</span></span>

## <span data-ttu-id="16874-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16874-131">RELATED LINKS</span></span>

[<span data-ttu-id="16874-132">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16874-132">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="16874-133">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16874-133">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="16874-134">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="16874-134">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="16874-135">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16874-135">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16874-136">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16874-136">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16874-137">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16874-137">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16874-138">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16874-138">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="16874-139">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="16874-139">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
