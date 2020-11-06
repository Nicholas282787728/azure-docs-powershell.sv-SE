---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4dbae539d43961d954dba6ea12bd88e08d9616ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578311"
---
# <span data-ttu-id="04730-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="04730-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04730-102">SYNOPSIS</span></span>
<span data-ttu-id="04730-103">Hämtar egenskaperna för en virtuell dator med Azure Resource Manager (ARM).</span><span class="sxs-lookup"><span data-stu-id="04730-103">Gets the properties of an Azure Resource Manager (ARM) virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04730-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04730-104">SYNTAX</span></span>

### <span data-ttu-id="04730-105">ListAllVirtualMachinesParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="04730-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04730-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="04730-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04730-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="04730-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04730-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="04730-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04730-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04730-109">DESCRIPTION</span></span>
<span data-ttu-id="04730-110">Cmdleten **Get-AzureRmVM** hämtar vyn modell och instans för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="04730-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="04730-111">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="04730-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="04730-112">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="04730-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="04730-113">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="04730-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="04730-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04730-114">EXAMPLES</span></span>

### <span data-ttu-id="04730-115">Exempel 1: Hämta egenskaper för modell och instans</span><span class="sxs-lookup"><span data-stu-id="04730-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="04730-116">Det här kommandot hämtar egenskaperna för vyn modell och vyn för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="04730-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="04730-117">Exempel 2: Hämta egenskaper för instans</span><span class="sxs-lookup"><span data-stu-id="04730-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="04730-118">Det här kommandot får egenskaper för den virtuella datorn som heter VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="04730-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="04730-119">Det här kommandot anger *status* -parametern.</span><span class="sxs-lookup"><span data-stu-id="04730-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="04730-120">Därför får kommandot bara till förekomst egenskaperna för vyn.</span><span class="sxs-lookup"><span data-stu-id="04730-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="04730-121">Exempel 3: Hämta egenskaper för alla virtuella datorer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="04730-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="04730-122">Det här kommandot får egenskaper för alla virtuella datorer i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="04730-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="04730-123">Exempel 4: Hämta alla virtuella datorer i ditt abonnemang</span><span class="sxs-lookup"><span data-stu-id="04730-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="04730-124">Det här kommandot får alla virtuella datorer i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="04730-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="04730-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04730-125">PARAMETERS</span></span>

### <span data-ttu-id="04730-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04730-126">-DefaultProfile</span></span>
<span data-ttu-id="04730-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04730-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04730-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="04730-128">-DisplayHint</span></span>
<span data-ttu-id="04730-129">Bestämmer hur det virtuella datorobjektet visas.</span><span class="sxs-lookup"><span data-stu-id="04730-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="04730-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="04730-130">Valid values are:</span></span>

<span data-ttu-id="04730-131">--Kompakt: visar endast de högsta nivå egenskaperna</span><span class="sxs-lookup"><span data-stu-id="04730-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="04730-132">--Expand: visar alla egenskaper på alla nivåer</span><span class="sxs-lookup"><span data-stu-id="04730-132">-- Expand: displays all properties in all levels</span></span>
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04730-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="04730-133">-Name</span></span>
<span data-ttu-id="04730-134">Anger namnet på den virtuella dator som ska visas.</span><span class="sxs-lookup"><span data-stu-id="04730-134">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04730-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="04730-135">-NextLink</span></span>
<span data-ttu-id="04730-136">Anger nästa länk.</span><span class="sxs-lookup"><span data-stu-id="04730-136">Specifies the next link.</span></span>

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04730-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04730-137">-ResourceGroupName</span></span>
<span data-ttu-id="04730-138">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="04730-138">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04730-139">-Status</span><span class="sxs-lookup"><span data-stu-id="04730-139">-Status</span></span>
<span data-ttu-id="04730-140">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="04730-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04730-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04730-141">CommonParameters</span></span>
<span data-ttu-id="04730-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04730-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04730-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04730-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04730-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04730-144">INPUTS</span></span>

### <span data-ttu-id="04730-145">Ingen</span><span class="sxs-lookup"><span data-stu-id="04730-145">None</span></span>
<span data-ttu-id="04730-146">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="04730-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04730-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04730-147">OUTPUTS</span></span>

### <span data-ttu-id="04730-148">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="04730-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="04730-149">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="04730-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="04730-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04730-150">NOTES</span></span>

## <span data-ttu-id="04730-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04730-151">RELATED LINKS</span></span>

[<span data-ttu-id="04730-152">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-152">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="04730-153">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-153">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="04730-154">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-154">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="04730-155">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-155">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="04730-156">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-156">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="04730-157">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="04730-157">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


