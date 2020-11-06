---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575708"
---
# <span data-ttu-id="df7a3-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="df7a3-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="df7a3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="df7a3-102">SYNOPSIS</span></span>
<span data-ttu-id="df7a3-103">Ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="df7a3-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df7a3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="df7a3-104">SYNTAX</span></span>

### <span data-ttu-id="df7a3-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="df7a3-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="df7a3-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="df7a3-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="df7a3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="df7a3-107">DESCRIPTION</span></span>
<span data-ttu-id="df7a3-108">Cmdleten **set-AzureRmVMBootDiagnostics** ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="df7a3-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="df7a3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="df7a3-109">EXAMPLES</span></span>

### <span data-ttu-id="df7a3-110">Exempel 1: Aktivera startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="df7a3-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="df7a3-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="df7a3-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="df7a3-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="df7a3-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="df7a3-113">Det andra kommandot aktiverar startdiagnostik för den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="df7a3-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="df7a3-114">Diagnostikdata lagras på det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="df7a3-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="df7a3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="df7a3-115">PARAMETERS</span></span>

### <span data-ttu-id="df7a3-116">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="df7a3-116">-Disable</span></span>
<span data-ttu-id="df7a3-117">Anger att den här cmdleten inaktiverar startdiagnostiken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="df7a3-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7a3-118">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="df7a3-118">-Enable</span></span>
<span data-ttu-id="df7a3-119">Anger att denna cmdlet aktiverar start Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="df7a3-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df7a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df7a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="df7a3-121">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="df7a3-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7a3-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="df7a3-122">-StorageAccountName</span></span>
<span data-ttu-id="df7a3-123">Anger namnet på det lagrings konto där Boot Diagnostics-data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="df7a3-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df7a3-124">-VM</span><span class="sxs-lookup"><span data-stu-id="df7a3-124">-VM</span></span>
<span data-ttu-id="df7a3-125">Anger den virtuella dator för vilken denna cmdlet ändrar startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="df7a3-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="df7a3-126">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="df7a3-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="df7a3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df7a3-127">CommonParameters</span></span>
<span data-ttu-id="df7a3-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df7a3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df7a3-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df7a3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df7a3-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="df7a3-130">INPUTS</span></span>

### <span data-ttu-id="df7a3-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="df7a3-131">None</span></span>
<span data-ttu-id="df7a3-132">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="df7a3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df7a3-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="df7a3-133">OUTPUTS</span></span>

## <span data-ttu-id="df7a3-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="df7a3-134">NOTES</span></span>

## <span data-ttu-id="df7a3-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="df7a3-135">RELATED LINKS</span></span>

[<span data-ttu-id="df7a3-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="df7a3-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="df7a3-137">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="df7a3-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


