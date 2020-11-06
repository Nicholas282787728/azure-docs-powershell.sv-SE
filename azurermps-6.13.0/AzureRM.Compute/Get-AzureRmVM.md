---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575291"
---
# <span data-ttu-id="ccb07-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="ccb07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccb07-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb07-103">Hämtar egenskaperna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ccb07-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccb07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccb07-104">SYNTAX</span></span>

### <span data-ttu-id="ccb07-105">ListAllVirtualMachinesParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ccb07-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccb07-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ccb07-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ccb07-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ccb07-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccb07-108">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="ccb07-108">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccb07-109">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="ccb07-109">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccb07-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccb07-110">DESCRIPTION</span></span>
<span data-ttu-id="ccb07-111">Cmdleten **Get-AzureRmVM** hämtar vyn modell och instans för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="ccb07-111">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="ccb07-112">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="ccb07-112">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="ccb07-113">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="ccb07-113">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="ccb07-114">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ccb07-114">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="ccb07-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccb07-115">EXAMPLES</span></span>

### <span data-ttu-id="ccb07-116">Exempel 1: Hämta egenskaper för modell och instans</span><span class="sxs-lookup"><span data-stu-id="ccb07-116">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ccb07-117">Det här kommandot hämtar egenskaperna för vyn modell och vyn för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ccb07-117">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="ccb07-118">Exempel 2: Hämta egenskaper för instans</span><span class="sxs-lookup"><span data-stu-id="ccb07-118">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="ccb07-119">Det här kommandot får egenskaper för den virtuella datorn som heter VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="ccb07-119">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ccb07-120">Det här kommandot anger *status* -parametern.</span><span class="sxs-lookup"><span data-stu-id="ccb07-120">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="ccb07-121">Därför får kommandot bara till förekomst egenskaperna för vyn.</span><span class="sxs-lookup"><span data-stu-id="ccb07-121">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="ccb07-122">Exempel 3: Hämta egenskaper för alla virtuella datorer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ccb07-122">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ccb07-123">Det här kommandot får egenskaper för alla virtuella datorer i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ccb07-123">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ccb07-124">Exempel 4: Hämta alla virtuella datorer i ditt abonnemang</span><span class="sxs-lookup"><span data-stu-id="ccb07-124">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="ccb07-125">Det här kommandot får alla virtuella datorer i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ccb07-125">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="ccb07-126">Exempel 5: Hämta alla virtuella datorer på platsen.</span><span class="sxs-lookup"><span data-stu-id="ccb07-126">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzureRmVM -Location "westus"
```

<span data-ttu-id="ccb07-127">Det här kommandot får alla virtuella datorer i västra USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="ccb07-127">This command gets all the virtual machines in West US region.</span></span>

## <span data-ttu-id="ccb07-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccb07-128">PARAMETERS</span></span>

### <span data-ttu-id="ccb07-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb07-129">-DefaultProfile</span></span>
<span data-ttu-id="ccb07-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccb07-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccb07-131">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="ccb07-131">-DisplayHint</span></span>
<span data-ttu-id="ccb07-132">Bestämmer hur det virtuella datorobjektet visas.</span><span class="sxs-lookup"><span data-stu-id="ccb07-132">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="ccb07-133">Giltiga värden är:--Compact: visar endast de högsta nivå egenskaperna--Expand: visar alla egenskaper på alla nivåer</span><span class="sxs-lookup"><span data-stu-id="ccb07-133">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb07-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="ccb07-134">-Location</span></span>
<span data-ttu-id="ccb07-135">Anger en plats för de virtuella datorerna som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ccb07-135">Specifies a location for the virtual machines to list.</span></span>

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb07-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="ccb07-136">-Name</span></span>
<span data-ttu-id="ccb07-137">Anger namnet på den virtuella dator som ska visas.</span><span class="sxs-lookup"><span data-stu-id="ccb07-137">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb07-138">-NextLink</span><span class="sxs-lookup"><span data-stu-id="ccb07-138">-NextLink</span></span>
<span data-ttu-id="ccb07-139">Anger nästa länk.</span><span class="sxs-lookup"><span data-stu-id="ccb07-139">Specifies the next link.</span></span>

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb07-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb07-140">-ResourceGroupName</span></span>
<span data-ttu-id="ccb07-141">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ccb07-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb07-142">-Status</span><span class="sxs-lookup"><span data-stu-id="ccb07-142">-Status</span></span>
<span data-ttu-id="ccb07-143">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="ccb07-143">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccb07-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb07-144">CommonParameters</span></span>
<span data-ttu-id="ccb07-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb07-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb07-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb07-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb07-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccb07-147">INPUTS</span></span>

### <span data-ttu-id="ccb07-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ccb07-148">System.String</span></span>

### <span data-ttu-id="ccb07-149">System. URI</span><span class="sxs-lookup"><span data-stu-id="ccb07-149">System.Uri</span></span>

### <span data-ttu-id="ccb07-150">Microsoft. Azure. commands. Compute. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="ccb07-150">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="ccb07-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccb07-151">OUTPUTS</span></span>

### <span data-ttu-id="ccb07-152">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ccb07-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ccb07-153">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="ccb07-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="ccb07-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccb07-154">NOTES</span></span>

## <span data-ttu-id="ccb07-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccb07-155">RELATED LINKS</span></span>

[<span data-ttu-id="ccb07-156">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-156">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="ccb07-157">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-157">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="ccb07-158">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-158">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="ccb07-159">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-159">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="ccb07-160">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-160">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="ccb07-161">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ccb07-161">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


