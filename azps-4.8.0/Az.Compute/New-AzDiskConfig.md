---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 4e2e09597cc52431657001e20ca34ad6e77aa40f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260830"
---
# <span data-ttu-id="b6a21-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b6a21-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="b6a21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6a21-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a21-103">Skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="b6a21-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="b6a21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6a21-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a21-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6a21-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a21-106">Cmdleten **New-AzDiskConfig** skapar ett konfigurerbart disk objekt.</span><span class="sxs-lookup"><span data-stu-id="b6a21-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="b6a21-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6a21-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a21-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b6a21-108">Example 1</span></span>
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

<span data-ttu-id="b6a21-109">Med det första kommandot skapas ett lokalt tomt disk objekt med storleken 5GB Standard_LRS lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b6a21-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="b6a21-110">Den anger också Windows OS-typ och aktiverar krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="b6a21-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="b6a21-111">Med det andra och tredje kommandot anges inställningarna för disk krypterings nycklar och nycklar krypterings nycklar för serviceobjektet.</span><span class="sxs-lookup"><span data-stu-id="b6a21-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="b6a21-112">Med det senaste kommandot tas serviceobjektet emot och en disk skapas med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b6a21-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b6a21-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b6a21-113">Example 2</span></span>
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

<span data-ttu-id="b6a21-114">Det första kommandot skapar ett lokalt disk objekt för uppladdning.</span><span class="sxs-lookup"><span data-stu-id="b6a21-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="b6a21-115">Det andra kommandot tar disk objekt och skapar en disk med namnet "Disk01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b6a21-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="b6a21-116">Det tredje kommandot får SAS-URL: en för disken.</span><span class="sxs-lookup"><span data-stu-id="b6a21-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="b6a21-117">Det fjärde kommandot får diskens status.</span><span class="sxs-lookup"><span data-stu-id="b6a21-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="b6a21-118">Om disk tillståndet är ' ReadyToUpload ' kan en användare ladda upp en disk från Blob Storage till URL-adressen för SAS med AzCopy.</span><span class="sxs-lookup"><span data-stu-id="b6a21-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="b6a21-119">Vid uppladdningen ändras disk tillståndet till ' ActiveUpload '.</span><span class="sxs-lookup"><span data-stu-id="b6a21-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="b6a21-120">Med kommandot senaste återkallas disk åtkomst för SAS-URL: en.</span><span class="sxs-lookup"><span data-stu-id="b6a21-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="b6a21-121">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="b6a21-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="b6a21-122">Skapa en disk från en bild version av ett delat Galleri.</span><span class="sxs-lookup"><span data-stu-id="b6a21-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="b6a21-123">ID är ID för den delade galleri bild versionen.</span><span class="sxs-lookup"><span data-stu-id="b6a21-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="b6a21-124">LUN behövs endast om källan är en data disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="b6a21-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6a21-125">PARAMETERS</span></span>

### <span data-ttu-id="b6a21-126">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b6a21-126">-CreateOption</span></span>
<span data-ttu-id="b6a21-127">Anger om den här cmdleten skapar en disk på den virtuella datorn från en plattform eller användare, skapar en tom disk eller kopplar en befintlig disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="b6a21-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a21-128">-DefaultProfile</span></span>
<span data-ttu-id="b6a21-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a21-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a21-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b6a21-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="b6a21-131">Anger disk krypterings nyckelvärdet på en disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-131">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="b6a21-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b6a21-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b6a21-133">Anger resurs-ID för den disk krypterings uppsättning som ska användas för att aktivera kryptering på rest.</span><span class="sxs-lookup"><span data-stu-id="b6a21-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="b6a21-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="b6a21-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="b6a21-135">Totalt antal IOPS som kommer att tillåtas för alla virtuella datorer som monterar den delade disken som ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="b6a21-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="b6a21-136">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="b6a21-136">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="b6a21-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="b6a21-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="b6a21-138">Antalet IOPS som är tillåtna för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="b6a21-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="b6a21-139">En operation kan överföras mellan 4K och 256 000 byte.</span><span class="sxs-lookup"><span data-stu-id="b6a21-139">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="b6a21-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="b6a21-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="b6a21-141">"Beskrivning": "det totala genomflödet (MBps) som kommer att tillåtas för alla virtuella datorer monterar den delade disken som ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="b6a21-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="b6a21-142">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="b6a21-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="b6a21-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="b6a21-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="b6a21-144">Bandbredd som tillåts för denna disk; anges endast för UltraSSD-diskar.</span><span class="sxs-lookup"><span data-stu-id="b6a21-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="b6a21-145">MBps betyder miljon tals byte per sekund-MB här använder ISO-notationen med 10.</span><span class="sxs-lookup"><span data-stu-id="b6a21-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="b6a21-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b6a21-146">-DiskSizeGB</span></span>
<span data-ttu-id="b6a21-147">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="b6a21-147">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b6a21-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b6a21-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b6a21-149">Aktivera krypterings inställningar.</span><span class="sxs-lookup"><span data-stu-id="b6a21-149">Enable encryption settings.</span></span>

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

