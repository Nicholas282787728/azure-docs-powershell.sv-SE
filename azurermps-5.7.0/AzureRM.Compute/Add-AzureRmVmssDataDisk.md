---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756101"
---
# <span data-ttu-id="b4f4d-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="b4f4d-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="b4f4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f4d-103">Lägger till en datadisk till VMSS.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4f4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4f4d-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4f4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f4d-106">Cmdleten **Add-AzureRmVmssDataDisk** lägger till en datadisk till instansen för virtuell dator Scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b4f4d-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="b4f4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="b4f4d-108">Exempel 1: lägga till en data disk</span><span class="sxs-lookup"><span data-stu-id="b4f4d-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="b4f4d-109">Det här kommandot lägger till en tom datadisk till VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="b4f4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4f4d-110">PARAMETERS</span></span>

### <span data-ttu-id="b4f4d-111">-Cachning</span><span class="sxs-lookup"><span data-stu-id="b4f4d-111">-Caching</span></span>
<span data-ttu-id="b4f4d-112">Anger diskens cachelagringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4d-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="b4f4d-113">-CreateOption</span></span>
<span data-ttu-id="b4f4d-114">Anger diskens skapande alternativ.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4d-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b4f4d-115">-DiskSizeGB</span></span>
<span data-ttu-id="b4f4d-116">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-116">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4d-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="b4f4d-117">-Lun</span></span>
<span data-ttu-id="b4f4d-118">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4f4d-119">-Name</span></span>
<span data-ttu-id="b4f4d-120">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="b4f4d-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b4f4d-121">-StorageAccountType</span></span>
<span data-ttu-id="b4f4d-122">Anger diskens lagrings kontotyp.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-122">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4d-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4f4d-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4f4d-124">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-124">Specify the VMSS object.</span></span>
<span data-ttu-id="b4f4d-125">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f4d-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4f4d-126">-Confirm</span></span>
<span data-ttu-id="b4f4d-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4f4d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4f4d-128">-WhatIf</span></span>
<span data-ttu-id="b4f4d-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4f4d-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4f4d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f4d-131">CommonParameters</span></span>
<span data-ttu-id="b4f4d-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f4d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f4d-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f4d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f4d-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4f4d-134">INPUTS</span></span>

### <span data-ttu-id="b4f4d-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4f4d-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="b4f4d-136">System. String system. Int32-system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] system. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute; Model. StorageAccountTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b4f4d-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b4f4d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4f4d-137">OUTPUTS</span></span>

### <span data-ttu-id="b4f4d-138">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b4f4d-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="b4f4d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4f4d-139">NOTES</span></span>

## <span data-ttu-id="b4f4d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4f4d-140">RELATED LINKS</span></span>
