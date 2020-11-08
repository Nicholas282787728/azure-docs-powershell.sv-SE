---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6a14a8472ca33fe9dbb15aa2ddf58208764a5a6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925262"
---
# <span data-ttu-id="b74d9-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b74d9-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="b74d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b74d9-102">SYNOPSIS</span></span>
<span data-ttu-id="b74d9-103">Inaktiverar kryptering på en IaaS virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b74d9-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="b74d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b74d9-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b74d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b74d9-105">DESCRIPTION</span></span>
<span data-ttu-id="b74d9-106">Cmdleten **disable-AzVMDiskEncryption** inaktiverar kryptering på infrastrukturen som en tjänst (IaaS) virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="b74d9-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="b74d9-107">Denna cmdlet stöds endast på virtuella Windows-datorer och inte virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="b74d9-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="b74d9-108">Denna cmdlet installerar ett tillägg på den virtuella datorn för att inaktivera kryptering.</span><span class="sxs-lookup"><span data-stu-id="b74d9-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="b74d9-109">Om parametern *Name* inte anges skapas ett tillägg med standard namnet "AzureDiskEncryption för Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="b74d9-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="b74d9-110">Varning: den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b74d9-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="b74d9-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b74d9-111">EXAMPLES</span></span>

### <span data-ttu-id="b74d9-112">Exempel 1: inaktivera kryptering för alla volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="b74d9-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="b74d9-113">Det här kommandot inaktiverar kryptering för volymer av typen allt för den virtuella datorn med namnet VM002 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="b74d9-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b74d9-114">Eftersom parametern *VolumeType* inte anges ställer cmdleten in värdet till all.</span><span class="sxs-lookup"><span data-stu-id="b74d9-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="b74d9-115">Exempel 2: inaktivera kryptering för data volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="b74d9-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="b74d9-116">Det här kommandot inaktiverar kryptering för volymer av typen data för den virtuella datorn med namnet VM004 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="b74d9-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="b74d9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b74d9-117">PARAMETERS</span></span>

### <span data-ttu-id="b74d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b74d9-118">-DefaultProfile</span></span>
<span data-ttu-id="b74d9-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b74d9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b74d9-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="b74d9-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="b74d9-121">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="b74d9-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="b74d9-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="b74d9-123">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="b74d9-123">The extension publisher name.</span></span> <span data-ttu-id="b74d9-124">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="b74d9-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="b74d9-125">-ExtensionType</span></span>
<span data-ttu-id="b74d9-126">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="b74d9-126">The extension type.</span></span> <span data-ttu-id="b74d9-127">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="b74d9-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-128">-Force</span><span class="sxs-lookup"><span data-stu-id="b74d9-128">-Force</span></span>
<span data-ttu-id="b74d9-129">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="b74d9-129">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="b74d9-130">-Name</span></span>
<span data-ttu-id="b74d9-131">Specifes namnet på resursen för Azure Resource Manager som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="b74d9-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="b74d9-132">Om den här parametern inte anges använder denna cmdlet standardinställningen "AzureDiskEncryption för Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="b74d9-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b74d9-133">-ResourceGroupName</span></span>
<span data-ttu-id="b74d9-134">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b74d9-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="b74d9-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="b74d9-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="b74d9-136">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="b74d9-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="b74d9-137">Om du inte anger ett värde för den här parametern används den senaste versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="b74d9-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="b74d9-138">-VMName</span></span>
<span data-ttu-id="b74d9-139">Anger namnet på den virtuella dator som denna cmdlet inaktiverar kryptering på.</span><span class="sxs-lookup"><span data-stu-id="b74d9-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="b74d9-140">-VolumeType</span></span>
<span data-ttu-id="b74d9-141">Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b74d9-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="b74d9-142">Giltiga värden för Windows Virtual-datorer är:</span><span class="sxs-lookup"><span data-stu-id="b74d9-142">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="b74d9-143">Alla</span><span class="sxs-lookup"><span data-stu-id="b74d9-143">All</span></span>
- <span data-ttu-id="b74d9-144">TIDIGARE</span><span class="sxs-lookup"><span data-stu-id="b74d9-144">OS</span></span>
- <span data-ttu-id="b74d9-145">Värde.</span><span class="sxs-lookup"><span data-stu-id="b74d9-145">Data.</span></span>
<span data-ttu-id="b74d9-146">Om du inte anger ett värde för den här parametern är standardvärdet alla.</span><span class="sxs-lookup"><span data-stu-id="b74d9-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="b74d9-147">Det går för närvarande inte att inaktivera kryptering för Linux.</span><span class="sxs-lookup"><span data-stu-id="b74d9-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b74d9-148">-Confirm</span></span>
<span data-ttu-id="b74d9-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b74d9-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b74d9-150">-WhatIf</span></span>
<span data-ttu-id="b74d9-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b74d9-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b74d9-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b74d9-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b74d9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74d9-153">CommonParameters</span></span>
<span data-ttu-id="b74d9-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b74d9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74d9-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b74d9-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74d9-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b74d9-156">INPUTS</span></span>

### <span data-ttu-id="b74d9-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="b74d9-157">None</span></span>
<span data-ttu-id="b74d9-158">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b74d9-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b74d9-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b74d9-159">OUTPUTS</span></span>

### <span data-ttu-id="b74d9-160">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b74d9-160">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b74d9-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b74d9-161">NOTES</span></span>

## <span data-ttu-id="b74d9-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b74d9-162">RELATED LINKS</span></span>

[<span data-ttu-id="b74d9-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="b74d9-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="b74d9-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="b74d9-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="b74d9-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="b74d9-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)

