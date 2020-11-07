---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: 411e822153c0b95bbf30829f8da915039d01ea32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928910"
---
# <span data-ttu-id="86ca8-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="86ca8-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="86ca8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="86ca8-103">Tar bort en datadisk från VMSS.</span><span class="sxs-lookup"><span data-stu-id="86ca8-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ca8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86ca8-104">SYNTAX</span></span>

### <span data-ttu-id="86ca8-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ca8-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ca8-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="86ca8-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ca8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86ca8-107">DESCRIPTION</span></span>
<span data-ttu-id="86ca8-108">Cmdleten **Remove-AzureRmVmssDataDisk** tar bort en datadisk från den virtuella datorns Scale set-instans (VMSS).</span><span class="sxs-lookup"><span data-stu-id="86ca8-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="86ca8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86ca8-109">EXAMPLES</span></span>

### <span data-ttu-id="86ca8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="86ca8-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="86ca8-111">Det här kommandot tar bort data disken ' DataDisk1 ' från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="86ca8-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="86ca8-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="86ca8-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="86ca8-113">Det här kommandot tar bort data disken för LUN 0 från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="86ca8-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="86ca8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86ca8-114">PARAMETERS</span></span>

### <span data-ttu-id="86ca8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ca8-115">-DefaultProfile</span></span>
<span data-ttu-id="86ca8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86ca8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86ca8-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="86ca8-117">-Lun</span></span>
<span data-ttu-id="86ca8-118">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="86ca8-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="86ca8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="86ca8-119">-Name</span></span>
<span data-ttu-id="86ca8-120">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="86ca8-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="86ca8-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="86ca8-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="86ca8-122">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="86ca8-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="86ca8-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="86ca8-123">-Confirm</span></span>
<span data-ttu-id="86ca8-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="86ca8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ca8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ca8-125">-WhatIf</span></span>
<span data-ttu-id="86ca8-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="86ca8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ca8-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="86ca8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ca8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ca8-128">CommonParameters</span></span>
<span data-ttu-id="86ca8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ca8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ca8-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ca8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ca8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86ca8-131">INPUTS</span></span>

### <span data-ttu-id="86ca8-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="86ca8-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="86ca8-133">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="86ca8-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="86ca8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86ca8-134">OUTPUTS</span></span>

### <span data-ttu-id="86ca8-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="86ca8-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="86ca8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86ca8-136">NOTES</span></span>

## <span data-ttu-id="86ca8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86ca8-137">RELATED LINKS</span></span>

