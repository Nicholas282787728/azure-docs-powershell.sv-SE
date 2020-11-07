---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: c77413f27bcde145334221465cbe792a5e1eaa5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745485"
---
# <span data-ttu-id="e57b3-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="e57b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e57b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e57b3-103">Tar bort en Runbook.</span><span class="sxs-lookup"><span data-stu-id="e57b3-103">Removes a runbook.</span></span>

## <span data-ttu-id="e57b3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e57b3-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e57b3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e57b3-105">DESCRIPTION</span></span>
<span data-ttu-id="e57b3-106">Cmdleten **Remove-AzAutomationRunbook** tar bort en Runbook från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e57b3-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="e57b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e57b3-107">EXAMPLES</span></span>

### <span data-ttu-id="e57b3-108">Exempel 1: ta bort en Runbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e57b3-109">Det här kommandot tar bort Runbook-flödet med namnet Runbook03 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e57b3-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e57b3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e57b3-110">PARAMETERS</span></span>

### <span data-ttu-id="e57b3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e57b3-111">-AutomationAccountName</span></span>
<span data-ttu-id="e57b3-112">Anger namnet på det Automation-konto som denna cmdlet tar bort en Runbook för.</span><span class="sxs-lookup"><span data-stu-id="e57b3-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57b3-113">-DefaultProfile</span></span>
<span data-ttu-id="e57b3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e57b3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e57b3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e57b3-115">-Force</span></span>
<span data-ttu-id="e57b3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="e57b3-116">ps_force</span></span>

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

### <span data-ttu-id="e57b3-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e57b3-117">-Name</span></span>
<span data-ttu-id="e57b3-118">Anger namnet på den Runbook som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="e57b3-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57b3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57b3-119">-ResourceGroupName</span></span>
<span data-ttu-id="e57b3-120">Anger namnet på den resurs grupp för vilken denna cmdlet publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="e57b3-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57b3-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e57b3-121">-Confirm</span></span>
<span data-ttu-id="e57b3-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e57b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e57b3-123">-WhatIf</span></span>
<span data-ttu-id="e57b3-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e57b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e57b3-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e57b3-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e57b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57b3-126">CommonParameters</span></span>
<span data-ttu-id="e57b3-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57b3-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e57b3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57b3-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e57b3-129">INPUTS</span></span>

### <span data-ttu-id="e57b3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e57b3-130">System.String</span></span>

## <span data-ttu-id="e57b3-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e57b3-131">OUTPUTS</span></span>

### <span data-ttu-id="e57b3-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="e57b3-132">System.Void</span></span>

## <span data-ttu-id="e57b3-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e57b3-133">NOTES</span></span>

## <span data-ttu-id="e57b3-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e57b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="e57b3-135">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-140">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="e57b3-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e57b3-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


