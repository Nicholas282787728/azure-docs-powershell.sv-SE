---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093162"
---
# <span data-ttu-id="10389-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="10389-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="10389-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10389-102">SYNOPSIS</span></span>
<span data-ttu-id="10389-103">Anger data disk egenskaper för den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="10389-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="10389-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10389-104">SYNTAX</span></span>

### <span data-ttu-id="10389-105">UpdateAzureVMImageParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="10389-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="10389-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="10389-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="10389-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10389-107">DESCRIPTION</span></span>
<span data-ttu-id="10389-108">Cmdleten **set-AzureVMImageDataDiskConfig** anger data disk egenskaper för den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="10389-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="10389-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10389-109">EXAMPLES</span></span>

### <span data-ttu-id="10389-110">Exempel 1: ange data disk egenskaper på en virtuell dator bild</span><span class="sxs-lookup"><span data-stu-id="10389-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="10389-111">Det här kommandot anger data disk egenskaper på en virtuell dator och uppdaterar sedan den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="10389-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="10389-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10389-112">PARAMETERS</span></span>

### <span data-ttu-id="10389-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="10389-113">-DataDiskName</span></span>
<span data-ttu-id="10389-114">Anger namnet på den data disk som denna cmdlet konfigurerar.</span><span class="sxs-lookup"><span data-stu-id="10389-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10389-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="10389-115">-DiskConfig</span></span>
<span data-ttu-id="10389-116">Anger det disk konfigurations objekt som kapslar in operativ system disken och data disk objekt.</span><span class="sxs-lookup"><span data-stu-id="10389-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="10389-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="10389-117">-HostCaching</span></span>
<span data-ttu-id="10389-118">Anger attributet Host cache för operativ system disken.</span><span class="sxs-lookup"><span data-stu-id="10389-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="10389-119">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="10389-119">Valid values are:</span></span>

<span data-ttu-id="10389-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="10389-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10389-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="10389-121">-InformationAction</span></span>
<span data-ttu-id="10389-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="10389-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="10389-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="10389-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10389-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="10389-124">Continue</span></span>
- <span data-ttu-id="10389-125">Över</span><span class="sxs-lookup"><span data-stu-id="10389-125">Ignore</span></span>
- <span data-ttu-id="10389-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="10389-126">Inquire</span></span>
- <span data-ttu-id="10389-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="10389-127">SilentlyContinue</span></span>
- <span data-ttu-id="10389-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="10389-128">Stop</span></span>
- <span data-ttu-id="10389-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="10389-129">Suspend</span></span>

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

### <span data-ttu-id="10389-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="10389-130">-InformationVariable</span></span>
<span data-ttu-id="10389-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="10389-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="10389-132">-LUN</span><span class="sxs-lookup"><span data-stu-id="10389-132">-Lun</span></span>
<span data-ttu-id="10389-133">Anger den plats där data enheten är monterad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="10389-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10389-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="10389-134">-MediaLink</span></span>
<span data-ttu-id="10389-135">Anger URI för platsen där den nya virtuella hård disken skapas när den nya data disken läggs till.</span><span class="sxs-lookup"><span data-stu-id="10389-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10389-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10389-136">CommonParameters</span></span>
<span data-ttu-id="10389-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10389-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10389-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10389-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10389-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10389-139">INPUTS</span></span>

## <span data-ttu-id="10389-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10389-140">OUTPUTS</span></span>

### <span data-ttu-id="10389-141">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="10389-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="10389-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10389-142">NOTES</span></span>

## <span data-ttu-id="10389-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10389-143">RELATED LINKS</span></span>

[<span data-ttu-id="10389-144">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="10389-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


