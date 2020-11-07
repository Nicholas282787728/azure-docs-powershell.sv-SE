---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: c1a1b95dcaa06d922b0357d0e9e6a1b75fa7d793
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925297"
---
# <span data-ttu-id="2f866-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2f866-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="2f866-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f866-102">SYNOPSIS</span></span>
<span data-ttu-id="2f866-103">Lägger till en datadisk till VMSS.</span><span class="sxs-lookup"><span data-stu-id="2f866-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="2f866-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f866-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f866-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f866-105">DESCRIPTION</span></span>
<span data-ttu-id="2f866-106">Cmdleten **Add-AzVmssDataDisk** lägger till en datadisk till instansen för virtuell dator Scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2f866-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="2f866-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f866-107">EXAMPLES</span></span>

### <span data-ttu-id="2f866-108">Exempel 1: lägga till en data disk</span><span class="sxs-lookup"><span data-stu-id="2f866-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="2f866-109">Det här kommandot lägger till en tom datadisk till VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="2f866-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="2f866-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f866-110">PARAMETERS</span></span>

### <span data-ttu-id="2f866-111">-Cachning</span><span class="sxs-lookup"><span data-stu-id="2f866-111">-Caching</span></span>
<span data-ttu-id="2f866-112">Anger diskens cachelagringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="2f866-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="2f866-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="2f866-113">-CreateOption</span></span>
<span data-ttu-id="2f866-114">Anger diskens skapande alternativ.</span><span class="sxs-lookup"><span data-stu-id="2f866-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="2f866-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f866-115">-DefaultProfile</span></span>
<span data-ttu-id="2f866-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f866-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f866-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2f866-117">-DiskSizeGB</span></span>
<span data-ttu-id="2f866-118">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="2f866-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2f866-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="2f866-119">-Lun</span></span>
<span data-ttu-id="2f866-120">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="2f866-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="2f866-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f866-121">-Name</span></span>
<span data-ttu-id="2f866-122">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="2f866-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="2f866-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2f866-123">-StorageAccountType</span></span>
<span data-ttu-id="2f866-124">Anger diskens lagrings kontotyp.</span><span class="sxs-lookup"><span data-stu-id="2f866-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="2f866-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2f866-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2f866-126">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="2f866-126">Specify the VMSS object.</span></span>
<span data-ttu-id="2f866-127">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="2f866-127">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f866-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2f866-128">-WriteAccelerator</span></span>
<span data-ttu-id="2f866-129">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="2f866-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f866-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f866-130">-Confirm</span></span>
<span data-ttu-id="2f866-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f866-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f866-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f866-132">-WhatIf</span></span>
<span data-ttu-id="2f866-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2f866-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f866-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2f866-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f866-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f866-135">CommonParameters</span></span>
<span data-ttu-id="2f866-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f866-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f866-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f866-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f866-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f866-138">INPUTS</span></span>

### <span data-ttu-id="2f866-139">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2f866-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="2f866-140">System. String system. Int32-system. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. DiskCreateOptionTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] system. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute; Model. StorageAccountTypes, Microsoft. Azure. Management. Compute, version = 14.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2f866-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="2f866-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f866-141">OUTPUTS</span></span>

### <span data-ttu-id="2f866-142">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2f866-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="2f866-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f866-143">NOTES</span></span>

## <span data-ttu-id="2f866-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f866-144">RELATED LINKS</span></span>

