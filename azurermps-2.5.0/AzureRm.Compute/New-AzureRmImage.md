---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimage
schema: 2.0.0
ms.openlocfilehash: 0a03126be62c528d0879eaff093d6a3969802ce5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929105"
---
# <span data-ttu-id="b0b79-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="b0b79-101">New-AzureRmImage</span></span>

## <span data-ttu-id="b0b79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b0b79-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b79-103">Skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="b0b79-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0b79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b0b79-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b0b79-105">DESCRIPTION</span></span>
<span data-ttu-id="b0b79-106">**New-AzureRmImage-** cmdleten skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="b0b79-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="b0b79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b0b79-107">EXAMPLES</span></span>

### <span data-ttu-id="b0b79-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b0b79-108">Example 1</span></span>
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

<span data-ttu-id="b0b79-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="b0b79-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="b0b79-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="b0b79-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="b0b79-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="b0b79-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="b0b79-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="b0b79-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="b0b79-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="b0b79-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="b0b79-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b0b79-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b0b79-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b0b79-115">PARAMETERS</span></span>

### <span data-ttu-id="b0b79-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0b79-116">-AsJob</span></span>
<span data-ttu-id="b0b79-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b0b79-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b79-118">-DefaultProfile</span></span>
<span data-ttu-id="b0b79-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b0b79-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0b79-120">-Image</span><span class="sxs-lookup"><span data-stu-id="b0b79-120">-Image</span></span>
<span data-ttu-id="b0b79-121">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="b0b79-121">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b79-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b0b79-122">-ImageName</span></span>
<span data-ttu-id="b0b79-123">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="b0b79-123">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="b0b79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b79-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0b79-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b0b79-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b0b79-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b0b79-126">-Confirm</span></span>
<span data-ttu-id="b0b79-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b0b79-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b79-128">-WhatIf</span></span>
<span data-ttu-id="b0b79-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b0b79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0b79-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b0b79-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b79-131">CommonParameters</span></span>
<span data-ttu-id="b0b79-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b79-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b79-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b79-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b0b79-134">INPUTS</span></span>

### <span data-ttu-id="b0b79-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b0b79-135">System.String</span></span>
<span data-ttu-id="b0b79-136">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b0b79-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b0b79-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b0b79-137">OUTPUTS</span></span>

### <span data-ttu-id="b0b79-138">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b0b79-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="b0b79-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="b0b79-139">System.Object</span></span>

## <span data-ttu-id="b0b79-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b0b79-140">NOTES</span></span>

## <span data-ttu-id="b0b79-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b0b79-141">RELATED LINKS</span></span>

