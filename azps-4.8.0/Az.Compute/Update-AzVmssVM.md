---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260792"
---
# <span data-ttu-id="190a1-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="190a1-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="190a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="190a1-102">SYNOPSIS</span></span>
<span data-ttu-id="190a1-103">Uppdaterar tillståndet för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="190a1-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="190a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="190a1-104">SYNTAX</span></span>

### <span data-ttu-id="190a1-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="190a1-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190a1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="190a1-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="190a1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="190a1-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="190a1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="190a1-108">DESCRIPTION</span></span>
<span data-ttu-id="190a1-109">Uppdaterar tillståndet för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="190a1-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="190a1-110">För tillfället är den enda tillåtna uppdateringen att lägga till en hanterad data disk.</span><span class="sxs-lookup"><span data-stu-id="190a1-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="190a1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="190a1-111">EXAMPLES</span></span>

### <span data-ttu-id="190a1-112">Exempel 1: lägga till en hanterad datadisk till en VMSS VM med New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="190a1-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="190a1-113">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="190a1-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="190a1-114">Med nästa kommando skapas ett data disk objekt med den hanterade disken.</span><span class="sxs-lookup"><span data-stu-id="190a1-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="190a1-115">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="190a1-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="190a1-116">Det sista kommandot uppdaterar den VMSS virtuella datorn genom att lägga till en ny data skiva.</span><span class="sxs-lookup"><span data-stu-id="190a1-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="190a1-117">Exempel 2: lägga till en hanterad datadisk till en VMSS VM med Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="190a1-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="190a1-118">Det första kommandot får en befintlig hanterad disk.</span><span class="sxs-lookup"><span data-stu-id="190a1-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="190a1-119">Nästa kommando hämtar en befintlig VMSS-VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="190a1-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="190a1-120">Nästa kommando lägger till den hanterade disken till den lokala VMSS VM i $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="190a1-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="190a1-121">Det sista kommandot uppdaterar den VMSS virtuella dator med tillagd data skiva.</span><span class="sxs-lookup"><span data-stu-id="190a1-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="190a1-122">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="190a1-122">Example 3</span></span>

<span data-ttu-id="190a1-123">Uppdaterar tillståndet för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="190a1-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="190a1-124">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="190a1-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="190a1-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="190a1-125">PARAMETERS</span></span>

### <span data-ttu-id="190a1-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="190a1-126">-AsJob</span></span>
<span data-ttu-id="190a1-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="190a1-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="190a1-128">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="190a1-128">-DataDisk</span></span>

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

### <span data-ttu-id="190a1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="190a1-129">-DefaultProfile</span></span>
<span data-ttu-id="190a1-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="190a1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="190a1-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="190a1-131">-InstanceId</span></span>
<span data-ttu-id="190a1-132">Anger instans-ID för en VMSS VM.</span><span class="sxs-lookup"><span data-stu-id="190a1-132">Specifies the instance ID of a VMSS VM.</span></span>

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

### <span data-ttu-id="190a1-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="190a1-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="190a1-134">Anger att den virtuella datorns skalnings uppsättnings virtuella dator inte ska tas bort under en skalnings åtgärd.</span><span class="sxs-lookup"><span data-stu-id="190a1-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

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

### <span data-ttu-id="190a1-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="190a1-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="190a1-136">Anger att modell uppdateringar eller åtgärder (inklusive skalning-in) som initieras på VMSS inte ska tillämpas på den virtuella VMSS.</span><span class="sxs-lookup"><span data-stu-id="190a1-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

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

### <span data-ttu-id="190a1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="190a1-137">-ResourceGroupName</span></span>
<span data-ttu-id="190a1-138">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="190a1-138">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="190a1-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="190a1-139">-ResourceId</span></span>
<span data-ttu-id="190a1-140">Resurs-ID för virtuell dator skalförändra angiven virtuell dator</span><span class="sxs-lookup"><span data-stu-id="190a1-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="190a1-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="190a1-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="190a1-142">Skala för lokal virtuell dator-ange virtuellt dator objekt</span><span class="sxs-lookup"><span data-stu-id="190a1-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="190a1-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="190a1-143">-VMScaleSetName</span></span>
<span data-ttu-id="190a1-144">Namnet på den virtuella datorns skal uppsättning</span><span class="sxs-lookup"><span data-stu-id="190a1-144">The name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="190a1-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="190a1-145">-Confirm</span></span>
<span data-ttu-id="190a1-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="190a1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="190a1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="190a1-147">-WhatIf</span></span>
<span data-ttu-id="190a1-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="190a1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="190a1-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="190a1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="190a1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="190a1-150">CommonParameters</span></span>
<span data-ttu-id="190a1-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="190a1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="190a1-152">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="190a1-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="190a1-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="190a1-153">INPUTS</span></span>

### <span data-ttu-id="190a1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="190a1-154">System.String</span></span>

### <span data-ttu-id="190a1-155">Microsoft. Azure. kommandon. Compute. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="190a1-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="190a1-156">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="190a1-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="190a1-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="190a1-157">OUTPUTS</span></span>

### <span data-ttu-id="190a1-158">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="190a1-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="190a1-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="190a1-159">NOTES</span></span>

## <span data-ttu-id="190a1-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="190a1-160">RELATED LINKS</span></span>