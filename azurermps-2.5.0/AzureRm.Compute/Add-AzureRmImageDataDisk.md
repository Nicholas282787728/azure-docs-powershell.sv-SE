---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b4412cb85534d1aae780b16450726920921d811e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929129"
---
# <span data-ttu-id="2a20b-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="2a20b-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="2a20b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a20b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a20b-103">Lägger till en datadisk till ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="2a20b-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a20b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a20b-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a20b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a20b-105">DESCRIPTION</span></span>
<span data-ttu-id="2a20b-106">Cmdleten **Add-AzureRmImageDataDisk** lägger till en datadisk till ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="2a20b-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="2a20b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a20b-107">EXAMPLES</span></span>

### <span data-ttu-id="2a20b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2a20b-108">Example 1</span></span>
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

<span data-ttu-id="2a20b-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="2a20b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="2a20b-110">Med nästa tre kommandon kopplas sökvägar till operativ system diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="2a20b-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="2a20b-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="2a20b-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="2a20b-112">Nästa tre kommandon alla lägger till en operativ system disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="2a20b-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="2a20b-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="2a20b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="2a20b-114">Med kommandot slut skapas en bild med namnet ImageName01 i resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2a20b-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="2a20b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a20b-115">PARAMETERS</span></span>

### <span data-ttu-id="2a20b-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="2a20b-116">-BlobUri</span></span>
<span data-ttu-id="2a20b-117">Anger länken, som en URI, för blobben.</span><span class="sxs-lookup"><span data-stu-id="2a20b-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a20b-118">-Cachning</span><span class="sxs-lookup"><span data-stu-id="2a20b-118">-Caching</span></span>
<span data-ttu-id="2a20b-119">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="2a20b-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a20b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a20b-120">-DefaultProfile</span></span>
<span data-ttu-id="2a20b-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a20b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a20b-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2a20b-122">-DiskSizeGB</span></span>
<span data-ttu-id="2a20b-123">Anger storleken på disken i GB (gigabyte).</span><span class="sxs-lookup"><span data-stu-id="2a20b-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="2a20b-124">-Image</span><span class="sxs-lookup"><span data-stu-id="2a20b-124">-Image</span></span>
<span data-ttu-id="2a20b-125">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="2a20b-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a20b-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="2a20b-126">-Lun</span></span>
<span data-ttu-id="2a20b-127">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="2a20b-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a20b-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="2a20b-128">-ManagedDiskId</span></span>
<span data-ttu-id="2a20b-129">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="2a20b-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="2a20b-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="2a20b-130">-SnapshotId</span></span>
<span data-ttu-id="2a20b-131">Anger ID för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="2a20b-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="2a20b-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2a20b-132">-StorageAccountType</span></span>
<span data-ttu-id="2a20b-133">Lagrings konto typen för data avbildnings disken</span><span class="sxs-lookup"><span data-stu-id="2a20b-133">The Storage Account type of the data image disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a20b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2a20b-134">-Confirm</span></span>
<span data-ttu-id="2a20b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2a20b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a20b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a20b-136">-WhatIf</span></span>
<span data-ttu-id="2a20b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2a20b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a20b-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2a20b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a20b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a20b-139">CommonParameters</span></span>
<span data-ttu-id="2a20b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a20b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a20b-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a20b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a20b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a20b-142">INPUTS</span></span>

### <span data-ttu-id="2a20b-143">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="2a20b-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="2a20b-144">System. Int32 system. String system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2a20b-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2a20b-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a20b-145">OUTPUTS</span></span>

### <span data-ttu-id="2a20b-146">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="2a20b-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="2a20b-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a20b-147">NOTES</span></span>

## <span data-ttu-id="2a20b-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a20b-148">RELATED LINKS</span></span>

