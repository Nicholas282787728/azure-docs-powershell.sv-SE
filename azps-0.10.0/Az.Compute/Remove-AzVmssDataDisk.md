---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924929"
---
# <span data-ttu-id="d06b0-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="d06b0-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="d06b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d06b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d06b0-103">Tar bort en datadisk från VMSS.</span><span class="sxs-lookup"><span data-stu-id="d06b0-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="d06b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d06b0-104">SYNTAX</span></span>

### <span data-ttu-id="d06b0-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d06b0-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d06b0-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="d06b0-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d06b0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d06b0-107">DESCRIPTION</span></span>
<span data-ttu-id="d06b0-108">Cmdleten **Remove-AzVmssDataDisk** tar bort en datadisk från den virtuella datorns Scale set-instans (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d06b0-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="d06b0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d06b0-109">EXAMPLES</span></span>

### <span data-ttu-id="d06b0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d06b0-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="d06b0-111">Det här kommandot tar bort data disken ' DataDisk1 ' från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d06b0-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="d06b0-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d06b0-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="d06b0-113">Det här kommandot tar bort data disken för LUN 0 från VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d06b0-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="d06b0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d06b0-114">PARAMETERS</span></span>

### <span data-ttu-id="d06b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d06b0-115">-DefaultProfile</span></span>
<span data-ttu-id="d06b0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d06b0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d06b0-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="d06b0-117">-Lun</span></span>
<span data-ttu-id="d06b0-118">Anger diskens logiska enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="d06b0-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="d06b0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d06b0-119">-Name</span></span>
<span data-ttu-id="d06b0-120">Anger namnet på disken.</span><span class="sxs-lookup"><span data-stu-id="d06b0-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="d06b0-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d06b0-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d06b0-122">Ange VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="d06b0-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="d06b0-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d06b0-123">-Confirm</span></span>
<span data-ttu-id="d06b0-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d06b0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d06b0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d06b0-125">-WhatIf</span></span>
<span data-ttu-id="d06b0-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d06b0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d06b0-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d06b0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d06b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d06b0-128">CommonParameters</span></span>
<span data-ttu-id="d06b0-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d06b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d06b0-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d06b0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d06b0-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d06b0-131">INPUTS</span></span>

### <span data-ttu-id="d06b0-132">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d06b0-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="d06b0-133">System. String-system. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d06b0-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d06b0-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d06b0-134">OUTPUTS</span></span>

### <span data-ttu-id="d06b0-135">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d06b0-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="d06b0-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d06b0-136">NOTES</span></span>

## <span data-ttu-id="d06b0-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d06b0-137">RELATED LINKS</span></span>

