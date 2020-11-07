---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756233"
---
# <span data-ttu-id="a282e-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a282e-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="a282e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a282e-102">SYNOPSIS</span></span>
<span data-ttu-id="a282e-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="a282e-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a282e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a282e-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a282e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a282e-105">DESCRIPTION</span></span>
<span data-ttu-id="a282e-106">Cmdleten **New-AzureRmDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="a282e-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="a282e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a282e-107">EXAMPLES</span></span>

### <span data-ttu-id="a282e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a282e-108">Example 1</span></span>
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

<span data-ttu-id="a282e-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a282e-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="a282e-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="a282e-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="a282e-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="a282e-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="a282e-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="a282e-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a282e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a282e-113">PARAMETERS</span></span>

### <span data-ttu-id="a282e-114">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a282e-114">-CreateOption</span></span>
<span data-ttu-id="a282e-115">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="a282e-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a282e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a282e-116">-DefaultProfile</span></span>
<span data-ttu-id="a282e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a282e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a282e-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a282e-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="a282e-119">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="a282e-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="a282e-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="a282e-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="a282e-121">Antalet IOPS som är tillåtna för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="a282e-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a282e-122">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="a282e-122">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a282e-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="a282e-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="a282e-124">Bandbredd som tillåts för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="a282e-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="a282e-125">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="a282e-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a282e-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a282e-126">-DiskSizeGB</span></span>
<span data-ttu-id="a282e-127">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="a282e-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a282e-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a282e-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a282e-129">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="a282e-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a282e-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a282e-130">-ImageReference</span></span>
<span data-ttu-id="a282e-131">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="a282e-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="a282e-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a282e-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="a282e-133">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="a282e-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="a282e-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="a282e-134">-Location</span></span>
<span data-ttu-id="a282e-135">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="a282e-135">Specifies a location.</span></span>

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

### <span data-ttu-id="a282e-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="a282e-136">-OsType</span></span>
<span data-ttu-id="a282e-137">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="a282e-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a282e-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a282e-138">-SkuName</span></span>
<span data-ttu-id="a282e-139">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="a282e-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="a282e-140">Tillgängliga värden är Standard_LRS, Premium_LRS, StandardSSD_LRS och UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="a282e-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="a282e-141">UltraSSD_LRS kan endast användas med ett tomt värde för CreateOption-parametern.</span><span class="sxs-lookup"><span data-stu-id="a282e-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="a282e-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a282e-142">-SourceResourceId</span></span>
<span data-ttu-id="a282e-143">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a282e-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="a282e-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a282e-144">-SourceUri</span></span>
<span data-ttu-id="a282e-145">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="a282e-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a282e-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a282e-146">-StorageAccountId</span></span>
<span data-ttu-id="a282e-147">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="a282e-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a282e-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a282e-148">-Tag</span></span>
<span data-ttu-id="a282e-149">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="a282e-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a282e-150">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="a282e-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a282e-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="a282e-151">-Zone</span></span>
<span data-ttu-id="a282e-152">Anger listan med logiska zoner för disk.</span><span class="sxs-lookup"><span data-stu-id="a282e-152">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a282e-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a282e-153">-Confirm</span></span>
<span data-ttu-id="a282e-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a282e-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a282e-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a282e-155">-WhatIf</span></span>
<span data-ttu-id="a282e-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a282e-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a282e-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a282e-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a282e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a282e-158">CommonParameters</span></span>
<span data-ttu-id="a282e-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a282e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a282e-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a282e-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a282e-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a282e-161">INPUTS</span></span>

### <span data-ttu-id="a282e-162">System. String</span><span class="sxs-lookup"><span data-stu-id="a282e-162">System.String</span></span>

### <span data-ttu-id="a282e-163">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a282e-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a282e-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a282e-164">System.Int32</span></span>

### <span data-ttu-id="a282e-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="a282e-165">System.String[]</span></span>

### <span data-ttu-id="a282e-166">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a282e-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a282e-167">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="a282e-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="a282e-168">System. Nullable ' 1 [[system. Boolean, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a282e-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a282e-169">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="a282e-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a282e-170">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a282e-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a282e-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a282e-171">OUTPUTS</span></span>

### <span data-ttu-id="a282e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="a282e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="a282e-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a282e-173">NOTES</span></span>

## <span data-ttu-id="a282e-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a282e-174">RELATED LINKS</span></span>
