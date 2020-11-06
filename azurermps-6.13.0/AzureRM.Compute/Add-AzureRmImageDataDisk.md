---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmImageDataDisk.md
ms.openlocfilehash: fddf20c748591f339ffa3cf66f3aba4a189ec3db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578931"
---
# <span data-ttu-id="ad775-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="ad775-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="ad775-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad775-102">SYNOPSIS</span></span>
<span data-ttu-id="ad775-103">Lägger till en datadisk till ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="ad775-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad775-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad775-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad775-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad775-105">DESCRIPTION</span></span>
<span data-ttu-id="ad775-106">Cmdleten **Add-AzureRmImageDataDisk** lägger till en datadisk till ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="ad775-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="ad775-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad775-107">EXAMPLES</span></span>

### <span data-ttu-id="ad775-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ad775-108">Example 1</span></span>
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

<span data-ttu-id="ad775-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="ad775-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="ad775-110">Med nästa tre kommandon kopplas sökvägar till operativ system diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="ad775-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="ad775-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="ad775-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="ad775-112">Nästa tre kommandon alla lägger till en operativ system disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="ad775-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="ad775-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="ad775-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="ad775-114">Med kommandot slut skapas en bild med namnet ImageName01 i resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ad775-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="ad775-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad775-115">PARAMETERS</span></span>

### <span data-ttu-id="ad775-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="ad775-116">-BlobUri</span></span>
<span data-ttu-id="ad775-117">Anger länken, som en URI, för blobben.</span><span class="sxs-lookup"><span data-stu-id="ad775-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad775-118">-Cachning</span><span class="sxs-lookup"><span data-stu-id="ad775-118">-Caching</span></span>
<span data-ttu-id="ad775-119">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="ad775-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad775-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad775-120">-DefaultProfile</span></span>
<span data-ttu-id="ad775-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad775-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad775-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ad775-122">-DiskSizeGB</span></span>
<span data-ttu-id="ad775-123">Anger storleken på disken i GB (gigabyte).</span><span class="sxs-lookup"><span data-stu-id="ad775-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="ad775-124">-Image</span><span class="sxs-lookup"><span data-stu-id="ad775-124">-Image</span></span>
<span data-ttu-id="ad775-125">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="ad775-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="ad775-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="ad775-126">-Lun</span></span>
<span data-ttu-id="ad775-127">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="ad775-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad775-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="ad775-128">-ManagedDiskId</span></span>
<span data-ttu-id="ad775-129">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="ad775-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="ad775-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="ad775-130">-SnapshotId</span></span>
<span data-ttu-id="ad775-131">Anger ID för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="ad775-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="ad775-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ad775-132">-StorageAccountType</span></span>
<span data-ttu-id="ad775-133">Lagrings konto typen för data avbildnings disken</span><span class="sxs-lookup"><span data-stu-id="ad775-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="ad775-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ad775-134">-Confirm</span></span>
<span data-ttu-id="ad775-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ad775-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad775-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad775-136">-WhatIf</span></span>
<span data-ttu-id="ad775-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ad775-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad775-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ad775-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad775-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad775-139">CommonParameters</span></span>
<span data-ttu-id="ad775-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad775-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad775-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad775-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad775-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad775-142">INPUTS</span></span>

### <span data-ttu-id="ad775-143">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ad775-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="ad775-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad775-144">System.Int32</span></span>

### <span data-ttu-id="ad775-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ad775-145">System.String</span></span>

### <span data-ttu-id="ad775-146">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 21.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ad775-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="ad775-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad775-147">OUTPUTS</span></span>

### <span data-ttu-id="ad775-148">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="ad775-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="ad775-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad775-149">NOTES</span></span>

## <span data-ttu-id="ad775-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad775-150">RELATED LINKS</span></span>
