---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 5fd3e89a20dba274c1bdcad69bed150e9d20fc22
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917454"
---
# <span data-ttu-id="58009-101">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-101">Get-AzVM</span></span>

## <span data-ttu-id="58009-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58009-102">SYNOPSIS</span></span>
<span data-ttu-id="58009-103">Hämtar egenskaperna för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58009-103">Gets the properties of a virtual machine.</span></span>

## <span data-ttu-id="58009-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58009-104">SYNTAX</span></span>

### <span data-ttu-id="58009-105">DefaultParamSet (standard)</span><span class="sxs-lookup"><span data-stu-id="58009-105">DefaultParamSet (Default)</span></span>
```
Get-AzVM [[-ResourceGroupName] <String>] [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58009-106">GetVirtualMachineInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="58009-106">GetVirtualMachineInResourceGroupParamSet</span></span>
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58009-107">ListLocationVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="58009-107">ListLocationVirtualMachinesParamSet</span></span>
```
Get-AzVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58009-108">ListNextLinkVirtualMachinesParamSet</span><span class="sxs-lookup"><span data-stu-id="58009-108">ListNextLinkVirtualMachinesParamSet</span></span>
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58009-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58009-109">DESCRIPTION</span></span>
<span data-ttu-id="58009-110">Cmdleten **Get-AzVM** hämtar vyn modell och instans för en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="58009-110">The **Get-AzVM** cmdlet gets the model view and instance view of an Azure virtual machine.</span></span>
<span data-ttu-id="58009-111">Model-vyn är de användardefinierade egenskaperna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="58009-111">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="58009-112">Instans visningen är den virtuella datorns status för förekomst nivå.</span><span class="sxs-lookup"><span data-stu-id="58009-112">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="58009-113">Ange en *status* parameter för att få en instans av en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="58009-113">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="58009-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58009-114">EXAMPLES</span></span>

### <span data-ttu-id="58009-115">Exempel 1: Hämta egenskaper för modell och instans</span><span class="sxs-lookup"><span data-stu-id="58009-115">Example 1: Get model and instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"

ResourceGroupName        : ResourceGroup11
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/M
icrosoft.Compute/virtualMachines/VirtualMachine07
VmId                     : 00000000-0000-0000-0000-000000000000
Name                     : VirtualMachine07
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {"creationSource":"acs-VirtualMachine07"}
AvailabilitySetReference : {Id}
DiagnosticsProfile       : {BootDiagnostics}
Extensions               : {linuxdiagnostic, waitforleader}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, LinuxConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
```

<span data-ttu-id="58009-116">Det här kommandot hämtar egenskaperna för vyn modell och vyn för den virtuella datorn med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="58009-116">This command gets the model view and instance view properties of the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="58009-117">Exempel 2: Hämta egenskaper för instans</span><span class="sxs-lookup"><span data-stu-id="58009-117">Example 2: Get instance view properties</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status

ResourceGroupName       : ResourceGroup11
Name                    : VirtualMachine07
Disks[0]                :
  Name                  : VirtualMachine07-osdisk
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Time                : 3/1/2019 12:59:30 AM
Extensions[0]           :
  Name                  : linuxdiagnostic
  Type                  : Microsoft.OSTCExtensions.LinuxDiagnostic
  TypeHandlerVersion    : 2.3.9029
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Invalid config settings given: Empty storageAccountName. Install will proceed, but enable
can't proceed, in which case it's still considered a success as it's an external error.
Extensions[1]           :
  Name                  : waitforleader
  Type                  : Microsoft.OSTCExtensions.CustomScriptForLinux
  TypeHandlerVersion    : 1.5.4
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Provisioning succeeded
    Message             : Command is finished.
---stdout---
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
waiting for leader.mesos
PING leader.mesos (xxx.xx.x.x) 56(84) bytes of data.
64 bytes from xxx.xx.x.x: icmp_seq=1 ttl=64 time=0.022 ms

--- leader.mesos ping statistics ---
1 packets transmitted, 1 received, 0% packet loss, time 0ms
rtt min/avg/max/mdev = 0.022/0.022/0.022/0.000 ms
leader.mesos up

---errout---
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos
ping: unknown host leader.mesos


PlatformFaultDomain     : 0
PlatformUpdateDomain    : 0
VMAgent                 :
  VmAgentVersion        : 2.2.37
  ExtensionHandlers[0]  :
    Type                : Microsoft.OSTCExtensions.LinuxDiagnostic
    TypeHandlerVersion  : 2.3.9029
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  ExtensionHandlers[1]  :
    Type                : Microsoft.OSTCExtensions.CustomScriptForLinux
    TypeHandlerVersion  : 1.5.4
    Status              :
      Code              : ProvisioningState/succeeded
      Level             : Info
      DisplayStatus     : Ready
      Message           : Plugin enabled
  Statuses[0]           :
    Code                : ProvisioningState/succeeded
    Level               : Info
    DisplayStatus       : Ready
    Message             : Guest Agent is running
    Time                : 3/1/2019 2:04:12 AM
Statuses[0]             :
  Code                  : ProvisioningState/succeeded
  Level                 : Info
  DisplayStatus         : Provisioning succeeded
  Time                  : 3/1/2019 1:01:57 AM
Statuses[1]             :
  Code                  : PowerState/running
  Level                 : Info
  DisplayStatus         : VM running
```

