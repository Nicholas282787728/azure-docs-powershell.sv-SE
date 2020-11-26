---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270849"
---
# <span data-ttu-id="9a5ad-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a5ad-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="9a5ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5ad-103">Uppdatering för scope med privata länkar</span><span class="sxs-lookup"><span data-stu-id="9a5ad-103">Update for private link scope</span></span>

## <span data-ttu-id="9a5ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a5ad-104">SYNTAX</span></span>

### <span data-ttu-id="9a5ad-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9a5ad-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5ad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a5ad-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a5ad-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a5ad-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5ad-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a5ad-108">DESCRIPTION</span></span>
<span data-ttu-id="9a5ad-109">Uppdatering för scope med privata länkar</span><span class="sxs-lookup"><span data-stu-id="9a5ad-109">Update for private link scope</span></span>

## <span data-ttu-id="9a5ad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a5ad-110">EXAMPLES</span></span>

### <span data-ttu-id="9a5ad-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9a5ad-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="9a5ad-112">uppdatera omfattningen för den privata länken med namnet "scope_name" under resurs gruppen "rg_name" för att använda tagg "Key: Value"</span><span class="sxs-lookup"><span data-stu-id="9a5ad-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="9a5ad-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9a5ad-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="9a5ad-114">uppdatera omfattningen för den privata länken med resurs-ID för att använda taggen "Key: Value"</span><span class="sxs-lookup"><span data-stu-id="9a5ad-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="9a5ad-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9a5ad-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="9a5ad-116">uppdatera omfattningen för den privata länken med ange ett objekt för att använda flaggan "Key: Value"</span><span class="sxs-lookup"><span data-stu-id="9a5ad-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="9a5ad-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a5ad-117">PARAMETERS</span></span>

### <span data-ttu-id="9a5ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5ad-118">-DefaultProfile</span></span>
<span data-ttu-id="9a5ad-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a5ad-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a5ad-120">-InputObject</span></span>
<span data-ttu-id="9a5ad-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a5ad-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="9a5ad-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a5ad-122">-Name</span></span>
<span data-ttu-id="9a5ad-123">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="9a5ad-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="9a5ad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5ad-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a5ad-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9a5ad-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9a5ad-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a5ad-126">-ResourceId</span></span>
<span data-ttu-id="9a5ad-127">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="9a5ad-127">Resource Id</span></span>

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

### <span data-ttu-id="9a5ad-128">-Taggar</span><span class="sxs-lookup"><span data-stu-id="9a5ad-128">-Tags</span></span>
<span data-ttu-id="9a5ad-129">Taggen</span><span class="sxs-lookup"><span data-stu-id="9a5ad-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5ad-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9a5ad-130">-Confirm</span></span>
<span data-ttu-id="9a5ad-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5ad-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5ad-132">-WhatIf</span></span>
<span data-ttu-id="9a5ad-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5ad-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5ad-135">CommonParameters</span></span>
<span data-ttu-id="9a5ad-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5ad-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a5ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5ad-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a5ad-138">INPUTS</span></span>

### <span data-ttu-id="9a5ad-139">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a5ad-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="9a5ad-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9a5ad-140">System.String</span></span>

## <span data-ttu-id="9a5ad-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a5ad-141">OUTPUTS</span></span>

### <span data-ttu-id="9a5ad-142">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9a5ad-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="9a5ad-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a5ad-143">NOTES</span></span>

## <span data-ttu-id="9a5ad-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a5ad-144">RELATED LINKS</span></span>