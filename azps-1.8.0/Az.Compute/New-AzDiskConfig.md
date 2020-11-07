---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 273a4388665e12cf58d1fe2d7e067648862bf4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754549"
---
# <span data-ttu-id="f6924-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="f6924-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="f6924-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6924-102">SYNOPSIS</span></span>
<span data-ttu-id="f6924-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="f6924-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="f6924-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6924-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6924-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6924-105">DESCRIPTION</span></span>
<span data-ttu-id="f6924-106">Cmdleten **New-AzDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="f6924-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="f6924-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6924-107">EXAMPLES</span></span>

### <span data-ttu-id="f6924-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6924-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="f6924-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f6924-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="f6924-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="f6924-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="f6924-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="f6924-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="f6924-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f6924-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f6924-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f6924-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="f6924-114">Det första kommandot skapar ett lokalt disk objekt för uppladdning.</span><span class="sxs-lookup"><span data-stu-id="f6924-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="f6924-115">Det andra kommandot tar disk objekt och skapar en disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f6924-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="f6924-116">Det tredje kommandot får SAS-URL: en för disken.</span><span class="sxs-lookup"><span data-stu-id="f6924-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="f6924-117">Det fjärde kommandot får diskens status.</span><span class="sxs-lookup"><span data-stu-id="f6924-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="f6924-118">Om disk tillståndet är ' ReadyToUpload ' kan en användare ladda upp en disk från Blob Storage till URL-adressen för SAS med AzCopy.</span><span class="sxs-lookup"><span data-stu-id="f6924-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="f6924-119">Vid uppladdningen ändras disk tillståndet till ' ActiveUpload '.</span><span class="sxs-lookup"><span data-stu-id="f6924-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="f6924-120">Med kommandot senaste återkallas disk åtkomst för SAS-URL: en.</span><span class="sxs-lookup"><span data-stu-id="f6924-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="f6924-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6924-121">PARAMETERS</span></span>

### <span data-ttu-id="f6924-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="f6924-122">-CreateOption</span></span>
<span data-ttu-id="f6924-123">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="f6924-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="f6924-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6924-124">-DefaultProfile</span></span>
<span data-ttu-id="f6924-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6924-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6924-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f6924-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="f6924-127">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="f6924-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="f6924-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6924-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="f6924-129">Antalet IOPS som är tillåtna för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="f6924-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="f6924-130">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="f6924-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="f6924-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="f6924-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="f6924-132">Bandbredd som tillåts för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="f6924-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="f6924-133">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="f6924-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="f6924-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f6924-134">-DiskSizeGB</span></span>
<span data-ttu-id="f6924-135">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="f6924-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="f6924-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="f6924-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="f6924-137">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="f6924-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="f6924-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="f6924-138">-HyperVGeneration</span></span>
<span data-ttu-id="f6924-139">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="f6924-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="f6924-140">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="f6924-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="f6924-141">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="f6924-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="f6924-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="f6924-142">-ImageReference</span></span>
<span data-ttu-id="f6924-143">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="f6924-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="f6924-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f6924-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="f6924-145">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="f6924-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="f6924-146">-Plats</span><span class="sxs-lookup"><span data-stu-id="f6924-146">-Location</span></span>
<span data-ttu-id="f6924-147">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="f6924-147">Specifies a location.</span></span>

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

### <span data-ttu-id="f6924-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="f6924-148">-OsType</span></span>
<span data-ttu-id="f6924-149">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="f6924-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f6924-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f6924-150">-SkuName</span></span>
<span data-ttu-id="f6924-151">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="f6924-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="f6924-152">Tillgängliga värden är Standard_LRS, Premium_LRS, StandardSSD_LRS och UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="f6924-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="f6924-153">UltraSSD_LRS kan endast användas med ett tomt värde för CreateOption-parametern.</span><span class="sxs-lookup"><span data-stu-id="f6924-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="f6924-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f6924-154">-SourceResourceId</span></span>
<span data-ttu-id="f6924-155">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f6924-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="f6924-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="f6924-156">-SourceUri</span></span>
<span data-ttu-id="f6924-157">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="f6924-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="f6924-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f6924-158">-StorageAccountId</span></span>
<span data-ttu-id="f6924-159">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f6924-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="f6924-160">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f6924-160">-Tag</span></span>
<span data-ttu-id="f6924-161">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f6924-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f6924-162">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="f6924-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f6924-163">-Zone</span><span class="sxs-lookup"><span data-stu-id="f6924-163">-Zone</span></span>
<span data-ttu-id="f6924-164">Anger listan med logiska zoner för disk.</span><span class="sxs-lookup"><span data-stu-id="f6924-164">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="f6924-165">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6924-165">-Confirm</span></span>
<span data-ttu-id="f6924-166">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6924-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6924-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6924-167">-WhatIf</span></span>
<span data-ttu-id="f6924-168">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6924-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6924-169">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6924-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6924-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6924-170">CommonParameters</span></span>
<span data-ttu-id="f6924-171">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6924-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6924-172">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6924-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6924-173">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6924-173">INPUTS</span></span>

### <span data-ttu-id="f6924-174">System. String</span><span class="sxs-lookup"><span data-stu-id="f6924-174">System.String</span></span>

### <span data-ttu-id="f6924-175">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f6924-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f6924-176">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6924-176">System.Int32</span></span>

### <span data-ttu-id="f6924-177">System. string []</span><span class="sxs-lookup"><span data-stu-id="f6924-177">System.String[]</span></span>

### <span data-ttu-id="f6924-178">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="f6924-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f6924-179">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="f6924-179">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="f6924-180">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f6924-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f6924-181">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="f6924-181">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="f6924-182">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="f6924-182">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="f6924-183">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6924-183">OUTPUTS</span></span>

### <span data-ttu-id="f6924-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="f6924-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="f6924-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6924-185">NOTES</span></span>

## <span data-ttu-id="f6924-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6924-186">RELATED LINKS</span></span>