<span data-ttu-id="58009-118">Det här kommandot får egenskaper för den virtuella datorn som heter VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="58009-118">This command gets properties of the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="58009-119">Det här kommandot anger *status* -parametern.</span><span class="sxs-lookup"><span data-stu-id="58009-119">This command specifies the *Status* parameter.</span></span>
<span data-ttu-id="58009-120">Därför får kommandot bara till förekomst egenskaperna för vyn.</span><span class="sxs-lookup"><span data-stu-id="58009-120">Therefore, the command gets only the instance view properties.</span></span>

### <span data-ttu-id="58009-121">Exempel 3: Hämta egenskaper för alla virtuella datorer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="58009-121">Example 3: Get properties for all virtual machines in a resource group</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
ResourceGroup11     test1         eastus Standard_DS1_v2 Windows          test1
ResourceGroup11     test2         westus Standard_DS1_v2 Windows          test2
ResourceGroup11     test3         eastus Standard_DS1_v2 Windows          test3
```

<span data-ttu-id="58009-122">Det här kommandot får egenskaper för alla virtuella datorer i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="58009-122">This command gets properties for all the virtual machines in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="58009-123">Exempel 4: Hämta alla virtuella datorer i ditt abonnemang</span><span class="sxs-lookup"><span data-stu-id="58009-123">Example 4: Get all virtual machines in your subscription</span></span>
```
PS C:\> Get-AzVM

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="58009-124">Det här kommandot får alla virtuella datorer i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="58009-124">This command gets all the virtual machines in your subscription.</span></span>

### <span data-ttu-id="58009-125">Exempel 5: Hämta alla virtuella datorer på platsen.</span><span class="sxs-lookup"><span data-stu-id="58009-125">Example 5: Get all virtual machines in the location.</span></span>
```
PS C:\> Get-AzVM -Location "westus"

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST2               test4         westus Standard_DS1_v2 Windows          test4
```

<span data-ttu-id="58009-126">Det här kommandot får alla virtuella datorer i västra USA-regionen.</span><span class="sxs-lookup"><span data-stu-id="58009-126">This command gets all the virtual machines in West US region.</span></span>

### <span data-ttu-id="58009-127">Exempel 6: Hämta alla virtuella datorer med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="58009-127">Example 6: Get all virtual machines using filtering</span></span>
```
PS C:\> Get-AzVM -Name test*

ResourceGroupName    Name       Location          VmSize  OsType            NIC
-----------------    ----       --------          ------  ------            ---
TEST1               test1         eastus Standard_DS1_v2 Windows          test1
TEST1               test2         westus Standard_DS1_v2 Windows          test2
TEST1               test3         eastus Standard_DS1_v2 Windows          test3
TEST2               test4         westus Standard_DS1_v2 Windows          test4
TEST2               test5         eastus Standard_DS1_v2 Windows          test5
```

