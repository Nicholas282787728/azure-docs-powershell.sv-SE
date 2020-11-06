---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576622"
---
# <span data-ttu-id="4133b-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4133b-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="4133b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4133b-102">SYNOPSIS</span></span>
<span data-ttu-id="4133b-103">Lägger till ett nätverks gränssnitt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4133b-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4133b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4133b-104">SYNTAX</span></span>

### <span data-ttu-id="4133b-105">GetNicFromNicId (standard)</span><span class="sxs-lookup"><span data-stu-id="4133b-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="4133b-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="4133b-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="4133b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4133b-107">DESCRIPTION</span></span>
<span data-ttu-id="4133b-108">Cmdleten **Add-AzureRmVMNetworkInterface** lägger till ett nätverks gränssnitt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4133b-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="4133b-109">Du kan lägga till ett gränssnitt när du skapar en virtuell dator eller lägger till en på en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4133b-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="4133b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4133b-110">EXAMPLES</span></span>

### <span data-ttu-id="4133b-111">Exempel 1: lägga till ett nätverks gränssnitt till en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4133b-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="4133b-112">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="4133b-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4133b-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="4133b-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="4133b-114">Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4133b-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="4133b-115">Exempel 2: lägga till ett nätverks gränssnitt till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="4133b-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="4133b-116">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="4133b-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="4133b-117">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="4133b-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="4133b-118">Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4133b-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="4133b-119">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4133b-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="4133b-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4133b-120">PARAMETERS</span></span>

### <span data-ttu-id="4133b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4133b-121">-Id</span></span>
<span data-ttu-id="4133b-122">Anger ID för ett nätverks gränssnitt att lägga till på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4133b-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="4133b-123">Du kan använda cmdleten [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) för att få ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4133b-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4133b-124">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4133b-124">-NetworkInterface</span></span>
<span data-ttu-id="4133b-125">Anger nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4133b-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4133b-126">-Primär</span><span class="sxs-lookup"><span data-stu-id="4133b-126">-Primary</span></span>
<span data-ttu-id="4133b-127">Anger att nätverks gränssnittet läggs till i det primära gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="4133b-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4133b-128">-VM</span><span class="sxs-lookup"><span data-stu-id="4133b-128">-VM</span></span>
<span data-ttu-id="4133b-129">Anger ett lokalt virtuellt dator objekt där du kan lägga till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="4133b-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="4133b-130">Använd cmdleten **New-AzureRmVMConfig** för att skapa en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4133b-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="4133b-131">Använd cmdleten **Get-AzureRmVM** för att få en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4133b-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="4133b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4133b-132">CommonParameters</span></span>
<span data-ttu-id="4133b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4133b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4133b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4133b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4133b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4133b-135">INPUTS</span></span>

### <span data-ttu-id="4133b-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="4133b-136">None</span></span>
<span data-ttu-id="4133b-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4133b-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4133b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4133b-138">OUTPUTS</span></span>

## <span data-ttu-id="4133b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4133b-139">NOTES</span></span>

## <span data-ttu-id="4133b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4133b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4133b-141">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4133b-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="4133b-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4133b-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4133b-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="4133b-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
