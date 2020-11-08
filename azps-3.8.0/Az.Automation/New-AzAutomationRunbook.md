---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: 25690d1e125dbfe2a7588665ff4dbc71215e21d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092693"
---
# <span data-ttu-id="bb524-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="bb524-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb524-102">SYNOPSIS</span></span>
<span data-ttu-id="bb524-103">Skapar en automatiserad Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="bb524-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="bb524-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb524-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb524-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb524-105">DESCRIPTION</span></span>
<span data-ttu-id="bb524-106">Cmdleten **New-AzAutomationRunbook** skapar en tom Azure Automation-Runbook genom att använda APS.</span><span class="sxs-lookup"><span data-stu-id="bb524-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="bb524-107">Ange ett namn för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="bb524-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="bb524-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb524-108">EXAMPLES</span></span>

### <span data-ttu-id="bb524-109">Exempel 1: skapa en Runbook</span><span class="sxs-lookup"><span data-stu-id="bb524-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bb524-110">Det här kommandot skapar en Runbook med namnet Runbook02 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bb524-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="bb524-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb524-111">PARAMETERS</span></span>

### <span data-ttu-id="bb524-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb524-112">-AutomationAccountName</span></span>
<span data-ttu-id="bb524-113">Anger namnet på Automation-kontot som den här cmdleten skapar en Runbook i.</span><span class="sxs-lookup"><span data-stu-id="bb524-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="bb524-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb524-114">-DefaultProfile</span></span>
<span data-ttu-id="bb524-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bb524-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb524-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="bb524-116">-Description</span></span>
<span data-ttu-id="bb524-117">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="bb524-117">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb524-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="bb524-118">-LogProgress</span></span>
<span data-ttu-id="bb524-119">Anger om Runbook loggar status.</span><span class="sxs-lookup"><span data-stu-id="bb524-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb524-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="bb524-120">-LogVerbose</span></span>
<span data-ttu-id="bb524-121">Anger om loggning innehåller detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="bb524-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb524-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb524-122">-Name</span></span>
<span data-ttu-id="bb524-123">Anger ett namn för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="bb524-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="bb524-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb524-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb524-125">Anger namnet på den resurs grupp för vilken denna cmdlet skapar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="bb524-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="bb524-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="bb524-126">-Tags</span></span>
<span data-ttu-id="bb524-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="bb524-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bb524-128">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="bb524-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb524-129">– Skriv</span><span class="sxs-lookup"><span data-stu-id="bb524-129">-Type</span></span>
<span data-ttu-id="bb524-130">Anger den typ av Runbook som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="bb524-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="bb524-131">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="bb524-131">Valid values are:</span></span>
- <span data-ttu-id="bb524-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="bb524-132">PowerShell</span></span>
- <span data-ttu-id="bb524-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="bb524-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="bb524-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bb524-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="bb524-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="bb524-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="bb524-136">Graph</span><span class="sxs-lookup"><span data-stu-id="bb524-136">Graph</span></span>
- <span data-ttu-id="bb524-137">Python2 värde diagrammet är föråldrat.</span><span class="sxs-lookup"><span data-stu-id="bb524-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="bb524-138">Den motsvarar GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="bb524-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb524-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb524-139">CommonParameters</span></span>
<span data-ttu-id="bb524-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb524-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb524-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb524-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb524-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb524-142">INPUTS</span></span>

### <span data-ttu-id="bb524-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bb524-143">System.String</span></span>

### <span data-ttu-id="bb524-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bb524-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="bb524-145">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bb524-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bb524-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb524-146">OUTPUTS</span></span>

### <span data-ttu-id="bb524-147">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="bb524-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="bb524-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb524-148">NOTES</span></span>

## <span data-ttu-id="bb524-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb524-149">RELATED LINKS</span></span>

[<span data-ttu-id="bb524-150">Exportera-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="bb524-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="bb524-152">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="bb524-153">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="bb524-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="bb524-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="bb524-156">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="bb524-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
