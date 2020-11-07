---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754778"
---
# <span data-ttu-id="168aa-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="168aa-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="168aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="168aa-102">SYNOPSIS</span></span>
<span data-ttu-id="168aa-103">Registrerar en virtuell Azure-dator som en DSC-nod för ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="168aa-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="168aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="168aa-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="168aa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="168aa-105">DESCRIPTION</span></span>
<span data-ttu-id="168aa-106">**Register-AzAutomationDscNode** cmdlet registrerar en virtuell Azure-dator som en DSC-nod (önskad tillstånds konfiguration) i ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="168aa-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="168aa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="168aa-107">EXAMPLES</span></span>

### <span data-ttu-id="168aa-108">Exempel 1: registrera en virtuell Azure-dator som en Azure DSC-nod</span><span class="sxs-lookup"><span data-stu-id="168aa-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="168aa-109">Det här kommandot registrerar den virtuella Azure-datorn med namnet VirtualMachine01 som en DSC-nod i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="168aa-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="168aa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="168aa-110">PARAMETERS</span></span>

### <span data-ttu-id="168aa-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="168aa-111">-ActionAfterReboot</span></span>
<span data-ttu-id="168aa-112">Anger den åtgärd som den virtuella datorn tar när den startas om.</span><span class="sxs-lookup"><span data-stu-id="168aa-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="168aa-113">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="168aa-113">Valid values are:</span></span> 
- <span data-ttu-id="168aa-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="168aa-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="168aa-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="168aa-115">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168aa-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="168aa-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="168aa-117">Anger om nya konfigurationer som den här DSC-noden hämtas från Azure Automation DSC pull server ersätter befintliga moduler som redan finns på målnoden.</span><span class="sxs-lookup"><span data-stu-id="168aa-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168aa-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="168aa-118">-AutomationAccountName</span></span>
<span data-ttu-id="168aa-119">Anger namnet på ett Automation-konto där denna cmdlet registrerar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="168aa-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="168aa-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="168aa-120">-AzureVMLocation</span></span>
<span data-ttu-id="168aa-121">Den virtuella Azure VM-platsen.</span><span class="sxs-lookup"><span data-stu-id="168aa-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="168aa-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="168aa-122">-AzureVMName</span></span>
<span data-ttu-id="168aa-123">Namnet på den virtuella Azure-datorn som ska registreras för hantering med Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="168aa-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="168aa-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="168aa-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="168aa-125">Namnet på den virtuella Azure VM-resursen.</span><span class="sxs-lookup"><span data-stu-id="168aa-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="168aa-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="168aa-126">-ConfigurationMode</span></span>
<span data-ttu-id="168aa-127">Anger DSC-konfigurationsverktyget.</span><span class="sxs-lookup"><span data-stu-id="168aa-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="168aa-128">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="168aa-128">Valid values are:</span></span> 
- <span data-ttu-id="168aa-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="168aa-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="168aa-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="168aa-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="168aa-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="168aa-131">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168aa-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="168aa-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="168aa-133">Anger frekvensen, i minuter, där bakgrunds programmet för DSC försöker implementera den aktuella konfigurationen på målnoden.</span><span class="sxs-lookup"><span data-stu-id="168aa-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168aa-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="168aa-134">-DefaultProfile</span></span>
<span data-ttu-id="168aa-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="168aa-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="168aa-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="168aa-136">-NodeConfigurationName</span></span>
<span data-ttu-id="168aa-137">Anger namnet på den noduppsättning som den här cmdleten konfigurerar den virtuella datorn för att ta emot från Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="168aa-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="168aa-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="168aa-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="168aa-139">Anger om den virtuella datorn ska startas om, om det behövs.</span><span class="sxs-lookup"><span data-stu-id="168aa-139">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168aa-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="168aa-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="168aa-141">Anger hur ofta, i minuter, den lokala Configuration Manager ska kunna hämta den senaste noden.</span><span class="sxs-lookup"><span data-stu-id="168aa-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="168aa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="168aa-142">-ResourceGroupName</span></span>
<span data-ttu-id="168aa-143">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="168aa-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="168aa-144">Det Automation-konto som den här cmdleten registrerar en virtuell dator tillhör som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="168aa-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="168aa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="168aa-145">CommonParameters</span></span>
<span data-ttu-id="168aa-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="168aa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="168aa-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="168aa-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="168aa-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="168aa-148">INPUTS</span></span>

### <span data-ttu-id="168aa-149">System. String</span><span class="sxs-lookup"><span data-stu-id="168aa-149">System.String</span></span>

### <span data-ttu-id="168aa-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="168aa-150">System.Int32</span></span>

### <span data-ttu-id="168aa-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="168aa-151">System.Boolean</span></span>

## <span data-ttu-id="168aa-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="168aa-152">OUTPUTS</span></span>

### <span data-ttu-id="168aa-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="168aa-153">System.Void</span></span>

## <span data-ttu-id="168aa-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="168aa-154">NOTES</span></span>

## <span data-ttu-id="168aa-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="168aa-155">RELATED LINKS</span></span>

[<span data-ttu-id="168aa-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="168aa-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="168aa-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="168aa-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="168aa-158">Avregistrera-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="168aa-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


