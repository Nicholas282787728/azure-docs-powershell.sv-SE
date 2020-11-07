---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 588e6bd1789eafeab6109d6d53ffcfa6671bb410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754448"
---
# <span data-ttu-id="9082a-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="9082a-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="9082a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9082a-102">SYNOPSIS</span></span>
<span data-ttu-id="9082a-103">Anger profil egenskaperna för VMSS operativ system.</span><span class="sxs-lookup"><span data-stu-id="9082a-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="9082a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9082a-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9082a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9082a-105">DESCRIPTION</span></span>
<span data-ttu-id="9082a-106">Cmdleten **set-AzVmssOsProfile** anger den virtuella datorns skalnings profil egenskaper.</span><span class="sxs-lookup"><span data-stu-id="9082a-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="9082a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9082a-107">EXAMPLES</span></span>

### <span data-ttu-id="9082a-108">Exempel 1: Ange profil egenskaperna för en VMSS</span><span class="sxs-lookup"><span data-stu-id="9082a-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="9082a-109">Det här kommandot anger profil egenskaper för operativ systemet för de virtuella datorerna som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="9082a-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="9082a-110">Kommandot anger prefixet för alla virtuella datorer i VMSS för att testa och förse administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="9082a-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="9082a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9082a-111">PARAMETERS</span></span>

### <span data-ttu-id="9082a-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="9082a-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="9082a-113">Anger ett obevakat innehålls objekt.</span><span class="sxs-lookup"><span data-stu-id="9082a-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="9082a-114">Du kan använda Add-AzVMAdditionalUnattendContent för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="9082a-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="9082a-115">-AdminPassword</span></span>
<span data-ttu-id="9082a-116">Anger det administratörs lösen ord som ska användas för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="9082a-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9082a-117">-AdminUsername</span></span>
<span data-ttu-id="9082a-118">Anger det administratörs konto namn som ska användas för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="9082a-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="9082a-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="9082a-120">Anger det här prefixet för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="9082a-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="9082a-121">Dator namn måste vara mellan 1 och 15 tecken långa.</span><span class="sxs-lookup"><span data-stu-id="9082a-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="9082a-122">-CustomData</span></span>
<span data-ttu-id="9082a-123">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="9082a-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="9082a-124">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9082a-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="9082a-125">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="9082a-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9082a-126">-DefaultProfile</span></span>
<span data-ttu-id="9082a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9082a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9082a-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="9082a-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="9082a-129">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="9082a-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-130">-Lyssnare</span><span class="sxs-lookup"><span data-stu-id="9082a-130">-Listener</span></span>
<span data-ttu-id="9082a-131">Anger WinRM-lyssnarna (Windows Remote Management).</span><span class="sxs-lookup"><span data-stu-id="9082a-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="9082a-132">Detta möjliggör fjärran sluten Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9082a-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="9082a-133">Du kan använda Add-AzVmssWinRMListener cmdlet för att skapa lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="9082a-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="9082a-134">-PublicKey</span></span>
<span data-ttu-id="9082a-135">Anger det offentliga objektet för SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="9082a-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="9082a-136">Du kan använda Add-AzVMSshPublicKey-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="9082a-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="9082a-137">-Secret</span></span>
<span data-ttu-id="9082a-138">Anger det hemligheter-objekt som innehåller certifikat referenser som ska placeras på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9082a-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="9082a-139">Du kan använda Add-AzVmssSecret cmdlet för att skapa hemligheter-objekt.</span><span class="sxs-lookup"><span data-stu-id="9082a-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="9082a-140">-TimeZone</span></span>
<span data-ttu-id="9082a-141">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9082a-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9082a-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="9082a-143">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="9082a-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="9082a-144">Du kan använda New-AzVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="9082a-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="9082a-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="9082a-146">Anger om de virtuella datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="9082a-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="9082a-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="9082a-148">Anger om virtuell dator agent ska etableras på de virtuella datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="9082a-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9082a-149">-Confirm</span></span>
<span data-ttu-id="9082a-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9082a-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9082a-151">-WhatIf</span></span>
<span data-ttu-id="9082a-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9082a-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9082a-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9082a-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9082a-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9082a-154">CommonParameters</span></span>
<span data-ttu-id="9082a-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9082a-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9082a-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9082a-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9082a-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9082a-157">INPUTS</span></span>

### <span data-ttu-id="9082a-158">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9082a-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="9082a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="9082a-159">System.String</span></span>

### <span data-ttu-id="9082a-160">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9082a-160">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9082a-161">Microsoft. Azure. Management. Compute. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="9082a-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="9082a-162">Microsoft. Azure. Management. Compute. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="9082a-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="9082a-163">Microsoft. Azure. Management. Compute. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="9082a-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="9082a-164">Microsoft. Azure. Management. Compute. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="9082a-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="9082a-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9082a-165">OUTPUTS</span></span>

### <span data-ttu-id="9082a-166">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9082a-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9082a-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9082a-167">NOTES</span></span>

## <span data-ttu-id="9082a-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9082a-168">RELATED LINKS</span></span>

[<span data-ttu-id="9082a-169">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="9082a-169">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="9082a-170">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="9082a-170">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="9082a-171">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="9082a-171">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="9082a-172">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="9082a-172">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="9082a-173">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="9082a-173">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


