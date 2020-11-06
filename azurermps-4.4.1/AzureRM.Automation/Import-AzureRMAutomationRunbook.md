---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578555"
---
# <span data-ttu-id="ee51e-101">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-101">Import-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ee51e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee51e-102">SYNOPSIS</span></span>
<span data-ttu-id="ee51e-103">Importerar en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="ee51e-103">Imports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee51e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee51e-104">SYNTAX</span></span>

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee51e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee51e-105">DESCRIPTION</span></span>
<span data-ttu-id="ee51e-106">Cmdleten **import-AzureRmAutomationRunbook** importerar en Azure Automation-Runbook.</span><span class="sxs-lookup"><span data-stu-id="ee51e-106">The **Import-AzureRmAutomationRunbook** cmdlet imports an Azure Automation runbook.</span></span> <span data-ttu-id="ee51e-107">Ange sökvägen till en wps_2-skriptfil (. ps1) som du vill importera för wps_2 och wps_2 arbets flödes-eller graphrunbook-filer för grafiska runbooks.</span><span class="sxs-lookup"><span data-stu-id="ee51e-107">Specify the path to a wps_2 script (.ps1 ) file to import for wps_2 and wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file for graphical runbooks.</span></span> <span data-ttu-id="ee51e-108">Namnet på filen blir namnet på Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="ee51e-108">The name of the file becomes the name of the runbook.</span></span> <span data-ttu-id="ee51e-109">För wps_2 arbets flödes Runbooks måste skriptet innehålla en enda wps_2 arbets flödes definition som matchar namnet på filen.</span><span class="sxs-lookup"><span data-stu-id="ee51e-109">For wps_2 Workflow runbooks, the script must contain a single wps_2 Workflow definition that matches the name of the file.</span></span>

## <span data-ttu-id="ee51e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee51e-110">EXAMPLES</span></span>

### <span data-ttu-id="ee51e-111">Exempel 1: importera en Runbook från en fil</span><span class="sxs-lookup"><span data-stu-id="ee51e-111">Example 1: Import a runbook from a file</span></span>
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

<span data-ttu-id="ee51e-112">Det första kommandot tilldelar två par tecken/värdepar till variabeln $Tags.</span><span class="sxs-lookup"><span data-stu-id="ee51e-112">The first command assigns two key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="ee51e-113">Med det andra kommandot importeras en grafisk Runbook med namnet GraphicalRunbook06 till Automation-kontot med namnet AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="ee51e-113">The second command imports a graphical runbook called GraphicalRunbook06 into the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="ee51e-114">Kommandot tilldelar också taggarna som lagras i $Tags.</span><span class="sxs-lookup"><span data-stu-id="ee51e-114">The command also assigns the tags stored in $Tags.</span></span>

## <span data-ttu-id="ee51e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee51e-115">PARAMETERS</span></span>

### <span data-ttu-id="ee51e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ee51e-116">-AutomationAccountName</span></span>
<span data-ttu-id="ee51e-117">Anger namnet på det Automation-konto där denna cmdlet importerar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="ee51e-117">Specifies the name of the Automation account into which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="ee51e-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ee51e-118">-Description</span></span>
<span data-ttu-id="ee51e-119">Anger en beskrivning av den importerade Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="ee51e-119">Specifies a description for the imported runbook.</span></span>

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

### <span data-ttu-id="ee51e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ee51e-120">-Force</span></span>
<span data-ttu-id="ee51e-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="ee51e-121">ps_force</span></span>

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

### <span data-ttu-id="ee51e-122">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="ee51e-122">-LogProgress</span></span>
<span data-ttu-id="ee51e-123">Anger om förlopps information för Runbook loggar in.</span><span class="sxs-lookup"><span data-stu-id="ee51e-123">Specifies whether the runbook logs progress information.</span></span>

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

