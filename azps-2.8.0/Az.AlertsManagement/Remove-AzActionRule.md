---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 2e0f204fa5eaed80133d699f0381e9116911b581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745908"
---
# <span data-ttu-id="ef314-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="ef314-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="ef314-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef314-102">SYNOPSIS</span></span>
<span data-ttu-id="ef314-103">Tar bort en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="ef314-103">Deletes a action group</span></span>

## <span data-ttu-id="ef314-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef314-104">SYNTAX</span></span>

### <span data-ttu-id="ef314-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="ef314-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef314-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ef314-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef314-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef314-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef314-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef314-108">DESCRIPTION</span></span>
<span data-ttu-id="ef314-109">**Remove-AzActionRule** cmdlet tar bort en åtgärds regel.</span><span class="sxs-lookup"><span data-stu-id="ef314-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="ef314-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef314-110">EXAMPLES</span></span>

### <span data-ttu-id="ef314-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef314-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="ef314-112">Denna cmdlet tar bort åtgärds regeln med namn ActionRuleName i resurs grupp test-rg</span><span class="sxs-lookup"><span data-stu-id="ef314-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="ef314-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef314-113">PARAMETERS</span></span>

### <span data-ttu-id="ef314-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef314-114">-DefaultProfile</span></span>
<span data-ttu-id="ef314-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef314-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef314-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef314-116">-InputObject</span></span>
<span data-ttu-id="ef314-117">Resurs för åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="ef314-117">The action rule resource</span></span>

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

### <span data-ttu-id="ef314-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef314-118">-Name</span></span>
<span data-ttu-id="ef314-119">Namn på åtgärds regel</span><span class="sxs-lookup"><span data-stu-id="ef314-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef314-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef314-120">-PassThru</span></span>
<span data-ttu-id="ef314-121">PassThru returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ef314-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ef314-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ef314-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef314-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef314-123">-ResourceGroupName</span></span>
<span data-ttu-id="ef314-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ef314-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef314-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef314-125">-ResourceId</span></span>
<span data-ttu-id="ef314-126">Hämta åtgärds regel efter resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ef314-126">Get Action rule by resoure id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef314-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef314-127">-Confirm</span></span>
<span data-ttu-id="ef314-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef314-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef314-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef314-129">-WhatIf</span></span>
<span data-ttu-id="ef314-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef314-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef314-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef314-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef314-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef314-132">CommonParameters</span></span>
<span data-ttu-id="ef314-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef314-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef314-134">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef314-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef314-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef314-135">INPUTS</span></span>

### <span data-ttu-id="ef314-136">Microsoft. Azure. commands. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="ef314-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="ef314-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef314-137">OUTPUTS</span></span>

### <span data-ttu-id="ef314-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef314-138">System.Boolean</span></span>

## <span data-ttu-id="ef314-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef314-139">NOTES</span></span>

## <span data-ttu-id="ef314-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef314-140">RELATED LINKS</span></span>