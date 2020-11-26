---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272863"
---
# <span data-ttu-id="f3b82-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f3b82-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="f3b82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f3b82-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b82-103">Tar bort ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="f3b82-103">Removes a route filter.</span></span>

## <span data-ttu-id="f3b82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f3b82-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3b82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f3b82-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b82-106">Cmdleten **Remove-AzRouteFilter** tar bort ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="f3b82-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="f3b82-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f3b82-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b82-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f3b82-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f3b82-109">Kommandot tar bort väg filtret med namnet RouteFilter01 i resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f3b82-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f3b82-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f3b82-110">PARAMETERS</span></span>

### <span data-ttu-id="f3b82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b82-111">-DefaultProfile</span></span>
<span data-ttu-id="f3b82-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b82-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b82-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f3b82-113">-Force</span></span>
<span data-ttu-id="f3b82-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f3b82-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f3b82-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f3b82-115">-Name</span></span>
<span data-ttu-id="f3b82-116">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="f3b82-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b82-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b82-117">-PassThru</span></span>
<span data-ttu-id="f3b82-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f3b82-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="f3b82-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3b82-119">-ResourceGroupName</span></span>
<span data-ttu-id="f3b82-120">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f3b82-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3b82-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f3b82-121">-Confirm</span></span>
<span data-ttu-id="f3b82-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f3b82-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b82-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b82-123">-WhatIf</span></span>
<span data-ttu-id="f3b82-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f3b82-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3b82-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f3b82-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b82-126">CommonParameters</span></span>
<span data-ttu-id="f3b82-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b82-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b82-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b82-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f3b82-129">INPUTS</span></span>

### <span data-ttu-id="f3b82-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f3b82-130">System.String</span></span>

## <span data-ttu-id="f3b82-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f3b82-131">OUTPUTS</span></span>

### <span data-ttu-id="f3b82-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3b82-132">System.Boolean</span></span>

## <span data-ttu-id="f3b82-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f3b82-133">NOTES</span></span>

## <span data-ttu-id="f3b82-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f3b82-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3b82-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f3b82-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="f3b82-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f3b82-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="f3b82-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f3b82-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="f3b82-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3b82-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f3b82-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3b82-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f3b82-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3b82-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f3b82-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3b82-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="f3b82-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="f3b82-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)