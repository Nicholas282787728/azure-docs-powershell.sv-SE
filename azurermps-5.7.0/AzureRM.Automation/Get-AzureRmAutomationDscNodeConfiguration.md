---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: b0fbea9b12fb8fbb76d0f5e8fd34efba4949acb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758346"
---
# <span data-ttu-id="e5995-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5995-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="e5995-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5995-102">SYNOPSIS</span></span>
<span data-ttu-id="e5995-103">Hämtar metadata för DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="e5995-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5995-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5995-104">SYNTAX</span></span>

### <span data-ttu-id="e5995-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="e5995-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5995-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e5995-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5995-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e5995-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5995-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5995-108">DESCRIPTION</span></span>
<span data-ttu-id="e5995-109">Cmdleten **Get-AzureRmAutomationDscNodeConfiguration** hämtar metadata för de önskade DSC-NODKONFIGURATIONER (APS Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e5995-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="e5995-110">Automation lagrar DSC-nodkonfigurationer som ett MOF-konfigurationsobjekt (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="e5995-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="e5995-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5995-111">EXAMPLES</span></span>

### <span data-ttu-id="e5995-112">Exempel 1: Hämta alla DSC-nodkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="e5995-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e5995-113">Det här kommandot får metadata för alla DSC-nodkonfigurationer i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e5995-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e5995-114">Exempel 2: Hämta alla DSC-nodkonfigurationer för en DSC-konfiguration</span><span class="sxs-lookup"><span data-stu-id="e5995-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="e5995-115">Det här kommandot får metadata för alla DSC-nodkonfigurationer i Automation-kontot som heter Contoso17 att DSC-konfigurationen med namnet ContosoConfiguration genererades.</span><span class="sxs-lookup"><span data-stu-id="e5995-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="e5995-116">Exempel 3: Hämta en DSC-noduppsättning med namn</span><span class="sxs-lookup"><span data-stu-id="e5995-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="e5995-117">Med det här kommandot får du metadata för en DSC-nodadress med namnet ContosoConfiguration. webserver i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e5995-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e5995-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5995-118">PARAMETERS</span></span>

### <span data-ttu-id="e5995-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5995-119">-AutomationAccountName</span></span>
<span data-ttu-id="e5995-120">Anger namnet på ett Automation-konto som innehåller DSC-nodkonfigurationer för vilka denna cmdlet får metadata.</span><span class="sxs-lookup"><span data-stu-id="e5995-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="e5995-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e5995-121">-ConfigurationName</span></span>
<span data-ttu-id="e5995-122">Anger namnet på den DSC-konfiguration för vilken denna cmdlet hämtar metadata för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e5995-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5995-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5995-123">-DefaultProfile</span></span>
<span data-ttu-id="e5995-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e5995-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5995-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5995-125">-Name</span></span>
<span data-ttu-id="e5995-126">Anger namnet på DSC-nodadressen för vilken denna cmdlet får metadata.</span><span class="sxs-lookup"><span data-stu-id="e5995-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5995-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5995-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5995-128">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e5995-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e5995-129">Denna cmdlet får metadata för DSC-nodkonfigurationer i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e5995-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e5995-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="e5995-130">-RollupStatus</span></span>
<span data-ttu-id="e5995-131">Anger upplyftnings statusen för DSC-nodkonfigurationer som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="e5995-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="e5995-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e5995-132">Valid values are:</span></span> 

- <span data-ttu-id="e5995-133">Dålig</span><span class="sxs-lookup"><span data-stu-id="e5995-133">Bad</span></span> 
- <span data-ttu-id="e5995-134">Bra</span><span class="sxs-lookup"><span data-stu-id="e5995-134">Good</span></span>

```yaml
Type: String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5995-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5995-135">CommonParameters</span></span>
<span data-ttu-id="e5995-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5995-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5995-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5995-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5995-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5995-138">INPUTS</span></span>

### <span data-ttu-id="e5995-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="e5995-139">None</span></span>
<span data-ttu-id="e5995-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e5995-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5995-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5995-141">OUTPUTS</span></span>

### <span data-ttu-id="e5995-142">Microsoft. Azure. commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="e5995-142">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="e5995-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5995-143">NOTES</span></span>

## <span data-ttu-id="e5995-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5995-144">RELATED LINKS</span></span>

[<span data-ttu-id="e5995-145">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5995-145">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


