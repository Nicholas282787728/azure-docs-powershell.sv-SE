---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581792"
---
# <span data-ttu-id="3f694-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f694-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="3f694-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f694-102">SYNOPSIS</span></span>
<span data-ttu-id="3f694-103">Importerar ett MOF-dokument som DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="3f694-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f694-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f694-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f694-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f694-105">DESCRIPTION</span></span>
<span data-ttu-id="3f694-106">Cmdleten **import-AzureRmAutomationDscConfiguration** importerar ett MOF-konfigurationsobjekt (Managed Object Format) till Azure Automation som en önskad konfiguration för State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="3f694-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="3f694-107">Ange sökvägen till en. MOF-fil.</span><span class="sxs-lookup"><span data-stu-id="3f694-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="3f694-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f694-108">EXAMPLES</span></span>

### <span data-ttu-id="3f694-109">Exempel 1: importera DSC-nodkonfigurationer till Automation</span><span class="sxs-lookup"><span data-stu-id="3f694-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="3f694-110">Det här kommandot importerar en DSC-noduppsättning från filen med namnet webserver webserver. MOF till det Automation-konto som heter Contoso17, under DSC-konfiguration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3f694-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="3f694-111">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="3f694-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3f694-112">Om det finns en befintlig DSC-nodadress med namnet ContosoConfiguration. webserver ersätter det här kommandot det.</span><span class="sxs-lookup"><span data-stu-id="3f694-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="3f694-113">Exempel 2: importera DSC-nodkonfigurationer till Automation och skapa en ny version och inte befintliga NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3f694-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="3f694-114">Det här kommandot importerar en DSC-noduppsättning från filen med namnet webserver webserver. MOF till det Automation-konto som heter Contoso17, under DSC-konfiguration ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3f694-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="3f694-115">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="3f694-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3f694-116">Om det finns en befintlig DSC-nodadress med namnet ContosoConfiguration. webserver, lägger det här kommandot till en ny version med namnet ContosoConfiguration [2]. webserver.</span><span class="sxs-lookup"><span data-stu-id="3f694-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="3f694-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f694-117">PARAMETERS</span></span>

### <span data-ttu-id="3f694-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3f694-118">-AutomationAccountName</span></span>
<span data-ttu-id="3f694-119">Anger namnet på det Automation-konto där denna cmdlet importerar en DSC-noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="3f694-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="3f694-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3f694-120">-ConfigurationName</span></span>
<span data-ttu-id="3f694-121">Anger namnet på en DSC-konfiguration som ska användas som namn område och container för den nod som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="3f694-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="3f694-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f694-122">-DefaultProfile</span></span>
<span data-ttu-id="3f694-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3f694-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f694-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3f694-124">-Force</span></span>
<span data-ttu-id="3f694-125">Anger att denna cmdlet ersätter en befintlig DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="3f694-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="3f694-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="3f694-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="3f694-127">Skapar en ny version för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="3f694-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="3f694-128">-Path</span><span class="sxs-lookup"><span data-stu-id="3f694-128">-Path</span></span>
<span data-ttu-id="3f694-129">Anger sökvägen till MOF-konfigurationsfilen som denna cmdlet importerar.</span><span class="sxs-lookup"><span data-stu-id="3f694-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="3f694-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f694-130">-ResourceGroupName</span></span>
<span data-ttu-id="3f694-131">Anger namnet på en resurs grupp för vilken denna cmdlet importerar en DSC-noduppsättning.</span><span class="sxs-lookup"><span data-stu-id="3f694-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="3f694-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f694-132">-Confirm</span></span>
<span data-ttu-id="3f694-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f694-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f694-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f694-134">-WhatIf</span></span>
<span data-ttu-id="3f694-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f694-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f694-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f694-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f694-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f694-137">CommonParameters</span></span>
<span data-ttu-id="3f694-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f694-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f694-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f694-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f694-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f694-140">INPUTS</span></span>

### <span data-ttu-id="3f694-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3f694-141">System.String</span></span>

## <span data-ttu-id="3f694-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f694-142">OUTPUTS</span></span>

### <span data-ttu-id="3f694-143">Microsoft. Azure. commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f694-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="3f694-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f694-144">NOTES</span></span>

## <span data-ttu-id="3f694-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f694-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f694-146">Exportera-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f694-146">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="3f694-147">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3f694-147">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


