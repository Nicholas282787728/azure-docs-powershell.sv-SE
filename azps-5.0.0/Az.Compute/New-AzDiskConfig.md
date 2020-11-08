---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269478"
---
# <span data-ttu-id="5dbd2-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="5dbd2-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="5dbd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5dbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbd2-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="5dbd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5dbd2-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dbd2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5dbd2-105">DESCRIPTION</span></span>
<span data-ttu-id="5dbd2-106">Cmdleten **New-AzDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="5dbd2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5dbd2-107">EXAMPLES</span></span>

### <span data-ttu-id="5dbd2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5dbd2-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="5dbd2-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="5dbd2-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="5dbd2-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="5dbd2-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5dbd2-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5dbd2-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5dbd2-113">Example 2</span></span>
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

<span data-ttu-id="5dbd2-114">Det första kommandot skapar ett lokalt disk objekt för uppladdning.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="5dbd2-115">Det andra kommandot tar disk objekt och skapar en disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5dbd2-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="5dbd2-116">Det tredje kommandot får SAS-URL: en för disken.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="5dbd2-117">Det fjärde kommandot får diskens status.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="5dbd2-118">Om disk tillståndet är ' ReadyToUpload ' kan en användare ladda upp en disk från Blob Storage till URL-adressen för SAS med AzCopy.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="5dbd2-119">Vid uppladdningen ändras disk tillståndet till ' ActiveUpload '.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="5dbd2-120">Med kommandot senaste återkallas disk åtkomst för SAS-URL: en.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="5dbd2-121">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="5dbd2-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="5dbd2-122">Skapa en disk från en bild version av ett delat Galleri.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="5dbd2-123">ID är ID för den delade galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="5dbd2-124">LUN behövs endast om källan är en data disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="5dbd2-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5dbd2-125">PARAMETERS</span></span>

### <span data-ttu-id="5dbd2-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="5dbd2-126">-CreateOption</span></span>
<span data-ttu-id="5dbd2-127">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="5dbd2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbd2-128">-DefaultProfile</span></span>
<span data-ttu-id="5dbd2-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dbd2-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="5dbd2-130">-DiskAccessId</span></span>
<span data-ttu-id="5dbd2-131">Hämtar eller anger ARM-ID för DiskAccess-resursen för användning av privata slut punkter på.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="5dbd2-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5dbd2-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="5dbd2-133">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-133">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="5dbd2-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="5dbd2-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="5dbd2-135">Anger resurs-ID för den disk krypterings uppsättning som ska användas för att aktivera kryptering på rest.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="5dbd2-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="5dbd2-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="5dbd2-137">Totalt antal IOPS som kommer att tillåtas för alla virtuella datorer som monterar den delade disken som ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5dbd2-138">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-138">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd2-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="5dbd2-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="5dbd2-140">Antalet IOPS som är tillåtna för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5dbd2-141">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-141">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd2-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="5dbd2-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="5dbd2-143">"Beskrivning": "det totala genomflödet (MBps) som kommer att tillåtas för alla virtuella datorer monterar den delade disken som ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5dbd2-144">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd2-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="5dbd2-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="5dbd2-146">Bandbredd som tillåts för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5dbd2-147">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd2-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5dbd2-148">-DiskSizeGB</span></span>
<span data-ttu-id="5dbd2-149">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-149">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="5dbd2-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="5dbd2-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="5dbd2-151">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-151">Enable encryption settings.</span></span>

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

### <span data-ttu-id="5dbd2-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="5dbd2-152">-EncryptionType</span></span>
<span data-ttu-id="5dbd2-153">Den typ av nycklar som används för att kryptera diskens data.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="5dbd2-154">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="5dbd2-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="5dbd2-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="5dbd2-155">-GalleryImageReference</span></span>
<span data-ttu-id="5dbd2-156">GalleryImageReference-objektet.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="5dbd2-157">Krävs om du skapar från en galleri bild.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="5dbd2-158">ID: t är ARM-ID för den version av delad text som du kan skapa en disk från.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="5dbd2-159">Ett LUN behövs om källan till kopian är en av data diskarna i galleriet. om det är null kopieras bildens OS-disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="5dbd2-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="5dbd2-160">-HyperVGeneration</span></span>
<span data-ttu-id="5dbd2-161">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="5dbd2-162">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="5dbd2-163">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="5dbd2-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="5dbd2-164">-ImageReference</span></span>
<span data-ttu-id="5dbd2-165">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-165">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="5dbd2-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5dbd2-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="5dbd2-167">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-167">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="5dbd2-168">-Plats</span><span class="sxs-lookup"><span data-stu-id="5dbd2-168">-Location</span></span>
<span data-ttu-id="5dbd2-169">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-169">Specifies a location.</span></span>

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

