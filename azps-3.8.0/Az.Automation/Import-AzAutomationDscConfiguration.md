---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: 21b3e8c29d9d74f548ca9d212a72d4b70520aa82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092709"
---
# <span data-ttu-id="f0ef8-101">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0ef8-101">Import-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="f0ef8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ef8-103">Importerar en DSC-konfiguration till Automation.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-103">Imports a DSC configuration into Automation.</span></span>

## <span data-ttu-id="f0ef8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0ef8-104">SYNTAX</span></span>

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ef8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0ef8-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ef8-106">Cmdleten **import-AzAutomationDscConfiguration** importerar en DSC-konfiguration (önskad tillstånds konfiguration) till Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-106">The **Import-AzAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="f0ef8-107">Ange sökvägen till ett APS-skript som innehåller en enkel DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="f0ef8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0ef8-108">EXAMPLES</span></span>

### <span data-ttu-id="f0ef8-109">Exempel 1: importera en DSC-konfiguration till Automation</span><span class="sxs-lookup"><span data-stu-id="f0ef8-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="f0ef8-110">Det här kommandot importerar DSC-konfigurationen i filen som heter client.ps1 till Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="f0ef8-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="f0ef8-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="f0ef8-112">Om det finns en befintlig DSC-konfiguration ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="f0ef8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0ef8-113">PARAMETERS</span></span>

### <span data-ttu-id="f0ef8-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0ef8-114">-AutomationAccountName</span></span>
<span data-ttu-id="f0ef8-115">Anger namnet på det Automation-konto där denna cmdlet importerar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="f0ef8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ef8-116">-DefaultProfile</span></span>
<span data-ttu-id="f0ef8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f0ef8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0ef8-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="f0ef8-118">-Description</span></span>
<span data-ttu-id="f0ef8-119">Anger en beskrivning av den konfiguration som importeras med den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="f0ef8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f0ef8-120">-Force</span></span>
<span data-ttu-id="f0ef8-121">Anger att denna cmdlet ersätter en befintlig DSC-konfiguration i Automation.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="f0ef8-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f0ef8-122">-LogVerbose</span></span>
<span data-ttu-id="f0ef8-123">Anger om denna cmdlet aktiverar eller inaktiverar utförlig loggning för kompilering av denna DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="f0ef8-124">Ange ett värde för $True för att aktivera utförlig loggning eller $False för att stänga av det.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

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

### <span data-ttu-id="f0ef8-125">-Publicerad</span><span class="sxs-lookup"><span data-stu-id="f0ef8-125">-Published</span></span>
<span data-ttu-id="f0ef8-126">Anger att denna cmdlet importerar DSC-konfigurationen i publicerings tillståndet.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="f0ef8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ef8-127">-ResourceGroupName</span></span>
<span data-ttu-id="f0ef8-128">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en DSC-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="f0ef8-129">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="f0ef8-129">-SourcePath</span></span>
<span data-ttu-id="f0ef8-130">Anger sökvägen för det wps_2-skript som innehåller DSC-konfigurationen som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="f0ef8-131">-Taggar</span><span class="sxs-lookup"><span data-stu-id="f0ef8-131">-Tags</span></span>
<span data-ttu-id="f0ef8-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f0ef8-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f0ef8-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f0ef8-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0ef8-134">-Confirm</span></span>
<span data-ttu-id="f0ef8-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ef8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ef8-136">-WhatIf</span></span>
<span data-ttu-id="f0ef8-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ef8-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ef8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ef8-139">CommonParameters</span></span>
<span data-ttu-id="f0ef8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ef8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ef8-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0ef8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ef8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0ef8-142">INPUTS</span></span>

### <span data-ttu-id="f0ef8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f0ef8-143">System.String</span></span>

### <span data-ttu-id="f0ef8-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="f0ef8-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="f0ef8-145">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0ef8-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f0ef8-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0ef8-146">OUTPUTS</span></span>

### <span data-ttu-id="f0ef8-147">Microsoft. Azure. commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0ef8-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="f0ef8-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0ef8-148">NOTES</span></span>

## <span data-ttu-id="f0ef8-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0ef8-149">RELATED LINKS</span></span>

[<span data-ttu-id="f0ef8-150">Exportera-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0ef8-150">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="f0ef8-151">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0ef8-151">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)
