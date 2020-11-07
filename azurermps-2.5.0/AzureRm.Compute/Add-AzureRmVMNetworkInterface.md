---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmnetworkinterface
schema: 2.0.0
ms.openlocfilehash: 112403f4cb742c5df39538eb2d8d8fac629d3379
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930754"
---
# <span data-ttu-id="aa4bc-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aa4bc-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="aa4bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa4bc-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4bc-103">Lägger till ett nätverks gränssnitt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa4bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa4bc-104">SYNTAX</span></span>

### <span data-ttu-id="aa4bc-105">GetNicFromNicId (standard)</span><span class="sxs-lookup"><span data-stu-id="aa4bc-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa4bc-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="aa4bc-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa4bc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa4bc-107">DESCRIPTION</span></span>
<span data-ttu-id="aa4bc-108">Cmdleten **Add-AzureRmVMNetworkInterface** lägger till ett nätverks gränssnitt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="aa4bc-109">Du kan lägga till ett gränssnitt när du skapar en virtuell dator eller lägger till en på en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="aa4bc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa4bc-110">EXAMPLES</span></span>

### <span data-ttu-id="aa4bc-111">Exempel 1: lägga till ett nätverks gränssnitt till en ny virtuell dator</span><span class="sxs-lookup"><span data-stu-id="aa4bc-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="aa4bc-112">Det första kommandot skapar ett virtuellt dator objekt och lagrar det sedan i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="aa4bc-113">Kommandot tilldelar den virtuella datorn ett namn och en storlek.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="aa4bc-114">Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="aa4bc-115">Exempel 2: lägga till ett nätverks gränssnitt till en befintlig virtuell dator</span><span class="sxs-lookup"><span data-stu-id="aa4bc-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="aa4bc-116">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="aa4bc-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="aa4bc-117">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="aa4bc-118">Det andra kommandot lägger till ett nätverks gränssnitt till den virtuella datorn som lagras i $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="aa4bc-119">Det sista kommandot uppdaterar tillståndet för den virtuella datorn som lagras i $VirtualMachine i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="aa4bc-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa4bc-120">PARAMETERS</span></span>

### <span data-ttu-id="aa4bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4bc-121">-DefaultProfile</span></span>
<span data-ttu-id="aa4bc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa4bc-123">-ID</span><span class="sxs-lookup"><span data-stu-id="aa4bc-123">-Id</span></span>
<span data-ttu-id="aa4bc-124">Anger ID för ett nätverks gränssnitt att lägga till på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="aa4bc-125">Du kan använda cmdleten [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) för att få ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-125">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

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

### <span data-ttu-id="aa4bc-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="aa4bc-126">-NetworkInterface</span></span>
<span data-ttu-id="aa4bc-127">Anger nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-127">Specifies the network interface.</span></span>

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

### <span data-ttu-id="aa4bc-128">-Primär</span><span class="sxs-lookup"><span data-stu-id="aa4bc-128">-Primary</span></span>
<span data-ttu-id="aa4bc-129">Anger att nätverks gränssnittet läggs till i det primära gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

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

### <span data-ttu-id="aa4bc-130">-VM</span><span class="sxs-lookup"><span data-stu-id="aa4bc-130">-VM</span></span>
<span data-ttu-id="aa4bc-131">Anger ett lokalt virtuellt dator objekt där du kan lägga till ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="aa4bc-132">Använd cmdleten **New-AzureRmVMConfig** för att skapa en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-132">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="aa4bc-133">Använd cmdleten **Get-AzureRmVM** för att få en befintlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-133">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

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

### <span data-ttu-id="aa4bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4bc-134">CommonParameters</span></span>
<span data-ttu-id="aa4bc-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa4bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4bc-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4bc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4bc-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa4bc-137">INPUTS</span></span>

### <span data-ttu-id="aa4bc-138">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. Models. PSNetworkInterface]</span><span class="sxs-lookup"><span data-stu-id="aa4bc-138">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]</span></span>
<span data-ttu-id="aa4bc-139">Parametern ' NetworkInterface ' godkänner värdet för typen system. Collections. Generic. list ' 1 [Microsoft. Azure. commands. Network. Models. PSNetworkInterface] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="aa4bc-139">Parameter 'NetworkInterface' accepts value of type 'System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]' from the pipeline</span></span>

### <span data-ttu-id="aa4bc-140">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="aa4bc-140">PSVirtualMachine</span></span>
<span data-ttu-id="aa4bc-141">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="aa4bc-141">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="aa4bc-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa4bc-142">OUTPUTS</span></span>

### <span data-ttu-id="aa4bc-143">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="aa4bc-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="aa4bc-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa4bc-144">NOTES</span></span>

## <span data-ttu-id="aa4bc-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa4bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="aa4bc-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="aa4bc-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="aa4bc-147">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="aa4bc-147">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="aa4bc-148">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="aa4bc-148">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
