---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524890"
---
# <span data-ttu-id="ea5d7-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="ea5d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5d7-103">Tar bort en Runbook.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-103">Removes a runbook.</span></span>

## <span data-ttu-id="ea5d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea5d7-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea5d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5d7-106">Cmdleten **Remove-AzAutomationRunbook** tar bort en Runbook från Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="ea5d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea5d7-107">EXAMPLES</span></span>

### <span data-ttu-id="ea5d7-108">Exempel 1: ta bort en Runbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ea5d7-109">Det här kommandot tar bort Runbook-flödet med namnet Runbook03 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ea5d7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea5d7-110">PARAMETERS</span></span>

### <span data-ttu-id="ea5d7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ea5d7-111">-AutomationAccountName</span></span>
<span data-ttu-id="ea5d7-112">Anger namnet på det Automation-konto som denna cmdlet tar bort en Runbook för.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="ea5d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5d7-113">-DefaultProfile</span></span>
<span data-ttu-id="ea5d7-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ea5d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea5d7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ea5d7-115">-Force</span></span>
<span data-ttu-id="ea5d7-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="ea5d7-116">ps_force</span></span>

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

### <span data-ttu-id="ea5d7-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ea5d7-117">-Name</span></span>
<span data-ttu-id="ea5d7-118">Anger namnet på den Runbook som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea5d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea5d7-120">Anger namnet på den resurs grupp för vilken denna cmdlet publicerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="ea5d7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea5d7-121">-Confirm</span></span>
<span data-ttu-id="ea5d7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5d7-123">-WhatIf</span></span>
<span data-ttu-id="ea5d7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea5d7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5d7-126">CommonParameters</span></span>
<span data-ttu-id="ea5d7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5d7-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea5d7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5d7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea5d7-129">INPUTS</span></span>

### <span data-ttu-id="ea5d7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ea5d7-130">System.String</span></span>

## <span data-ttu-id="ea5d7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea5d7-131">OUTPUTS</span></span>

### <span data-ttu-id="ea5d7-132">System. Void</span><span class="sxs-lookup"><span data-stu-id="ea5d7-132">System.Void</span></span>

## <span data-ttu-id="ea5d7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea5d7-133">NOTES</span></span>

## <span data-ttu-id="ea5d7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea5d7-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea5d7-135">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-140">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="ea5d7-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ea5d7-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


