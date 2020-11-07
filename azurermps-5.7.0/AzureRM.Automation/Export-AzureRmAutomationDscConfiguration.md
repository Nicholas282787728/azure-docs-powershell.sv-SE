---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2f739c9471e2a6144c12033ade885a445bade12e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757422"
---
# <span data-ttu-id="69745-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="69745-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="69745-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69745-102">SYNOPSIS</span></span>
<span data-ttu-id="69745-103">Exporterar en DSC-konfiguration från Automation till en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="69745-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69745-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69745-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69745-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69745-105">DESCRIPTION</span></span>
<span data-ttu-id="69745-106">Cmdleten **export-AzureRmAutomationDscConfiguration** exporterar en DSC-konfiguration (önskad tillstånds konfiguration) från Azure Automation till en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="69745-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="69745-107">Den exporterade filen har fil namns tillägget. ps1.</span><span class="sxs-lookup"><span data-stu-id="69745-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="69745-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69745-108">EXAMPLES</span></span>

### <span data-ttu-id="69745-109">Exempel 1: exportera den publicerade versionen av en DSC-konfiguration</span><span class="sxs-lookup"><span data-stu-id="69745-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="69745-110">Det här kommandot exporterar den publicerade versionen av en DSC-konfiguration i Automation till den angivna mappen, som är Skriv bordet.</span><span class="sxs-lookup"><span data-stu-id="69745-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="69745-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69745-111">PARAMETERS</span></span>

### <span data-ttu-id="69745-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="69745-112">-AutomationAccountName</span></span>
<span data-ttu-id="69745-113">Anger namnet på det Automation-konto som innehåller den DSC som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="69745-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="69745-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69745-114">-DefaultProfile</span></span>
<span data-ttu-id="69745-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="69745-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69745-116">-Force</span><span class="sxs-lookup"><span data-stu-id="69745-116">-Force</span></span>
<span data-ttu-id="69745-117">Anger att denna cmdlet ersätter en befintlig lokal fil med en ny fil med samma namn.</span><span class="sxs-lookup"><span data-stu-id="69745-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="69745-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="69745-118">-Name</span></span>
<span data-ttu-id="69745-119">Anger namnet på den DSC-konfiguration som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="69745-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69745-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="69745-120">-OutputFolder</span></span>
<span data-ttu-id="69745-121">Anger mappen utdata där denna cmdlet exporterar DSC-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="69745-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="69745-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69745-122">-ResourceGroupName</span></span>
<span data-ttu-id="69745-123">Anger namnet på en resurs grupp för vilken denna cmdlet exporterar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="69745-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="69745-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="69745-124">-Slot</span></span>
<span data-ttu-id="69745-125">Anger vilken version av DSC-konfigurationen som denna cmdlet exporterar.</span><span class="sxs-lookup"><span data-stu-id="69745-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="69745-126">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="69745-126">Valid values are:</span></span> 

- <span data-ttu-id="69745-127">Runbook</span><span class="sxs-lookup"><span data-stu-id="69745-127">Draft</span></span>
- <span data-ttu-id="69745-128">Opublicera</span><span class="sxs-lookup"><span data-stu-id="69745-128">Published</span></span> 

<span data-ttu-id="69745-129">Standardvärdet är publicerat.</span><span class="sxs-lookup"><span data-stu-id="69745-129">The default value is Published.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69745-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="69745-130">-Confirm</span></span>
<span data-ttu-id="69745-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="69745-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69745-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69745-132">-WhatIf</span></span>
<span data-ttu-id="69745-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="69745-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69745-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="69745-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69745-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69745-135">CommonParameters</span></span>
<span data-ttu-id="69745-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69745-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69745-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69745-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69745-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69745-138">INPUTS</span></span>

### <span data-ttu-id="69745-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="69745-139">None</span></span>
<span data-ttu-id="69745-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="69745-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69745-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69745-141">OUTPUTS</span></span>

### <span data-ttu-id="69745-142">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="69745-142">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="69745-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69745-143">NOTES</span></span>

## <span data-ttu-id="69745-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69745-144">RELATED LINKS</span></span>

[<span data-ttu-id="69745-145">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="69745-145">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="69745-146">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="69745-146">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


