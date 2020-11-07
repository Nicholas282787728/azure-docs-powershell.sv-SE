---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: f7f2a9ee7119b54722862b3796e9a5372b9b1d09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754542"
---
# <span data-ttu-id="096fe-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="096fe-101">New-AzImageConfig</span></span>

## <span data-ttu-id="096fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="096fe-102">SYNOPSIS</span></span>
<span data-ttu-id="096fe-103">Skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="096fe-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="096fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="096fe-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="096fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="096fe-105">DESCRIPTION</span></span>
<span data-ttu-id="096fe-106">**New-AzImageConfig-** cmdleten skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="096fe-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="096fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="096fe-107">EXAMPLES</span></span>

### <span data-ttu-id="096fe-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="096fe-108">Example 1</span></span>
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

<span data-ttu-id="096fe-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="096fe-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="096fe-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="096fe-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="096fe-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="096fe-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="096fe-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="096fe-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="096fe-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="096fe-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="096fe-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="096fe-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="096fe-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="096fe-115">PARAMETERS</span></span>

### <span data-ttu-id="096fe-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="096fe-116">-DataDisk</span></span>
<span data-ttu-id="096fe-117">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="096fe-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="096fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096fe-118">-DefaultProfile</span></span>
<span data-ttu-id="096fe-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="096fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="096fe-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="096fe-120">-Location</span></span>
<span data-ttu-id="096fe-121">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="096fe-121">Specifies a location.</span></span>

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

### <span data-ttu-id="096fe-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="096fe-122">-OsDisk</span></span>
<span data-ttu-id="096fe-123">Anger operativ systemets disk.</span><span class="sxs-lookup"><span data-stu-id="096fe-123">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="096fe-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="096fe-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="096fe-125">Anger ID för den virtuella käll datorn.</span><span class="sxs-lookup"><span data-stu-id="096fe-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="096fe-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="096fe-126">-Tag</span></span>
<span data-ttu-id="096fe-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="096fe-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="096fe-128">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="096fe-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="096fe-129">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="096fe-129">-ZoneResilient</span></span>
<span data-ttu-id="096fe-130">Aktivera zon elastisk</span><span class="sxs-lookup"><span data-stu-id="096fe-130">Enable zone resilient</span></span>

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

### <span data-ttu-id="096fe-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="096fe-131">-Confirm</span></span>
<span data-ttu-id="096fe-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="096fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="096fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="096fe-133">-WhatIf</span></span>
<span data-ttu-id="096fe-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="096fe-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="096fe-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="096fe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="096fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096fe-136">CommonParameters</span></span>
<span data-ttu-id="096fe-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="096fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096fe-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096fe-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="096fe-139">INPUTS</span></span>

### <span data-ttu-id="096fe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="096fe-140">System.String</span></span>

### <span data-ttu-id="096fe-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="096fe-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="096fe-142">Microsoft. Azure. Management. Compute. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="096fe-142">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="096fe-143">Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="096fe-143">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="096fe-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="096fe-144">OUTPUTS</span></span>

### <span data-ttu-id="096fe-145">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="096fe-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="096fe-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="096fe-146">NOTES</span></span>

## <span data-ttu-id="096fe-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="096fe-147">RELATED LINKS</span></span>
