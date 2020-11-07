---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: e3e03083e831f38143423e69c84a67bfbc0440db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924822"
---
# <span data-ttu-id="66fa2-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="66fa2-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="66fa2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="66fa2-103">Ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="66fa2-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="66fa2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66fa2-104">SYNTAX</span></span>

### <span data-ttu-id="66fa2-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="66fa2-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66fa2-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="66fa2-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66fa2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66fa2-107">DESCRIPTION</span></span>
<span data-ttu-id="66fa2-108">Cmdleten **set-AzVMBootDiagnostic** ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="66fa2-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="66fa2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66fa2-109">EXAMPLES</span></span>

### <span data-ttu-id="66fa2-110">Exempel 1: Aktivera startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="66fa2-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="66fa2-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzVM**.</span><span class="sxs-lookup"><span data-stu-id="66fa2-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="66fa2-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="66fa2-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="66fa2-113">Det andra kommandot aktiverar startdiagnostik för den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="66fa2-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="66fa2-114">Diagnostikdata lagras på det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="66fa2-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="66fa2-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66fa2-115">PARAMETERS</span></span>

### <span data-ttu-id="66fa2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fa2-116">-DefaultProfile</span></span>
<span data-ttu-id="66fa2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66fa2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66fa2-118">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="66fa2-118">-Disable</span></span>
<span data-ttu-id="66fa2-119">Anger att den här cmdleten inaktiverar startdiagnostiken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="66fa2-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="66fa2-120">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="66fa2-120">-Enable</span></span>
<span data-ttu-id="66fa2-121">Anger att denna cmdlet aktiverar start Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="66fa2-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="66fa2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fa2-122">-ResourceGroupName</span></span>
<span data-ttu-id="66fa2-123">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="66fa2-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="66fa2-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="66fa2-124">-StorageAccountName</span></span>
<span data-ttu-id="66fa2-125">Anger namnet på det lagrings konto där Boot Diagnostics-data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="66fa2-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="66fa2-126">-VM</span><span class="sxs-lookup"><span data-stu-id="66fa2-126">-VM</span></span>
<span data-ttu-id="66fa2-127">Anger den virtuella dator för vilken denna cmdlet ändrar startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="66fa2-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="66fa2-128">Använd Get-AzVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="66fa2-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="66fa2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fa2-129">CommonParameters</span></span>
<span data-ttu-id="66fa2-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fa2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fa2-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66fa2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fa2-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66fa2-132">INPUTS</span></span>

### <span data-ttu-id="66fa2-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66fa2-133">PSVirtualMachine</span></span>
<span data-ttu-id="66fa2-134">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="66fa2-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="66fa2-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66fa2-135">OUTPUTS</span></span>

### <span data-ttu-id="66fa2-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66fa2-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="66fa2-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66fa2-137">NOTES</span></span>

## <span data-ttu-id="66fa2-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66fa2-138">RELATED LINKS</span></span>

[<span data-ttu-id="66fa2-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="66fa2-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="66fa2-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="66fa2-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


