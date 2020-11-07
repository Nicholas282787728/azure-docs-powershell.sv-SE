---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 1a0fd95df118e734ed594cf1efe35eb8f8476f50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579827"
---
# <span data-ttu-id="721d5-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="721d5-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="721d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="721d5-102">SYNOPSIS</span></span>
<span data-ttu-id="721d5-103">Registrerar en virtuell Azure-dator som en DSC-nod för ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="721d5-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="721d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="721d5-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="721d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="721d5-105">DESCRIPTION</span></span>
<span data-ttu-id="721d5-106">**Register-AzureRmAutomationDscNode** cmdlet registrerar en virtuell Azure-dator som en DSC-nod (önskad tillstånds konfiguration) i ett Azure Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="721d5-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="721d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="721d5-107">EXAMPLES</span></span>

### <span data-ttu-id="721d5-108">Exempel 1: registrera en virtuell Azure-dator som en Azure DSC-nod</span><span class="sxs-lookup"><span data-stu-id="721d5-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="721d5-109">Det här kommandot registrerar den virtuella Azure-datorn med namnet VirtualMachine01 som en DSC-nod i Automation-kontot med namnet Contoso17.</span><span class="sxs-lookup"><span data-stu-id="721d5-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="721d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="721d5-110">PARAMETERS</span></span>

### <span data-ttu-id="721d5-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="721d5-111">-ActionAfterReboot</span></span>
<span data-ttu-id="721d5-112">Anger den åtgärd som den virtuella datorn tar när den startas om.</span><span class="sxs-lookup"><span data-stu-id="721d5-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="721d5-113">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="721d5-113">Valid values are:</span></span> 

- <span data-ttu-id="721d5-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="721d5-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="721d5-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="721d5-115">StopConfiguration</span></span>

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

### <span data-ttu-id="721d5-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="721d5-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="721d5-117">Anger om nya konfigurationer som den här DSC-noden hämtas från Azure Automation DSC pull server ersätter befintliga moduler som redan finns på målnoden.</span><span class="sxs-lookup"><span data-stu-id="721d5-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="721d5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="721d5-118">-AutomationAccountName</span></span>
<span data-ttu-id="721d5-119">Anger namnet på ett Automation-konto där denna cmdlet registrerar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="721d5-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="721d5-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="721d5-120">-AzureVMLocation</span></span>
<span data-ttu-id="721d5-121">Anger den plats där denna cmdlet registrerar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="721d5-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="721d5-122">Använd Get-AzureRMLocation cmdlet för att få giltiga platser.</span><span class="sxs-lookup"><span data-stu-id="721d5-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="721d5-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="721d5-123">-AzureVMName</span></span>
<span data-ttu-id="721d5-124">Anger namnet på den virtuella Azure-datorn som denna cmdlet registrerar för Management.</span><span class="sxs-lookup"><span data-stu-id="721d5-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="721d5-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="721d5-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="721d5-126">Anger namnet på resurs gruppen för den virtuella Azure-datorn som denna cmdlet registrerar.</span><span class="sxs-lookup"><span data-stu-id="721d5-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="721d5-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="721d5-127">-ConfigurationMode</span></span>
<span data-ttu-id="721d5-128">Anger DSC-konfigurationsverktyget.</span><span class="sxs-lookup"><span data-stu-id="721d5-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="721d5-129">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="721d5-129">Valid values are:</span></span> 

- <span data-ttu-id="721d5-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="721d5-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="721d5-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="721d5-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="721d5-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="721d5-132">ApplyOnly</span></span>

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

### <span data-ttu-id="721d5-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="721d5-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="721d5-134">Anger frekvensen, i minuter, där bakgrunds programmet för DSC försöker implementera den aktuella konfigurationen på målnoden.</span><span class="sxs-lookup"><span data-stu-id="721d5-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="721d5-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="721d5-135">-NodeConfigurationName</span></span>
<span data-ttu-id="721d5-136">Anger namnet på den noduppsättning som den här cmdleten konfigurerar den virtuella datorn för att ta emot från Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="721d5-136">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="721d5-137">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="721d5-137">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="721d5-138">Anger om den virtuella datorn ska startas om, om det behövs.</span><span class="sxs-lookup"><span data-stu-id="721d5-138">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="721d5-139">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="721d5-139">-RefreshFrequencyMins</span></span>
<span data-ttu-id="721d5-140">Anger hur ofta, i minuter, den lokala Configuration Manager ska kunna hämta den senaste noden.</span><span class="sxs-lookup"><span data-stu-id="721d5-140">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="721d5-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="721d5-141">-ResourceGroupName</span></span>
<span data-ttu-id="721d5-142">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="721d5-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="721d5-143">Det Automation-konto som den här cmdleten registrerar en virtuell dator tillhör som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="721d5-143">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="721d5-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="721d5-144">-DefaultProfile</span></span>
<span data-ttu-id="721d5-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="721d5-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="721d5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="721d5-146">CommonParameters</span></span>
<span data-ttu-id="721d5-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="721d5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="721d5-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="721d5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="721d5-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="721d5-149">INPUTS</span></span>

## <span data-ttu-id="721d5-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="721d5-150">OUTPUTS</span></span>

## <span data-ttu-id="721d5-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="721d5-151">NOTES</span></span>

## <span data-ttu-id="721d5-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="721d5-152">RELATED LINKS</span></span>

[<span data-ttu-id="721d5-153">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="721d5-153">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="721d5-154">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="721d5-154">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="721d5-155">Avregistrera-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="721d5-155">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)

