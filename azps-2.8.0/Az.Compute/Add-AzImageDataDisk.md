---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 5b3ea899b7cd1b5868fd3f230358a75e92ec1d3e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745257"
---
# <span data-ttu-id="053f2-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="053f2-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="053f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="053f2-102">SYNOPSIS</span></span>
<span data-ttu-id="053f2-103">Lägger till en datadisk till ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="053f2-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="053f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="053f2-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="053f2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="053f2-105">DESCRIPTION</span></span>
<span data-ttu-id="053f2-106">Cmdleten **Add-AzImageDataDisk** lägger till en datadisk till ett bild objekt.</span><span class="sxs-lookup"><span data-stu-id="053f2-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="053f2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="053f2-107">EXAMPLES</span></span>

### <span data-ttu-id="053f2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="053f2-108">Example 1</span></span>
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

<span data-ttu-id="053f2-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="053f2-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="053f2-110">Med nästa tre kommandon kopplas sökvägar till operativ system diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="053f2-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="053f2-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="053f2-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="053f2-112">Nästa tre kommandon alla lägger till en operativ system disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="053f2-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="053f2-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="053f2-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="053f2-114">Med kommandot slut skapas en bild med namnet ImageName01 i resurs grupp ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="053f2-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="053f2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="053f2-115">PARAMETERS</span></span>

### <span data-ttu-id="053f2-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="053f2-116">-BlobUri</span></span>
<span data-ttu-id="053f2-117">Anger länken, som en URI, för blobben.</span><span class="sxs-lookup"><span data-stu-id="053f2-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="053f2-118">-Cachning</span><span class="sxs-lookup"><span data-stu-id="053f2-118">-Caching</span></span>
<span data-ttu-id="053f2-119">Anger diskens cacheläge.</span><span class="sxs-lookup"><span data-stu-id="053f2-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="053f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="053f2-120">-DefaultProfile</span></span>
<span data-ttu-id="053f2-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="053f2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="053f2-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="053f2-122">-DiskSizeGB</span></span>
<span data-ttu-id="053f2-123">Anger storleken på disken i GB (gigabyte).</span><span class="sxs-lookup"><span data-stu-id="053f2-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="053f2-124">-Image</span><span class="sxs-lookup"><span data-stu-id="053f2-124">-Image</span></span>
<span data-ttu-id="053f2-125">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="053f2-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="053f2-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="053f2-126">-Lun</span></span>
<span data-ttu-id="053f2-127">Anger LUN (Logical Unit Number).</span><span class="sxs-lookup"><span data-stu-id="053f2-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="053f2-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="053f2-128">-ManagedDiskId</span></span>
<span data-ttu-id="053f2-129">Anger ID för en hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="053f2-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="053f2-130">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="053f2-130">-SnapshotId</span></span>
<span data-ttu-id="053f2-131">Anger ID för en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="053f2-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="053f2-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="053f2-132">-StorageAccountType</span></span>
<span data-ttu-id="053f2-133">Lagrings konto typen för data avbildnings disken</span><span class="sxs-lookup"><span data-stu-id="053f2-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="053f2-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="053f2-134">-Confirm</span></span>
<span data-ttu-id="053f2-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="053f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="053f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="053f2-136">-WhatIf</span></span>
<span data-ttu-id="053f2-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="053f2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="053f2-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="053f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="053f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="053f2-139">CommonParameters</span></span>
<span data-ttu-id="053f2-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="053f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="053f2-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="053f2-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="053f2-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="053f2-142">INPUTS</span></span>

### <span data-ttu-id="053f2-143">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="053f2-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="053f2-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="053f2-144">System.Int32</span></span>

### <span data-ttu-id="053f2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="053f2-145">System.String</span></span>

### <span data-ttu-id="053f2-146">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="053f2-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="053f2-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="053f2-147">OUTPUTS</span></span>

### <span data-ttu-id="053f2-148">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="053f2-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="053f2-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="053f2-149">NOTES</span></span>

## <span data-ttu-id="053f2-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="053f2-150">RELATED LINKS</span></span>
