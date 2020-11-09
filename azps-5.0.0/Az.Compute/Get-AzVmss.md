---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324744"
---
# <span data-ttu-id="9db12-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-101">Get-AzVmss</span></span>

## <span data-ttu-id="9db12-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9db12-102">SYNOPSIS</span></span>
<span data-ttu-id="9db12-103">Hämtar egenskaperna för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="9db12-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="9db12-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9db12-104">SYNTAX</span></span>

### <span data-ttu-id="9db12-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="9db12-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9db12-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9db12-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9db12-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="9db12-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9db12-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9db12-108">DESCRIPTION</span></span>
<span data-ttu-id="9db12-109">Cmdleten **Get-AzVmss** hämtar modellen och instans vyn för en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9db12-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9db12-110">Model-vyn är de användardefinierade egenskaperna för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9db12-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="9db12-111">Instans visningen är instans nivå statusen för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9db12-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="9db12-112">Ange parametern *InstanceView* om du bara vill få instans visningen av en virtuell dators skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9db12-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="9db12-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9db12-113">EXAMPLES</span></span>

### <span data-ttu-id="9db12-114">Exempel 1: Hämta egenskaper för en VMSS</span><span class="sxs-lookup"><span data-stu-id="9db12-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="9db12-115">Det här kommandot får egenskaperna för VMSS med namnet VMSS001 som tillhör resurs gruppen med namnet Group001.</span><span class="sxs-lookup"><span data-stu-id="9db12-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="9db12-116">Eftersom kommandot inte anger parameter för *InstanceView* -växeln får cmdleten modell läget för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9db12-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="9db12-117">Exempel 2: Hämta alla VMSS i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="9db12-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="9db12-118">Hämta alla VMSS i resurs gruppen "Group001"</span><span class="sxs-lookup"><span data-stu-id="9db12-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="9db12-119">Exempel 3: Hämta alla VMSS i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="9db12-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="9db12-120">Skaffa alla VMSS i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9db12-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="9db12-121">Exempel 4: Hämta alla VMSS med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="9db12-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="9db12-122">Hämta alla VMSS i prenumerationen som börjar med "VMSS00".</span><span class="sxs-lookup"><span data-stu-id="9db12-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="9db12-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9db12-123">PARAMETERS</span></span>

### <span data-ttu-id="9db12-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9db12-124">-DefaultProfile</span></span>
<span data-ttu-id="9db12-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9db12-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9db12-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="9db12-126">-InstanceView</span></span>
<span data-ttu-id="9db12-127">Anger att denna cmdlet endast får instans visning av den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9db12-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db12-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="9db12-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="9db12-129">Anger att den här cmdleten visar system uppgraderings historiken för den virtuella datorns skal uppsättning.</span><span class="sxs-lookup"><span data-stu-id="9db12-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9db12-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9db12-130">-ResourceGroupName</span></span>
<span data-ttu-id="9db12-131">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="9db12-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9db12-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9db12-132">-VMScaleSetName</span></span>
<span data-ttu-id="9db12-133">Arter namnet på VMSS.</span><span class="sxs-lookup"><span data-stu-id="9db12-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9db12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9db12-134">CommonParameters</span></span>
<span data-ttu-id="9db12-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9db12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9db12-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9db12-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9db12-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9db12-137">INPUTS</span></span>

### <span data-ttu-id="9db12-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9db12-138">System.String</span></span>

## <span data-ttu-id="9db12-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9db12-139">OUTPUTS</span></span>

### <span data-ttu-id="9db12-140">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="9db12-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="9db12-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9db12-141">NOTES</span></span>

## <span data-ttu-id="9db12-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9db12-142">RELATED LINKS</span></span>

[<span data-ttu-id="9db12-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="9db12-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="9db12-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="9db12-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="9db12-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="9db12-148">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="9db12-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9db12-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


