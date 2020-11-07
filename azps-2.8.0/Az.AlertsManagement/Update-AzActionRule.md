---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 9991829a70029366086a58020aa53f839db8b6c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745906"
---
# <span data-ttu-id="e24e7-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="e24e7-101">Update-AzActionRule</span></span>

## <span data-ttu-id="e24e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e24e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e24e7-103">Uppdaterar egenskaper för åtgärds regler.</span><span class="sxs-lookup"><span data-stu-id="e24e7-103">Updates action rule properties.</span></span>

## <span data-ttu-id="e24e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e24e7-104">SYNTAX</span></span>

### <span data-ttu-id="e24e7-105">ByNameSimplifiedPatch (standard)</span><span class="sxs-lookup"><span data-stu-id="e24e7-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e24e7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e24e7-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e24e7-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e24e7-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e24e7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e24e7-108">DESCRIPTION</span></span>
<span data-ttu-id="e24e7-109">**Update-AzActionRule** egenskaper för åtgärds regel – status och taggar.</span><span class="sxs-lookup"><span data-stu-id="e24e7-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="e24e7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e24e7-110">EXAMPLES</span></span>

### <span data-ttu-id="e24e7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e24e7-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="e24e7-112">Denna cmdlet inaktiverar åtgärds regeln.</span><span class="sxs-lookup"><span data-stu-id="e24e7-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="e24e7-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e24e7-113">PARAMETERS</span></span>

### <span data-ttu-id="e24e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24e7-114">-DefaultProfile</span></span>
<span data-ttu-id="e24e7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e24e7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e24e7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e24e7-116">-InputObject</span></span>
<span data-ttu-id="e24e7-117">Resurs för åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="e24e7-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e7-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e24e7-118">-Name</span></span>
<span data-ttu-id="e24e7-119">Namn på åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="e24e7-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24e7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e24e7-120">-ResourceGroupName</span></span>
<span data-ttu-id="e24e7-121">Namn på åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="e24e7-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24e7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e24e7-122">-ResourceId</span></span>
<span data-ttu-id="e24e7-123">Åtgärds regelns resurs-ID</span><span class="sxs-lookup"><span data-stu-id="e24e7-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e24e7-124">-Status</span><span class="sxs-lookup"><span data-stu-id="e24e7-124">-Status</span></span>
<span data-ttu-id="e24e7-125">Åtgärds regel status</span><span class="sxs-lookup"><span data-stu-id="e24e7-125">Action rule status</span></span>

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

### <span data-ttu-id="e24e7-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e24e7-126">-Tag</span></span>
<span data-ttu-id="e24e7-127">Åtgärds regel koder</span><span class="sxs-lookup"><span data-stu-id="e24e7-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e24e7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e24e7-128">-Confirm</span></span>
<span data-ttu-id="e24e7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e24e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24e7-130">-WhatIf</span></span>
<span data-ttu-id="e24e7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e24e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e24e7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e24e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24e7-133">CommonParameters</span></span>
<span data-ttu-id="e24e7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e24e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24e7-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e24e7-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24e7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e24e7-136">INPUTS</span></span>

### <span data-ttu-id="e24e7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e24e7-137">System.String</span></span>

### <span data-ttu-id="e24e7-138">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e24e7-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e24e7-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e24e7-139">OUTPUTS</span></span>

### <span data-ttu-id="e24e7-140">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e24e7-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e24e7-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e24e7-141">NOTES</span></span>

## <span data-ttu-id="e24e7-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e24e7-142">RELATED LINKS</span></span>