### <span data-ttu-id="5dbd2-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="5dbd2-170">-LogicalSectorSize</span></span>
<span data-ttu-id="5dbd2-171">Logisk sektor storlek i byte för Ultra disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="5dbd2-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="5dbd2-172">-MaxSharesCount</span></span>
<span data-ttu-id="5dbd2-173">Maximalt antal virtuella datorer som kan ansluta till disken samtidigt.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="5dbd2-174">Värdet större än en anger en disk som kan monteras på flera virtuella datorer samtidigt.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="5dbd2-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5dbd2-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="5dbd2-176">Nätverks åtkomst princip definierar nätverks åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="5dbd2-177">Möjliga värden är: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="5dbd2-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="5dbd2-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="5dbd2-178">-OsType</span></span>
<span data-ttu-id="5dbd2-179">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-179">Specifies the OS type.</span></span>

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

### <span data-ttu-id="5dbd2-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5dbd2-180">-SkuName</span></span>
<span data-ttu-id="5dbd2-181">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="5dbd2-182">Tillgängliga värden är Standard_LRS, Premium_LRS, StandardSSD_LRS och UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="5dbd2-183">UltraSSD_LRS kan endast användas med ett tomt värde för CreateOption-parametern.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="5dbd2-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="5dbd2-184">-SourceResourceId</span></span>
<span data-ttu-id="5dbd2-185">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="5dbd2-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="5dbd2-186">-SourceUri</span></span>
<span data-ttu-id="5dbd2-187">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="5dbd2-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5dbd2-188">-StorageAccountId</span></span>
<span data-ttu-id="5dbd2-189">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="5dbd2-190">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5dbd2-190">-Tag</span></span>
<span data-ttu-id="5dbd2-191">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5dbd2-192">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="5dbd2-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5dbd2-193">-Tier</span><span class="sxs-lookup"><span data-stu-id="5dbd2-193">-Tier</span></span>
<span data-ttu-id="5dbd2-194">Diskens prestanda nivå.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="5dbd2-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5dbd2-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="5dbd2-196">Anger storleken på överföringen inklusive VHD-foten när CreateOption är laddat upp.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="5dbd2-197">Det här värdet bör vara mellan 20972032 (20 MiB + 512 byte för VHD-foten) och 35183298347520 byte (32 TiB + 512-byte för VHD-foten).</span><span class="sxs-lookup"><span data-stu-id="5dbd2-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbd2-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="5dbd2-198">-Zone</span></span>
<span data-ttu-id="5dbd2-199">Anger listan med logiska zoner för disk.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-199">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="5dbd2-200">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5dbd2-200">-Confirm</span></span>
<span data-ttu-id="5dbd2-201">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dbd2-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dbd2-202">-WhatIf</span></span>
<span data-ttu-id="5dbd2-203">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5dbd2-204">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dbd2-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbd2-205">CommonParameters</span></span>
<span data-ttu-id="5dbd2-206">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dbd2-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbd2-207">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5dbd2-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbd2-208">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5dbd2-208">INPUTS</span></span>

### <span data-ttu-id="5dbd2-209">System. String</span><span class="sxs-lookup"><span data-stu-id="5dbd2-209">System.String</span></span>

### <span data-ttu-id="5dbd2-210">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5dbd2-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5dbd2-211">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5dbd2-211">System.Int32</span></span>

### <span data-ttu-id="5dbd2-212">System. string []</span><span class="sxs-lookup"><span data-stu-id="5dbd2-212">System.String[]</span></span>

### <span data-ttu-id="5dbd2-213">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5dbd2-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5dbd2-214">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="5dbd2-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="5dbd2-215">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5dbd2-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5dbd2-216">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="5dbd2-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="5dbd2-217">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="5dbd2-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="5dbd2-218">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5dbd2-218">OUTPUTS</span></span>

### <span data-ttu-id="5dbd2-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="5dbd2-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="5dbd2-220">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5dbd2-220">NOTES</span></span>

## <span data-ttu-id="5dbd2-221">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5dbd2-221">RELATED LINKS</span></span>
