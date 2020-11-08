---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093223"
---
# <span data-ttu-id="107c6-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="107c6-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="107c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="107c6-102">SYNOPSIS</span></span>
<span data-ttu-id="107c6-103">Tar bort konfigurationen för data diskar från DiskConfigSet-objektet.</span><span class="sxs-lookup"><span data-stu-id="107c6-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="107c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="107c6-104">SYNTAX</span></span>

### <span data-ttu-id="107c6-105">RemoveByDiskName (standard)</span><span class="sxs-lookup"><span data-stu-id="107c6-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="107c6-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="107c6-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="107c6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="107c6-107">DESCRIPTION</span></span>
<span data-ttu-id="107c6-108">Cmdleten **Remove-AzureVMImageDataDiskConfig** tar bort konfigurationen för data diskar från **DiskConfigSet** -objektet.</span><span class="sxs-lookup"><span data-stu-id="107c6-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="107c6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="107c6-109">EXAMPLES</span></span>

### <span data-ttu-id="107c6-110">Exempel 1: ta bort data disk konfigurationen från DiskConfigSet-objektet</span><span class="sxs-lookup"><span data-stu-id="107c6-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="107c6-111">Det här exemplet skapar en **DiskConfigSet** , konfigurerar den och tar sedan bort data disken.</span><span class="sxs-lookup"><span data-stu-id="107c6-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="107c6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="107c6-112">PARAMETERS</span></span>

### <span data-ttu-id="107c6-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="107c6-113">-DataDiskName</span></span>
<span data-ttu-id="107c6-114">Anger namnet på den data disk som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="107c6-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107c6-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="107c6-115">-DiskConfig</span></span>
<span data-ttu-id="107c6-116">Anger det disk konfigurations objekt som kapslar in operativ system disken och data disk objekt.</span><span class="sxs-lookup"><span data-stu-id="107c6-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="107c6-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="107c6-117">-InformationAction</span></span>
<span data-ttu-id="107c6-118">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="107c6-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="107c6-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="107c6-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="107c6-120">Vidare</span><span class="sxs-lookup"><span data-stu-id="107c6-120">Continue</span></span>
- <span data-ttu-id="107c6-121">Över</span><span class="sxs-lookup"><span data-stu-id="107c6-121">Ignore</span></span>
- <span data-ttu-id="107c6-122">Inquire</span><span class="sxs-lookup"><span data-stu-id="107c6-122">Inquire</span></span>
- <span data-ttu-id="107c6-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="107c6-123">SilentlyContinue</span></span>
- <span data-ttu-id="107c6-124">Stanna</span><span class="sxs-lookup"><span data-stu-id="107c6-124">Stop</span></span>
- <span data-ttu-id="107c6-125">Avbryt</span><span class="sxs-lookup"><span data-stu-id="107c6-125">Suspend</span></span>

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

### <span data-ttu-id="107c6-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="107c6-126">-InformationVariable</span></span>
<span data-ttu-id="107c6-127">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="107c6-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="107c6-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="107c6-128">-Lun</span></span>
<span data-ttu-id="107c6-129">Anger den plats där data enheten är monterad på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="107c6-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="107c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="107c6-130">CommonParameters</span></span>
<span data-ttu-id="107c6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="107c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="107c6-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="107c6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="107c6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="107c6-133">INPUTS</span></span>

## <span data-ttu-id="107c6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="107c6-134">OUTPUTS</span></span>

### <span data-ttu-id="107c6-135">Microsoft. WindowsAzure. kommandon. ServiceManagement. Model. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="107c6-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="107c6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="107c6-136">NOTES</span></span>

## <span data-ttu-id="107c6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="107c6-137">RELATED LINKS</span></span>

[<span data-ttu-id="107c6-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="107c6-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


