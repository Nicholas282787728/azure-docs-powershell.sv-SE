---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 02255fd8fd4db5747c820755bfd46ee3251aab9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573715"
---
# <span data-ttu-id="15693-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="15693-101">New-AzureRmImage</span></span>

## <span data-ttu-id="15693-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15693-102">SYNOPSIS</span></span>
<span data-ttu-id="15693-103">Skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="15693-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15693-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15693-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15693-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15693-105">DESCRIPTION</span></span>
<span data-ttu-id="15693-106">**New-AzureRmImage-** cmdleten skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="15693-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="15693-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15693-107">EXAMPLES</span></span>

### <span data-ttu-id="15693-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="15693-108">Example 1</span></span>
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

<span data-ttu-id="15693-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="15693-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="15693-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="15693-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="15693-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="15693-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="15693-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="15693-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="15693-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="15693-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="15693-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="15693-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="15693-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15693-115">PARAMETERS</span></span>

### <span data-ttu-id="15693-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15693-116">-DefaultProfile</span></span>
<span data-ttu-id="15693-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15693-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15693-118">-Image</span><span class="sxs-lookup"><span data-stu-id="15693-118">-Image</span></span>
<span data-ttu-id="15693-119">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="15693-119">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15693-120">-ImageName</span><span class="sxs-lookup"><span data-stu-id="15693-120">-ImageName</span></span>
<span data-ttu-id="15693-121">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="15693-121">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15693-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15693-122">-ResourceGroupName</span></span>
<span data-ttu-id="15693-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="15693-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15693-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="15693-124">-Confirm</span></span>
<span data-ttu-id="15693-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="15693-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15693-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15693-126">-WhatIf</span></span>
<span data-ttu-id="15693-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="15693-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15693-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="15693-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15693-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15693-129">CommonParameters</span></span>
<span data-ttu-id="15693-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15693-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15693-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15693-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15693-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15693-132">INPUTS</span></span>

### <span data-ttu-id="15693-133">System. String</span><span class="sxs-lookup"><span data-stu-id="15693-133">System.String</span></span>
<span data-ttu-id="15693-134">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="15693-134">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="15693-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15693-135">OUTPUTS</span></span>

### <span data-ttu-id="15693-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="15693-136">System.Object</span></span>

## <span data-ttu-id="15693-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15693-137">NOTES</span></span>

## <span data-ttu-id="15693-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15693-138">RELATED LINKS</span></span>

