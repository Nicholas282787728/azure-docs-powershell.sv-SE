---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: c76ccab31b3c5c11216a1a929e2a78df55713325
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745095"
---
# <span data-ttu-id="5321a-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="5321a-101">New-AzImageConfig</span></span>

## <span data-ttu-id="5321a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5321a-102">SYNOPSIS</span></span>
<span data-ttu-id="5321a-103">Skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="5321a-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="5321a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5321a-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5321a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5321a-105">DESCRIPTION</span></span>
<span data-ttu-id="5321a-106">**New-AzImageConfig-** cmdleten skapar ett konfigurerbart bild objekt.</span><span class="sxs-lookup"><span data-stu-id="5321a-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="5321a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5321a-107">EXAMPLES</span></span>

### <span data-ttu-id="5321a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5321a-108">Example 1</span></span>
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

<span data-ttu-id="5321a-109">Det första kommandot skapar ett bild objekt och lagrar det sedan i $imageConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="5321a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="5321a-110">Nästa tre kommandon tilldelar sökvägar till OS-diskar och två data diskar till $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2 variabler.</span><span class="sxs-lookup"><span data-stu-id="5321a-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="5321a-111">Den här metoden är endast för läsbarhet av följande kommandon.</span><span class="sxs-lookup"><span data-stu-id="5321a-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="5321a-112">Nästa tre kommandon alla lägger till en OS-disk och två data diskar i den bild som lagras i $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="5321a-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="5321a-113">URI: n för varje disk lagras i $osDiskVhdUri, $dataDiskVhdUri 1 och $dataDiskVhdUri 2.</span><span class="sxs-lookup"><span data-stu-id="5321a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="5321a-114">Med kommandot slut skapas en bild med namnet "ImageName01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5321a-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5321a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5321a-115">PARAMETERS</span></span>

### <span data-ttu-id="5321a-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="5321a-116">-DataDisk</span></span>
<span data-ttu-id="5321a-117">Anger data diskens objekt.</span><span class="sxs-lookup"><span data-stu-id="5321a-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="5321a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5321a-118">-DefaultProfile</span></span>
<span data-ttu-id="5321a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5321a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5321a-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="5321a-120">-HyperVGeneration</span></span>
<span data-ttu-id="5321a-121">Anger HyperVGeneration-typen för den virtuella dator som skapades från avbildningen.</span><span class="sxs-lookup"><span data-stu-id="5321a-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="5321a-122">Tillåtna värden är v1 och v2.</span><span class="sxs-lookup"><span data-stu-id="5321a-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="5321a-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="5321a-123">-Location</span></span>
<span data-ttu-id="5321a-124">Anger en plats.</span><span class="sxs-lookup"><span data-stu-id="5321a-124">Specifies a location.</span></span>

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

### <span data-ttu-id="5321a-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="5321a-125">-OsDisk</span></span>
<span data-ttu-id="5321a-126">Anger operativ systemets disk.</span><span class="sxs-lookup"><span data-stu-id="5321a-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="5321a-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5321a-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="5321a-128">Anger ID för den virtuella käll datorn.</span><span class="sxs-lookup"><span data-stu-id="5321a-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="5321a-129">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5321a-129">-Tag</span></span>
<span data-ttu-id="5321a-130">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="5321a-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5321a-131">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="5321a-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5321a-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="5321a-132">-ZoneResilient</span></span>
<span data-ttu-id="5321a-133">Aktivera zon elastisk</span><span class="sxs-lookup"><span data-stu-id="5321a-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="5321a-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5321a-134">-Confirm</span></span>
<span data-ttu-id="5321a-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5321a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5321a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5321a-136">-WhatIf</span></span>
<span data-ttu-id="5321a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5321a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5321a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5321a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5321a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5321a-139">CommonParameters</span></span>
<span data-ttu-id="5321a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5321a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5321a-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5321a-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5321a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5321a-142">INPUTS</span></span>

### <span data-ttu-id="5321a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5321a-143">System.String</span></span>

### <span data-ttu-id="5321a-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5321a-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5321a-145">Microsoft. Azure. Management. Compute. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="5321a-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="5321a-146">Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="5321a-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="5321a-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5321a-147">OUTPUTS</span></span>

### <span data-ttu-id="5321a-148">Microsoft. Azure. commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="5321a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="5321a-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5321a-149">NOTES</span></span>

## <span data-ttu-id="5321a-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5321a-150">RELATED LINKS</span></span>