### <span data-ttu-id="b6a21-150">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="b6a21-150">-DiskAccessId</span></span>
<span data-ttu-id="b6a21-151">Hämtar eller anger ARM-ID för DiskAccess-resursen för användning av privata slut punkter på.</span><span class="sxs-lookup"><span data-stu-id="b6a21-151">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="b6a21-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b6a21-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="b6a21-153">Nätverks åtkomst princip definierar nätverks åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="b6a21-153">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="b6a21-154">Möjliga värden är: "AllowAll", "AllowPrivate", "DenyAll"</span><span class="sxs-lookup"><span data-stu-id="b6a21-154">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="b6a21-155">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="b6a21-155">-EncryptionType</span></span>
<span data-ttu-id="b6a21-156">Den typ av nycklar som används för att kryptera diskens data.</span><span class="sxs-lookup"><span data-stu-id="b6a21-156">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="b6a21-157">Tillgängliga värden är: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '</span><span class="sxs-lookup"><span data-stu-id="b6a21-157">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="b6a21-158">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="b6a21-158">-GalleryImageReference</span></span>
<span data-ttu-id="b6a21-159">GalleryImageReference-objektet.</span><span class="sxs-lookup"><span data-stu-id="b6a21-159">The GalleryImageReference object.</span></span>  <span data-ttu-id="b6a21-160">Krävs om du skapar från en galleri bild.</span><span class="sxs-lookup"><span data-stu-id="b6a21-160">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="b6a21-161">ID: t är ARM-ID för den version av delad text som du kan skapa en disk från.</span><span class="sxs-lookup"><span data-stu-id="b6a21-161">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="b6a21-162">Ett LUN behövs om källan till kopian är en av data diskarna i galleriet. om det är null kopieras bildens OS-disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-162">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="b6a21-163">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="b6a21-163">-HyperVGeneration</span></span>
<span data-ttu-id="b6a21-164">Hypervisor-generering av den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="b6a21-164">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="b6a21-165">Gäller endast för OS-diskar.</span><span class="sxs-lookup"><span data-stu-id="b6a21-165">Applicable to OS disks only.</span></span>  <span data-ttu-id="b6a21-166">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="b6a21-166">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="b6a21-167">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="b6a21-167">-ImageReference</span></span>
<span data-ttu-id="b6a21-168">Anger bild referensen på en disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-168">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="b6a21-169">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b6a21-169">-KeyEncryptionKey</span></span>
<span data-ttu-id="b6a21-170">Anger Key Encryption på en disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-170">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="b6a21-171">-Plats</span><span class="sxs-lookup"><span data-stu-id="b6a21-171">-Location</span></span>
<span data-ttu-id="b6a21-172">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="b6a21-172">Specifies a location.</span></span>

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

