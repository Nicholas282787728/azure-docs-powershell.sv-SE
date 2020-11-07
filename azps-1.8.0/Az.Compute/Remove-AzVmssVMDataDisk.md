---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 998001d931ba30c560aabd15318359d5e37baccb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754496"
---
# <span data-ttu-id="30951-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="30951-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="30951-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30951-102">SYNOPSIS</span></span>
<span data-ttu-id="30951-103">Tar bort en datadisk från en virtuell dator skala ange virtuell dator</span><span class="sxs-lookup"><span data-stu-id="30951-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="30951-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30951-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30951-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30951-105">DESCRIPTION</span></span>
<span data-ttu-id="30951-106">Cmdleten **Remove-AzVmssVMDataDisk** tar bort en datadisk från en virtuell dators SKALNINGs dator</span><span class="sxs-lookup"><span data-stu-id="30951-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="30951-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30951-107">EXAMPLES</span></span>

### <span data-ttu-id="30951-108">Exempel 1: ta bort en datadisk från en virtuell dator skala ange virtuell dator</span><span class="sxs-lookup"><span data-stu-id="30951-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="30951-109">Det första kommandot getsan befintliga VMSS VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="30951-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="30951-110">Med det andra kommandot tas data disken LUN 0 bort från den virtuella datorns skal uppsättning den virtuella dator som lagras i $VmssVM det sista kommandot uppdaterar den VMSS virtuella dator med borttagen data disk.</span><span class="sxs-lookup"><span data-stu-id="30951-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="30951-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30951-111">PARAMETERS</span></span>

### <span data-ttu-id="30951-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30951-112">-DefaultProfile</span></span>
<span data-ttu-id="30951-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30951-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30951-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="30951-114">-Lun</span></span>
<span data-ttu-id="30951-115">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="30951-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30951-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="30951-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="30951-117">Den virtuella datorns skalning ange VM-profilen.</span><span class="sxs-lookup"><span data-stu-id="30951-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30951-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30951-118">CommonParameters</span></span>
<span data-ttu-id="30951-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30951-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30951-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30951-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30951-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30951-121">INPUTS</span></span>

### <span data-ttu-id="30951-122">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="30951-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="30951-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30951-123">OUTPUTS</span></span>

### <span data-ttu-id="30951-124">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="30951-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="30951-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30951-125">NOTES</span></span>

## <span data-ttu-id="30951-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30951-126">RELATED LINKS</span></span>