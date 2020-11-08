---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092675"
---
# <span data-ttu-id="93d7d-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="93d7d-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="93d7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="93d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="93d7d-103">Registrerar en virtuell Azure-dator som kör Windows OS som en DSC-nod för ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="93d7d-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="93d7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="93d7d-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93d7d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="93d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="93d7d-106">**Register-AzAutomationDscNode** cmdlet registrerar en virtuell Azure-dator som en DSC-nod (önskad tillstånds konfiguration) i ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="93d7d-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="93d7d-107">Denna cmdlet registrerar bara virtuella datorer som kör Windows OS som en automatiserings-DSC-nod för ett konto.</span><span class="sxs-lookup"><span data-stu-id="93d7d-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="93d7d-108">Om du behöver registrera en nod på ett Automation-konto i ett annat abonnemang måste du använda en ARM-mall i stället för cmdletar.</span><span class="sxs-lookup"><span data-stu-id="93d7d-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="93d7d-109">Se [dokumentationen](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) för Azure Automation för mer information.</span><span class="sxs-lookup"><span data-stu-id="93d7d-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="93d7d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="93d7d-110">EXAMPLES</span></span>

### <span data-ttu-id="93d7d-111">Exempel 1: registrera en virtuell Azure-dator som en Azure DSC-nod</span><span class="sxs-lookup"><span data-stu-id="93d7d-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="93d7d-112">Det här kommandot registrerar den virtuella Azure-datorn med namnet VirtualMachine01 som en DSC-nod i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="93d7d-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="93d7d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="93d7d-113">PARAMETERS</span></span>

### <span data-ttu-id="93d7d-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="93d7d-114">-ActionAfterReboot</span></span>
<span data-ttu-id="93d7d-115">Anger den åtgärd som den virtuella datorn tar när den startas om.</span><span class="sxs-lookup"><span data-stu-id="93d7d-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="93d7d-116">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="93d7d-116">Valid values are:</span></span> 
- <span data-ttu-id="93d7d-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="93d7d-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="93d7d-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="93d7d-118">StopConfiguration</span></span>

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

### <span data-ttu-id="93d7d-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="93d7d-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="93d7d-120">Anger om nya konfigurationer som den här DSC-noden hämtas från Azure Automation DSC pull server ersätter befintliga moduler som redan finns på målnoden.</span><span class="sxs-lookup"><span data-stu-id="93d7d-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="93d7d-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93d7d-121">-AutomationAccountName</span></span>
<span data-ttu-id="93d7d-122">Anger namnet på ett Automation-konto där denna cmdlet registrerar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="93d7d-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="93d7d-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="93d7d-123">-AzureVMLocation</span></span>
<span data-ttu-id="93d7d-124">Den virtuella Azure VM-platsen.</span><span class="sxs-lookup"><span data-stu-id="93d7d-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="93d7d-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="93d7d-125">-AzureVMName</span></span>
<span data-ttu-id="93d7d-126">Namnet på den virtuella Azure-datorn som ska registreras för hantering med Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="93d7d-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="93d7d-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93d7d-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="93d7d-128">Namnet på den virtuella Azure VM-resursen.</span><span class="sxs-lookup"><span data-stu-id="93d7d-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="93d7d-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="93d7d-129">-ConfigurationMode</span></span>
<span data-ttu-id="93d7d-130">Anger DSC-konfigurationsverktyget.</span><span class="sxs-lookup"><span data-stu-id="93d7d-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="93d7d-131">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="93d7d-131">Valid values are:</span></span> 
- <span data-ttu-id="93d7d-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="93d7d-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="93d7d-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="93d7d-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="93d7d-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="93d7d-134">ApplyOnly</span></span>

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

### <span data-ttu-id="93d7d-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="93d7d-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="93d7d-136">Anger frekvensen, i minuter, där bakgrunds programmet för DSC försöker implementera den aktuella konfigurationen på målnoden.</span><span class="sxs-lookup"><span data-stu-id="93d7d-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="93d7d-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d7d-137">-DefaultProfile</span></span>
<span data-ttu-id="93d7d-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="93d7d-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93d7d-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="93d7d-139">-NodeConfigurationName</span></span>
<span data-ttu-id="93d7d-140">Anger namnet på den noduppsättning som den här cmdleten konfigurerar den virtuella datorn för att ta emot från Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="93d7d-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="93d7d-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="93d7d-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="93d7d-142">Anger om den virtuella datorn ska startas om, om det behövs.</span><span class="sxs-lookup"><span data-stu-id="93d7d-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="93d7d-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="93d7d-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="93d7d-144">Anger hur ofta, i minuter, den lokala Configuration Manager ska kunna hämta den senaste noden.</span><span class="sxs-lookup"><span data-stu-id="93d7d-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="93d7d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93d7d-145">-ResourceGroupName</span></span>
<span data-ttu-id="93d7d-146">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="93d7d-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="93d7d-147">Det Automation-konto som den här cmdleten registrerar en virtuell dator tillhör som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="93d7d-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="93d7d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d7d-148">CommonParameters</span></span>
<span data-ttu-id="93d7d-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d7d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d7d-150">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93d7d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d7d-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="93d7d-151">INPUTS</span></span>

### <span data-ttu-id="93d7d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="93d7d-152">System.String</span></span>

### <span data-ttu-id="93d7d-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="93d7d-153">System.Int32</span></span>

### <span data-ttu-id="93d7d-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93d7d-154">System.Boolean</span></span>

## <span data-ttu-id="93d7d-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="93d7d-155">OUTPUTS</span></span>

### <span data-ttu-id="93d7d-156">System. Void</span><span class="sxs-lookup"><span data-stu-id="93d7d-156">System.Void</span></span>

## <span data-ttu-id="93d7d-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="93d7d-157">NOTES</span></span>

## <span data-ttu-id="93d7d-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="93d7d-158">RELATED LINKS</span></span>

[<span data-ttu-id="93d7d-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="93d7d-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="93d7d-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="93d7d-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="93d7d-161">Avregistrera-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="93d7d-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


