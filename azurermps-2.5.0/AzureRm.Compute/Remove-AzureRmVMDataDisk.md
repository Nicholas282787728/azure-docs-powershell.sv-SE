---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: ea8b069be4b153e6e4ca295a917e1c3e81629094
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930334"
---
# <span data-ttu-id="c7fe0-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c7fe0-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="c7fe0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fe0-103">Tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7fe0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7fe0-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7fe0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7fe0-105">DESCRIPTION</span></span>
<span data-ttu-id="c7fe0-106">Cmdleten **Remove-AzureRmVMDataDisk** tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="c7fe0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7fe0-107">EXAMPLES</span></span>

### <span data-ttu-id="c7fe0-108">Exempel 1: ta bort en data disk från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c7fe0-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="c7fe0-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="c7fe0-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="c7fe0-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="c7fe0-111">Det andra kommandot tar bort data disken med namnet Disk3 från den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="c7fe0-112">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="c7fe0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7fe0-113">PARAMETERS</span></span>

### <span data-ttu-id="c7fe0-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="c7fe0-114">-DataDiskNames</span></span>
<span data-ttu-id="c7fe0-115">Anger namnen på en eller flera data diskar som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c7fe0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fe0-116">-DefaultProfile</span></span>
<span data-ttu-id="c7fe0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7fe0-118">-VM</span><span class="sxs-lookup"><span data-stu-id="c7fe0-118">-VM</span></span>
<span data-ttu-id="c7fe0-119">Anger det lokala virtuella dator objekt som du kan ta bort en data disk från.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="c7fe0-120">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="c7fe0-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7fe0-121">-Confirm</span></span>
<span data-ttu-id="c7fe0-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="c7fe0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7fe0-123">-WhatIf</span></span>
<span data-ttu-id="c7fe0-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7fe0-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="c7fe0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fe0-126">CommonParameters</span></span>
<span data-ttu-id="c7fe0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fe0-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7fe0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fe0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7fe0-129">INPUTS</span></span>

### <span data-ttu-id="c7fe0-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c7fe0-130">PSVirtualMachine</span></span>
<span data-ttu-id="c7fe0-131">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c7fe0-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="c7fe0-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7fe0-132">OUTPUTS</span></span>

### <span data-ttu-id="c7fe0-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c7fe0-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c7fe0-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7fe0-134">NOTES</span></span>

## <span data-ttu-id="c7fe0-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7fe0-135">RELATED LINKS</span></span>

[<span data-ttu-id="c7fe0-136">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c7fe0-136">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="c7fe0-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c7fe0-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


