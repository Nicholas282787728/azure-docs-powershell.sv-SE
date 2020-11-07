---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929101"
---
# <span data-ttu-id="e81f7-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="e81f7-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="e81f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e81f7-102">SYNOPSIS</span></span>
<span data-ttu-id="e81f7-103">Skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="e81f7-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e81f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e81f7-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e81f7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e81f7-105">DESCRIPTION</span></span>
<span data-ttu-id="e81f7-106">**New-AzureRmImageConfig-** cmdleten skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="e81f7-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="e81f7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e81f7-107">EXAMPLES</span></span>

### <span data-ttu-id="e81f7-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e81f7-108">Example 1</span></span>
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

<span data-ttu-id="e81f7-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="e81f7-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="e81f7-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="e81f7-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="e81f7-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="e81f7-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="e81f7-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="e81f7-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="e81f7-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="e81f7-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="e81f7-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e81f7-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e81f7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e81f7-115">PARAMETERS</span></span>

### <span data-ttu-id="e81f7-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="e81f7-116">-DataDisk</span></span>
<span data-ttu-id="e81f7-117">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="e81f7-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81f7-118">-DefaultProfile</span></span>
<span data-ttu-id="e81f7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e81f7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e81f7-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="e81f7-120">-Location</span></span>
<span data-ttu-id="e81f7-121">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="e81f7-121">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f7-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="e81f7-122">-OsDisk</span></span>
<span data-ttu-id="e81f7-123">Anger operativ systemets disk.</span><span class="sxs-lookup"><span data-stu-id="e81f7-123">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f7-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e81f7-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="e81f7-125">Anger ID för den virtuella käll datorn.</span><span class="sxs-lookup"><span data-stu-id="e81f7-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="e81f7-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e81f7-126">-Tag</span></span>
<span data-ttu-id="e81f7-127">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="e81f7-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e81f7-128">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e81f7-128">For example:</span></span>

<span data-ttu-id="e81f7-129">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e81f7-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81f7-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e81f7-130">-Confirm</span></span>
<span data-ttu-id="e81f7-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e81f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81f7-132">-WhatIf</span></span>
<span data-ttu-id="e81f7-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e81f7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e81f7-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e81f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81f7-135">CommonParameters</span></span>
<span data-ttu-id="e81f7-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81f7-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81f7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81f7-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e81f7-138">INPUTS</span></span>

### <span data-ttu-id="e81f7-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="e81f7-139">None</span></span>
<span data-ttu-id="e81f7-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e81f7-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e81f7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e81f7-141">OUTPUTS</span></span>

### <span data-ttu-id="e81f7-142">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="e81f7-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="e81f7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e81f7-143">NOTES</span></span>

## <span data-ttu-id="e81f7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e81f7-144">RELATED LINKS</span></span>

