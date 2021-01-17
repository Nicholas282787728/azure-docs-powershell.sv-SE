---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401456"
---
# <span data-ttu-id="42c4f-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="42c4f-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="42c4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="42c4f-103">ta bort scope för privat länk</span><span class="sxs-lookup"><span data-stu-id="42c4f-103">delete private link scope</span></span>

## <span data-ttu-id="42c4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42c4f-104">SYNTAX</span></span>

### <span data-ttu-id="42c4f-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="42c4f-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c4f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42c4f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c4f-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42c4f-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c4f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="42c4f-109">ta bort scope för privat länk</span><span class="sxs-lookup"><span data-stu-id="42c4f-109">delete private link scope</span></span>

## <span data-ttu-id="42c4f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42c4f-110">EXAMPLES</span></span>

### <span data-ttu-id="42c4f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="42c4f-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="42c4f-112">ta bort omfattningen för den privata länken med namnet "scope_name" under resurs gruppen "rg_name"</span><span class="sxs-lookup"><span data-stu-id="42c4f-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="42c4f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="42c4f-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="42c4f-114">ta bort scope för privat länk med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="42c4f-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="42c4f-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="42c4f-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="42c4f-116">ta bort scope för privat länk med ett omfångs objekt</span><span class="sxs-lookup"><span data-stu-id="42c4f-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="42c4f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42c4f-117">PARAMETERS</span></span>

### <span data-ttu-id="42c4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c4f-118">-DefaultProfile</span></span>
<span data-ttu-id="42c4f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42c4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c4f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42c4f-120">-InputObject</span></span>
<span data-ttu-id="42c4f-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="42c4f-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c4f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="42c4f-122">-Name</span></span>
<span data-ttu-id="42c4f-123">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="42c4f-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="42c4f-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="42c4f-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c4f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42c4f-126">-ResourceId</span></span>
<span data-ttu-id="42c4f-127">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="42c4f-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c4f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="42c4f-128">-Confirm</span></span>
<span data-ttu-id="42c4f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="42c4f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c4f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c4f-130">-WhatIf</span></span>
<span data-ttu-id="42c4f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="42c4f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c4f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="42c4f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c4f-133">CommonParameters</span></span>
<span data-ttu-id="42c4f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42c4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c4f-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42c4f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c4f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42c4f-136">INPUTS</span></span>

### <span data-ttu-id="42c4f-137">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="42c4f-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="42c4f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="42c4f-138">System.String</span></span>

## <span data-ttu-id="42c4f-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42c4f-139">OUTPUTS</span></span>

### <span data-ttu-id="42c4f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42c4f-140">System.Boolean</span></span>

## <span data-ttu-id="42c4f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42c4f-141">NOTES</span></span>

## <span data-ttu-id="42c4f-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42c4f-142">RELATED LINKS</span></span>
