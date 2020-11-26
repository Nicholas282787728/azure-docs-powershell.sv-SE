---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319651"
---
# <span data-ttu-id="db66a-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="db66a-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="db66a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db66a-102">SYNOPSIS</span></span>
<span data-ttu-id="db66a-103">Aktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="db66a-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="db66a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db66a-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db66a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db66a-105">DESCRIPTION</span></span>
<span data-ttu-id="db66a-106">Cmdleten **set-AzVmssDiskEncryptionExtension** aktiverar kryptering på en virtuell dators skalnings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="db66a-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="db66a-107">Denna cmdlet aktiverar kryptering genom att installera disk krypterings tillägget på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="db66a-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="db66a-108">För virtuella Linux-datorer måste parametern *VolumeType* vara tillgänglig och måste vara inställd på "data"</span><span class="sxs-lookup"><span data-stu-id="db66a-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="db66a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db66a-109">EXAMPLES</span></span>

### <span data-ttu-id="db66a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db66a-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="db66a-111">Det här kommandot aktiverar kryptering på alla diskar för alla Windows-VMs i en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="db66a-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="db66a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="db66a-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="db66a-113">Det här kommandot aktiverar kryptering på data diskarna för alla virtuella Linux-VM i en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="db66a-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="db66a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db66a-114">PARAMETERS</span></span>

### <span data-ttu-id="db66a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db66a-115">-DefaultProfile</span></span>
<span data-ttu-id="db66a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db66a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db66a-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="db66a-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="db66a-118">Inaktivera automatisk uppgradering av del version</span><span class="sxs-lookup"><span data-stu-id="db66a-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="db66a-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="db66a-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="db66a-120">ResourceID för det valv där den genererade krypterings knappen kommer att placeras</span><span class="sxs-lookup"><span data-stu-id="db66a-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="db66a-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="db66a-122">URL för det valv där den genererade krypterings knappen kommer att placeras</span><span class="sxs-lookup"><span data-stu-id="db66a-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="db66a-123">-ExtensionName</span></span>
<span data-ttu-id="db66a-124">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="db66a-124">The extension name.</span></span>
<span data-ttu-id="db66a-125">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för Linux VM</span><span class="sxs-lookup"><span data-stu-id="db66a-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="db66a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="db66a-126">-Force</span></span>
<span data-ttu-id="db66a-127">För att tvinga aktivera kryptering på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="db66a-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="db66a-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="db66a-128">-ForceUpdate</span></span>
<span data-ttu-id="db66a-129">Generera en tagg för tvångs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="db66a-129">Generate a tag for force update.</span></span>  <span data-ttu-id="db66a-130">Detta bör ges för att utföra upprepade krypterings åtgärder på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="db66a-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="db66a-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="db66a-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="db66a-132">Algoritm för krypteringsalgoritm som används för att kryptera volym krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="db66a-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="db66a-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="db66a-134">URL för en KeyEncryptionKey som används för att kryptera disk krypterings tangenten</span><span class="sxs-lookup"><span data-stu-id="db66a-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="db66a-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="db66a-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="db66a-136">ResourceID för det KeyEncryptionKey som används för att kryptera disk krypterings tangenten</span><span class="sxs-lookup"><span data-stu-id="db66a-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="db66a-137">-Lösen fras</span><span class="sxs-lookup"><span data-stu-id="db66a-137">-Passphrase</span></span>
<span data-ttu-id="db66a-138">Lösen frasen som anges i parametrar.</span><span class="sxs-lookup"><span data-stu-id="db66a-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="db66a-139">Denna parameter fungerar bara för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="db66a-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="db66a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db66a-140">-ResourceGroupName</span></span>
<span data-ttu-id="db66a-141">Namnet på den resurs grupp som den virtuella dator skalan tillhör</span><span class="sxs-lookup"><span data-stu-id="db66a-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="db66a-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="db66a-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="db66a-143">Type handler-versionen.</span><span class="sxs-lookup"><span data-stu-id="db66a-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="db66a-144">-VMScaleSetName</span></span>
<span data-ttu-id="db66a-145">Namn på den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="db66a-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="db66a-146">-VolumeType</span></span>
<span data-ttu-id="db66a-147">Anger den typ av volym för virtuell dator som du vill utföra krypteringen på: OS, data eller alla.</span><span class="sxs-lookup"><span data-stu-id="db66a-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="db66a-148">Linux: parametern **VolumeType** måste finnas och måste vara inställd på data.</span><span class="sxs-lookup"><span data-stu-id="db66a-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="db66a-149">Windows: parametern **VolumeType** , om den finns, måste vara inställd på antingen all eller OS.</span><span class="sxs-lookup"><span data-stu-id="db66a-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="db66a-150">Om parametern **VolumeType** utelämnas är den standardinställning för "alla".</span><span class="sxs-lookup"><span data-stu-id="db66a-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db66a-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db66a-151">-Confirm</span></span>
<span data-ttu-id="db66a-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db66a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db66a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db66a-153">-WhatIf</span></span>
<span data-ttu-id="db66a-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db66a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db66a-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db66a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db66a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db66a-156">CommonParameters</span></span>
<span data-ttu-id="db66a-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db66a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db66a-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db66a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db66a-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db66a-159">INPUTS</span></span>

### <span data-ttu-id="db66a-160">System. String</span><span class="sxs-lookup"><span data-stu-id="db66a-160">System.String</span></span>

### <span data-ttu-id="db66a-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db66a-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db66a-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db66a-162">OUTPUTS</span></span>

### <span data-ttu-id="db66a-163">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="db66a-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="db66a-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db66a-164">NOTES</span></span>

## <span data-ttu-id="db66a-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db66a-165">RELATED LINKS</span></span>