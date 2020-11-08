---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: 575dadabfeae1ec075f4ceab47bff99b3fd6b426
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092767"
---
# <span data-ttu-id="690a5-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="690a5-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="690a5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="690a5-102">SYNOPSIS</span></span>
<span data-ttu-id="690a5-103">Ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="690a5-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="690a5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="690a5-104">SYNTAX</span></span>

### <span data-ttu-id="690a5-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="690a5-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="690a5-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="690a5-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="690a5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="690a5-107">DESCRIPTION</span></span>
<span data-ttu-id="690a5-108">Cmdleten **set-AzVMBootDiagnostic** ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="690a5-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="690a5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="690a5-109">EXAMPLES</span></span>

### <span data-ttu-id="690a5-110">Exempel 1: Aktivera startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="690a5-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="690a5-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="690a5-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="690a5-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="690a5-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="690a5-113">Det andra kommandot aktiverar startdiagnostik för den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="690a5-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="690a5-114">Diagnostikdata lagras på det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="690a5-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="690a5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="690a5-115">PARAMETERS</span></span>

### <span data-ttu-id="690a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690a5-116">-DefaultProfile</span></span>
<span data-ttu-id="690a5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="690a5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="690a5-118">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="690a5-118">-Disable</span></span>
<span data-ttu-id="690a5-119">Anger att den här cmdleten inaktiverar startdiagnostiken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="690a5-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a5-120">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="690a5-120">-Enable</span></span>
<span data-ttu-id="690a5-121">Anger att denna cmdlet aktiverar start Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="690a5-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="690a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="690a5-123">Anger namnet på resurs gruppen för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="690a5-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690a5-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="690a5-124">-StorageAccountName</span></span>
<span data-ttu-id="690a5-125">Anger namnet på det lagrings konto där Boot Diagnostics-data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="690a5-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690a5-126">-VM</span><span class="sxs-lookup"><span data-stu-id="690a5-126">-VM</span></span>
<span data-ttu-id="690a5-127">Anger den virtuella dator för vilken denna cmdlet ändrar startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="690a5-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="690a5-128">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="690a5-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="690a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690a5-129">CommonParameters</span></span>
<span data-ttu-id="690a5-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="690a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690a5-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="690a5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690a5-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="690a5-132">INPUTS</span></span>

### <span data-ttu-id="690a5-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="690a5-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="690a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="690a5-134">System.String</span></span>

## <span data-ttu-id="690a5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="690a5-135">OUTPUTS</span></span>

### <span data-ttu-id="690a5-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="690a5-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="690a5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="690a5-137">NOTES</span></span>

## <span data-ttu-id="690a5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="690a5-138">RELATED LINKS</span></span>

[<span data-ttu-id="690a5-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="690a5-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="690a5-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="690a5-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


