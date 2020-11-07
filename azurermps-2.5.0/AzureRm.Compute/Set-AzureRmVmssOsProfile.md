---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssosprofile
schema: 2.0.0
ms.openlocfilehash: ff2b46c661640221326d50aa71c2659bd5672ab1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929942"
---
# <span data-ttu-id="54625-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="54625-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="54625-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="54625-102">SYNOPSIS</span></span>
<span data-ttu-id="54625-103">Anger profil egenskaperna för VMSS operativ system.</span><span class="sxs-lookup"><span data-stu-id="54625-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54625-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="54625-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54625-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="54625-105">DESCRIPTION</span></span>
<span data-ttu-id="54625-106">Cmdleten **set-AzureRmVmssOsProfile** anger den virtuella datorns skalnings profil egenskaper.</span><span class="sxs-lookup"><span data-stu-id="54625-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="54625-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="54625-107">EXAMPLES</span></span>

### <span data-ttu-id="54625-108">Exempel 1: Ange profil egenskaperna för en VMSS</span><span class="sxs-lookup"><span data-stu-id="54625-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="54625-109">Det här kommandot anger profil egenskaper för operativ systemet för de virtuella datorerna som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="54625-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="54625-110">Kommandot anger prefixet för alla virtuella datorer i VMSS för att testa och förse administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="54625-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="54625-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="54625-111">PARAMETERS</span></span>

### <span data-ttu-id="54625-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="54625-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="54625-113">Anger ett obevakat innehålls objekt.</span><span class="sxs-lookup"><span data-stu-id="54625-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="54625-114">Du kan använda Add-AzureRmVMAdditionalUnattendContent för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="54625-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="54625-115">-AdminPassword</span></span>
<span data-ttu-id="54625-116">Anger det administratörs lösen ord som ska användas för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="54625-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="54625-117">-AdminUsername</span></span>
<span data-ttu-id="54625-118">Anger det administratörs konto namn som ska användas för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="54625-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="54625-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="54625-120">Anger det här prefixet för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="54625-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="54625-121">Dator namn måste vara mellan 1 och 15 tecken långa.</span><span class="sxs-lookup"><span data-stu-id="54625-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="54625-122">-CustomData</span></span>
<span data-ttu-id="54625-123">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="54625-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="54625-124">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="54625-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="54625-125">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="54625-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54625-126">-DefaultProfile</span></span>
<span data-ttu-id="54625-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="54625-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54625-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="54625-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="54625-129">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="54625-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-130">-Lyssnare</span><span class="sxs-lookup"><span data-stu-id="54625-130">-Listener</span></span>
<span data-ttu-id="54625-131">Anger WinRM-lyssnarna (Windows Remote Management).</span><span class="sxs-lookup"><span data-stu-id="54625-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="54625-132">Detta möjliggör fjärran sluten Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="54625-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="54625-133">Du kan använda Add-AzureRmVmssWinRMListener cmdlet för att skapa lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="54625-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="54625-134">-PublicKey</span></span>
<span data-ttu-id="54625-135">Anger det offentliga objektet för SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="54625-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="54625-136">Du kan använda Add-AzureRmVMSshPublicKey-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="54625-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="54625-137">-Secret</span></span>
<span data-ttu-id="54625-138">Anger det hemligheter-objekt som innehåller certifikat referenser som ska placeras på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="54625-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="54625-139">Du kan använda Add-AzureRmVmssSecret cmdlet för att skapa hemligheter-objekt.</span><span class="sxs-lookup"><span data-stu-id="54625-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="54625-140">-TimeZone</span></span>
<span data-ttu-id="54625-141">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="54625-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54625-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="54625-143">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="54625-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="54625-144">Du kan använda New-AzureRmVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="54625-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="54625-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="54625-146">Anger om de virtuella datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="54625-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="54625-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="54625-148">Anger om virtuell dator agent ska etableras på de virtuella datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="54625-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54625-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="54625-149">-Confirm</span></span>
<span data-ttu-id="54625-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="54625-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54625-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54625-151">-WhatIf</span></span>
<span data-ttu-id="54625-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="54625-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54625-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="54625-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54625-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54625-154">CommonParameters</span></span>
<span data-ttu-id="54625-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54625-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54625-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54625-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54625-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="54625-157">INPUTS</span></span>

### <span data-ttu-id="54625-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54625-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="54625-159">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="54625-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="54625-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="54625-160">OUTPUTS</span></span>

### <span data-ttu-id="54625-161">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="54625-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="54625-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="54625-162">NOTES</span></span>

## <span data-ttu-id="54625-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="54625-163">RELATED LINKS</span></span>

[<span data-ttu-id="54625-164">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="54625-164">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="54625-165">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="54625-165">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="54625-166">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="54625-166">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="54625-167">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="54625-167">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="54625-168">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="54625-168">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


