---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577258"
---
# <span data-ttu-id="02927-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="02927-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="02927-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02927-102">SYNOPSIS</span></span>
<span data-ttu-id="02927-103">Inaktiverar kryptering på en IaaS virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="02927-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02927-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02927-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02927-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02927-105">DESCRIPTION</span></span>
<span data-ttu-id="02927-106">Cmdleten **disable-AzureRmVMDiskEncryption** inaktiverar kryptering på infrastrukturen som en tjänst (IaaS) virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="02927-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="02927-107">Denna cmdlet stöds endast på virtuella Windows-datorer och inte virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="02927-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="02927-108">Denna cmdlet installerar ett tillägg på den virtuella datorn för att inaktivera kryptering.</span><span class="sxs-lookup"><span data-stu-id="02927-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="02927-109">Om parametern *Name* inte anges skapas ett tillägg med standard namnet "AzureDiskEncryption för Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="02927-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="02927-110">Varning: den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="02927-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="02927-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02927-111">EXAMPLES</span></span>

### <span data-ttu-id="02927-112">Exempel 1: inaktivera kryptering för alla volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="02927-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="02927-113">Det här kommandot inaktiverar kryptering för volymer av typen allt för den virtuella datorn med namnet VM002 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="02927-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="02927-114">Eftersom parametern *VolumeType* inte anges ställer cmdleten in värdet till all.</span><span class="sxs-lookup"><span data-stu-id="02927-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="02927-115">Exempel 2: inaktivera kryptering för data volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="02927-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="02927-116">Det här kommandot inaktiverar kryptering för volymer av typen data för den virtuella datorn med namnet VM004 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="02927-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="02927-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02927-117">PARAMETERS</span></span>

### <span data-ttu-id="02927-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="02927-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="02927-119">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="02927-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02927-120">-Force</span><span class="sxs-lookup"><span data-stu-id="02927-120">-Force</span></span>
<span data-ttu-id="02927-121">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="02927-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="02927-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="02927-122">-Name</span></span>
<span data-ttu-id="02927-123">Specifes namnet på resursen för Azure Resource Manager som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="02927-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="02927-124">Om den här parametern inte anges använder denna cmdlet standardinställningen "AzureDiskEncryption för Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="02927-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="02927-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02927-125">-ResourceGroupName</span></span>
<span data-ttu-id="02927-126">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="02927-126">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="02927-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="02927-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="02927-128">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="02927-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="02927-129">Om du inte anger ett värde för den här parametern används den senaste versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="02927-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="02927-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="02927-130">-VMName</span></span>
<span data-ttu-id="02927-131">Anger namnet på den virtuella dator som denna cmdlet inaktiverar kryptering på.</span><span class="sxs-lookup"><span data-stu-id="02927-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="02927-132">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="02927-132">-VolumeType</span></span>
<span data-ttu-id="02927-133">Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="02927-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="02927-134">Giltiga värden för Windows Virtual-datorer är:</span><span class="sxs-lookup"><span data-stu-id="02927-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="02927-135">Alla</span><span class="sxs-lookup"><span data-stu-id="02927-135">All</span></span>
- <span data-ttu-id="02927-136">TIDIGARE</span><span class="sxs-lookup"><span data-stu-id="02927-136">OS</span></span>
- <span data-ttu-id="02927-137">Värde.</span><span class="sxs-lookup"><span data-stu-id="02927-137">Data.</span></span>
<span data-ttu-id="02927-138">Om du inte anger ett värde för den här parametern är standardvärdet alla.</span><span class="sxs-lookup"><span data-stu-id="02927-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="02927-139">Det går för närvarande inte att inaktivera kryptering för Linux.</span><span class="sxs-lookup"><span data-stu-id="02927-139">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="02927-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="02927-140">-Confirm</span></span>
<span data-ttu-id="02927-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="02927-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02927-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02927-142">-WhatIf</span></span>
<span data-ttu-id="02927-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="02927-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="02927-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="02927-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02927-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02927-145">CommonParameters</span></span>
<span data-ttu-id="02927-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02927-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02927-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02927-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02927-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02927-148">INPUTS</span></span>

### <span data-ttu-id="02927-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="02927-149">None</span></span>
<span data-ttu-id="02927-150">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="02927-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02927-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02927-151">OUTPUTS</span></span>

### <span data-ttu-id="02927-152">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="02927-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="02927-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02927-153">NOTES</span></span>

## <span data-ttu-id="02927-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02927-154">RELATED LINKS</span></span>

[<span data-ttu-id="02927-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="02927-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="02927-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="02927-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="02927-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="02927-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