### <span data-ttu-id="ee51e-124">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="ee51e-124">-LogVerbose</span></span>
<span data-ttu-id="ee51e-125">Anger om Runbook loggar detaljerad information.</span><span class="sxs-lookup"><span data-stu-id="ee51e-125">Specifies whether the runbook logs detailed information.</span></span>

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

### <span data-ttu-id="ee51e-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee51e-126">-Name</span></span>
<span data-ttu-id="ee51e-127">Anger namnet på den Runbook som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="ee51e-127">Specifies the name of the runbook that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee51e-128">-Path</span><span class="sxs-lookup"><span data-stu-id="ee51e-128">-Path</span></span>
<span data-ttu-id="ee51e-129">Anger sökvägen till en. ps1-eller. graphrunbook-fil som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="ee51e-129">Specifies the path of a .ps1 or .graphrunbook file that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee51e-130">-Publicerad</span><span class="sxs-lookup"><span data-stu-id="ee51e-130">-Published</span></span>
<span data-ttu-id="ee51e-131">Anger att denna cmdlet publicerar den Runbook som den importerar.</span><span class="sxs-lookup"><span data-stu-id="ee51e-131">Indicates that this cmdlet publishes the runbook that it imports.</span></span>

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

### <span data-ttu-id="ee51e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee51e-132">-ResourceGroupName</span></span>
<span data-ttu-id="ee51e-133">Anger namnet på den resurs grupp som denna cmdlet importerar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="ee51e-133">Specifies the name of the resource group for which this cmdlet imports a runbook.</span></span>

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

### <span data-ttu-id="ee51e-134">-Taggar</span><span class="sxs-lookup"><span data-stu-id="ee51e-134">-Tags</span></span>
<span data-ttu-id="ee51e-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ee51e-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ee51e-136">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ee51e-136">For example:</span></span>

<span data-ttu-id="ee51e-137">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="ee51e-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ee51e-138">– Skriv</span><span class="sxs-lookup"><span data-stu-id="ee51e-138">-Type</span></span>
<span data-ttu-id="ee51e-139">Anger den typ av Runbook som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ee51e-139">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="ee51e-140">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="ee51e-140">Valid values are:</span></span>

- <span data-ttu-id="ee51e-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee51e-141">PowerShell</span></span>
- <span data-ttu-id="ee51e-142">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="ee51e-142">GraphicalPowerShell</span></span>
- <span data-ttu-id="ee51e-143">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="ee51e-143">PowerShellWorkflow</span></span>
- <span data-ttu-id="ee51e-144">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="ee51e-144">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="ee51e-145">Graph</span><span class="sxs-lookup"><span data-stu-id="ee51e-145">Graph</span></span>

<span data-ttu-id="ee51e-146">Värde diagrammet är föråldrat.</span><span class="sxs-lookup"><span data-stu-id="ee51e-146">The value Graph is obsolete.</span></span>
<span data-ttu-id="ee51e-147">Den motsvarar GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="ee51e-147">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="ee51e-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ee51e-148">-Confirm</span></span>
<span data-ttu-id="ee51e-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ee51e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee51e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee51e-150">-WhatIf</span></span>
<span data-ttu-id="ee51e-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ee51e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee51e-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ee51e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee51e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee51e-153">-DefaultProfile</span></span>
<span data-ttu-id="ee51e-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee51e-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee51e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee51e-155">CommonParameters</span></span>
<span data-ttu-id="ee51e-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee51e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee51e-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee51e-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee51e-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee51e-158">INPUTS</span></span>

## <span data-ttu-id="ee51e-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee51e-159">OUTPUTS</span></span>

### <span data-ttu-id="ee51e-160">Microsoft. Azure. commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-160">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ee51e-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee51e-161">NOTES</span></span>

## <span data-ttu-id="ee51e-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee51e-162">RELATED LINKS</span></span>

[<span data-ttu-id="ee51e-163">Exportera-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-163">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-164">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-164">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-165">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-165">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-166">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-166">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-167">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-167">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-168">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-168">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-169">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-169">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ee51e-170">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ee51e-170">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
