---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: 0a7b11edad8fd19087b634111a67bc704abf6bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092311"
---
# <span data-ttu-id="eba97-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="eba97-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="eba97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eba97-102">SYNOPSIS</span></span>
<span data-ttu-id="eba97-103">Uppdaterar tillståndet för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="eba97-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="eba97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eba97-104">SYNTAX</span></span>

### <span data-ttu-id="eba97-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="eba97-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba97-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="eba97-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eba97-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="eba97-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eba97-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eba97-108">DESCRIPTION</span></span>
<span data-ttu-id="eba97-109">Uppdaterar tillståndet för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="eba97-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="eba97-110">För tillfället är den enda tillåtna uppdateringen att lägga till en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="eba97-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="eba97-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eba97-111">EXAMPLES</span></span>

### <span data-ttu-id="eba97-112">Exempel 1: lägga till en hanterad datadisk till en VMSS VM med New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="eba97-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="eba97-113">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="eba97-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="eba97-114">Med nästa kommando skapas ett data disk objekt med den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="eba97-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="eba97-115">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="eba97-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="eba97-116">Det sista kommandot uppdaterar den VMSS virtuella datorn genom att lägga till en ny data skiva.</span><span class="sxs-lookup"><span data-stu-id="eba97-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="eba97-117">Exempel 2: lägga till en hanterad datadisk till en VMSS VM med Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="eba97-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="eba97-118">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="eba97-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="eba97-119">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="eba97-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="eba97-120">Nästa kommando lägger till den hanterade disken till den lokala VMSS VM i $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="eba97-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="eba97-121">Det sista kommandot uppdaterar den VMSS virtuella dator med tillagd data skiva.</span><span class="sxs-lookup"><span data-stu-id="eba97-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="eba97-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eba97-122">PARAMETERS</span></span>

### <span data-ttu-id="eba97-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eba97-123">-AsJob</span></span>
<span data-ttu-id="eba97-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eba97-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eba97-125">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="eba97-125">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eba97-126">-DefaultProfile</span></span>
<span data-ttu-id="eba97-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eba97-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eba97-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="eba97-128">-InstanceId</span></span>
<span data-ttu-id="eba97-129">Anger instans-ID för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="eba97-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-130">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="eba97-130">-ProtectFromScaleIn</span></span>
<span data-ttu-id="eba97-131">Anger att den virtuella datorns skalnings uppsättnings virtuella dator inte ska tas bort under en skalnings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="eba97-131">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-132">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="eba97-132">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="eba97-133">Anger att modell uppdateringar eller åtgärder (inklusive skalning-in) som initieras på VMSS inte ska tillämpas på den virtuella VMSS.</span><span class="sxs-lookup"><span data-stu-id="eba97-133">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eba97-134">-ResourceGroupName</span></span>
<span data-ttu-id="eba97-135">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="eba97-135">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eba97-136">-ResourceId</span></span>
<span data-ttu-id="eba97-137">Resurs-ID för virtuell dator skalförändra angiven virtuell dator</span><span class="sxs-lookup"><span data-stu-id="eba97-137">The resource id for the virtual machine scale set VM</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-138">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eba97-138">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="eba97-139">Skala för lokal virtuell dator-ange virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="eba97-139">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-140">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="eba97-140">-VMScaleSetName</span></span>
<span data-ttu-id="eba97-141">Namnet på den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="eba97-141">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eba97-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eba97-142">-Confirm</span></span>
<span data-ttu-id="eba97-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eba97-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eba97-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eba97-144">-WhatIf</span></span>
<span data-ttu-id="eba97-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eba97-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eba97-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eba97-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eba97-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eba97-147">CommonParameters</span></span>
<span data-ttu-id="eba97-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eba97-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eba97-149">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eba97-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eba97-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eba97-150">INPUTS</span></span>

### <span data-ttu-id="eba97-151">System. String</span><span class="sxs-lookup"><span data-stu-id="eba97-151">System.String</span></span>

### <span data-ttu-id="eba97-152">Microsoft. Azure. kommandon. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="eba97-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="eba97-153">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eba97-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="eba97-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eba97-154">OUTPUTS</span></span>

### <span data-ttu-id="eba97-155">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="eba97-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="eba97-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eba97-156">NOTES</span></span>

## <span data-ttu-id="eba97-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eba97-157">RELATED LINKS</span></span>
