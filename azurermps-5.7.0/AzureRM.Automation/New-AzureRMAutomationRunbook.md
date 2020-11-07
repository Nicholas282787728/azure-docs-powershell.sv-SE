---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757420"
---
# <span data-ttu-id="08c36-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="08c36-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08c36-102">SYNOPSIS</span></span>
<span data-ttu-id="08c36-103">Skapar en automatiserad Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="08c36-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08c36-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08c36-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08c36-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08c36-105">DESCRIPTION</span></span>
<span data-ttu-id="08c36-106">Cmdleten **New-AzureRmAutomationRunbook** skapar en tom Azure Automation-Runbook genom att använda APS.</span><span class="sxs-lookup"><span data-stu-id="08c36-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="08c36-107">Ange ett namn för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="08c36-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="08c36-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08c36-108">EXAMPLES</span></span>

### <span data-ttu-id="08c36-109">Exempel 1: skapa en Runbook</span><span class="sxs-lookup"><span data-stu-id="08c36-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="08c36-110">Det här kommandot skapar en Runbook med namnet Runbook02 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="08c36-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="08c36-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08c36-111">PARAMETERS</span></span>

### <span data-ttu-id="08c36-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08c36-112">-AutomationAccountName</span></span>
<span data-ttu-id="08c36-113">Anger namnet på Automation-kontot som den här cmdleten skapar en Runbook i.</span><span class="sxs-lookup"><span data-stu-id="08c36-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c36-114">-DefaultProfile</span></span>
<span data-ttu-id="08c36-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="08c36-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="08c36-116">-Description</span></span>
<span data-ttu-id="08c36-117">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="08c36-117">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="08c36-118">-LogProgress</span></span>
<span data-ttu-id="08c36-119">Anger om Runbook loggar status.</span><span class="sxs-lookup"><span data-stu-id="08c36-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="08c36-120">-LogVerbose</span></span>
<span data-ttu-id="08c36-121">Anger om loggning innehåller detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="08c36-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="08c36-122">-Name</span></span>
<span data-ttu-id="08c36-123">Anger ett namn för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="08c36-123">Specifies a name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c36-124">-ResourceGroupName</span></span>
<span data-ttu-id="08c36-125">Anger namnet på den resurs grupp för vilken denna cmdlet skapar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="08c36-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="08c36-126">-Tags</span></span>
<span data-ttu-id="08c36-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="08c36-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="08c36-128">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="08c36-128">For example:</span></span>

<span data-ttu-id="08c36-129">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="08c36-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-130">– Skriv</span><span class="sxs-lookup"><span data-stu-id="08c36-130">-Type</span></span>
<span data-ttu-id="08c36-131">Anger den typ av Runbook som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="08c36-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="08c36-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="08c36-132">Valid values are:</span></span>

- <span data-ttu-id="08c36-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="08c36-133">PowerShell</span></span>
- <span data-ttu-id="08c36-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="08c36-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="08c36-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="08c36-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="08c36-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="08c36-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="08c36-137">Graph</span><span class="sxs-lookup"><span data-stu-id="08c36-137">Graph</span></span>

<span data-ttu-id="08c36-138">Värde diagrammet är föråldrat.</span><span class="sxs-lookup"><span data-stu-id="08c36-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="08c36-139">Den motsvarar GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="08c36-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08c36-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c36-140">CommonParameters</span></span>
<span data-ttu-id="08c36-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c36-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c36-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08c36-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c36-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08c36-143">INPUTS</span></span>

### <span data-ttu-id="08c36-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="08c36-144">None</span></span>
<span data-ttu-id="08c36-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="08c36-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="08c36-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08c36-146">OUTPUTS</span></span>

### <span data-ttu-id="08c36-147">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="08c36-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="08c36-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08c36-148">NOTES</span></span>

## <span data-ttu-id="08c36-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08c36-149">RELATED LINKS</span></span>

[<span data-ttu-id="08c36-150">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="08c36-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="08c36-152">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="08c36-153">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="08c36-154">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="08c36-155">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="08c36-156">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="08c36-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
