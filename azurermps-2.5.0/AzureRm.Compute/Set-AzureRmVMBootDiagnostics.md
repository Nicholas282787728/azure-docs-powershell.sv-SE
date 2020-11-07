---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
ms.openlocfilehash: 2faa28fc0f0e4c27e384c178b96b8d38cae16a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930622"
---
# <span data-ttu-id="9352c-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9352c-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="9352c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9352c-102">SYNOPSIS</span></span>
<span data-ttu-id="9352c-103">Ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9352c-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9352c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9352c-104">SYNTAX</span></span>

### <span data-ttu-id="9352c-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9352c-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9352c-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="9352c-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9352c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9352c-107">DESCRIPTION</span></span>
<span data-ttu-id="9352c-108">Cmdleten **set-AzureRmVMBootDiagnostics** ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="9352c-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="9352c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9352c-109">EXAMPLES</span></span>

### <span data-ttu-id="9352c-110">Exempel 1: Aktivera startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="9352c-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="9352c-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="9352c-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="9352c-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="9352c-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="9352c-113">Det andra kommandot aktiverar startdiagnostik för den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="9352c-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="9352c-114">Diagnostikdata lagras på det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="9352c-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="9352c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9352c-115">PARAMETERS</span></span>

### <span data-ttu-id="9352c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9352c-116">-DefaultProfile</span></span>
<span data-ttu-id="9352c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9352c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9352c-118">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="9352c-118">-Disable</span></span>
<span data-ttu-id="9352c-119">Anger att den här cmdleten inaktiverar startdiagnostiken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9352c-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="9352c-120">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="9352c-120">-Enable</span></span>
<span data-ttu-id="9352c-121">Anger att denna cmdlet aktiverar start Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="9352c-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="9352c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9352c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9352c-123">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9352c-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9352c-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9352c-124">-StorageAccountName</span></span>
<span data-ttu-id="9352c-125">Anger namnet på det lagrings konto där Boot Diagnostics-data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="9352c-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="9352c-126">-VM</span><span class="sxs-lookup"><span data-stu-id="9352c-126">-VM</span></span>
<span data-ttu-id="9352c-127">Anger den virtuella dator för vilken denna cmdlet ändrar startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="9352c-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="9352c-128">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="9352c-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="9352c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9352c-129">CommonParameters</span></span>
<span data-ttu-id="9352c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9352c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9352c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9352c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9352c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9352c-132">INPUTS</span></span>

### <span data-ttu-id="9352c-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9352c-133">PSVirtualMachine</span></span>
<span data-ttu-id="9352c-134">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9352c-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9352c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9352c-135">OUTPUTS</span></span>

### <span data-ttu-id="9352c-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9352c-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9352c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9352c-137">NOTES</span></span>

## <span data-ttu-id="9352c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9352c-138">RELATED LINKS</span></span>

[<span data-ttu-id="9352c-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9352c-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9352c-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="9352c-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


