---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271081"
---
# <span data-ttu-id="408ce-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="408ce-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="408ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="408ce-102">SYNOPSIS</span></span>
<span data-ttu-id="408ce-103">Importerar ett MOF-dokument som DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="408ce-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="408ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="408ce-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="408ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="408ce-105">DESCRIPTION</span></span>
<span data-ttu-id="408ce-106">Cmdleten **import-AzAutomationDscConfiguration** importerar ett MOF-konfigurationsobjekt (Managed Object Format) till Azure Automation som en önskad konfiguration för State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="408ce-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="408ce-107">Ange sökvägen till en. MOF-fil.</span><span class="sxs-lookup"><span data-stu-id="408ce-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="408ce-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="408ce-108">EXAMPLES</span></span>

### <span data-ttu-id="408ce-109">Exempel 1: importera DSC-nodkonfigurationer till Automation</span><span class="sxs-lookup"><span data-stu-id="408ce-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="408ce-110">Det här kommandot importerar en DSC-noduppsättning från filen med namnet webserver webserver. MOF till det Automation-konto som heter Contoso17, under DSC-konfiguration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="408ce-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="408ce-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="408ce-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="408ce-112">Om det finns en befintlig DSC-nodadress med namnet ContosoConfiguration. webserver ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="408ce-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="408ce-113">Exempel 2: importera DSC-nodkonfigurationer till Automation och skapa en ny version och inte befintliga NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="408ce-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="408ce-114">Det här kommandot importerar en DSC-noduppsättning från filen med namnet webserver webserver. MOF till det Automation-konto som heter Contoso17, under DSC-konfiguration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="408ce-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="408ce-115">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="408ce-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="408ce-116">Om det finns en befintlig DSC-nodadress med namnet ContosoConfiguration. webserver, lägger det här kommandot till en ny version med namnet ContosoConfiguration [2]. webserver.</span><span class="sxs-lookup"><span data-stu-id="408ce-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="408ce-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="408ce-117">PARAMETERS</span></span>

### <span data-ttu-id="408ce-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="408ce-118">-AutomationAccountName</span></span>
<span data-ttu-id="408ce-119">Anger namnet på det Automation-konto där denna cmdlet importerar en DSC-noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="408ce-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="408ce-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="408ce-120">-ConfigurationName</span></span>
<span data-ttu-id="408ce-121">Anger namnet på en DSC-konfiguration som ska användas som namn område och container för den nod som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="408ce-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408ce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408ce-122">-DefaultProfile</span></span>
<span data-ttu-id="408ce-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="408ce-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="408ce-124">-Force</span><span class="sxs-lookup"><span data-stu-id="408ce-124">-Force</span></span>
<span data-ttu-id="408ce-125">Anger att denna cmdlet ersätter en befintlig DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="408ce-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="408ce-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="408ce-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="408ce-127">Skapar en ny version för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="408ce-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408ce-128">-Path</span><span class="sxs-lookup"><span data-stu-id="408ce-128">-Path</span></span>
<span data-ttu-id="408ce-129">Anger sökvägen till MOF-konfigurationsfilen som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="408ce-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="408ce-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408ce-130">-ResourceGroupName</span></span>
<span data-ttu-id="408ce-131">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en DSC-noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="408ce-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="408ce-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="408ce-132">-Confirm</span></span>
<span data-ttu-id="408ce-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="408ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="408ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="408ce-134">-WhatIf</span></span>
<span data-ttu-id="408ce-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="408ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="408ce-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="408ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="408ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408ce-137">CommonParameters</span></span>
<span data-ttu-id="408ce-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408ce-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408ce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408ce-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="408ce-140">INPUTS</span></span>

### <span data-ttu-id="408ce-141">System. String</span><span class="sxs-lookup"><span data-stu-id="408ce-141">System.String</span></span>

## <span data-ttu-id="408ce-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="408ce-142">OUTPUTS</span></span>

### <span data-ttu-id="408ce-143">Microsoft. Azure. commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="408ce-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="408ce-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="408ce-144">NOTES</span></span>

## <span data-ttu-id="408ce-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="408ce-145">RELATED LINKS</span></span>

[<span data-ttu-id="408ce-146">Exportera-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="408ce-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="408ce-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="408ce-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


