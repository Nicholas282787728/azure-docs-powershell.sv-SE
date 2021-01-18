---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524988"
---
# <span data-ttu-id="3bbe4-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bbe4-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="3bbe4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3bbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbe4-103">Hämtar metadata för DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="3bbe4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3bbe4-104">SYNTAX</span></span>

### <span data-ttu-id="3bbe4-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="3bbe4-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bbe4-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3bbe4-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bbe4-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3bbe4-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bbe4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3bbe4-108">DESCRIPTION</span></span>
<span data-ttu-id="3bbe4-109">Cmdleten **Get-AzAutomationDscNodeConfiguration** hämtar metadata för de önskade DSC-NODKONFIGURATIONER (APS Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="3bbe4-110">Automation lagrar DSC-nodkonfigurationer som ett MOF-konfigurationsobjekt (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="3bbe4-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="3bbe4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3bbe4-111">EXAMPLES</span></span>

### <span data-ttu-id="3bbe4-112">Exempel 1: Hämta alla DSC-nodkonfigurationer</span><span class="sxs-lookup"><span data-stu-id="3bbe4-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3bbe4-113">Det här kommandot får metadata för alla DSC-nodkonfigurationer i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3bbe4-114">Exempel 2: Hämta alla DSC-nodkonfigurationer för en DSC-konfiguration</span><span class="sxs-lookup"><span data-stu-id="3bbe4-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="3bbe4-115">Det här kommandot får metadata för alla DSC-nodkonfigurationer i Automation-kontot som heter Contoso17 att DSC-konfigurationen med namnet ContosoConfiguration genererades.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="3bbe4-116">Exempel 3: Hämta en DSC-noduppsättning med namn</span><span class="sxs-lookup"><span data-stu-id="3bbe4-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="3bbe4-117">Med det här kommandot får du metadata för en DSC-nodadress med namnet ContosoConfiguration. webserver i Automation-kontot som heter Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3bbe4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3bbe4-118">PARAMETERS</span></span>

### <span data-ttu-id="3bbe4-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3bbe4-119">-AutomationAccountName</span></span>
<span data-ttu-id="3bbe4-120">Anger namnet på ett Automation-konto som innehåller DSC-nodkonfigurationer för vilka denna cmdlet får metadata.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="3bbe4-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3bbe4-121">-ConfigurationName</span></span>
<span data-ttu-id="3bbe4-122">Anger namnet på den DSC-konfiguration för vilken denna cmdlet hämtar metadata för nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbe4-123">-DefaultProfile</span></span>
<span data-ttu-id="3bbe4-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3bbe4-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bbe4-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="3bbe4-125">-Name</span></span>
<span data-ttu-id="3bbe4-126">Anger namnet på DSC-nodadressen för vilken denna cmdlet får metadata.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbe4-127">-ResourceGroupName</span></span>
<span data-ttu-id="3bbe4-128">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3bbe4-129">Denna cmdlet får metadata för DSC-nodkonfigurationer i resurs gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3bbe4-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="3bbe4-130">-RollupStatus</span></span>
<span data-ttu-id="3bbe4-131">Anger upplyftnings statusen för DSC-nodkonfigurationer som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="3bbe4-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="3bbe4-132">Valid values are:</span></span> 
- <span data-ttu-id="3bbe4-133">Dålig</span><span class="sxs-lookup"><span data-stu-id="3bbe4-133">Bad</span></span> 
- <span data-ttu-id="3bbe4-134">Bra</span><span class="sxs-lookup"><span data-stu-id="3bbe4-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bbe4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbe4-135">CommonParameters</span></span>
<span data-ttu-id="3bbe4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bbe4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbe4-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bbe4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbe4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3bbe4-138">INPUTS</span></span>

### <span data-ttu-id="3bbe4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3bbe4-139">System.String</span></span>

## <span data-ttu-id="3bbe4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3bbe4-140">OUTPUTS</span></span>

### <span data-ttu-id="3bbe4-141">Microsoft. Azure. commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="3bbe4-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="3bbe4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3bbe4-142">NOTES</span></span>

## <span data-ttu-id="3bbe4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3bbe4-143">RELATED LINKS</span></span>

[<span data-ttu-id="3bbe4-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bbe4-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


