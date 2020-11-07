---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755263"
---
# <span data-ttu-id="456e8-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="456e8-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="456e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="456e8-102">SYNOPSIS</span></span>
<span data-ttu-id="456e8-103">Tar bort en datadisk från VMSS.</span><span class="sxs-lookup"><span data-stu-id="456e8-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="456e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="456e8-104">SYNTAX</span></span>

### <span data-ttu-id="456e8-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="456e8-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="456e8-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="456e8-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="456e8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="456e8-107">DESCRIPTION</span></span>
<span data-ttu-id="456e8-108">Cmdleten **Remove-AzureRmVmssDataDisk** tar bort en datadisk från den virtuella datorns Scale set-instans (VMSS).</span><span class="sxs-lookup"><span data-stu-id="456e8-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="456e8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="456e8-109">EXAMPLES</span></span>

### <span data-ttu-id="456e8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="456e8-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="456e8-111">Det här kommandot tar bort data disken ' DataDisk1 ' från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="456e8-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="456e8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="456e8-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="456e8-113">Det här kommandot tar bort data disken för LUN 0 från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="456e8-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="456e8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="456e8-114">PARAMETERS</span></span>

### <span data-ttu-id="456e8-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="456e8-115">-Lun</span></span>
<span data-ttu-id="456e8-116">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="456e8-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456e8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="456e8-117">-Name</span></span>
<span data-ttu-id="456e8-118">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="456e8-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="456e8-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="456e8-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="456e8-120">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="456e8-120">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="456e8-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="456e8-121">-Confirm</span></span>
<span data-ttu-id="456e8-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="456e8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="456e8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="456e8-123">-WhatIf</span></span>
<span data-ttu-id="456e8-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="456e8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="456e8-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="456e8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="456e8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="456e8-126">CommonParameters</span></span>
<span data-ttu-id="456e8-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="456e8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="456e8-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="456e8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="456e8-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="456e8-129">INPUTS</span></span>

### <span data-ttu-id="456e8-130">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="456e8-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="456e8-131">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="456e8-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="456e8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="456e8-132">OUTPUTS</span></span>

### <span data-ttu-id="456e8-133">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="456e8-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="456e8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="456e8-134">NOTES</span></span>

## <span data-ttu-id="456e8-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="456e8-135">RELATED LINKS</span></span>

