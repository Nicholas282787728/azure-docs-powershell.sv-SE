---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: aeac00806ef77d756dc8060b06f7baa995568fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583596"
---
# <span data-ttu-id="2cd5b-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2cd5b-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="2cd5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd5b-103">Aktiverar disk kryptering på en virtuell dators skala.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cd5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cd5b-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cd5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="2cd5b-106">Cmdleten **set-AzureRmVmssDiskEncryptionExtension** aktiverar kryptering på en virtuell dators skalnings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="2cd5b-107">Denna cmdlet aktiverar kryptering genom att installera disk krypterings tillägget på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="2cd5b-108">Om ingen *namn* parameter anges installeras ett tillägg med standard namnet AzureDiskEncryption för virtuella datorer som kör operativ systemet Windows eller AzureDiskEncryptionForLinux för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="2cd5b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cd5b-109">EXAMPLES</span></span>

### <span data-ttu-id="2cd5b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2cd5b-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="2cd5b-111">Det här kommandot aktiverar kryptering på alla diskar för alla virtuella datorer i den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="2cd5b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cd5b-112">PARAMETERS</span></span>

### <span data-ttu-id="2cd5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd5b-113">-DefaultProfile</span></span>
<span data-ttu-id="2cd5b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cd5b-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2cd5b-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2cd5b-116">Inaktivera automatisk uppgradering av del version</span><span class="sxs-lookup"><span data-stu-id="2cd5b-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="2cd5b-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2cd5b-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="2cd5b-118">ResourceID för det valv där den genererade krypterings knappen kommer att placeras</span><span class="sxs-lookup"><span data-stu-id="2cd5b-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="2cd5b-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2cd5b-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="2cd5b-120">URL för det valv där den genererade krypterings knappen kommer att placeras</span><span class="sxs-lookup"><span data-stu-id="2cd5b-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="2cd5b-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="2cd5b-121">-ExtensionName</span></span>
<span data-ttu-id="2cd5b-122">Tillägget.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-122">The extension name.</span></span>
<span data-ttu-id="2cd5b-123">Om du inte anger den här parametern används standardvärden för AzureDiskEncryption för Windows VMs och AzureDiskEncryptionForLinux för Linux VM</span><span class="sxs-lookup"><span data-stu-id="2cd5b-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="2cd5b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2cd5b-124">-Force</span></span>
<span data-ttu-id="2cd5b-125">För att tvinga aktivera kryptering på den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="2cd5b-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="2cd5b-126">-ForceUpdate</span></span>
<span data-ttu-id="2cd5b-127">Generera en tagg för tvångs uppdatering.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-127">Generate a tag for force update.</span></span>  <span data-ttu-id="2cd5b-128">Detta bör ges för att utföra upprepade krypterings åtgärder på samma virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="2cd5b-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2cd5b-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="2cd5b-130">Algoritm för krypteringsalgoritm som används för att kryptera volym krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="2cd5b-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="2cd5b-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="2cd5b-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="2cd5b-132">URL för en KeyEncryptionKey som används för att kryptera disk krypterings tangenten</span><span class="sxs-lookup"><span data-stu-id="2cd5b-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="2cd5b-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2cd5b-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="2cd5b-134">ResourceID för det KeyEncryptionKey som används för att kryptera disk krypterings tangenten</span><span class="sxs-lookup"><span data-stu-id="2cd5b-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="2cd5b-135">-Lösen fras</span><span class="sxs-lookup"><span data-stu-id="2cd5b-135">-Passphrase</span></span>
<span data-ttu-id="2cd5b-136">Lösen frasen som anges i parametrar.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="2cd5b-137">Denna parameter fungerar bara för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="2cd5b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd5b-138">-ResourceGroupName</span></span>
<span data-ttu-id="2cd5b-139">Namnet på den resurs grupp som den virtuella dator skalan tillhör</span><span class="sxs-lookup"><span data-stu-id="2cd5b-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="2cd5b-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2cd5b-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="2cd5b-141">Type handler-versionen.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-141">The type handler version.</span></span>

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

### <span data-ttu-id="2cd5b-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2cd5b-142">-VMScaleSetName</span></span>
<span data-ttu-id="2cd5b-143">Namn på den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="2cd5b-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="2cd5b-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="2cd5b-144">-VolumeType</span></span>
<span data-ttu-id="2cd5b-145">Typ av volym (OS eller data) för att utföra krypterings åtgärd</span><span class="sxs-lookup"><span data-stu-id="2cd5b-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="2cd5b-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2cd5b-146">-Confirm</span></span>
<span data-ttu-id="2cd5b-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd5b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cd5b-148">-WhatIf</span></span>
<span data-ttu-id="2cd5b-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cd5b-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd5b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd5b-151">CommonParameters</span></span>
<span data-ttu-id="2cd5b-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd5b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd5b-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd5b-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd5b-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cd5b-154">INPUTS</span></span>

### <span data-ttu-id="2cd5b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2cd5b-155">System.String</span></span>

### <span data-ttu-id="2cd5b-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2cd5b-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2cd5b-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cd5b-157">OUTPUTS</span></span>

### <span data-ttu-id="2cd5b-158">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="2cd5b-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="2cd5b-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cd5b-159">NOTES</span></span>

## <span data-ttu-id="2cd5b-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cd5b-160">RELATED LINKS</span></span>
