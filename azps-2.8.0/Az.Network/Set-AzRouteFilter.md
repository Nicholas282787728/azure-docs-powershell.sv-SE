---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzRouteFilter.md
ms.openlocfilehash: ab0da083957fe18d1bb30d0b3d08d33515d0ff13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919484"
---
# <span data-ttu-id="92127-101">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-101">Set-AzRouteFilter</span></span>

## <span data-ttu-id="92127-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92127-102">SYNOPSIS</span></span>
<span data-ttu-id="92127-103">Uppdaterar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="92127-103">Updates a route filter.</span></span>

## <span data-ttu-id="92127-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92127-104">SYNTAX</span></span>

```
Set-AzRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92127-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92127-105">DESCRIPTION</span></span>
<span data-ttu-id="92127-106">Cmdleten **set-AzApplicationGateway** uppdaterar ett väg filter</span><span class="sxs-lookup"><span data-stu-id="92127-106">The **Set-AzApplicationGateway** cmdlet updates a route filter</span></span>

## <span data-ttu-id="92127-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92127-107">EXAMPLES</span></span>

### <span data-ttu-id="92127-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92127-108">Example 1</span></span>
```powershell
PS C:\> Set-AzRouteFilter -RouteFilter $rf
```

<span data-ttu-id="92127-109">Det här kommandot uppdaterar Route-filtret med inställningarna i variabeln $rf.</span><span class="sxs-lookup"><span data-stu-id="92127-109">This command updates the route filter with settings in the $rf variable.</span></span>

## <span data-ttu-id="92127-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92127-110">PARAMETERS</span></span>

### <span data-ttu-id="92127-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="92127-111">-AsJob</span></span>
<span data-ttu-id="92127-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="92127-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92127-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92127-113">-DefaultProfile</span></span>
<span data-ttu-id="92127-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92127-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92127-115">-Force</span><span class="sxs-lookup"><span data-stu-id="92127-115">-Force</span></span>
<span data-ttu-id="92127-116">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="92127-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="92127-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-117">-RouteFilter</span></span>
<span data-ttu-id="92127-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-118">The RouteFilter</span></span>

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

### <span data-ttu-id="92127-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92127-119">-Confirm</span></span>
<span data-ttu-id="92127-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92127-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92127-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92127-121">-WhatIf</span></span>
<span data-ttu-id="92127-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92127-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92127-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92127-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92127-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92127-124">CommonParameters</span></span>
<span data-ttu-id="92127-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92127-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92127-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92127-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92127-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92127-127">INPUTS</span></span>

### <span data-ttu-id="92127-128">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="92127-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92127-129">OUTPUTS</span></span>

### <span data-ttu-id="92127-130">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="92127-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92127-131">NOTES</span></span>

## <span data-ttu-id="92127-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92127-132">RELATED LINKS</span></span>

[<span data-ttu-id="92127-133">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-133">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="92127-134">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-134">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="92127-135">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="92127-135">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="92127-136">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92127-136">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="92127-137">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92127-137">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="92127-138">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92127-138">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="92127-139">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92127-139">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="92127-140">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="92127-140">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
