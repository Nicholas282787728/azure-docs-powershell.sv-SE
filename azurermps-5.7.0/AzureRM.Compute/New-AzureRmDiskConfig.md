---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: b2c922a1dcce683636d61b68c66ab8cfb82535c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576611"
---
# <span data-ttu-id="7087f-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="7087f-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="7087f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7087f-102">SYNOPSIS</span></span>
<span data-ttu-id="7087f-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="7087f-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7087f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7087f-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [-SkuName <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7087f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7087f-105">DESCRIPTION</span></span>
<span data-ttu-id="7087f-106">Cmdleten **New-AzureRmDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="7087f-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="7087f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7087f-107">EXAMPLES</span></span>

### <span data-ttu-id="7087f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7087f-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="7087f-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7087f-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="7087f-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="7087f-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="7087f-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="7087f-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="7087f-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7087f-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7087f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7087f-113">PARAMETERS</span></span>

### <span data-ttu-id="7087f-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="7087f-114">-CreateOption</span></span>
<span data-ttu-id="7087f-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="7087f-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="7087f-116">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7087f-116">-DiskEncryptionKey</span></span>
<span data-ttu-id="7087f-117">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="7087f-117">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="7087f-118">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="7087f-118">-DiskSizeGB</span></span>
<span data-ttu-id="7087f-119">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="7087f-119">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="7087f-120">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="7087f-120">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="7087f-121">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="7087f-121">Enable encryption settings.</span></span>

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

### <span data-ttu-id="7087f-122">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="7087f-122">-ImageReference</span></span>
<span data-ttu-id="7087f-123">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="7087f-123">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="7087f-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="7087f-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="7087f-125">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="7087f-125">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="7087f-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="7087f-126">-Location</span></span>
<span data-ttu-id="7087f-127">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="7087f-127">Specifies a location.</span></span>

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

### <span data-ttu-id="7087f-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="7087f-128">-OsType</span></span>
<span data-ttu-id="7087f-129">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="7087f-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="7087f-130">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7087f-130">-SkuName</span></span>
<span data-ttu-id="7087f-131">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="7087f-131">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="7087f-132">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7087f-132">-SourceResourceId</span></span>
<span data-ttu-id="7087f-133">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="7087f-133">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="7087f-134">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="7087f-134">-SourceUri</span></span>
<span data-ttu-id="7087f-135">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="7087f-135">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="7087f-136">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7087f-136">-StorageAccountId</span></span>
<span data-ttu-id="7087f-137">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="7087f-137">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="7087f-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7087f-138">-Tag</span></span>
<span data-ttu-id="7087f-139">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="7087f-139">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="7087f-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7087f-140">-Confirm</span></span>
<span data-ttu-id="7087f-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7087f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7087f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7087f-142">-WhatIf</span></span>
<span data-ttu-id="7087f-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7087f-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7087f-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7087f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7087f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7087f-145">CommonParameters</span></span>
<span data-ttu-id="7087f-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7087f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7087f-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7087f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7087f-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7087f-148">INPUTS</span></span>

### <span data-ttu-id="7087f-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7087f-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="7087f-150">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] system. String system. Collections. hash-system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]] Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="7087f-150">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="7087f-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7087f-151">OUTPUTS</span></span>

### <span data-ttu-id="7087f-152">Microsoft. Azure. Management. Compute. Models. disk</span><span class="sxs-lookup"><span data-stu-id="7087f-152">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="7087f-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7087f-153">NOTES</span></span>

## <span data-ttu-id="7087f-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7087f-154">RELATED LINKS</span></span>

