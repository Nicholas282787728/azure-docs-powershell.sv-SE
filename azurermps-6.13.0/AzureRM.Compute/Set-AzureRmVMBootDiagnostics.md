---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 290c726c53ea4479c4bd1f3cb9b2c607c04f20cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757120"
---
# <span data-ttu-id="3e628-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3e628-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="3e628-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e628-102">SYNOPSIS</span></span>
<span data-ttu-id="3e628-103">Ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3e628-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e628-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e628-104">SYNTAX</span></span>

### <span data-ttu-id="3e628-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3e628-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e628-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3e628-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e628-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e628-107">DESCRIPTION</span></span>
<span data-ttu-id="3e628-108">Cmdleten **set-AzureRmVMBootDiagnostics** ändrar startdiagnostik egenskaper för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="3e628-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="3e628-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e628-109">EXAMPLES</span></span>

### <span data-ttu-id="3e628-110">Exempel 1: Aktivera startdiagnostik</span><span class="sxs-lookup"><span data-stu-id="3e628-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="3e628-111">Det första kommandot får den virtuella datorn med namnet ContosoVM07 med hjälp av **Get-AzureRmVM**.</span><span class="sxs-lookup"><span data-stu-id="3e628-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="3e628-112">Kommandot sparar det i $VM variabel.</span><span class="sxs-lookup"><span data-stu-id="3e628-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="3e628-113">Det andra kommandot aktiverar startdiagnostik för den virtuella datorn i $VM.</span><span class="sxs-lookup"><span data-stu-id="3e628-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="3e628-114">Diagnostikdata lagras på det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="3e628-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="3e628-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e628-115">PARAMETERS</span></span>

### <span data-ttu-id="3e628-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e628-116">-DefaultProfile</span></span>
<span data-ttu-id="3e628-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e628-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e628-118">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="3e628-118">-Disable</span></span>
<span data-ttu-id="3e628-119">Anger att den här cmdleten inaktiverar startdiagnostiken för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3e628-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="3e628-120">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="3e628-120">-Enable</span></span>
<span data-ttu-id="3e628-121">Anger att denna cmdlet aktiverar start Diagnostics för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3e628-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="3e628-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e628-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e628-123">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="3e628-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3e628-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e628-124">-StorageAccountName</span></span>
<span data-ttu-id="3e628-125">Anger namnet på det lagrings konto där Boot Diagnostics-data ska sparas.</span><span class="sxs-lookup"><span data-stu-id="3e628-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="3e628-126">-VM</span><span class="sxs-lookup"><span data-stu-id="3e628-126">-VM</span></span>
<span data-ttu-id="3e628-127">Anger den virtuella dator för vilken denna cmdlet ändrar startdiagnostik.</span><span class="sxs-lookup"><span data-stu-id="3e628-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="3e628-128">Använd Get-AzureRmVM cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="3e628-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="3e628-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e628-129">CommonParameters</span></span>
<span data-ttu-id="3e628-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e628-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e628-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e628-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e628-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e628-132">INPUTS</span></span>

### <span data-ttu-id="3e628-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3e628-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="3e628-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3e628-134">System.String</span></span>

## <span data-ttu-id="3e628-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e628-135">OUTPUTS</span></span>

### <span data-ttu-id="3e628-136">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3e628-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3e628-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e628-137">NOTES</span></span>

## <span data-ttu-id="3e628-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e628-138">RELATED LINKS</span></span>

[<span data-ttu-id="3e628-139">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3e628-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="3e628-140">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="3e628-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


