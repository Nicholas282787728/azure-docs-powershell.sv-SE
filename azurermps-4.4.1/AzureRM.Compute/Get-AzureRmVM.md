---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: afe5c168c9a5f3633ce4766df5938a81ccc60510
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755509"
---
# <span data-ttu-id="6587c-101">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-101">Get-AzureRmVM</span></span>

## <span data-ttu-id="6587c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6587c-102">SYNOPSIS</span></span>
<span data-ttu-id="6587c-103">Hämtar egenskaperna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6587c-103">Gets the properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6587c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6587c-104">SYNTAX</span></span>

### <span data-ttu-id="6587c-105">ListAllVirtualMachinesParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6587c-105">ListAllVirtualMachinesParamSet (Default)</span></span>
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6587c-106">ListVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="6587c-106">ListVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6587c-107">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="6587c-107">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6587c-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="6587c-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6587c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6587c-109">DESCRIPTION</span></span>
<span data-ttu-id="6587c-110">Cmdleten **Get-AzureRmVM** hämtar vyn modell och instans för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="6587c-110">The **Get-AzureRmVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="6587c-111">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="6587c-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="6587c-112">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="6587c-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="6587c-113">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="6587c-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="6587c-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6587c-114">EXAMPLES</span></span>

### <span data-ttu-id="6587c-115">Exempel 1: Hämta egenskaper för modell och instans</span><span class="sxs-lookup"><span data-stu-id="6587c-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6587c-116">Det här kommandot hämtar egenskaperna för vyn modell och vyn för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6587c-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="6587c-117">Exempel 2: Hämta egenskaper för instans</span><span class="sxs-lookup"><span data-stu-id="6587c-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

<span data-ttu-id="6587c-118">Det här kommandot får egenskaper för den virtuella datorn som heter VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="6587c-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="6587c-119">Det här kommandot anger *status* -parametern.</span><span class="sxs-lookup"><span data-stu-id="6587c-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="6587c-120">Därför får kommandot bara till förekomst egenskaperna för vyn.</span><span class="sxs-lookup"><span data-stu-id="6587c-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="6587c-121">Exempel 3: Hämta egenskaper för alla virtuella datorer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="6587c-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="6587c-122">Det här kommandot får egenskaper för alla virtuella datorer i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6587c-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="6587c-123">Exempel 4: Hämta alla virtuella datorer i ditt abonnemang</span><span class="sxs-lookup"><span data-stu-id="6587c-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzureRmVM
```

<span data-ttu-id="6587c-124">Det här kommandot får alla virtuella datorer i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="6587c-124">This command gets all the virtual machines in your subscription.</span></span>

## <span data-ttu-id="6587c-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6587c-125">PARAMETERS</span></span>

### <span data-ttu-id="6587c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6587c-126">-DefaultProfile</span></span>
<span data-ttu-id="6587c-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6587c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6587c-128">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="6587c-128">-DisplayHint</span></span>
<span data-ttu-id="6587c-129">Bestämmer hur det virtuella datorobjektet visas.</span><span class="sxs-lookup"><span data-stu-id="6587c-129">Determines how the virtual machine object is displayed.</span></span>

<span data-ttu-id="6587c-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="6587c-130">Valid values are:</span></span>

<span data-ttu-id="6587c-131">--Kompakt: visar endast de högsta nivå egenskaperna</span><span class="sxs-lookup"><span data-stu-id="6587c-131">-- Compact: displays only top level properties</span></span>

<span data-ttu-id="6587c-132">--Expand: visar alla egenskaper på alla nivåer</span><span class="sxs-lookup"><span data-stu-id="6587c-132">-- Expand: displays all properties in all levels</span></span>
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

### <span data-ttu-id="6587c-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="6587c-133">-Name</span></span>
<span data-ttu-id="6587c-134">Anger namnet på den virtuella dator som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6587c-134">Specifies the name of the virtual machine to get.</span></span>

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

### <span data-ttu-id="6587c-135">-NextLink</span><span class="sxs-lookup"><span data-stu-id="6587c-135">-NextLink</span></span>
<span data-ttu-id="6587c-136">Anger nästa länk.</span><span class="sxs-lookup"><span data-stu-id="6587c-136">Specifies the next link.</span></span>

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

### <span data-ttu-id="6587c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6587c-137">-ResourceGroupName</span></span>
<span data-ttu-id="6587c-138">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6587c-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6587c-139">-Status</span><span class="sxs-lookup"><span data-stu-id="6587c-139">-Status</span></span>
<span data-ttu-id="6587c-140">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="6587c-140">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="6587c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6587c-141">CommonParameters</span></span>
<span data-ttu-id="6587c-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6587c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6587c-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6587c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6587c-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6587c-144">INPUTS</span></span>

## <span data-ttu-id="6587c-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6587c-145">OUTPUTS</span></span>

## <span data-ttu-id="6587c-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6587c-146">NOTES</span></span>

## <span data-ttu-id="6587c-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6587c-147">RELATED LINKS</span></span>

[<span data-ttu-id="6587c-148">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-148">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="6587c-149">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-149">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="6587c-150">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-150">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="6587c-151">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-151">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="6587c-152">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-152">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="6587c-153">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6587c-153">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