### <span data-ttu-id="b6a21-173">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="b6a21-173">-MaxSharesCount</span></span>
<span data-ttu-id="b6a21-174">Maximalt antal virtuella datorer som kan ansluta till disken samtidigt.</span><span class="sxs-lookup"><span data-stu-id="b6a21-174">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="b6a21-175">Värdet större än en anger en disk som kan monteras på flera virtuella datorer samtidigt.</span><span class="sxs-lookup"><span data-stu-id="b6a21-175">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="b6a21-176">-OsType</span><span class="sxs-lookup"><span data-stu-id="b6a21-176">-OsType</span></span>
<span data-ttu-id="b6a21-177">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="b6a21-177">Specifies the OS type.</span></span>

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

### <span data-ttu-id="b6a21-178">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b6a21-178">-SkuName</span></span>
<span data-ttu-id="b6a21-179">Anger lagrings kontots SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="b6a21-179">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="b6a21-180">Tillgängliga värden är Standard_LRS, Premium_LRS, StandardSSD_LRS och UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="b6a21-180">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="b6a21-181">UltraSSD_LRS kan endast användas med ett tomt värde för CreateOption-parametern.</span><span class="sxs-lookup"><span data-stu-id="b6a21-181">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="b6a21-182">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b6a21-182">-SourceResourceId</span></span>
<span data-ttu-id="b6a21-183">Anger käll resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="b6a21-183">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="b6a21-184">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b6a21-184">-SourceUri</span></span>
<span data-ttu-id="b6a21-185">Anger käll-URI.</span><span class="sxs-lookup"><span data-stu-id="b6a21-185">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="b6a21-186">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b6a21-186">-StorageAccountId</span></span>
<span data-ttu-id="b6a21-187">Anger ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="b6a21-187">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="b6a21-188">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b6a21-188">-Tag</span></span>
<span data-ttu-id="b6a21-189">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b6a21-189">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6a21-190">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="b6a21-190">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b6a21-191">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="b6a21-191">-UploadSizeInBytes</span></span>
<span data-ttu-id="b6a21-192">Anger storleken på överföringen inklusive VHD-foten när CreateOption är laddat upp.</span><span class="sxs-lookup"><span data-stu-id="b6a21-192">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="b6a21-193">Det här värdet bör vara mellan 20972032 (20 MiB + 512 byte för VHD-foten) och 35183298347520 byte (32 TiB + 512-byte för VHD-foten).</span><span class="sxs-lookup"><span data-stu-id="b6a21-193">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="b6a21-194">-Zone</span><span class="sxs-lookup"><span data-stu-id="b6a21-194">-Zone</span></span>
<span data-ttu-id="b6a21-195">Anger listan med logiska zoner för disk.</span><span class="sxs-lookup"><span data-stu-id="b6a21-195">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="b6a21-196">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b6a21-196">-Confirm</span></span>
<span data-ttu-id="b6a21-197">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b6a21-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6a21-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a21-198">-WhatIf</span></span>
<span data-ttu-id="b6a21-199">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b6a21-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6a21-200">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b6a21-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6a21-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a21-201">CommonParameters</span></span>
<span data-ttu-id="b6a21-202">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a21-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a21-203">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6a21-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a21-204">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6a21-204">INPUTS</span></span>

### <span data-ttu-id="b6a21-205">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a21-205">System.String</span></span>

### <span data-ttu-id="b6a21-206">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b6a21-206">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b6a21-207">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b6a21-207">System.Int32</span></span>

### <span data-ttu-id="b6a21-208">System. string []</span><span class="sxs-lookup"><span data-stu-id="b6a21-208">System.String[]</span></span>

### <span data-ttu-id="b6a21-209">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b6a21-209">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b6a21-210">Microsoft. Azure. Management. Compute. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="b6a21-210">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="b6a21-211">System. Nullable ' 1 [[system. Boolean, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b6a21-211">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b6a21-212">Microsoft. Azure. Management. Compute. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="b6a21-212">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="b6a21-213">Microsoft. Azure. Management. Compute. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="b6a21-213">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b6a21-214">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6a21-214">OUTPUTS</span></span>

### <span data-ttu-id="b6a21-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="b6a21-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="b6a21-216">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6a21-216">NOTES</span></span>

## <span data-ttu-id="b6a21-217">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6a21-217">RELATED LINKS</span></span>
