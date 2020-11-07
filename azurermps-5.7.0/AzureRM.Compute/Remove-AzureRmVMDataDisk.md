---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755774"
---
# <span data-ttu-id="33107-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="33107-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="33107-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="33107-102">SYNOPSIS</span></span>
<span data-ttu-id="33107-103">Tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="33107-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33107-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="33107-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33107-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="33107-105">DESCRIPTION</span></span>
<span data-ttu-id="33107-106">Cmdleten **Remove-AzureRmVMDataDisk** tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="33107-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="33107-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="33107-107">EXAMPLES</span></span>

### <span data-ttu-id="33107-108">Exempel 1: ta bort en data disk från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="33107-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="33107-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="33107-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="33107-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="33107-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="33107-111">Det andra kommandot tar bort data disken med namnet Disk3 från den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="33107-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="33107-112">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="33107-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="33107-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="33107-113">PARAMETERS</span></span>

### <span data-ttu-id="33107-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="33107-114">-DataDiskNames</span></span>
<span data-ttu-id="33107-115">Anger namnen på en eller flera data diskar som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="33107-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33107-116">-VM</span><span class="sxs-lookup"><span data-stu-id="33107-116">-VM</span></span>
<span data-ttu-id="33107-117">Anger det lokala virtuella dator objekt som du kan ta bort en data disk från.</span><span class="sxs-lookup"><span data-stu-id="33107-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="33107-118">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="33107-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33107-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="33107-119">-Confirm</span></span>
<span data-ttu-id="33107-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="33107-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33107-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33107-121">-WhatIf</span></span>
<span data-ttu-id="33107-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="33107-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33107-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="33107-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33107-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33107-124">CommonParameters</span></span>
<span data-ttu-id="33107-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33107-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33107-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33107-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33107-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="33107-127">INPUTS</span></span>

### <span data-ttu-id="33107-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="33107-128">None</span></span>
<span data-ttu-id="33107-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="33107-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33107-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="33107-130">OUTPUTS</span></span>

## <span data-ttu-id="33107-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="33107-131">NOTES</span></span>

## <span data-ttu-id="33107-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="33107-132">RELATED LINKS</span></span>

[<span data-ttu-id="33107-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="33107-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="33107-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="33107-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


