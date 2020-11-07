---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: ee3dd849a8f3877ac19ce86a7257d28fc18575c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755985"
---
# <span data-ttu-id="cf826-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cf826-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="cf826-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf826-102">SYNOPSIS</span></span>
<span data-ttu-id="cf826-103">Skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="cf826-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf826-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf826-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf826-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf826-105">DESCRIPTION</span></span>
<span data-ttu-id="cf826-106">**New-AzureRmSnapshotConfig-** cmdleten skapar ett konfigurerbart SnapShot-objekt.</span><span class="sxs-lookup"><span data-stu-id="cf826-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="cf826-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf826-107">EXAMPLES</span></span>

### <span data-ttu-id="cf826-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cf826-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="cf826-109">Det första kommandot skapar ett lokalt tomt SnapShot-objekt med storleks 5GB i Standard_LRS lagrings konto typ.</span><span class="sxs-lookup"><span data-stu-id="cf826-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="cf826-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="cf826-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="cf826-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar för krypterings nycklar för objektet ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cf826-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="cf826-112">Det sista kommandot tar ett SnapShot-objekt och skapar en fixering med namnet "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="cf826-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="cf826-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf826-113">PARAMETERS</span></span>

### <span data-ttu-id="cf826-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="cf826-114">-CreateOption</span></span>
<span data-ttu-id="cf826-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="cf826-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy, Restore

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cf826-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="cf826-117">Anger disk krypterings nyckelvärdet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cf826-117">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cf826-118">-DiskSizeGB</span></span>
<span data-ttu-id="cf826-119">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="cf826-119">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="cf826-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="cf826-121">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="cf826-121">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="cf826-122">-ImageReference</span></span>
<span data-ttu-id="cf826-123">Anger bild referensen för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cf826-123">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="cf826-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="cf826-125">Anger Key Encryption Key för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="cf826-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="cf826-126">-Location</span></span>
<span data-ttu-id="cf826-127">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="cf826-127">Specifies a location.</span></span>

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

### <span data-ttu-id="cf826-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="cf826-128">-OsType</span></span>
<span data-ttu-id="cf826-129">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="cf826-129">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="cf826-130">-SkuName</span></span>
<span data-ttu-id="cf826-131">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="cf826-131">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="cf826-132">-SourceResourceId</span></span>
<span data-ttu-id="cf826-133">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="cf826-133">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="cf826-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="cf826-134">-SourceUri</span></span>
<span data-ttu-id="cf826-135">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="cf826-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="cf826-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cf826-136">-StorageAccountId</span></span>
<span data-ttu-id="cf826-137">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="cf826-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="cf826-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cf826-138">-Tag</span></span>
<span data-ttu-id="cf826-139">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="cf826-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf826-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cf826-140">-Confirm</span></span>
<span data-ttu-id="cf826-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cf826-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf826-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf826-142">-WhatIf</span></span>
<span data-ttu-id="cf826-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cf826-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf826-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cf826-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf826-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf826-145">CommonParameters</span></span>
<span data-ttu-id="cf826-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf826-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf826-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf826-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf826-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf826-148">INPUTS</span></span>

### <span data-ttu-id="cf826-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cf826-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="cf826-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String system. Collections. hash-system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="cf826-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="cf826-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf826-151">OUTPUTS</span></span>

### <span data-ttu-id="cf826-152">Microsoft. Azure. Management. Compute. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="cf826-152">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="cf826-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf826-153">NOTES</span></span>

## <span data-ttu-id="cf826-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf826-154">RELATED LINKS</span></span>
