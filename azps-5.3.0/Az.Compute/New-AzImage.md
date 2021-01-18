---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImage.md
ms.openlocfilehash: ff291afae70636863dff8ce34b5610cd77ce1251
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526883"
---
# <span data-ttu-id="853d7-101">New-AzImage</span><span class="sxs-lookup"><span data-stu-id="853d7-101">New-AzImage</span></span>

## <span data-ttu-id="853d7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="853d7-102">SYNOPSIS</span></span>
<span data-ttu-id="853d7-103">Skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="853d7-103">Creates an image.</span></span>

## <span data-ttu-id="853d7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="853d7-104">SYNTAX</span></span>

```
New-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="853d7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="853d7-105">DESCRIPTION</span></span>
<span data-ttu-id="853d7-106">**New-AzImage-** cmdleten skapar en bild.</span><span class="sxs-lookup"><span data-stu-id="853d7-106">The **New-AzImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="853d7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="853d7-107">EXAMPLES</span></span>

### <span data-ttu-id="853d7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="853d7-108">Example 1</span></span>
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

<span data-ttu-id="853d7-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="853d7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="853d7-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="853d7-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="853d7-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="853d7-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="853d7-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="853d7-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="853d7-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="853d7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="853d7-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="853d7-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="853d7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="853d7-115">PARAMETERS</span></span>

### <span data-ttu-id="853d7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="853d7-116">-AsJob</span></span>
<span data-ttu-id="853d7-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="853d7-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="853d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="853d7-118">-DefaultProfile</span></span>
<span data-ttu-id="853d7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="853d7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="853d7-120">-Image</span><span class="sxs-lookup"><span data-stu-id="853d7-120">-Image</span></span>
<span data-ttu-id="853d7-121">Anger ett lokalt bild objekt.</span><span class="sxs-lookup"><span data-stu-id="853d7-121">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="853d7-122">-ImageName</span><span class="sxs-lookup"><span data-stu-id="853d7-122">-ImageName</span></span>
<span data-ttu-id="853d7-123">Anger namnet på en bild.</span><span class="sxs-lookup"><span data-stu-id="853d7-123">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="853d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="853d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="853d7-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="853d7-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="853d7-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="853d7-126">-Confirm</span></span>
<span data-ttu-id="853d7-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="853d7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="853d7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="853d7-128">-WhatIf</span></span>
<span data-ttu-id="853d7-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="853d7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="853d7-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="853d7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="853d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="853d7-131">CommonParameters</span></span>
<span data-ttu-id="853d7-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="853d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="853d7-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="853d7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="853d7-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="853d7-134">INPUTS</span></span>

### <span data-ttu-id="853d7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="853d7-135">System.String</span></span>

### <span data-ttu-id="853d7-136">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="853d7-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="853d7-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="853d7-137">OUTPUTS</span></span>

### <span data-ttu-id="853d7-138">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="853d7-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="853d7-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="853d7-139">NOTES</span></span>

## <span data-ttu-id="853d7-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="853d7-140">RELATED LINKS</span></span>
