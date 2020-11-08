---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099428"
---
# <span data-ttu-id="23a90-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="23a90-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="23a90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23a90-102">SYNOPSIS</span></span>
<span data-ttu-id="23a90-103">Skapar ett objekt för disk konfigurations uppsättning.</span><span class="sxs-lookup"><span data-stu-id="23a90-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="23a90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23a90-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="23a90-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23a90-105">DESCRIPTION</span></span>
<span data-ttu-id="23a90-106">Cmdleten **New-AzureVMImageDiskConfigSet** skapar ett objekt för disk konfigurations uppsättning som skickas till cmdleten för avbildnings uppdatering.</span><span class="sxs-lookup"><span data-stu-id="23a90-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="23a90-107">OSDiskConfig och DataDiskConfig-objektet kapslas in.</span><span class="sxs-lookup"><span data-stu-id="23a90-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="23a90-108">Använd cmdletarna **set-AzureVMImageOSDiskConfig** och **set-AzureVMImageDataDiskConfig** för att ange OS-disk-och data disk egenskaper för den virtuella dator avbildningen.</span><span class="sxs-lookup"><span data-stu-id="23a90-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="23a90-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23a90-109">EXAMPLES</span></span>

### <span data-ttu-id="23a90-110">Exempel 1: skapa en uppsättning objekt för disk konfiguration</span><span class="sxs-lookup"><span data-stu-id="23a90-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="23a90-111">Det här kommandot skapar ett objekt för disk konfigurations uppsättning och lagrar resultatet i variabeln som heter $Disk.</span><span class="sxs-lookup"><span data-stu-id="23a90-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="23a90-112">När disk konfigurationen har skapats används den för att ange OSDiskConfig och DataDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="23a90-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="23a90-113">Sedan uppdateras den virtuella datorn med konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="23a90-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="23a90-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23a90-114">PARAMETERS</span></span>

### <span data-ttu-id="23a90-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="23a90-115">-InformationAction</span></span>
<span data-ttu-id="23a90-116">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="23a90-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="23a90-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="23a90-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23a90-118">Vidare</span><span class="sxs-lookup"><span data-stu-id="23a90-118">Continue</span></span>
- <span data-ttu-id="23a90-119">Över</span><span class="sxs-lookup"><span data-stu-id="23a90-119">Ignore</span></span>
- <span data-ttu-id="23a90-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="23a90-120">Inquire</span></span>
- <span data-ttu-id="23a90-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="23a90-121">SilentlyContinue</span></span>
- <span data-ttu-id="23a90-122">Stanna</span><span class="sxs-lookup"><span data-stu-id="23a90-122">Stop</span></span>
- <span data-ttu-id="23a90-123">Avbryt</span><span class="sxs-lookup"><span data-stu-id="23a90-123">Suspend</span></span>

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

### <span data-ttu-id="23a90-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="23a90-124">-InformationVariable</span></span>
<span data-ttu-id="23a90-125">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="23a90-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="23a90-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a90-126">CommonParameters</span></span>
<span data-ttu-id="23a90-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a90-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a90-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a90-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a90-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23a90-129">INPUTS</span></span>

## <span data-ttu-id="23a90-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23a90-130">OUTPUTS</span></span>

### <span data-ttu-id="23a90-131">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="23a90-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="23a90-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23a90-132">NOTES</span></span>

## <span data-ttu-id="23a90-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23a90-133">RELATED LINKS</span></span>

[<span data-ttu-id="23a90-134">Get-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="23a90-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="23a90-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="23a90-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="23a90-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="23a90-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


