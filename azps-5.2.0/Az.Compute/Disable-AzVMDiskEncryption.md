---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413163"
---
# <span data-ttu-id="a8ad3-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a8ad3-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="a8ad3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ad3-103">Inaktiverar kryptering på en IaaS virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="a8ad3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8ad3-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ad3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8ad3-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ad3-106">Cmdleten **disable-AzVMDiskEncryption** inaktiverar kryptering på infrastrukturen som en tjänst (IaaS) virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="a8ad3-107">Denna cmdlet stöds endast på virtuella Windows-datorer och inte virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="a8ad3-108">Denna cmdlet installerar ett tillägg på den virtuella datorn för att inaktivera kryptering.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="a8ad3-109">Om parametern *Name* inte anges skapas ett tillägg med standard namnet "AzureDiskEncryption för Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="a8ad3-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="a8ad3-110">Varning: den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="a8ad3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8ad3-111">EXAMPLES</span></span>

### <span data-ttu-id="a8ad3-112">Exempel 1: inaktivera kryptering för alla volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="a8ad3-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="a8ad3-113">Det här kommandot inaktiverar kryptering för volymer av typen allt för den virtuella datorn med namnet VM002 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="a8ad3-114">Eftersom parametern *VolumeType* inte anges ställer cmdleten in värdet till all.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="a8ad3-115">Exempel 2: inaktivera kryptering för data volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="a8ad3-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="a8ad3-116">Det här kommandot inaktiverar kryptering för volymer av typen data för den virtuella datorn med namnet VM004 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a8ad3-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8ad3-117">PARAMETERS</span></span>

### <span data-ttu-id="a8ad3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ad3-118">-DefaultProfile</span></span>
<span data-ttu-id="a8ad3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ad3-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a8ad3-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a8ad3-121">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ad3-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="a8ad3-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="a8ad3-123">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-123">The extension publisher name.</span></span> <span data-ttu-id="a8ad3-124">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="a8ad3-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="a8ad3-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a8ad3-125">-ExtensionType</span></span>
<span data-ttu-id="a8ad3-126">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-126">The extension type.</span></span> <span data-ttu-id="a8ad3-127">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="a8ad3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a8ad3-128">-Force</span></span>
<span data-ttu-id="a8ad3-129">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a8ad3-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8ad3-130">-Name</span></span>
<span data-ttu-id="a8ad3-131">Anger namnet på resursen för Azure Resource Manager (ARM) som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="a8ad3-132">Om den här parametern inte anges använder denna cmdlet standardinställningen "AzureDiskEncryption för Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="a8ad3-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ad3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ad3-133">-ResourceGroupName</span></span>
<span data-ttu-id="a8ad3-134">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="a8ad3-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a8ad3-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="a8ad3-136">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="a8ad3-137">Om du inte anger ett värde för den här parametern används den senaste versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ad3-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="a8ad3-138">-VMName</span></span>
<span data-ttu-id="a8ad3-139">Anger namnet på den virtuella dator som denna cmdlet inaktiverar kryptering på.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ad3-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="a8ad3-140">-VolumeType</span></span>
<span data-ttu-id="a8ad3-141">Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="a8ad3-142">Giltiga värden för Windows Virtual-datorer är:</span><span class="sxs-lookup"><span data-stu-id="a8ad3-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="a8ad3-143">Alla</span><span class="sxs-lookup"><span data-stu-id="a8ad3-143">All</span></span>
- <span data-ttu-id="a8ad3-144">TIDIGARE</span><span class="sxs-lookup"><span data-stu-id="a8ad3-144">OS</span></span>
- <span data-ttu-id="a8ad3-145">Värde.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-145">Data.</span></span>
<span data-ttu-id="a8ad3-146">Om du inte anger ett värde för den här parametern är standardvärdet alla.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="a8ad3-147">Det går för närvarande inte att inaktivera kryptering för Linux.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ad3-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8ad3-148">-Confirm</span></span>
<span data-ttu-id="a8ad3-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ad3-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ad3-150">-WhatIf</span></span>
<span data-ttu-id="a8ad3-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ad3-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ad3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ad3-153">CommonParameters</span></span>
<span data-ttu-id="a8ad3-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ad3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ad3-155">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8ad3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ad3-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8ad3-156">INPUTS</span></span>

### <span data-ttu-id="a8ad3-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a8ad3-157">System.String</span></span>

### <span data-ttu-id="a8ad3-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8ad3-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8ad3-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8ad3-159">OUTPUTS</span></span>

### <span data-ttu-id="a8ad3-160">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a8ad3-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a8ad3-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8ad3-161">NOTES</span></span>

## <span data-ttu-id="a8ad3-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8ad3-162">RELATED LINKS</span></span>

[<span data-ttu-id="a8ad3-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="a8ad3-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="a8ad3-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a8ad3-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="a8ad3-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a8ad3-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


