---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 44df831ce0f8e6454607e4f0956906466ebc9f39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754479"
---
# <span data-ttu-id="f6633-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="f6633-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="f6633-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6633-102">SYNOPSIS</span></span>
<span data-ttu-id="f6633-103">Ställer in disk egenskaper för operativ systemet på ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="f6633-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="f6633-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6633-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6633-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6633-105">DESCRIPTION</span></span>
<span data-ttu-id="f6633-106">Cmdleten **set-AzImageOsDisk** anger operativ systemets disk egenskaper för ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="f6633-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="f6633-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6633-107">EXAMPLES</span></span>

### <span data-ttu-id="f6633-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6633-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="f6633-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="f6633-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="f6633-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="f6633-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="f6633-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="f6633-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="f6633-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="f6633-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="f6633-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="f6633-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="f6633-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f6633-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f6633-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6633-115">PARAMETERS</span></span>

### <span data-ttu-id="f6633-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="f6633-116">-BlobUri</span></span>
<span data-ttu-id="f6633-117">Anger BLOB-URI.</span><span class="sxs-lookup"><span data-stu-id="f6633-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="f6633-118">-Cachning</span><span class="sxs-lookup"><span data-stu-id="f6633-118">-Caching</span></span>
<span data-ttu-id="f6633-119">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="f6633-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6633-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6633-120">-DefaultProfile</span></span>
<span data-ttu-id="f6633-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6633-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6633-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f6633-122">-DiskSizeGB</span></span>
<span data-ttu-id="f6633-123">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="f6633-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="f6633-124">-Image</span><span class="sxs-lookup"><span data-stu-id="f6633-124">-Image</span></span>
<span data-ttu-id="f6633-125">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="f6633-125">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6633-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f6633-126">-ManagedDiskId</span></span>
<span data-ttu-id="f6633-127">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="f6633-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="f6633-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="f6633-128">-OsState</span></span>
<span data-ttu-id="f6633-129">Anger OS-tillståndet.</span><span class="sxs-lookup"><span data-stu-id="f6633-129">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6633-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="f6633-130">-OsType</span></span>
<span data-ttu-id="f6633-131">Anger OS-typen.</span><span class="sxs-lookup"><span data-stu-id="f6633-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="f6633-132">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f6633-132">-SnapshotId</span></span>
<span data-ttu-id="f6633-133">Anger ID för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="f6633-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="f6633-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f6633-134">-StorageAccountType</span></span>
<span data-ttu-id="f6633-135">Lagrings konto typen för OS-bildskivan</span><span class="sxs-lookup"><span data-stu-id="f6633-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="f6633-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6633-136">-Confirm</span></span>
<span data-ttu-id="f6633-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6633-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6633-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6633-138">-WhatIf</span></span>
<span data-ttu-id="f6633-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6633-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6633-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6633-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6633-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6633-141">CommonParameters</span></span>
<span data-ttu-id="f6633-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6633-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6633-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6633-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6633-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6633-144">INPUTS</span></span>

### <span data-ttu-id="f6633-145">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="f6633-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="f6633-146">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f6633-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f6633-147">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f6633-147">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f6633-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f6633-148">System.String</span></span>

### <span data-ttu-id="f6633-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="f6633-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="f6633-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f6633-150">System.Int32</span></span>

## <span data-ttu-id="f6633-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6633-151">OUTPUTS</span></span>

### <span data-ttu-id="f6633-152">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="f6633-152">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="f6633-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6633-153">NOTES</span></span>

## <span data-ttu-id="f6633-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6633-154">RELATED LINKS</span></span>