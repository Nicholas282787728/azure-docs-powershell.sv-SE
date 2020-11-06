---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 52ed2c5925758a4d40fdf39dcdadf73eb2fc53b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573016"
---
# <span data-ttu-id="2e295-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="2e295-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="2e295-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e295-102">SYNOPSIS</span></span>
<span data-ttu-id="2e295-103">Exporterar RAW-innehållet i en DSC-rapport som skickas från en DSC-nod till Automation.</span><span class="sxs-lookup"><span data-stu-id="2e295-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e295-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e295-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e295-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e295-105">DESCRIPTION</span></span>
<span data-ttu-id="2e295-106">Cmdleten **export-AzureRmAutomationDscNodeReportContent** exporterar det råa innehållet i en DSC-rapport (Desired State Configuration) för en APS.</span><span class="sxs-lookup"><span data-stu-id="2e295-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="2e295-107">En DSC-nod skickar en DSC-rapport till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2e295-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="2e295-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e295-108">EXAMPLES</span></span>

### <span data-ttu-id="2e295-109">Exempel 1: exportera en rapport från en DSC-nod</span><span class="sxs-lookup"><span data-stu-id="2e295-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="2e295-110">Denna uppsättning kommandon exporterar den senaste rapporten från DSC-noden som heter Computer14 till Skriv bordet.</span><span class="sxs-lookup"><span data-stu-id="2e295-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="2e295-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e295-111">PARAMETERS</span></span>

### <span data-ttu-id="2e295-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2e295-112">-AutomationAccountName</span></span>
<span data-ttu-id="2e295-113">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="2e295-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="2e295-114">Denna cmdlet exporterar rapport innehåll för en DSC-nod som tillhör det Automation-konto som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2e295-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="2e295-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e295-115">-DefaultProfile</span></span>
<span data-ttu-id="2e295-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2e295-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e295-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e295-117">-Force</span></span>
<span data-ttu-id="2e295-118">Anger att denna cmdlet ersätter en befintlig lokal fil med en ny fil med samma namn.</span><span class="sxs-lookup"><span data-stu-id="2e295-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="2e295-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="2e295-119">-NodeId</span></span>
<span data-ttu-id="2e295-120">Anger det unika ID: t för DSC-noden för vilken denna cmdlet exporterar rapport innehållet.</span><span class="sxs-lookup"><span data-stu-id="2e295-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e295-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="2e295-121">-OutputFolder</span></span>
<span data-ttu-id="2e295-122">Anger mappen utdata där denna cmdlet exporterar rapport innehållet.</span><span class="sxs-lookup"><span data-stu-id="2e295-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="2e295-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="2e295-123">-ReportId</span></span>
<span data-ttu-id="2e295-124">Anger unikt ID för DSC-nodens rapport som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="2e295-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e295-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e295-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e295-126">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2e295-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2e295-127">Denna cmdlet exporterar innehållet i en rapport för DSC-noden som tillhör resurs gruppen som denna cmdlet anger.</span><span class="sxs-lookup"><span data-stu-id="2e295-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="2e295-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e295-128">-Confirm</span></span>
<span data-ttu-id="2e295-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e295-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e295-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e295-130">-WhatIf</span></span>
<span data-ttu-id="2e295-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e295-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e295-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e295-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e295-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e295-133">CommonParameters</span></span>
<span data-ttu-id="2e295-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e295-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e295-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e295-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e295-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e295-136">INPUTS</span></span>

### <span data-ttu-id="2e295-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2e295-137">System.Guid</span></span>

### <span data-ttu-id="2e295-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2e295-138">System.String</span></span>

## <span data-ttu-id="2e295-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e295-139">OUTPUTS</span></span>

### <span data-ttu-id="2e295-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="2e295-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="2e295-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e295-141">NOTES</span></span>

## <span data-ttu-id="2e295-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e295-142">RELATED LINKS</span></span>

[<span data-ttu-id="2e295-143">Exportera-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="2e295-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="2e295-144">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="2e295-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="2e295-145">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="2e295-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


