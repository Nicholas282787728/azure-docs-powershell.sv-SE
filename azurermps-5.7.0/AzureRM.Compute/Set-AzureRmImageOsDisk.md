---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmImageOsDisk.md
ms.openlocfilehash: 8deb191a6a26e4fb0001a1cbb78540460256dd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573528"
---
# <span data-ttu-id="805d2-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="805d2-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="805d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="805d2-102">SYNOPSIS</span></span>
<span data-ttu-id="805d2-103">Ställer in disk egenskaper för operativ systemet på ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="805d2-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="805d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="805d2-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <Image> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="805d2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="805d2-105">DESCRIPTION</span></span>
<span data-ttu-id="805d2-106">Cmdleten **set-AzureRmImageOsDisk** anger operativ systemets disk egenskaper för ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="805d2-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="805d2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="805d2-107">EXAMPLES</span></span>

### <span data-ttu-id="805d2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="805d2-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="805d2-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="805d2-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="805d2-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="805d2-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="805d2-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="805d2-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="805d2-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="805d2-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="805d2-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="805d2-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="805d2-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="805d2-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="805d2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="805d2-115">PARAMETERS</span></span>

### <span data-ttu-id="805d2-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="805d2-116">-BlobUri</span></span>
<span data-ttu-id="805d2-117">Anger BLOB-URI.</span><span class="sxs-lookup"><span data-stu-id="805d2-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="805d2-118">-Cachning</span><span class="sxs-lookup"><span data-stu-id="805d2-118">-Caching</span></span>
<span data-ttu-id="805d2-119">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="805d2-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805d2-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="805d2-120">-DiskSizeGB</span></span>
<span data-ttu-id="805d2-121">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="805d2-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805d2-122">-Image</span><span class="sxs-lookup"><span data-stu-id="805d2-122">-Image</span></span>
<span data-ttu-id="805d2-123">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="805d2-123">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="805d2-124">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="805d2-124">-ManagedDiskId</span></span>
<span data-ttu-id="805d2-125">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="805d2-125">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="805d2-126">-OsState</span><span class="sxs-lookup"><span data-stu-id="805d2-126">-OsState</span></span>
<span data-ttu-id="805d2-127">Anger OS-tillståndet.</span><span class="sxs-lookup"><span data-stu-id="805d2-127">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805d2-128">-OsType</span><span class="sxs-lookup"><span data-stu-id="805d2-128">-OsType</span></span>
<span data-ttu-id="805d2-129">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="805d2-129">Specifies the OS type.</span></span>

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

### <span data-ttu-id="805d2-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="805d2-130">-SnapshotId</span></span>
<span data-ttu-id="805d2-131">Anger ID för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="805d2-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="805d2-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="805d2-132">-StorageAccountType</span></span>
<span data-ttu-id="805d2-133">Lagrings konto typen för OS-bildskivan</span><span class="sxs-lookup"><span data-stu-id="805d2-133">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="805d2-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="805d2-134">-Confirm</span></span>
<span data-ttu-id="805d2-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="805d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="805d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805d2-136">-WhatIf</span></span>
<span data-ttu-id="805d2-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="805d2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="805d2-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="805d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="805d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805d2-139">CommonParameters</span></span>
<span data-ttu-id="805d2-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="805d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805d2-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805d2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805d2-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="805d2-142">INPUTS</span></span>

### <span data-ttu-id="805d2-143">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="805d2-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="805d2-144">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] system. String system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="805d2-144">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="805d2-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="805d2-145">OUTPUTS</span></span>

### <span data-ttu-id="805d2-146">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="805d2-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="805d2-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="805d2-147">NOTES</span></span>

## <span data-ttu-id="805d2-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="805d2-148">RELATED LINKS</span></span>

