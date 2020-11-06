---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578551"
---
# <span data-ttu-id="3afa4-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3afa4-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="3afa4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3afa4-102">SYNOPSIS</span></span>
<span data-ttu-id="3afa4-103">Importerar en DSC-konfiguration till Automation.</span><span class="sxs-lookup"><span data-stu-id="3afa4-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3afa4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3afa4-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3afa4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3afa4-105">DESCRIPTION</span></span>
<span data-ttu-id="3afa4-106">Cmdleten **import-AzureRmAutomationDscConfiguration** importerar en DSC-konfiguration (önskad tillstånds konfiguration) till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3afa4-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="3afa4-107">Ange sökvägen till ett APS-skript som innehåller en enkel DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3afa4-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="3afa4-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3afa4-108">EXAMPLES</span></span>

### <span data-ttu-id="3afa4-109">Exempel 1: importera en DSC-konfiguration till Automation</span><span class="sxs-lookup"><span data-stu-id="3afa4-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="3afa4-110">Det här kommandot importerar DSC-konfigurationen i filen som heter client.ps1 till Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3afa4-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="3afa4-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="3afa4-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="3afa4-112">Om det finns en befintlig DSC-konfiguration ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="3afa4-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="3afa4-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3afa4-113">PARAMETERS</span></span>

### <span data-ttu-id="3afa4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3afa4-114">-AutomationAccountName</span></span>
<span data-ttu-id="3afa4-115">Anger namnet på det Automation-konto där denna cmdlet importerar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3afa4-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="3afa4-116">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="3afa4-116">-Description</span></span>
<span data-ttu-id="3afa4-117">Anger en beskrivning av den konfiguration som importeras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3afa4-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3afa4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3afa4-118">-Force</span></span>
<span data-ttu-id="3afa4-119">Anger att denna cmdlet ersätter en befintlig DSC-konfiguration i Automation.</span><span class="sxs-lookup"><span data-stu-id="3afa4-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="3afa4-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="3afa4-120">-LogVerbose</span></span>
<span data-ttu-id="3afa4-121">Anger om denna cmdlet aktiverar eller inaktiverar utförlig loggning för kompilering av denna DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3afa4-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="3afa4-122">Ange ett värde för $True för att aktivera utförlig loggning eller $False för att stänga av det.</span><span class="sxs-lookup"><span data-stu-id="3afa4-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="3afa4-123">-Publicerad</span><span class="sxs-lookup"><span data-stu-id="3afa4-123">-Published</span></span>
<span data-ttu-id="3afa4-124">Anger att denna cmdlet importerar DSC-konfigurationen i publicerings tillståndet.</span><span class="sxs-lookup"><span data-stu-id="3afa4-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="3afa4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3afa4-125">-ResourceGroupName</span></span>
<span data-ttu-id="3afa4-126">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3afa4-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="3afa4-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="3afa4-127">-SourcePath</span></span>
<span data-ttu-id="3afa4-128">Anger sökvägen för det wps_2-skript som innehåller DSC-konfigurationen som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="3afa4-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3afa4-129">-Taggar</span><span class="sxs-lookup"><span data-stu-id="3afa4-129">-Tags</span></span>
<span data-ttu-id="3afa4-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="3afa4-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3afa4-131">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="3afa4-131">For example:</span></span>

<span data-ttu-id="3afa4-132">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="3afa4-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3afa4-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3afa4-133">-Confirm</span></span>
<span data-ttu-id="3afa4-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3afa4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3afa4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3afa4-135">-WhatIf</span></span>
<span data-ttu-id="3afa4-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3afa4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3afa4-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3afa4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3afa4-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3afa4-138">-DefaultProfile</span></span>
<span data-ttu-id="3afa4-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3afa4-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3afa4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3afa4-140">CommonParameters</span></span>
<span data-ttu-id="3afa4-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3afa4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3afa4-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3afa4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3afa4-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3afa4-143">INPUTS</span></span>

## <span data-ttu-id="3afa4-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3afa4-144">OUTPUTS</span></span>

### <span data-ttu-id="3afa4-145">Microsoft. Azure. commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3afa4-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="3afa4-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3afa4-146">NOTES</span></span>

## <span data-ttu-id="3afa4-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3afa4-147">RELATED LINKS</span></span>

[<span data-ttu-id="3afa4-148">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3afa4-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="3afa4-149">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3afa4-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
