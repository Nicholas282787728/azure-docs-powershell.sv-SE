---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 3529ca1d26504558036f3496c9bc75ec10e666ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924954"
---
# <span data-ttu-id="774fb-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="774fb-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="774fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="774fb-102">SYNOPSIS</span></span>
<span data-ttu-id="774fb-103">Tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="774fb-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="774fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="774fb-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="774fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="774fb-105">DESCRIPTION</span></span>
<span data-ttu-id="774fb-106">Cmdleten **Remove-AzVMDataDisk** tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="774fb-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="774fb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="774fb-107">EXAMPLES</span></span>

### <span data-ttu-id="774fb-108">Exempel 1: ta bort en data disk från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="774fb-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="774fb-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="774fb-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="774fb-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="774fb-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="774fb-111">Det andra kommandot tar bort data disken med namnet Disk3 från den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="774fb-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="774fb-112">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="774fb-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="774fb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="774fb-113">PARAMETERS</span></span>

### <span data-ttu-id="774fb-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="774fb-114">-DataDiskNames</span></span>
<span data-ttu-id="774fb-115">Anger namnen på en eller flera data diskar som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="774fb-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="774fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="774fb-116">-DefaultProfile</span></span>
<span data-ttu-id="774fb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="774fb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="774fb-118">-VM</span><span class="sxs-lookup"><span data-stu-id="774fb-118">-VM</span></span>
<span data-ttu-id="774fb-119">Anger det lokala virtuella dator objekt som du kan ta bort en data disk från.</span><span class="sxs-lookup"><span data-stu-id="774fb-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="774fb-120">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="774fb-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="774fb-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="774fb-121">-Confirm</span></span>
<span data-ttu-id="774fb-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="774fb-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="774fb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="774fb-123">-WhatIf</span></span>
<span data-ttu-id="774fb-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="774fb-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="774fb-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="774fb-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="774fb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="774fb-126">CommonParameters</span></span>
<span data-ttu-id="774fb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="774fb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="774fb-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="774fb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="774fb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="774fb-129">INPUTS</span></span>

### <span data-ttu-id="774fb-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="774fb-130">PSVirtualMachine</span></span>
<span data-ttu-id="774fb-131">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="774fb-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="774fb-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="774fb-132">OUTPUTS</span></span>

### <span data-ttu-id="774fb-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="774fb-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="774fb-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="774fb-134">NOTES</span></span>

## <span data-ttu-id="774fb-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="774fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="774fb-136">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="774fb-136">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="774fb-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="774fb-137">Get-AzVM</span></span>](./Get-AzVM.md)


