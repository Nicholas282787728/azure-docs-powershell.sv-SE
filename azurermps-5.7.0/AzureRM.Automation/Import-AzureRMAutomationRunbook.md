---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1f7c50f0f5b11c80fce203b0c44128e380834bdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573563"
---
# <span data-ttu-id="5fa72-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="5fa72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5fa72-102">SYNOPSIS</span></span>
<span data-ttu-id="5fa72-103">Importerar en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="5fa72-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fa72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5fa72-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fa72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5fa72-105">DESCRIPTION</span></span>
<span data-ttu-id="5fa72-106">Cmdleten **import-AzureRmAutomationRunbook** importerar en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="5fa72-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="5fa72-107">Ange sökvägen till en wps_2-skriptfil (. ps1) som ska importeras för wps_2 och wps_2 arbets flödes-Runbook-filer (. graphrunbook) för grafiska runbooks eller (. py) för python 2 Runbooks.</span><span class="sxs-lookup"><span data-stu-id="5fa72-107">Specify the path to a wps_2 script (.ps1) file to import for wps_2 and wps_2 Workflow runbooks, (.graphrunbook) file for graphical runbooks, or (.py) file for python 2 runbooks.</span></span> <span data-ttu-id="5fa72-108">För wps_2 arbets flödes Runbooks måste skriptet innehålla en enda wps_2 arbets flödes definition som matchar namnet på filen.</span><span class="sxs-lookup"><span data-stu-id="5fa72-108">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="5fa72-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5fa72-109">EXAMPLES</span></span>

### <span data-ttu-id="5fa72-110">Exempel 1: importera en Runbook från en fil</span><span class="sxs-lookup"><span data-stu-id="5fa72-110">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="5fa72-111">Det första kommandot tilldelar två par tecken/värdepar till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="5fa72-111">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="5fa72-112">Med det andra kommandot importeras en grafisk Runbook med namnet GraphicalRunbook06 till Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="5fa72-112">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5fa72-113">Kommandot tilldelar också taggarna som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="5fa72-113">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="5fa72-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5fa72-114">PARAMETERS</span></span>

### <span data-ttu-id="5fa72-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5fa72-115">-AutomationAccountName</span></span>
<span data-ttu-id="5fa72-116">Anger namnet på det Automation-konto där denna cmdlet importerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="5fa72-116">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="5fa72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fa72-117">-DefaultProfile</span></span>
<span data-ttu-id="5fa72-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5fa72-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fa72-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="5fa72-119">-Description</span></span>
<span data-ttu-id="5fa72-120">Anger en beskrivning av den importerade Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="5fa72-120">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="5fa72-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5fa72-121">-Force</span></span>
<span data-ttu-id="5fa72-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="5fa72-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-123">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="5fa72-123">-LogProgress</span></span>
<span data-ttu-id="5fa72-124">Anger om förlopps information för Runbook loggar in.</span><span class="sxs-lookup"><span data-stu-id="5fa72-124">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="5fa72-125">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="5fa72-125">-LogVerbose</span></span>
<span data-ttu-id="5fa72-126">Anger om Runbook loggar detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="5fa72-126">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="5fa72-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="5fa72-127">-Name</span></span>
<span data-ttu-id="5fa72-128">Anger namnet på den Runbook som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="5fa72-128">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5fa72-129">-Path</span></span>
<span data-ttu-id="5fa72-130">Anger sökvägen till en. ps1-eller. graphrunbook-fil som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="5fa72-130">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-131">-Publicerad</span><span class="sxs-lookup"><span data-stu-id="5fa72-131">-Published</span></span>
<span data-ttu-id="5fa72-132">Anger att denna cmdlet publicerar den Runbook som den importerar.</span><span class="sxs-lookup"><span data-stu-id="5fa72-132">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fa72-133">-ResourceGroupName</span></span>
<span data-ttu-id="5fa72-134">Anger namnet på den resurs grupp som denna cmdlet importerar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="5fa72-134">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="5fa72-135">-Taggar</span><span class="sxs-lookup"><span data-stu-id="5fa72-135">-Tags</span></span>
<span data-ttu-id="5fa72-136">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5fa72-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5fa72-137">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="5fa72-137">For example:</span></span>

<span data-ttu-id="5fa72-138">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="5fa72-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5fa72-139">– Skriv</span><span class="sxs-lookup"><span data-stu-id="5fa72-139">-Type</span></span>
<span data-ttu-id="5fa72-140">Anger den typ av Runbook som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="5fa72-140">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="5fa72-141">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="5fa72-141">Valid values are:</span></span>

- <span data-ttu-id="5fa72-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5fa72-142">PowerShell</span></span>
- <span data-ttu-id="5fa72-143">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="5fa72-143">GraphicalPowerShell</span></span>
- <span data-ttu-id="5fa72-144">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="5fa72-144">PowerShellWorkflow</span></span>
- <span data-ttu-id="5fa72-145">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="5fa72-145">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="5fa72-146">Graph</span><span class="sxs-lookup"><span data-stu-id="5fa72-146">Graph</span></span>
- <span data-ttu-id="5fa72-147">Python2</span><span class="sxs-lookup"><span data-stu-id="5fa72-147">Python2</span></span>

<span data-ttu-id="5fa72-148">Värde diagrammet är föråldrat.</span><span class="sxs-lookup"><span data-stu-id="5fa72-148">The value Graph is obsolete.</span></span>
<span data-ttu-id="5fa72-149">Den motsvarar GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="5fa72-149">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5fa72-150">-Confirm</span></span>
<span data-ttu-id="5fa72-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5fa72-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fa72-152">-WhatIf</span></span>
<span data-ttu-id="5fa72-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5fa72-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fa72-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5fa72-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fa72-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fa72-155">CommonParameters</span></span>
<span data-ttu-id="5fa72-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fa72-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fa72-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fa72-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fa72-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5fa72-158">INPUTS</span></span>

### <span data-ttu-id="5fa72-159">Ingen</span><span class="sxs-lookup"><span data-stu-id="5fa72-159">None</span></span>
<span data-ttu-id="5fa72-160">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5fa72-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fa72-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5fa72-161">OUTPUTS</span></span>

### <span data-ttu-id="5fa72-162">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-162">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="5fa72-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5fa72-163">NOTES</span></span>

## <span data-ttu-id="5fa72-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5fa72-164">RELATED LINKS</span></span>

[<span data-ttu-id="5fa72-165">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-165">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-166">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-166">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-167">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-167">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-168">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-168">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-169">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-169">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-170">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-170">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-171">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-171">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="5fa72-172">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="5fa72-172">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
