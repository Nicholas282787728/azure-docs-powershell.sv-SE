---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: b78b992e74252f645faabcf284c817b1cb3c1d5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573743"
---
# <span data-ttu-id="94a63-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="94a63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94a63-102">SYNOPSIS</span></span>
<span data-ttu-id="94a63-103">Exporterar en automatiserings Runbook.</span><span class="sxs-lookup"><span data-stu-id="94a63-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94a63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94a63-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94a63-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94a63-105">DESCRIPTION</span></span>
<span data-ttu-id="94a63-106">Cmdleten **export-AzureRmAutomationRunbook** exporterar en Azure Automation-Runbook till en wps_2-skriptfil (. ps1) för wps_2 eller Wps_2 arbets flödes Runbooks eller till en grafisk Runbook (. graphrunbook) för grafiska runbooks.</span><span class="sxs-lookup"><span data-stu-id="94a63-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="94a63-107">Namnet på runbooken blir namnet på den exporterade filen.</span><span class="sxs-lookup"><span data-stu-id="94a63-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="94a63-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94a63-108">EXAMPLES</span></span>

### <span data-ttu-id="94a63-109">Exempel 1: exportera en Runbook</span><span class="sxs-lookup"><span data-stu-id="94a63-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="94a63-110">Det här kommandot exporterar den publicerade versionen av en automatiserings Runbook till ett användar skriv bord.</span><span class="sxs-lookup"><span data-stu-id="94a63-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="94a63-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94a63-111">PARAMETERS</span></span>

### <span data-ttu-id="94a63-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94a63-112">-AutomationAccountName</span></span>
<span data-ttu-id="94a63-113">Anger namnet på det Automation-konto som denna cmdlet exporterar en Runbook till.</span><span class="sxs-lookup"><span data-stu-id="94a63-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="94a63-114">-Force</span><span class="sxs-lookup"><span data-stu-id="94a63-114">-Force</span></span>
<span data-ttu-id="94a63-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="94a63-115">ps_force</span></span>

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

### <span data-ttu-id="94a63-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="94a63-116">-Name</span></span>
<span data-ttu-id="94a63-117">Anger namnet på den Runbook som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="94a63-117">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="94a63-118">Namnet på Runbook-flödet blir namnet på export filen.</span><span class="sxs-lookup"><span data-stu-id="94a63-118">The name of the runbook becomes the name of the export file.</span></span>

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

### <span data-ttu-id="94a63-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="94a63-119">-OutputFolder</span></span>
<span data-ttu-id="94a63-120">Anger sökvägen till en mapp där den här cmdleten skapar export filen.</span><span class="sxs-lookup"><span data-stu-id="94a63-120">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

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

### <span data-ttu-id="94a63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94a63-121">-ResourceGroupName</span></span>
<span data-ttu-id="94a63-122">Anger namnet på den resurs grupp för vilken denna cmdlet exporterar en Runbook.</span><span class="sxs-lookup"><span data-stu-id="94a63-122">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="94a63-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="94a63-123">-Slot</span></span>
<span data-ttu-id="94a63-124">Anger om denna cmdlet exporterar utkastet eller det publicerade innehållet för Runbook-flödet.</span><span class="sxs-lookup"><span data-stu-id="94a63-124">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="94a63-125">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="94a63-125">Valid values are:</span></span> 

- <span data-ttu-id="94a63-126">Opublicera</span><span class="sxs-lookup"><span data-stu-id="94a63-126">Published</span></span> 
- <span data-ttu-id="94a63-127">Runbook</span><span class="sxs-lookup"><span data-stu-id="94a63-127">Draft</span></span>

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

### <span data-ttu-id="94a63-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94a63-128">-Confirm</span></span>
<span data-ttu-id="94a63-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94a63-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94a63-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94a63-130">-WhatIf</span></span>
<span data-ttu-id="94a63-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94a63-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94a63-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94a63-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94a63-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94a63-133">-DefaultProfile</span></span>
<span data-ttu-id="94a63-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="94a63-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94a63-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94a63-135">CommonParameters</span></span>
<span data-ttu-id="94a63-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94a63-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94a63-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94a63-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94a63-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94a63-138">INPUTS</span></span>

## <span data-ttu-id="94a63-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94a63-139">OUTPUTS</span></span>

### <span data-ttu-id="94a63-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="94a63-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="94a63-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94a63-141">NOTES</span></span>

## <span data-ttu-id="94a63-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94a63-142">RELATED LINKS</span></span>

[<span data-ttu-id="94a63-143">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-143">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-144">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-144">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-145">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-145">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-146">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-147">Publicera – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-147">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-148">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-148">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-149">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-149">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="94a63-150">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="94a63-150">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


