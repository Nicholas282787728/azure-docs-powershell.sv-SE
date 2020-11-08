---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationRunbook.md
ms.openlocfilehash: 03a57c35063a401aa5f730e11538532bdbbbc58c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090445"
---
# <span data-ttu-id="656c8-101">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-101">Export-AzAutomationRunbook</span></span>

## <span data-ttu-id="656c8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="656c8-102">SYNOPSIS</span></span>
<span data-ttu-id="656c8-103">Exporterar en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="656c8-103">Exports an Automation runbook.</span></span>

## <span data-ttu-id="656c8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="656c8-104">SYNTAX</span></span>

```
Export-AzAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="656c8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="656c8-105">DESCRIPTION</span></span>
<span data-ttu-id="656c8-106">Cmdleten **export-AzAutomationRunbook** exporterar en Azure Automation-Runbook till en wps_2-skriptfil (. ps1) för wps_2 eller Wps_2 arbets flödes Runbooks eller till en grafisk Runbook (. graphrunbook) för grafiska runbooks.</span><span class="sxs-lookup"><span data-stu-id="656c8-106">The **Export-AzAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="656c8-107">Namnet på runbooken blir namnet på den exporterade filen.</span><span class="sxs-lookup"><span data-stu-id="656c8-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="656c8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="656c8-108">EXAMPLES</span></span>

### <span data-ttu-id="656c8-109">Exempel 1: exportera en Runbook</span><span class="sxs-lookup"><span data-stu-id="656c8-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="656c8-110">Det här kommandot exporterar den publicerade versionen av en automatiserings Runbook till ett användar skriv bord.</span><span class="sxs-lookup"><span data-stu-id="656c8-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="656c8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="656c8-111">PARAMETERS</span></span>

### <span data-ttu-id="656c8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="656c8-112">-AutomationAccountName</span></span>
<span data-ttu-id="656c8-113">Anger namnet på det Automation-konto som denna cmdlet exporterar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="656c8-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="656c8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="656c8-114">-DefaultProfile</span></span>
<span data-ttu-id="656c8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="656c8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="656c8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="656c8-116">-Force</span></span>
<span data-ttu-id="656c8-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="656c8-117">ps_force</span></span>

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

### <span data-ttu-id="656c8-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="656c8-118">-Name</span></span>
<span data-ttu-id="656c8-119">Anger namnet på den Runbook som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="656c8-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="656c8-120">Namnet på Runbook-flödet blir namnet på export filen.</span><span class="sxs-lookup"><span data-stu-id="656c8-120">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="656c8-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="656c8-121">-OutputFolder</span></span>
<span data-ttu-id="656c8-122">Anger sökvägen till en mapp där den här cmdleten skapar export filen.</span><span class="sxs-lookup"><span data-stu-id="656c8-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="656c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="656c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="656c8-124">Anger namnet på den resurs grupp för vilken denna cmdlet exporterar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="656c8-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="656c8-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="656c8-125">-Slot</span></span>
<span data-ttu-id="656c8-126">Anger om denna cmdlet exporterar utkastet eller det publicerade innehållet för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="656c8-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="656c8-127">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="656c8-127">Valid values are:</span></span> 
- <span data-ttu-id="656c8-128">Opublicera</span><span class="sxs-lookup"><span data-stu-id="656c8-128">Published</span></span> 
- <span data-ttu-id="656c8-129">Runbook</span><span class="sxs-lookup"><span data-stu-id="656c8-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="656c8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="656c8-130">-Confirm</span></span>
<span data-ttu-id="656c8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="656c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="656c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="656c8-132">-WhatIf</span></span>
<span data-ttu-id="656c8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="656c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="656c8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="656c8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="656c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="656c8-135">CommonParameters</span></span>
<span data-ttu-id="656c8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="656c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="656c8-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="656c8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="656c8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="656c8-138">INPUTS</span></span>

### <span data-ttu-id="656c8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="656c8-139">System.String</span></span>

## <span data-ttu-id="656c8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="656c8-140">OUTPUTS</span></span>

### <span data-ttu-id="656c8-141">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="656c8-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="656c8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="656c8-142">NOTES</span></span>

## <span data-ttu-id="656c8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="656c8-143">RELATED LINKS</span></span>

[<span data-ttu-id="656c8-144">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-144">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-145">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-145">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-146">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-146">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-148">Publicera – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-148">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-149">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-149">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-150">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-150">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="656c8-151">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="656c8-151">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


