---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e8d7cfcf595d7dd445d66865d922676c96b7e6d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573565"
---
# <span data-ttu-id="508a2-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="508a2-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="508a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="508a2-102">SYNOPSIS</span></span>
<span data-ttu-id="508a2-103">Importerar en DSC-konfiguration till Automation.</span><span class="sxs-lookup"><span data-stu-id="508a2-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="508a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="508a2-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="508a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="508a2-105">DESCRIPTION</span></span>
<span data-ttu-id="508a2-106">Cmdleten **import-AzureRmAutomationDscConfiguration** importerar en DSC-konfiguration (önskad tillstånds konfiguration) till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="508a2-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="508a2-107">Ange sökvägen till ett APS-skript som innehåller en enkel DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="508a2-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="508a2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="508a2-108">EXAMPLES</span></span>

### <span data-ttu-id="508a2-109">Exempel 1: importera en DSC-konfiguration till Automation</span><span class="sxs-lookup"><span data-stu-id="508a2-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="508a2-110">Det här kommandot importerar DSC-konfigurationen i filen som heter client.ps1 till Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="508a2-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="508a2-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="508a2-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="508a2-112">Om det finns en befintlig DSC-konfiguration ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="508a2-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="508a2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="508a2-113">PARAMETERS</span></span>

### <span data-ttu-id="508a2-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="508a2-114">-AutomationAccountName</span></span>
<span data-ttu-id="508a2-115">Anger namnet på det Automation-konto där denna cmdlet importerar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="508a2-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="508a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="508a2-116">-DefaultProfile</span></span>
<span data-ttu-id="508a2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="508a2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="508a2-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="508a2-118">-Description</span></span>
<span data-ttu-id="508a2-119">Anger en beskrivning av den konfiguration som importeras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="508a2-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="508a2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="508a2-120">-Force</span></span>
<span data-ttu-id="508a2-121">Anger att denna cmdlet ersätter en befintlig DSC-konfiguration i Automation.</span><span class="sxs-lookup"><span data-stu-id="508a2-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="508a2-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="508a2-122">-LogVerbose</span></span>
<span data-ttu-id="508a2-123">Anger om denna cmdlet aktiverar eller inaktiverar utförlig loggning för kompilering av denna DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="508a2-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="508a2-124">Ange ett värde för $True för att aktivera utförlig loggning eller $False för att stänga av det.</span><span class="sxs-lookup"><span data-stu-id="508a2-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="508a2-125">-Publicerad</span><span class="sxs-lookup"><span data-stu-id="508a2-125">-Published</span></span>
<span data-ttu-id="508a2-126">Anger att denna cmdlet importerar DSC-konfigurationen i publicerings tillståndet.</span><span class="sxs-lookup"><span data-stu-id="508a2-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="508a2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="508a2-127">-ResourceGroupName</span></span>
<span data-ttu-id="508a2-128">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="508a2-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="508a2-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="508a2-129">-SourcePath</span></span>
<span data-ttu-id="508a2-130">Anger sökvägen för det wps_2-skript som innehåller DSC-konfigurationen som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="508a2-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="508a2-131">-Taggar</span><span class="sxs-lookup"><span data-stu-id="508a2-131">-Tags</span></span>
<span data-ttu-id="508a2-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="508a2-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="508a2-133">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="508a2-133">For example:</span></span>

<span data-ttu-id="508a2-134">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="508a2-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="508a2-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="508a2-135">-Confirm</span></span>
<span data-ttu-id="508a2-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="508a2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="508a2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="508a2-137">-WhatIf</span></span>
<span data-ttu-id="508a2-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="508a2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="508a2-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="508a2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="508a2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="508a2-140">CommonParameters</span></span>
<span data-ttu-id="508a2-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="508a2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="508a2-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="508a2-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="508a2-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="508a2-143">INPUTS</span></span>

### <span data-ttu-id="508a2-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="508a2-144">None</span></span>
<span data-ttu-id="508a2-145">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="508a2-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="508a2-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="508a2-146">OUTPUTS</span></span>

### <span data-ttu-id="508a2-147">Microsoft. Azure. commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="508a2-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="508a2-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="508a2-148">NOTES</span></span>

## <span data-ttu-id="508a2-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="508a2-149">RELATED LINKS</span></span>

[<span data-ttu-id="508a2-150">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="508a2-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="508a2-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="508a2-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
