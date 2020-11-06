---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 2227193923b014f69da0ddb60ae9ee00bdc14b6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585776"
---
# <span data-ttu-id="37b8d-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="37b8d-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="37b8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="37b8d-103">Inaktiverar kryptering på en IaaS virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="37b8d-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37b8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37b8d-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37b8d-105">DESCRIPTION</span></span>
<span data-ttu-id="37b8d-106">Cmdleten **disable-AzureRmVMDiskEncryption** inaktiverar kryptering på infrastrukturen som en tjänst (IaaS) virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="37b8d-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="37b8d-107">Denna cmdlet stöds endast på virtuella Windows-datorer och inte virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="37b8d-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="37b8d-108">Denna cmdlet installerar ett tillägg på den virtuella datorn för att inaktivera kryptering.</span><span class="sxs-lookup"><span data-stu-id="37b8d-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="37b8d-109">Om parametern *Name* inte anges skapas ett tillägg med standard namnet "AzureDiskEncryption för Windows VMS".</span><span class="sxs-lookup"><span data-stu-id="37b8d-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="37b8d-110">Varning: den här cmdleten startar om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="37b8d-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="37b8d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37b8d-111">EXAMPLES</span></span>

### <span data-ttu-id="37b8d-112">Exempel 1: inaktivera kryptering för alla volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="37b8d-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="37b8d-113">Det här kommandot inaktiverar kryptering för volymer av typen allt för den virtuella datorn med namnet VM002 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="37b8d-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="37b8d-114">Eftersom parametern *VolumeType* inte anges ställer cmdleten in värdet till all.</span><span class="sxs-lookup"><span data-stu-id="37b8d-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="37b8d-115">Exempel 2: inaktivera kryptering för data volymer på en virtuell Windows-dator</span><span class="sxs-lookup"><span data-stu-id="37b8d-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="37b8d-116">Det här kommandot inaktiverar kryptering för volymer av typen data för den virtuella datorn med namnet VM004 som tillhör resurs gruppen med namnet Group002.</span><span class="sxs-lookup"><span data-stu-id="37b8d-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="37b8d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37b8d-117">PARAMETERS</span></span>

### <span data-ttu-id="37b8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b8d-118">-DefaultProfile</span></span>
<span data-ttu-id="37b8d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37b8d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b8d-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="37b8d-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="37b8d-121">Anger att denna cmdlet inaktiverar automatisk omuppgradering av den mindre versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="37b8d-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37b8d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="37b8d-122">-Force</span></span>
<span data-ttu-id="37b8d-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="37b8d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37b8d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="37b8d-124">-Name</span></span>
<span data-ttu-id="37b8d-125">Specifes namnet på resursen för Azure Resource Manager som representerar tillägget.</span><span class="sxs-lookup"><span data-stu-id="37b8d-125">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="37b8d-126">Om den här parametern inte anges använder denna cmdlet standardinställningen "AzureDiskEncryption för Windows VMs".</span><span class="sxs-lookup"><span data-stu-id="37b8d-126">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="37b8d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b8d-127">-ResourceGroupName</span></span>
<span data-ttu-id="37b8d-128">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="37b8d-128">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="37b8d-129">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="37b8d-129">-TypeHandlerVersion</span></span>
<span data-ttu-id="37b8d-130">Anger krypterings tillägget.</span><span class="sxs-lookup"><span data-stu-id="37b8d-130">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="37b8d-131">Om du inte anger ett värde för den här parametern används den senaste versionen av tillägget.</span><span class="sxs-lookup"><span data-stu-id="37b8d-131">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="37b8d-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="37b8d-132">-VMName</span></span>
<span data-ttu-id="37b8d-133">Anger namnet på den virtuella dator som denna cmdlet inaktiverar kryptering på.</span><span class="sxs-lookup"><span data-stu-id="37b8d-133">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="37b8d-134">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="37b8d-134">-VolumeType</span></span>
<span data-ttu-id="37b8d-135">Anger vilken typ av virtuell dator volym som ska utföra krypterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="37b8d-135">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="37b8d-136">Giltiga värden för Windows Virtual-datorer är:</span><span class="sxs-lookup"><span data-stu-id="37b8d-136">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="37b8d-137">Alla</span><span class="sxs-lookup"><span data-stu-id="37b8d-137">All</span></span>
- <span data-ttu-id="37b8d-138">TIDIGARE</span><span class="sxs-lookup"><span data-stu-id="37b8d-138">OS</span></span>
- <span data-ttu-id="37b8d-139">Värde.</span><span class="sxs-lookup"><span data-stu-id="37b8d-139">Data.</span></span>
<span data-ttu-id="37b8d-140">Om du inte anger ett värde för den här parametern är standardvärdet alla.</span><span class="sxs-lookup"><span data-stu-id="37b8d-140">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="37b8d-141">Det går för närvarande inte att inaktivera kryptering för Linux.</span><span class="sxs-lookup"><span data-stu-id="37b8d-141">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="37b8d-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37b8d-142">-Confirm</span></span>
<span data-ttu-id="37b8d-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37b8d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b8d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b8d-144">-WhatIf</span></span>
<span data-ttu-id="37b8d-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="37b8d-145">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="37b8d-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="37b8d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b8d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b8d-147">CommonParameters</span></span>
<span data-ttu-id="37b8d-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b8d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b8d-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b8d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b8d-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37b8d-150">INPUTS</span></span>

## <span data-ttu-id="37b8d-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37b8d-151">OUTPUTS</span></span>

### <span data-ttu-id="37b8d-152">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="37b8d-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="37b8d-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37b8d-153">NOTES</span></span>

## <span data-ttu-id="37b8d-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37b8d-154">RELATED LINKS</span></span>

[<span data-ttu-id="37b8d-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="37b8d-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="37b8d-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="37b8d-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="37b8d-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="37b8d-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


