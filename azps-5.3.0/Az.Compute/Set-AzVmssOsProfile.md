---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524445"
---
# <span data-ttu-id="386ff-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="386ff-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="386ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="386ff-102">SYNOPSIS</span></span>
<span data-ttu-id="386ff-103">Anger profil egenskaperna för VMSS operativ system.</span><span class="sxs-lookup"><span data-stu-id="386ff-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="386ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="386ff-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="386ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="386ff-105">DESCRIPTION</span></span>
<span data-ttu-id="386ff-106">Cmdleten **set-AzVmssOsProfile** anger den virtuella datorns skalnings profil egenskaper.</span><span class="sxs-lookup"><span data-stu-id="386ff-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="386ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="386ff-107">EXAMPLES</span></span>

### <span data-ttu-id="386ff-108">Exempel 1: Ange profil egenskaperna för en VMSS</span><span class="sxs-lookup"><span data-stu-id="386ff-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="386ff-109">Det här kommandot anger profil egenskaper för operativ systemet för de virtuella datorerna som tillhör VMSS med namnet ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="386ff-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="386ff-110">Kommandot anger prefixet för alla virtuella datorer i VMSS för att testa och förse administratörens användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="386ff-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="386ff-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="386ff-111">PARAMETERS</span></span>

### <span data-ttu-id="386ff-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="386ff-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="386ff-113">Anger ett obevakat innehålls objekt.</span><span class="sxs-lookup"><span data-stu-id="386ff-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="386ff-114">Du kan använda Add-AzVMAdditionalUnattendContent för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="386ff-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="386ff-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="386ff-115">-AdminPassword</span></span>
<span data-ttu-id="386ff-116">Anger det administratörs lösen ord som ska användas för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="386ff-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="386ff-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="386ff-117">-AdminUsername</span></span>
<span data-ttu-id="386ff-118">Anger det administratörs konto namn som ska användas för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="386ff-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="386ff-119">**Begränsning i Windows:** Kan inte sluta med \" .\"</span><span class="sxs-lookup"><span data-stu-id="386ff-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="386ff-120">**Otillåtna värden:** \" administratör \" , \" administratör \" , \" användare \" , \" user1 \" , \" test \" , \" user2 \" , \" test1 \" , \" user3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" actuser \" , \" ADM \" , \" admin2 \" , \" ASPNET \" , \" säkerhets kopiering \" , \" konsol \" , \" David \" , \" gäst \" , \" John \" , \" Owner \" , \" root \" , \" Server \" , \" SQL \" , \" support \" , \" support_388945a0 \" , \" sys \" , \" TEST2 \" , \" test3 \" , \" user4 \" , \" user5 \" .</span><span class="sxs-lookup"><span data-stu-id="386ff-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="386ff-121">**Minimilängd (Linux):** 1 tecken</span><span class="sxs-lookup"><span data-stu-id="386ff-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="386ff-122">**Max längd (Linux):** 64 tecken</span><span class="sxs-lookup"><span data-stu-id="386ff-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="386ff-123">**Max längd (Windows):** 20 tecken</span><span class="sxs-lookup"><span data-stu-id="386ff-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="386ff-124">Information om rot åtkomst till Virtual Linux-tjänsten finns i [använda rot behörigheter på virtuella Linux-datorer i Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="386ff-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="386ff-125">En lista med inbyggda systemanvändare på Linux som inte ska användas i det här fältet finns i [välja användar namn för Linux på Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="386ff-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="386ff-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="386ff-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="386ff-127">Anger det här prefixet för alla virtuella dator instanser i VMSS.</span><span class="sxs-lookup"><span data-stu-id="386ff-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="386ff-128">Dator namn måste vara mellan 1 och 15 tecken långa.</span><span class="sxs-lookup"><span data-stu-id="386ff-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="386ff-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="386ff-129">-CustomData</span></span>
<span data-ttu-id="386ff-130">Anger en Base-64-kodad sträng med anpassade data.</span><span class="sxs-lookup"><span data-stu-id="386ff-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="386ff-131">Det här är avkodat till en binär matris som sparats som en fil på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="386ff-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="386ff-132">Den maximala längden för den binära matrisen är 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="386ff-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="386ff-133">Information om hur du använder Cloud-Init för din virtuella dator finns i [använda Cloud-Init för att anpassa en virtuella dator för Linux när den skapas](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="386ff-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="386ff-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386ff-134">-DefaultProfile</span></span>
<span data-ttu-id="386ff-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="386ff-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="386ff-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="386ff-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="386ff-137">Indikerar att denna cmdlet inaktiverar lösenordsautentisering.</span><span class="sxs-lookup"><span data-stu-id="386ff-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="386ff-138">-Lyssnare</span><span class="sxs-lookup"><span data-stu-id="386ff-138">-Listener</span></span>
<span data-ttu-id="386ff-139">Anger WinRM-lyssnarna (Windows Remote Management).</span><span class="sxs-lookup"><span data-stu-id="386ff-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="386ff-140">Detta möjliggör fjärran sluten Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="386ff-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="386ff-141">Du kan använda Add-AzVmssWinRMListener cmdlet för att skapa lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="386ff-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="386ff-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="386ff-142">-PublicKey</span></span>
<span data-ttu-id="386ff-143">Anger det offentliga objektet för SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="386ff-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="386ff-144">Du kan använda Add-AzVMSshPublicKey-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="386ff-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="386ff-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="386ff-145">-Secret</span></span>
<span data-ttu-id="386ff-146">Anger det hemligheter-objekt som innehåller certifikat referenser som ska placeras på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="386ff-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="386ff-147">Du kan använda Add-AzVmssSecret cmdlet för att skapa hemligheter-objekt.</span><span class="sxs-lookup"><span data-stu-id="386ff-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="386ff-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="386ff-148">-TimeZone</span></span>
<span data-ttu-id="386ff-149">Anger tids zonen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="386ff-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="386ff-150">t. \" Pacific, normal tid \" .</span><span class="sxs-lookup"><span data-stu-id="386ff-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="386ff-151">Möjliga värden kan vara [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) värde från tids zoner som returneras av [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span><span class="sxs-lookup"><span data-stu-id="386ff-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="386ff-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="386ff-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="386ff-153">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="386ff-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="386ff-154">Du kan använda New-AzVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="386ff-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="386ff-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="386ff-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="386ff-156">Anger om de virtuella datorerna i VMSS är aktiverade för automatiska uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="386ff-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="386ff-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="386ff-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="386ff-158">Anger om virtuell dator agent ska etableras på de virtuella datorerna i VMSS.</span><span class="sxs-lookup"><span data-stu-id="386ff-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="386ff-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="386ff-159">-Confirm</span></span>
<span data-ttu-id="386ff-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="386ff-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="386ff-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="386ff-161">-WhatIf</span></span>
<span data-ttu-id="386ff-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="386ff-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="386ff-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="386ff-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="386ff-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386ff-164">CommonParameters</span></span>
<span data-ttu-id="386ff-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="386ff-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="386ff-166">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="386ff-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386ff-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="386ff-167">INPUTS</span></span>

### <span data-ttu-id="386ff-168">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="386ff-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="386ff-169">System. String</span><span class="sxs-lookup"><span data-stu-id="386ff-169">System.String</span></span>

### <span data-ttu-id="386ff-170">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="386ff-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="386ff-171">Microsoft. Azure. Management. Compute. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="386ff-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="386ff-172">Microsoft. Azure. Management. Compute. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="386ff-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="386ff-173">Microsoft. Azure. Management. Compute. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="386ff-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="386ff-174">Microsoft. Azure. Management. Compute. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="386ff-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="386ff-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="386ff-175">OUTPUTS</span></span>

### <span data-ttu-id="386ff-176">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="386ff-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="386ff-177">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="386ff-177">NOTES</span></span>

## <span data-ttu-id="386ff-178">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="386ff-178">RELATED LINKS</span></span>

[<span data-ttu-id="386ff-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="386ff-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="386ff-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="386ff-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="386ff-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="386ff-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="386ff-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="386ff-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="386ff-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="386ff-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


