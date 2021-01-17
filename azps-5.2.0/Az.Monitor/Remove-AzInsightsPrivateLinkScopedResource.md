---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388167"
---
# <span data-ttu-id="c2df7-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="c2df7-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="c2df7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2df7-102">SYNOPSIS</span></span>
<span data-ttu-id="c2df7-103">ta bort resurs för begränsad länk</span><span class="sxs-lookup"><span data-stu-id="c2df7-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="c2df7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2df7-104">SYNTAX</span></span>

### <span data-ttu-id="c2df7-105">ByScopeParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2df7-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2df7-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2df7-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2df7-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2df7-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2df7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2df7-108">DESCRIPTION</span></span>
<span data-ttu-id="c2df7-109">ta bort resurs för begränsad länk</span><span class="sxs-lookup"><span data-stu-id="c2df7-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="c2df7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2df7-110">EXAMPLES</span></span>

### <span data-ttu-id="c2df7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2df7-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="c2df7-112">ta bort webbprogramsomfattande resurser</span><span class="sxs-lookup"><span data-stu-id="c2df7-112">delete private link scoped resource</span></span>

## <span data-ttu-id="c2df7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2df7-113">PARAMETERS</span></span>

### <span data-ttu-id="c2df7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2df7-114">-DefaultProfile</span></span>
<span data-ttu-id="c2df7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2df7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2df7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2df7-116">-InputObject</span></span>
<span data-ttu-id="c2df7-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c2df7-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="c2df7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2df7-118">-Name</span></span>
<span data-ttu-id="c2df7-119">Omfångs resurs namn</span><span class="sxs-lookup"><span data-stu-id="c2df7-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2df7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2df7-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2df7-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c2df7-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2df7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2df7-122">-ResourceId</span></span>
<span data-ttu-id="c2df7-123">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c2df7-123">Resource Id</span></span>

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

### <span data-ttu-id="c2df7-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="c2df7-124">-ScopeName</span></span>
<span data-ttu-id="c2df7-125">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="c2df7-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2df7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2df7-126">-Confirm</span></span>
<span data-ttu-id="c2df7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2df7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2df7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2df7-128">-WhatIf</span></span>
<span data-ttu-id="c2df7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2df7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2df7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2df7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2df7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2df7-131">CommonParameters</span></span>
<span data-ttu-id="c2df7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2df7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2df7-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2df7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2df7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2df7-134">INPUTS</span></span>

### <span data-ttu-id="c2df7-135">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c2df7-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="c2df7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2df7-136">System.String</span></span>

## <span data-ttu-id="c2df7-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2df7-137">OUTPUTS</span></span>

### <span data-ttu-id="c2df7-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2df7-138">System.Boolean</span></span>

## <span data-ttu-id="c2df7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2df7-139">NOTES</span></span>

## <span data-ttu-id="c2df7-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2df7-140">RELATED LINKS</span></span>
