---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: c42aae31bb525f9da6a2963a945a6244373ac8db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745088"
---
# <span data-ttu-id="fd4bf-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="fd4bf-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="fd4bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd4bf-102">SYNOPSIS</span></span>
<span data-ttu-id="fd4bf-103">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="fd4bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd4bf-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd4bf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd4bf-105">DESCRIPTION</span></span>
<span data-ttu-id="fd4bf-106">**New-AzSnapshotConfig-** cmdleten skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="fd4bf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd4bf-107">EXAMPLES</span></span>

### <span data-ttu-id="fd4bf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd4bf-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="fd4bf-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="fd4bf-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="fd4bf-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="fd4bf-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fd4bf-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="fd4bf-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd4bf-113">PARAMETERS</span></span>

### <span data-ttu-id="fd4bf-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="fd4bf-114">-CreateOption</span></span>
<span data-ttu-id="fd4bf-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="fd4bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd4bf-116">-DefaultProfile</span></span>
<span data-ttu-id="fd4bf-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd4bf-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fd4bf-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="fd4bf-119">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="fd4bf-120">-DiskSizeGB</span></span>
<span data-ttu-id="fd4bf-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="fd4bf-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="fd4bf-123">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-123">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-124">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="fd4bf-124">-HyperVGeneration</span></span>
<span data-ttu-id="fd4bf-125">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-125">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="fd4bf-126">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-126">Applicable to OS disks only.</span></span>  <span data-ttu-id="fd4bf-127">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-127">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="fd4bf-128">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="fd4bf-128">-ImageReference</span></span>
<span data-ttu-id="fd4bf-129">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-129">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-130">-Inkrementellt</span><span class="sxs-lookup"><span data-stu-id="fd4bf-130">-Incremental</span></span>
<span data-ttu-id="fd4bf-131">Anger en stegvis ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-131">Specifies an incremental snapshot.</span></span> <span data-ttu-id="fd4bf-132">Inkrementella ögonblicks bilder på samma disk tar mindre plats än fullständiga stillbilder och kan omräknas.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-132">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="fd4bf-133">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="fd4bf-133">-KeyEncryptionKey</span></span>
<span data-ttu-id="fd4bf-134">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-134">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="fd4bf-135">-Location</span></span>
<span data-ttu-id="fd4bf-136">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-136">Specifies a location.</span></span>

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

### <span data-ttu-id="fd4bf-137">-OsType</span><span class="sxs-lookup"><span data-stu-id="fd4bf-137">-OsType</span></span>
<span data-ttu-id="fd4bf-138">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-138">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fd4bf-139">-SkuName</span></span>
<span data-ttu-id="fd4bf-140">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-140">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-141">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="fd4bf-141">-SourceResourceId</span></span>
<span data-ttu-id="fd4bf-142">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-142">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="fd4bf-143">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="fd4bf-143">-SourceUri</span></span>
<span data-ttu-id="fd4bf-144">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-144">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="fd4bf-145">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fd4bf-145">-StorageAccountId</span></span>
<span data-ttu-id="fd4bf-146">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-146">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="fd4bf-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fd4bf-147">-Tag</span></span>
<span data-ttu-id="fd4bf-148">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fd4bf-149">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="fd4bf-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd4bf-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd4bf-150">-Confirm</span></span>
<span data-ttu-id="fd4bf-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd4bf-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd4bf-152">-WhatIf</span></span>
<span data-ttu-id="fd4bf-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd4bf-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd4bf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd4bf-155">CommonParameters</span></span>
<span data-ttu-id="fd4bf-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd4bf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd4bf-157">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd4bf-157">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd4bf-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd4bf-158">INPUTS</span></span>

### <span data-ttu-id="fd4bf-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fd4bf-159">System.String</span></span>

### <span data-ttu-id="fd4bf-160">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="fd4bf-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="fd4bf-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fd4bf-161">System.Int32</span></span>

### <span data-ttu-id="fd4bf-162">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="fd4bf-162">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fd4bf-163">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="fd4bf-163">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="fd4bf-164">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd4bf-164">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd4bf-165">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="fd4bf-165">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="fd4bf-166">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="fd4bf-166">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="fd4bf-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd4bf-167">OUTPUTS</span></span>

### <span data-ttu-id="fd4bf-168">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="fd4bf-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="fd4bf-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd4bf-169">NOTES</span></span>

## <span data-ttu-id="fd4bf-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd4bf-170">RELATED LINKS</span></span>
