---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 5f723ea475ed909ee5445f3788386a2163af697d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755778"
---
# <span data-ttu-id="dc1de-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="dc1de-101">New-AzureRmImage</span></span>

## <span data-ttu-id="dc1de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc1de-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1de-103">Skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="dc1de-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc1de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc1de-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc1de-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc1de-105">DESCRIPTION</span></span>
<span data-ttu-id="dc1de-106">**New-AzureRmImage-** cmdleten skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="dc1de-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="dc1de-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc1de-107">EXAMPLES</span></span>

### <span data-ttu-id="dc1de-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc1de-108">Example 1</span></span>
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

<span data-ttu-id="dc1de-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="dc1de-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="dc1de-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="dc1de-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="dc1de-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="dc1de-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="dc1de-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="dc1de-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="dc1de-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="dc1de-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="dc1de-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="dc1de-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dc1de-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc1de-115">PARAMETERS</span></span>

### <span data-ttu-id="dc1de-116">-Image</span><span class="sxs-lookup"><span data-stu-id="dc1de-116">-Image</span></span>
<span data-ttu-id="dc1de-117">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="dc1de-117">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc1de-118">-ImageName</span><span class="sxs-lookup"><span data-stu-id="dc1de-118">-ImageName</span></span>
<span data-ttu-id="dc1de-119">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="dc1de-119">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc1de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1de-120">-ResourceGroupName</span></span>
<span data-ttu-id="dc1de-121">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="dc1de-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc1de-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc1de-122">-Confirm</span></span>
<span data-ttu-id="dc1de-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc1de-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc1de-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc1de-124">-WhatIf</span></span>
<span data-ttu-id="dc1de-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc1de-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc1de-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc1de-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc1de-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1de-127">CommonParameters</span></span>
<span data-ttu-id="dc1de-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1de-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1de-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1de-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1de-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc1de-130">INPUTS</span></span>

### <span data-ttu-id="dc1de-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dc1de-131">System.String</span></span>
<span data-ttu-id="dc1de-132">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="dc1de-132">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="dc1de-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc1de-133">OUTPUTS</span></span>

### <span data-ttu-id="dc1de-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="dc1de-134">System.Object</span></span>

## <span data-ttu-id="dc1de-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc1de-135">NOTES</span></span>

## <span data-ttu-id="dc1de-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc1de-136">RELATED LINKS</span></span>

