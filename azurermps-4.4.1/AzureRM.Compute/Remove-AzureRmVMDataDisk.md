---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 774166f88e4ca94e5e21c2b96817596c082a429c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573709"
---
# <span data-ttu-id="65590-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="65590-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="65590-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65590-102">SYNOPSIS</span></span>
<span data-ttu-id="65590-103">Tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="65590-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65590-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65590-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65590-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65590-105">DESCRIPTION</span></span>
<span data-ttu-id="65590-106">Cmdleten **Remove-AzureRmVMDataDisk** tar bort en datadisk från en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="65590-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="65590-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65590-107">EXAMPLES</span></span>

### <span data-ttu-id="65590-108">Exempel 1: ta bort en data disk från en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="65590-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="65590-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="65590-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="65590-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="65590-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="65590-111">Det andra kommandot tar bort data disken med namnet Disk3 från den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="65590-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="65590-112">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="65590-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="65590-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65590-113">PARAMETERS</span></span>

### <span data-ttu-id="65590-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="65590-114">-DataDiskNames</span></span>
<span data-ttu-id="65590-115">Anger namnen på en eller flera data diskar som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="65590-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65590-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65590-116">-DefaultProfile</span></span>
<span data-ttu-id="65590-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65590-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65590-118">-VM</span><span class="sxs-lookup"><span data-stu-id="65590-118">-VM</span></span>
<span data-ttu-id="65590-119">Anger det lokala virtuella dator objekt som du kan ta bort en data disk från.</span><span class="sxs-lookup"><span data-stu-id="65590-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="65590-120">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="65590-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65590-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65590-121">-Confirm</span></span>
<span data-ttu-id="65590-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65590-122">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65590-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65590-123">-WhatIf</span></span>
<span data-ttu-id="65590-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65590-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65590-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65590-125">The cmdlet is not run.</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65590-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65590-126">CommonParameters</span></span>
<span data-ttu-id="65590-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65590-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65590-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65590-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65590-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65590-129">INPUTS</span></span>

## <span data-ttu-id="65590-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65590-130">OUTPUTS</span></span>

## <span data-ttu-id="65590-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65590-131">NOTES</span></span>

## <span data-ttu-id="65590-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65590-132">RELATED LINKS</span></span>

[<span data-ttu-id="65590-133">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="65590-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="65590-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="65590-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


