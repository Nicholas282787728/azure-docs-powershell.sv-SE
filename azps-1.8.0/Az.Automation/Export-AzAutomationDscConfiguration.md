---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 8abd6859054245c6265cc32695fa56168aabd1c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754881"
---
# <span data-ttu-id="7cc9c-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc9c-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="7cc9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7cc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc9c-103">Exporterar en DSC-konfiguration från Automation till en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="7cc9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7cc9c-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cc9c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7cc9c-105">DESCRIPTION</span></span>
<span data-ttu-id="7cc9c-106">Cmdleten **export-AzAutomationDscConfiguration** exporterar en DSC-konfiguration (önskad tillstånds konfiguration) från Azure Automation till en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="7cc9c-107">Den exporterade filen har fil namns tillägget. ps1.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="7cc9c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7cc9c-108">EXAMPLES</span></span>

### <span data-ttu-id="7cc9c-109">Exempel 1: exportera den publicerade versionen av en DSC-konfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc9c-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="7cc9c-110">Det här kommandot exporterar den publicerade versionen av en DSC-konfiguration i Automation till den angivna mappen, som är Skriv bordet.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="7cc9c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7cc9c-111">PARAMETERS</span></span>

### <span data-ttu-id="7cc9c-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7cc9c-112">-AutomationAccountName</span></span>
<span data-ttu-id="7cc9c-113">Anger namnet på det Automation-konto som innehåller den DSC som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="7cc9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc9c-114">-DefaultProfile</span></span>
<span data-ttu-id="7cc9c-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7cc9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cc9c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7cc9c-116">-Force</span></span>
<span data-ttu-id="7cc9c-117">Anger att denna cmdlet ersätter en befintlig lokal fil med en ny fil med samma namn.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="7cc9c-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7cc9c-118">-Name</span></span>
<span data-ttu-id="7cc9c-119">Anger namnet på den DSC-konfiguration som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc9c-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="7cc9c-120">-OutputFolder</span></span>
<span data-ttu-id="7cc9c-121">Anger mappen utdata där denna cmdlet exporterar DSC-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="7cc9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="7cc9c-123">Anger namnet på en resurs grupp för vilken denna cmdlet exporterar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="7cc9c-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="7cc9c-124">-Slot</span></span>
<span data-ttu-id="7cc9c-125">Anger vilken version av DSC-konfigurationen som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="7cc9c-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="7cc9c-126">Valid values are:</span></span> 
- <span data-ttu-id="7cc9c-127">Runbook</span><span class="sxs-lookup"><span data-stu-id="7cc9c-127">Draft</span></span>
- <span data-ttu-id="7cc9c-128">Publicerat standardvärdet är publicerat.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc9c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7cc9c-129">-Confirm</span></span>
<span data-ttu-id="7cc9c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cc9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cc9c-131">-WhatIf</span></span>
<span data-ttu-id="7cc9c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cc9c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cc9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc9c-134">CommonParameters</span></span>
<span data-ttu-id="7cc9c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc9c-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc9c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc9c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7cc9c-137">INPUTS</span></span>

### <span data-ttu-id="7cc9c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc9c-138">System.String</span></span>

## <span data-ttu-id="7cc9c-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7cc9c-139">OUTPUTS</span></span>

### <span data-ttu-id="7cc9c-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="7cc9c-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="7cc9c-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7cc9c-141">NOTES</span></span>

## <span data-ttu-id="7cc9c-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7cc9c-142">RELATED LINKS</span></span>

[<span data-ttu-id="7cc9c-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc9c-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="7cc9c-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cc9c-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


