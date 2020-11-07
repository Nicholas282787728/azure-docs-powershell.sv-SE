---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925697"
---
# <span data-ttu-id="59349-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="59349-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="59349-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59349-102">SYNOPSIS</span></span>
<span data-ttu-id="59349-103">ta bort resurs för begränsad länk</span><span class="sxs-lookup"><span data-stu-id="59349-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="59349-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59349-104">SYNTAX</span></span>

### <span data-ttu-id="59349-105">ByScopeParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="59349-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59349-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59349-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59349-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59349-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59349-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59349-108">DESCRIPTION</span></span>
<span data-ttu-id="59349-109">ta bort resurs för begränsad länk</span><span class="sxs-lookup"><span data-stu-id="59349-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="59349-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59349-110">EXAMPLES</span></span>

### <span data-ttu-id="59349-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59349-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="59349-112">ta bort webbprogramsomfattande resurser</span><span class="sxs-lookup"><span data-stu-id="59349-112">delete private link scoped resource</span></span>

## <span data-ttu-id="59349-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59349-113">PARAMETERS</span></span>

### <span data-ttu-id="59349-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59349-114">-DefaultProfile</span></span>
<span data-ttu-id="59349-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59349-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59349-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59349-116">-InputObject</span></span>
<span data-ttu-id="59349-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="59349-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="59349-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="59349-118">-Name</span></span>
<span data-ttu-id="59349-119">Omfångs resurs namn</span><span class="sxs-lookup"><span data-stu-id="59349-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="59349-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59349-120">-ResourceGroupName</span></span>
<span data-ttu-id="59349-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="59349-121">Resource Group Name</span></span>

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

### <span data-ttu-id="59349-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59349-122">-ResourceId</span></span>
<span data-ttu-id="59349-123">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="59349-123">Resource Id</span></span>

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

### <span data-ttu-id="59349-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="59349-124">-ScopeName</span></span>
<span data-ttu-id="59349-125">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="59349-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="59349-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59349-126">-Confirm</span></span>
<span data-ttu-id="59349-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59349-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59349-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59349-128">-WhatIf</span></span>
<span data-ttu-id="59349-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59349-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59349-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59349-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59349-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59349-131">CommonParameters</span></span>
<span data-ttu-id="59349-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59349-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59349-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59349-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59349-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59349-134">INPUTS</span></span>

### <span data-ttu-id="59349-135">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="59349-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="59349-136">System. String</span><span class="sxs-lookup"><span data-stu-id="59349-136">System.String</span></span>

## <span data-ttu-id="59349-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59349-137">OUTPUTS</span></span>

### <span data-ttu-id="59349-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59349-138">System.Boolean</span></span>

## <span data-ttu-id="59349-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59349-139">NOTES</span></span>

## <span data-ttu-id="59349-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59349-140">RELATED LINKS</span></span>
