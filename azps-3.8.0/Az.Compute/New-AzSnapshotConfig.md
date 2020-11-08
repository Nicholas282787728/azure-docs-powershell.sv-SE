---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 2989a5be6ef6eee137f296ab1379931070082fe9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926418"
---
# <span data-ttu-id="790a2-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="790a2-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="790a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="790a2-102">SYNOPSIS</span></span>
<span data-ttu-id="790a2-103">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="790a2-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="790a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="790a2-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="790a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="790a2-105">DESCRIPTION</span></span>
<span data-ttu-id="790a2-106">**New-AzSnapshotConfig-** cmdleten skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="790a2-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="790a2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="790a2-107">EXAMPLES</span></span>

### <span data-ttu-id="790a2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="790a2-108">Example 1</span></span>
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

<span data-ttu-id="790a2-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="790a2-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="790a2-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="790a2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="790a2-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="790a2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="790a2-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="790a2-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="790a2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="790a2-113">PARAMETERS</span></span>

### <span data-ttu-id="790a2-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="790a2-114">-CreateOption</span></span>
<span data-ttu-id="790a2-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="790a2-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="790a2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790a2-116">-DefaultProfile</span></span>
<span data-ttu-id="790a2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="790a2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="790a2-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="790a2-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="790a2-119">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="790a2-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="790a2-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="790a2-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="790a2-121">Anger resurs-ID för den disk krypterings uppsättning som ska användas för att aktivera kryptering på rest.</span><span class="sxs-lookup"><span data-stu-id="790a2-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="790a2-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="790a2-122">-DiskSizeGB</span></span>
<span data-ttu-id="790a2-123">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="790a2-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="790a2-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="790a2-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="790a2-125">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="790a2-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="790a2-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="790a2-126">-EncryptionType</span></span>
<span data-ttu-id="790a2-127">Den typ av nycklar som används för att kryptera diskens data.</span><span class="sxs-lookup"><span data-stu-id="790a2-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="790a2-128">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="790a2-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="790a2-129">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="790a2-129">-HyperVGeneration</span></span>
<span data-ttu-id="790a2-130">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="790a2-130">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="790a2-131">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="790a2-131">Applicable to OS disks only.</span></span>  <span data-ttu-id="790a2-132">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="790a2-132">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="790a2-133">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="790a2-133">-ImageReference</span></span>
<span data-ttu-id="790a2-134">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="790a2-134">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="790a2-135">-Inkrementellt</span><span class="sxs-lookup"><span data-stu-id="790a2-135">-Incremental</span></span>
<span data-ttu-id="790a2-136">Anger en stegvis ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="790a2-136">Specifies an incremental snapshot.</span></span> <span data-ttu-id="790a2-137">Inkrementella ögonblicks bilder på samma disk tar mindre plats än fullständiga stillbilder och kan omräknas.</span><span class="sxs-lookup"><span data-stu-id="790a2-137">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="790a2-138">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="790a2-138">-KeyEncryptionKey</span></span>
<span data-ttu-id="790a2-139">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="790a2-139">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="790a2-140">-Plats</span><span class="sxs-lookup"><span data-stu-id="790a2-140">-Location</span></span>
<span data-ttu-id="790a2-141">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="790a2-141">Specifies a location.</span></span>

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

### <span data-ttu-id="790a2-142">-OsType</span><span class="sxs-lookup"><span data-stu-id="790a2-142">-OsType</span></span>
<span data-ttu-id="790a2-143">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="790a2-143">Specifies the OS type.</span></span>

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

### <span data-ttu-id="790a2-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="790a2-144">-SkuName</span></span>
<span data-ttu-id="790a2-145">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="790a2-145">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="790a2-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="790a2-146">-SourceResourceId</span></span>
<span data-ttu-id="790a2-147">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="790a2-147">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="790a2-148">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="790a2-148">-SourceUri</span></span>
<span data-ttu-id="790a2-149">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="790a2-149">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="790a2-150">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="790a2-150">-StorageAccountId</span></span>
<span data-ttu-id="790a2-151">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="790a2-151">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="790a2-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="790a2-152">-Tag</span></span>
<span data-ttu-id="790a2-153">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="790a2-153">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="790a2-154">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="790a2-154">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="790a2-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="790a2-155">-Confirm</span></span>
<span data-ttu-id="790a2-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="790a2-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="790a2-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="790a2-157">-WhatIf</span></span>
<span data-ttu-id="790a2-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="790a2-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="790a2-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="790a2-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="790a2-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790a2-160">CommonParameters</span></span>
<span data-ttu-id="790a2-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="790a2-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790a2-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="790a2-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790a2-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="790a2-163">INPUTS</span></span>

### <span data-ttu-id="790a2-164">System. String</span><span class="sxs-lookup"><span data-stu-id="790a2-164">System.String</span></span>

### <span data-ttu-id="790a2-165">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="790a2-165">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="790a2-166">System. Int32</span><span class="sxs-lookup"><span data-stu-id="790a2-166">System.Int32</span></span>

### <span data-ttu-id="790a2-167">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="790a2-167">System.Collections.Hashtable</span></span>

### <span data-ttu-id="790a2-168">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="790a2-168">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="790a2-169">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="790a2-169">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="790a2-170">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="790a2-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="790a2-171">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="790a2-171">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="790a2-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="790a2-172">OUTPUTS</span></span>

### <span data-ttu-id="790a2-173">Microsoft. Azure. commands. Compute. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="790a2-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="790a2-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="790a2-174">NOTES</span></span>

## <span data-ttu-id="790a2-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="790a2-175">RELATED LINKS</span></span>