---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272735"
---
# <span data-ttu-id="8e520-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="8e520-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="8e520-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e520-102">SYNOPSIS</span></span>
<span data-ttu-id="8e520-103">Lägger till en datadisk till VMSS.</span><span class="sxs-lookup"><span data-stu-id="8e520-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="8e520-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e520-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e520-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e520-105">DESCRIPTION</span></span>
<span data-ttu-id="8e520-106">Cmdleten **Add-AzVmssDataDisk** lägger till en datadisk till instansen för virtuell dator Scale set (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8e520-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="8e520-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e520-107">EXAMPLES</span></span>

### <span data-ttu-id="8e520-108">Exempel 1: lägga till en data disk</span><span class="sxs-lookup"><span data-stu-id="8e520-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="8e520-109">Det här kommandot lägger till en tom datadisk till VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="8e520-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="8e520-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e520-110">PARAMETERS</span></span>

### <span data-ttu-id="8e520-111">-Cachning</span><span class="sxs-lookup"><span data-stu-id="8e520-111">-Caching</span></span>
<span data-ttu-id="8e520-112">Anger diskens cachelagringsalternativ.</span><span class="sxs-lookup"><span data-stu-id="8e520-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="8e520-113">-CreateOption</span></span>
<span data-ttu-id="8e520-114">Anger diskens skapande alternativ.</span><span class="sxs-lookup"><span data-stu-id="8e520-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="8e520-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e520-115">-DefaultProfile</span></span>
<span data-ttu-id="8e520-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e520-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e520-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="8e520-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="8e520-118">Anger resurs-ID för kund hanterad disk krypterings uppsättning.</span><span class="sxs-lookup"><span data-stu-id="8e520-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="8e520-119">Detta kan endast anges för hanterade diskar.</span><span class="sxs-lookup"><span data-stu-id="8e520-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="8e520-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="8e520-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="8e520-121">Anger Read-Write IOPS för den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="8e520-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="8e520-122">Bör endast användas när StorageAccountType är UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="8e520-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="8e520-123">Om inget anges tilldelas ett standardvärde baserat på diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="8e520-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="8e520-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="8e520-125">Anger bandbredden i MB per sekund för den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="8e520-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="8e520-126">Bör endast användas när StorageAccountType är UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="8e520-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="8e520-127">Om inget anges tilldelas ett standardvärde baserat på diskSizeGB.</span><span class="sxs-lookup"><span data-stu-id="8e520-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8e520-128">-DiskSizeGB</span></span>
<span data-ttu-id="8e520-129">Anger diskens storlek i GB.</span><span class="sxs-lookup"><span data-stu-id="8e520-129">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-130">-LUN</span><span class="sxs-lookup"><span data-stu-id="8e520-130">-Lun</span></span>
<span data-ttu-id="8e520-131">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="8e520-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e520-132">-Name</span></span>
<span data-ttu-id="8e520-133">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="8e520-133">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8e520-134">-StorageAccountType</span></span>
<span data-ttu-id="8e520-135">Anger diskens lagrings kontotyp.</span><span class="sxs-lookup"><span data-stu-id="8e520-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="8e520-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8e520-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8e520-137">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="8e520-137">Specify the VMSS object.</span></span>
<span data-ttu-id="8e520-138">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="8e520-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e520-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="8e520-139">-WriteAccelerator</span></span>
<span data-ttu-id="8e520-140">Anger om WriteAccelerator ska aktive ras eller inaktive ras på data disken.</span><span class="sxs-lookup"><span data-stu-id="8e520-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="8e520-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e520-141">-Confirm</span></span>
<span data-ttu-id="8e520-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e520-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e520-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e520-143">-WhatIf</span></span>
<span data-ttu-id="8e520-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e520-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e520-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e520-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e520-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e520-146">CommonParameters</span></span>
<span data-ttu-id="8e520-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e520-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e520-148">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e520-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e520-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e520-149">INPUTS</span></span>

### <span data-ttu-id="8e520-150">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8e520-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="8e520-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8e520-151">System.String</span></span>

### <span data-ttu-id="8e520-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8e520-152">System.Int32</span></span>

### <span data-ttu-id="8e520-153">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8e520-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8e520-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e520-154">OUTPUTS</span></span>

### <span data-ttu-id="8e520-155">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8e520-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8e520-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e520-156">NOTES</span></span>

## <span data-ttu-id="8e520-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e520-157">RELATED LINKS</span></span>