<span data-ttu-id="58009-128">Det här kommandot får alla virtuella datorer i ditt abonnemang som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="58009-128">This command gets all the virtual machines in your subscription that start with "test".</span></span>

## <span data-ttu-id="58009-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58009-129">PARAMETERS</span></span>

### <span data-ttu-id="58009-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58009-130">-DefaultProfile</span></span>
<span data-ttu-id="58009-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58009-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58009-132">-DisplayHint</span><span class="sxs-lookup"><span data-stu-id="58009-132">-DisplayHint</span></span>
<span data-ttu-id="58009-133">Bestämmer hur det virtuella datorobjektet visas.</span><span class="sxs-lookup"><span data-stu-id="58009-133">Determines how the virtual machine object is displayed.</span></span>
<span data-ttu-id="58009-134">Giltiga värden är:--Compact: visar endast de högsta nivå egenskaperna--Expand: visar alla egenskaper på alla nivåer</span><span class="sxs-lookup"><span data-stu-id="58009-134">Valid values are: -- Compact: displays only top level properties -- Expand: displays all properties in all levels</span></span>

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

### <span data-ttu-id="58009-135">-Plats</span><span class="sxs-lookup"><span data-stu-id="58009-135">-Location</span></span>
<span data-ttu-id="58009-136">Anger en plats för de virtuella datorerna som ska visas.</span><span class="sxs-lookup"><span data-stu-id="58009-136">Specifies a location for the virtual machines to list.</span></span>

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

### <span data-ttu-id="58009-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="58009-137">-Name</span></span>
<span data-ttu-id="58009-138">Anger namnet på den virtuella dator som ska visas.</span><span class="sxs-lookup"><span data-stu-id="58009-138">Specifies the name of the virtual machine to get.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="58009-139">-NextLink</span><span class="sxs-lookup"><span data-stu-id="58009-139">-NextLink</span></span>
<span data-ttu-id="58009-140">Anger nästa länk.</span><span class="sxs-lookup"><span data-stu-id="58009-140">Specifies the next link.</span></span>

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

### <span data-ttu-id="58009-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58009-141">-ResourceGroupName</span></span>
<span data-ttu-id="58009-142">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="58009-142">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="58009-143">-Status</span><span class="sxs-lookup"><span data-stu-id="58009-143">-Status</span></span>
<span data-ttu-id="58009-144">Anger att denna cmdlet endast får till gång till den virtuella datorns instans.</span><span class="sxs-lookup"><span data-stu-id="58009-144">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="58009-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58009-145">CommonParameters</span></span>
<span data-ttu-id="58009-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58009-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58009-147">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58009-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58009-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58009-148">INPUTS</span></span>

### <span data-ttu-id="58009-149">System. String</span><span class="sxs-lookup"><span data-stu-id="58009-149">System.String</span></span>

### <span data-ttu-id="58009-150">System. URI</span><span class="sxs-lookup"><span data-stu-id="58009-150">System.Uri</span></span>

### <span data-ttu-id="58009-151">Microsoft. Azure. commands. Compute. Models. DisplayHintType</span><span class="sxs-lookup"><span data-stu-id="58009-151">Microsoft.Azure.Commands.Compute.Models.DisplayHintType</span></span>

## <span data-ttu-id="58009-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58009-152">OUTPUTS</span></span>

### <span data-ttu-id="58009-153">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="58009-153">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="58009-154">Microsoft. Azure. commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="58009-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="58009-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58009-155">NOTES</span></span>

## <span data-ttu-id="58009-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58009-156">RELATED LINKS</span></span>

[<span data-ttu-id="58009-157">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-157">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="58009-158">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-158">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="58009-159">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-159">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="58009-160">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-160">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="58009-161">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-161">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="58009-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="58009-162">Update-AzVM</span></span>](./Update-AzVM.md)


