---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093170"
---
# <span data-ttu-id="a46a1-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a46a1-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="a46a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a46a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a46a1-103">Ställer in disk egenskaper för operativ systemet på en virtuell dator bild.</span><span class="sxs-lookup"><span data-stu-id="a46a1-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="a46a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a46a1-104">SYNTAX</span></span>

### <span data-ttu-id="a46a1-105">UpdateAzureVMImageParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a46a1-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a46a1-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="a46a1-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a46a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a46a1-107">DESCRIPTION</span></span>
<span data-ttu-id="a46a1-108">Cmdleten **set-AzureVMImageOSDiskConfig** anger operativ systemets disk egenskaper på en virtuell dator bild.</span><span class="sxs-lookup"><span data-stu-id="a46a1-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="a46a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a46a1-109">EXAMPLES</span></span>

### <span data-ttu-id="a46a1-110">Exempel 1: Ange disk egenskaper för operativ systemet på en virtuell dator bild</span><span class="sxs-lookup"><span data-stu-id="a46a1-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="a46a1-111">I det här exemplet ställs disk egenskaper för operativ systemet in på en virtuell dator bild.</span><span class="sxs-lookup"><span data-stu-id="a46a1-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="a46a1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a46a1-112">PARAMETERS</span></span>

### <span data-ttu-id="a46a1-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="a46a1-113">-DiskConfig</span></span>
<span data-ttu-id="a46a1-114">Anger det disk konfigurations objekt som kapslar in operativ system disken och data disk objekt.</span><span class="sxs-lookup"><span data-stu-id="a46a1-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="a46a1-115">-HostCaching</span></span>
<span data-ttu-id="a46a1-116">Anger attributet Host cache för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="a46a1-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="a46a1-117">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a46a1-117">Valid values are:</span></span>

<span data-ttu-id="a46a1-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a46a1-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a46a1-119">-InformationAction</span></span>
<span data-ttu-id="a46a1-120">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="a46a1-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a46a1-121">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a46a1-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a46a1-122">Vidare</span><span class="sxs-lookup"><span data-stu-id="a46a1-122">Continue</span></span>
- <span data-ttu-id="a46a1-123">Över</span><span class="sxs-lookup"><span data-stu-id="a46a1-123">Ignore</span></span>
- <span data-ttu-id="a46a1-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="a46a1-124">Inquire</span></span>
- <span data-ttu-id="a46a1-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a46a1-125">SilentlyContinue</span></span>
- <span data-ttu-id="a46a1-126">Stanna</span><span class="sxs-lookup"><span data-stu-id="a46a1-126">Stop</span></span>
- <span data-ttu-id="a46a1-127">Avbryt</span><span class="sxs-lookup"><span data-stu-id="a46a1-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a46a1-128">-InformationVariable</span></span>
<span data-ttu-id="a46a1-129">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="a46a1-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="a46a1-130">-MediaLink</span></span>
<span data-ttu-id="a46a1-131">Anger URI för platsen där den nya virtuella hård disken skapas när den nya data disken läggs till.</span><span class="sxs-lookup"><span data-stu-id="a46a1-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-132">-OS</span><span class="sxs-lookup"><span data-stu-id="a46a1-132">-OS</span></span>
<span data-ttu-id="a46a1-133">Anger disk konfigurationens operativ system.</span><span class="sxs-lookup"><span data-stu-id="a46a1-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="a46a1-134">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a46a1-134">Valid values are:</span></span>

- <span data-ttu-id="a46a1-135">Windows</span><span class="sxs-lookup"><span data-stu-id="a46a1-135">Windows</span></span>
- <span data-ttu-id="a46a1-136">Linux</span><span class="sxs-lookup"><span data-stu-id="a46a1-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="a46a1-137">-OSState</span></span>
<span data-ttu-id="a46a1-138">Anger operativ system tillståndet för den virtuella dator avbildningen</span><span class="sxs-lookup"><span data-stu-id="a46a1-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="a46a1-139">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="a46a1-139">Valid values are:</span></span>

- <span data-ttu-id="a46a1-140">Generalized</span><span class="sxs-lookup"><span data-stu-id="a46a1-140">Generalized</span></span>
- <span data-ttu-id="a46a1-141">Specialverktyg</span><span class="sxs-lookup"><span data-stu-id="a46a1-141">Specialized</span></span>

<span data-ttu-id="a46a1-142">Användning av den här parametern anger hur du vill avbilda den virtuella dator avbildningen till Azure.</span><span class="sxs-lookup"><span data-stu-id="a46a1-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46a1-143">CommonParameters</span></span>
<span data-ttu-id="a46a1-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a46a1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46a1-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46a1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46a1-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a46a1-146">INPUTS</span></span>

## <span data-ttu-id="a46a1-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a46a1-147">OUTPUTS</span></span>

### <span data-ttu-id="a46a1-148">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="a46a1-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="a46a1-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a46a1-149">NOTES</span></span>

## <span data-ttu-id="a46a1-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a46a1-150">RELATED LINKS</span></span>

[<span data-ttu-id="a46a1-151">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="a46a1-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


