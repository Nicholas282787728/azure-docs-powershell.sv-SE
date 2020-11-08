---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925701"
---
# <span data-ttu-id="0d273-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0d273-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0d273-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d273-102">SYNOPSIS</span></span>
<span data-ttu-id="0d273-103">ta bort scope för privat länk</span><span class="sxs-lookup"><span data-stu-id="0d273-103">delete private link scope</span></span>

## <span data-ttu-id="0d273-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d273-104">SYNTAX</span></span>

### <span data-ttu-id="0d273-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0d273-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d273-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d273-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d273-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d273-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d273-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d273-108">DESCRIPTION</span></span>
<span data-ttu-id="0d273-109">ta bort scope för privat länk</span><span class="sxs-lookup"><span data-stu-id="0d273-109">delete private link scope</span></span>

## <span data-ttu-id="0d273-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d273-110">EXAMPLES</span></span>

### <span data-ttu-id="0d273-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0d273-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="0d273-112">ta bort omfattningen för den privata länken med namnet "scope_name" under resurs gruppen "rg_name"</span><span class="sxs-lookup"><span data-stu-id="0d273-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="0d273-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0d273-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="0d273-114">ta bort scope för privat länk med resurs-ID</span><span class="sxs-lookup"><span data-stu-id="0d273-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="0d273-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="0d273-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="0d273-116">ta bort scope för privat länk med ett omfångs objekt</span><span class="sxs-lookup"><span data-stu-id="0d273-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="0d273-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d273-117">PARAMETERS</span></span>

### <span data-ttu-id="0d273-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d273-118">-DefaultProfile</span></span>
<span data-ttu-id="0d273-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d273-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d273-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d273-120">-InputObject</span></span>
<span data-ttu-id="0d273-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0d273-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="0d273-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d273-122">-Name</span></span>
<span data-ttu-id="0d273-123">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="0d273-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="0d273-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d273-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d273-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0d273-125">Resource Group Name</span></span>

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

### <span data-ttu-id="0d273-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d273-126">-ResourceId</span></span>
<span data-ttu-id="0d273-127">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="0d273-127">Resource Id</span></span>

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

### <span data-ttu-id="0d273-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d273-128">-Confirm</span></span>
<span data-ttu-id="0d273-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d273-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d273-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d273-130">-WhatIf</span></span>
<span data-ttu-id="0d273-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d273-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d273-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d273-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d273-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d273-133">CommonParameters</span></span>
<span data-ttu-id="0d273-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d273-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d273-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d273-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d273-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d273-136">INPUTS</span></span>

### <span data-ttu-id="0d273-137">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0d273-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="0d273-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0d273-138">System.String</span></span>

## <span data-ttu-id="0d273-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d273-139">OUTPUTS</span></span>

### <span data-ttu-id="0d273-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d273-140">System.Boolean</span></span>

## <span data-ttu-id="0d273-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d273-141">NOTES</span></span>

## <span data-ttu-id="0d273-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d273-142">RELATED LINKS</span></span>