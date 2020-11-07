---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3ac2a0ba40b7bcd6b845bd069fced292e959cba5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745244"
---
# <span data-ttu-id="977d8-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="977d8-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="977d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="977d8-102">SYNOPSIS</span></span>
<span data-ttu-id="977d8-103">Lägger till ett nätverks gränssnitt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="977d8-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="977d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="977d8-104">SYNTAX</span></span>

### <span data-ttu-id="977d8-105">GetNicFromNicId (standard)</span><span class="sxs-lookup"><span data-stu-id="977d8-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="977d8-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="977d8-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="977d8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="977d8-107">DESCRIPTION</span></span>
<span data-ttu-id="977d8-108">Cmdleten **Add-AzVMNetworkInterface** lägger till ett nätverks gränssnitt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="977d8-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="977d8-109">Du kan lägga till ett gränssnitt när du skapar en virtuell dator eller lägger till en på en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="977d8-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="977d8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="977d8-110">EXAMPLES</span></span>

### <span data-ttu-id="977d8-111">Exempel 1: lägga till ett nätverks gränssnitt till en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="977d8-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="977d8-112">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="977d8-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="977d8-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="977d8-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="977d8-114">Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="977d8-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="977d8-115">Exempel 2: lägga till ett nätverks gränssnitt till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="977d8-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="977d8-116">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="977d8-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="977d8-117">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="977d8-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="977d8-118">Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="977d8-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="977d8-119">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="977d8-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="977d8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="977d8-120">PARAMETERS</span></span>

### <span data-ttu-id="977d8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977d8-121">-DefaultProfile</span></span>
<span data-ttu-id="977d8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="977d8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="977d8-123">-ID</span><span class="sxs-lookup"><span data-stu-id="977d8-123">-Id</span></span>
<span data-ttu-id="977d8-124">Anger ID för ett nätverks gränssnitt att lägga till på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="977d8-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="977d8-125">Du kan använda cmdleten [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) för att få ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="977d8-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="977d8-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="977d8-126">-NetworkInterface</span></span>
<span data-ttu-id="977d8-127">Anger nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="977d8-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="977d8-128">-Primär</span><span class="sxs-lookup"><span data-stu-id="977d8-128">-Primary</span></span>
<span data-ttu-id="977d8-129">Anger att nätverks gränssnittet läggs till i det primära gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="977d8-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="977d8-130">-VM</span><span class="sxs-lookup"><span data-stu-id="977d8-130">-VM</span></span>
<span data-ttu-id="977d8-131">Anger ett lokalt virtuellt dator objekt där du kan lägga till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="977d8-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="977d8-132">Använd cmdleten **New-AzVMConfig** för att skapa en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="977d8-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="977d8-133">Använd cmdleten **Get-AzVM** för att få en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="977d8-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

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

### <span data-ttu-id="977d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977d8-134">CommonParameters</span></span>
<span data-ttu-id="977d8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977d8-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="977d8-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977d8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="977d8-137">INPUTS</span></span>

### <span data-ttu-id="977d8-138">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="977d8-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="977d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="977d8-139">System.String</span></span>

### <span data-ttu-id="977d8-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Internal. Network. Common. INetworkInterfaceReference, Microsoft. Azure. PowerShell. clients. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="977d8-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="977d8-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="977d8-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="977d8-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="977d8-142">OUTPUTS</span></span>

### <span data-ttu-id="977d8-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="977d8-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="977d8-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="977d8-144">NOTES</span></span>

## <span data-ttu-id="977d8-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="977d8-145">RELATED LINKS</span></span>

[<span data-ttu-id="977d8-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="977d8-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="977d8-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="977d8-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="977d8-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="977d8-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
