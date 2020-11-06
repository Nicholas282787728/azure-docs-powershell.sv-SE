---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmssVMDataDisk.md
ms.openlocfilehash: 5c82c2dfb852cd6c3d397b34e90d9a611ff0efaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585056"
---
# <span data-ttu-id="aaf9e-101">Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="aaf9e-101">Remove-AzureRmVmssVMDataDisk</span></span>

## <span data-ttu-id="aaf9e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aaf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf9e-103">Tar bort en datadisk från en virtuell dator skala ange virtuell dator</span><span class="sxs-lookup"><span data-stu-id="aaf9e-103">Removes a data disk from a virtual machine scale set VM</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaf9e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aaf9e-104">SYNTAX</span></span>

```
Remove-AzureRmVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaf9e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aaf9e-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf9e-106">Cmdleten **Remove-AzureRmVmssVMDataDisk** tar bort en datadisk från en virtuell dators SKALNINGs dator</span><span class="sxs-lookup"><span data-stu-id="aaf9e-106">The **Remove-AzureRmVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="aaf9e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aaf9e-107">EXAMPLES</span></span>

### <span data-ttu-id="aaf9e-108">Exempel 1: ta bort en datadisk från en virtuell dator skala ange virtuell dator</span><span class="sxs-lookup"><span data-stu-id="aaf9e-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzureRmVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="aaf9e-109">Det första kommandot getsan befintliga VMSS VM som anges av resurs gruppens namn, VMSS namn och instans-ID.</span><span class="sxs-lookup"><span data-stu-id="aaf9e-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="aaf9e-110">Med det andra kommandot tas data disken LUN 0 bort från den virtuella datorns skal uppsättning den virtuella dator som lagras i $VmssVM det sista kommandot uppdaterar den VMSS virtuella dator med borttagen data disk.</span><span class="sxs-lookup"><span data-stu-id="aaf9e-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="aaf9e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aaf9e-111">PARAMETERS</span></span>

### <span data-ttu-id="aaf9e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf9e-112">-DefaultProfile</span></span>
<span data-ttu-id="aaf9e-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aaf9e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf9e-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="aaf9e-114">-Lun</span></span>
<span data-ttu-id="aaf9e-115">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="aaf9e-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="aaf9e-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="aaf9e-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="aaf9e-117">Den virtuella datorns skalning ange VM-profilen.</span><span class="sxs-lookup"><span data-stu-id="aaf9e-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf9e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf9e-118">CommonParameters</span></span>
<span data-ttu-id="aaf9e-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf9e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf9e-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf9e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf9e-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aaf9e-121">INPUTS</span></span>

### <span data-ttu-id="aaf9e-122">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="aaf9e-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="aaf9e-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aaf9e-123">OUTPUTS</span></span>

### <span data-ttu-id="aaf9e-124">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="aaf9e-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="aaf9e-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aaf9e-125">NOTES</span></span>

## <span data-ttu-id="aaf9e-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aaf9e-126">RELATED LINKS</span></span>
