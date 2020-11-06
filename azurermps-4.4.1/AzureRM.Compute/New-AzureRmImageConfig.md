---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: a18fe089cba54f6cbf0d70469a17f2d8f797b2e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573714"
---
# <span data-ttu-id="c4433-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="c4433-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="c4433-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4433-102">SYNOPSIS</span></span>
<span data-ttu-id="c4433-103">Skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="c4433-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4433-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4433-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4433-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4433-105">DESCRIPTION</span></span>
<span data-ttu-id="c4433-106">**New-AzureRmImageConfig-** cmdleten skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="c4433-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="c4433-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4433-107">EXAMPLES</span></span>

### <span data-ttu-id="c4433-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4433-108">Example 1</span></span>
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

<span data-ttu-id="c4433-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="c4433-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="c4433-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="c4433-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="c4433-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="c4433-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="c4433-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="c4433-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c4433-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="c4433-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="c4433-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c4433-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c4433-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4433-115">PARAMETERS</span></span>

### <span data-ttu-id="c4433-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="c4433-116">-DataDisk</span></span>
<span data-ttu-id="c4433-117">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="c4433-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4433-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4433-118">-DefaultProfile</span></span>
<span data-ttu-id="c4433-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4433-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4433-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="c4433-120">-Location</span></span>
<span data-ttu-id="c4433-121">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="c4433-121">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4433-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="c4433-122">-OsDisk</span></span>
<span data-ttu-id="c4433-123">Anger operativ systemets disk.</span><span class="sxs-lookup"><span data-stu-id="c4433-123">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4433-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c4433-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="c4433-125">Anger ID för den virtuella käll datorn.</span><span class="sxs-lookup"><span data-stu-id="c4433-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="c4433-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c4433-126">-Tag</span></span>
<span data-ttu-id="c4433-127">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="c4433-127">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4433-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4433-128">-Confirm</span></span>
<span data-ttu-id="c4433-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4433-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4433-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4433-130">-WhatIf</span></span>
<span data-ttu-id="c4433-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4433-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4433-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4433-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4433-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4433-133">CommonParameters</span></span>
<span data-ttu-id="c4433-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4433-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4433-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4433-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4433-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4433-136">INPUTS</span></span>

### <span data-ttu-id="c4433-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c4433-137">System.String</span></span>
<span data-ttu-id="c4433-138">System. Collection. hash Microsoft. Azure. Management. Compute. Models. ImageOSDisk Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="c4433-138">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="c4433-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4433-139">OUTPUTS</span></span>

### <span data-ttu-id="c4433-140">Microsoft. Azure. Management. Compute. Models. image</span><span class="sxs-lookup"><span data-stu-id="c4433-140">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="c4433-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4433-141">NOTES</span></span>

## <span data-ttu-id="c4433-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4433-142">RELATED LINKS</span></span>

