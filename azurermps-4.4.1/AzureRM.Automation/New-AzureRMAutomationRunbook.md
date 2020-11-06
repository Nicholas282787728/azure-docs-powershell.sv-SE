---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578540"
---
# <span data-ttu-id="1eeeb-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="1eeeb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1eeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="1eeeb-103">Skapar en automatiserad Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eeeb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1eeeb-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eeeb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1eeeb-105">DESCRIPTION</span></span>
<span data-ttu-id="1eeeb-106">Cmdleten **New-AzureRmAutomationRunbook** skapar en tom Azure Automation-Runbook genom att använda APS.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="1eeeb-107">Ange ett namn för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="1eeeb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1eeeb-108">EXAMPLES</span></span>

### <span data-ttu-id="1eeeb-109">Exempel 1: skapa en Runbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1eeeb-110">Det här kommandot skapar en Runbook med namnet Runbook02 i Azure Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1eeeb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1eeeb-111">PARAMETERS</span></span>

### <span data-ttu-id="1eeeb-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1eeeb-112">-AutomationAccountName</span></span>
<span data-ttu-id="1eeeb-113">Anger namnet på Automation-kontot som den här cmdleten skapar en Runbook i.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="1eeeb-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="1eeeb-114">-Description</span></span>
<span data-ttu-id="1eeeb-115">Anger en beskrivning av Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="1eeeb-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="1eeeb-116">-LogProgress</span></span>
<span data-ttu-id="1eeeb-117">Anger om Runbook loggar status.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="1eeeb-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="1eeeb-118">-LogVerbose</span></span>
<span data-ttu-id="1eeeb-119">Anger om loggning innehåller detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="1eeeb-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1eeeb-120">-Name</span></span>
<span data-ttu-id="1eeeb-121">Anger ett namn för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="1eeeb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eeeb-122">-ResourceGroupName</span></span>
<span data-ttu-id="1eeeb-123">Anger namnet på den resurs grupp för vilken denna cmdlet skapar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="1eeeb-124">-Taggar</span><span class="sxs-lookup"><span data-stu-id="1eeeb-124">-Tags</span></span>
<span data-ttu-id="1eeeb-125">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1eeeb-126">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1eeeb-126">For example:</span></span>

<span data-ttu-id="1eeeb-127">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1eeeb-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1eeeb-128">– Skriv</span><span class="sxs-lookup"><span data-stu-id="1eeeb-128">-Type</span></span>
<span data-ttu-id="1eeeb-129">Anger den typ av Runbook som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="1eeeb-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1eeeb-130">Valid values are:</span></span>

- <span data-ttu-id="1eeeb-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1eeeb-131">PowerShell</span></span>
- <span data-ttu-id="1eeeb-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="1eeeb-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="1eeeb-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="1eeeb-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="1eeeb-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="1eeeb-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="1eeeb-135">Graph</span><span class="sxs-lookup"><span data-stu-id="1eeeb-135">Graph</span></span>

<span data-ttu-id="1eeeb-136">Värde diagrammet är föråldrat.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="1eeeb-137">Den motsvarar GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eeeb-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eeeb-138">-DefaultProfile</span></span>
<span data-ttu-id="1eeeb-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eeeb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eeeb-140">CommonParameters</span></span>
<span data-ttu-id="1eeeb-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eeeb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eeeb-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eeeb-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eeeb-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1eeeb-143">INPUTS</span></span>

## <span data-ttu-id="1eeeb-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1eeeb-144">OUTPUTS</span></span>

### <span data-ttu-id="1eeeb-145">Microsoft. Azure. commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="1eeeb-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="1eeeb-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1eeeb-146">NOTES</span></span>

## <span data-ttu-id="1eeeb-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1eeeb-147">RELATED LINKS</span></span>

[<span data-ttu-id="1eeeb-148">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1eeeb-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1eeeb-150">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1eeeb-151">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1eeeb-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1eeeb-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1eeeb-154">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1eeeb-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
