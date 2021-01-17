---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405024"
---
# <span data-ttu-id="ed37a-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="ed37a-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="ed37a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed37a-102">SYNOPSIS</span></span>
<span data-ttu-id="ed37a-103">skapa en resurs för webbprogramsomfattande privata länkar</span><span class="sxs-lookup"><span data-stu-id="ed37a-103">create for private link scoped resource</span></span>

## <span data-ttu-id="ed37a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed37a-104">SYNTAX</span></span>

### <span data-ttu-id="ed37a-105">ByResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ed37a-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed37a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed37a-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed37a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed37a-107">DESCRIPTION</span></span>
<span data-ttu-id="ed37a-108">skapa för en resurs för webbprogramsomfattande privata länkar, omfattnings resursen kan vara logganalys-arbetsyta eller Application Insights-komponent</span><span class="sxs-lookup"><span data-stu-id="ed37a-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="ed37a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed37a-109">EXAMPLES</span></span>

### <span data-ttu-id="ed37a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ed37a-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="ed37a-111">skapa en beskrivande resurs "scoped_resource_name" som är länkad till komponenten Application Insights "ai_name"</span><span class="sxs-lookup"><span data-stu-id="ed37a-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="ed37a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed37a-112">PARAMETERS</span></span>

### <span data-ttu-id="ed37a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed37a-113">-DefaultProfile</span></span>
<span data-ttu-id="ed37a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed37a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed37a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed37a-115">-InputObject</span></span>
<span data-ttu-id="ed37a-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ed37a-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="ed37a-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="ed37a-117">-LinkedResourceId</span></span>
<span data-ttu-id="ed37a-118">LA/AI resurs-ID som du vill länka</span><span class="sxs-lookup"><span data-stu-id="ed37a-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed37a-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed37a-119">-Name</span></span>
<span data-ttu-id="ed37a-120">Omfångs resurs namn</span><span class="sxs-lookup"><span data-stu-id="ed37a-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed37a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed37a-121">-ResourceGroupName</span></span>
<span data-ttu-id="ed37a-122">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ed37a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="ed37a-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="ed37a-123">-ScopeName</span></span>
<span data-ttu-id="ed37a-124">Namn på privat länk</span><span class="sxs-lookup"><span data-stu-id="ed37a-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="ed37a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed37a-125">-Confirm</span></span>
<span data-ttu-id="ed37a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed37a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed37a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed37a-127">-WhatIf</span></span>
<span data-ttu-id="ed37a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed37a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed37a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed37a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed37a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed37a-130">CommonParameters</span></span>
<span data-ttu-id="ed37a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed37a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed37a-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed37a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed37a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed37a-133">INPUTS</span></span>

### <span data-ttu-id="ed37a-134">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="ed37a-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="ed37a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ed37a-135">System.String</span></span>

## <span data-ttu-id="ed37a-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed37a-136">OUTPUTS</span></span>

### <span data-ttu-id="ed37a-137">Microsoft. Azure. commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="ed37a-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="ed37a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed37a-138">NOTES</span></span>

## <span data-ttu-id="ed37a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed37a-139">RELATED LINKS</span></span>
