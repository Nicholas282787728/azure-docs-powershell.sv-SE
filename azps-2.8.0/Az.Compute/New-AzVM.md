---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 4350a1bca25d94f2d3fab27c202eda4392180027
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745086"
---
# <span data-ttu-id="0d8ec-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-101">New-AzVM</span></span>

## <span data-ttu-id="0d8ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8ec-103">Skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="0d8ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d8ec-104">SYNTAX</span></span>

### <span data-ttu-id="0d8ec-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="0d8ec-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>]
 [-HostId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d8ec-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8ec-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d8ec-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d8ec-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>] [-HostId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d8ec-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d8ec-108">DESCRIPTION</span></span>
<span data-ttu-id="0d8ec-109">Cmdleten **New-AzVM** skapar en virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="0d8ec-110">Denna cmdlet tar ett virtuellt dator objekt som indata.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="0d8ec-111">Använd New-AzVMConfig cmdlet för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="0d8ec-112">Andra cmdletar kan användas för att konfigurera den virtuella datorn, till exempel set-AzVMOperatingSystem, set-AzVMSourceImage, Add-AzVMNetworkInterface och set-AzVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="0d8ec-113">Med `SimpleParameterSet` är det enkelt att skapa en virtuell dator med de vanligaste argumenten för att skapa virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="0d8ec-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d8ec-114">EXAMPLES</span></span>

### <span data-ttu-id="0d8ec-115">Exempel 1: skapa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="0d8ec-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="0d8ec-116">Det här exemplet visar hur du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="0d8ec-117">Skriptet frågar efter den virtuella datorns användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="0d8ec-118">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="0d8ec-119">Exempel 2: skapa en virtuell dator från en anpassad användar bild</span><span class="sxs-lookup"><span data-stu-id="0d8ec-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="0d8ec-120">I det här exemplet används en befintlig sys-prepped, en allmän, anpassad operativ Systems bild och kopplar en datadisk till den, etablerar ett nytt nätverk, distribuerar VHD och kör det.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="0d8ec-121">Det här manuset kan användas för automatisk etablering eftersom det använder den lokala virtuella datorns administratörs inloggnings uppgifter i stället för **att ringa upp** ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="0d8ec-122">Det här skriptet förutsätter att du redan är inloggad på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="0d8ec-123">Du kan bekräfta din inloggnings status genom att använda cmdleten **Get-AzSubscription** .</span><span class="sxs-lookup"><span data-stu-id="0d8ec-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="0d8ec-124">Exempel 3: skapa en virtuell dator från en Marketplace-avbildning utan offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="0d8ec-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="0d8ec-125">I det här exemplet etableras ett nytt nätverk och en Windows VM distribueras från Marketplace utan att en offentlig IP-adress eller nätverks säkerhets grupp skapas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="0d8ec-126">Det här manuset kan användas för automatisk etablering eftersom det använder den lokala virtuella datorns administratörs inloggnings uppgifter i stället för **att ringa upp** ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="0d8ec-127">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d8ec-127">PARAMETERS</span></span>

### <span data-ttu-id="0d8ec-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d8ec-128">-AddressPrefix</span></span>
<span data-ttu-id="0d8ec-129">Adressprefixet för det virtuella nätverk som kommer att skapas för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="0d8ec-130">-AllocationMethod</span></span>
<span data-ttu-id="0d8ec-131">Metod för IP-tilldelning för den offentliga IP-adressen som skapas för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d8ec-132">-AsJob</span></span>
<span data-ttu-id="0d8ec-133">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-133">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="0d8ec-134">-AvailabilitySetName</span></span>
<span data-ttu-id="0d8ec-135">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-136">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="0d8ec-136">-Credential</span></span>
<span data-ttu-id="0d8ec-137">Administratörs uppgifterna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-137">The administrator credentials for the VM.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="0d8ec-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="0d8ec-139">Anger storleken på data diskarna i GB.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8ec-140">-DefaultProfile</span></span>
<span data-ttu-id="0d8ec-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d8ec-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="0d8ec-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="0d8ec-143">Anger att denna cmdlet inte installerar **BG info** -tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="0d8ec-144">-DiskFile</span></span>
<span data-ttu-id="0d8ec-145">Den lokala sökvägen till den virtuella hård disk filen laddas upp till molnet och för att skapa den virtuella datorn, och den måste ha ". VHD" som dess suffix.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="0d8ec-146">-DomainNameLabel</span></span>
<span data-ttu-id="0d8ec-147">Etiketten för under domänen för det fullständigt kvalificerade domän namnet (FQDN) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="0d8ec-148">Det här tar formuläret `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="0d8ec-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="0d8ec-149">-EnableUltraSSD</span></span>
<span data-ttu-id="0d8ec-150">Använda UltraSSD-diskar för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="0d8ec-151">-EvictionPolicy</span></span>
<span data-ttu-id="0d8ec-152">Borttagnings principen för den virtuella datorn med den högsta prioriteten.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-152">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="0d8ec-153">Det enda värdet som stöds är "frigör".</span><span class="sxs-lookup"><span data-stu-id="0d8ec-153">Only supported value is 'Deallocate'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-154">-HostId</span><span class="sxs-lookup"><span data-stu-id="0d8ec-154">-HostId</span></span>
<span data-ttu-id="0d8ec-155">ID för värden</span><span class="sxs-lookup"><span data-stu-id="0d8ec-155">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-156">-Image</span><span class="sxs-lookup"><span data-stu-id="0d8ec-156">-Image</span></span>
<span data-ttu-id="0d8ec-157">Det eget namn på den virtuella datorn som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-157">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="0d8ec-158">Dessa inkluderar: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Corei, Debian, openSUSE-skottår, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-158">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0d8ec-159">-LicenseType</span></span>
<span data-ttu-id="0d8ec-160">Anger en licens typ, vilket betyder att avbildningen eller disken för den virtuella datorn har licensierats lokalt.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-160">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="0d8ec-161">Det här värdet används endast för bilder som innehåller operativ systemet Windows Server.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-161">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="0d8ec-162">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="0d8ec-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d8ec-163">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="0d8ec-163">Windows_Client</span></span>
- <span data-ttu-id="0d8ec-164">Windows_Server det här värdet kan inte uppdateras.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-164">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="0d8ec-165">Om du anger den här parametern för en uppdatering måste värdet matcha startvärdet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-165">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="0d8ec-166">-Linux</span></span>
<span data-ttu-id="0d8ec-167">Anger om disk filen är för Linux VM, om den anges; eller Windows, om det inte anges som standard.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-167">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-168">-Plats</span><span class="sxs-lookup"><span data-stu-id="0d8ec-168">-Location</span></span>
<span data-ttu-id="0d8ec-169">Anger en plats för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-169">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="0d8ec-170">-MaxPrice</span></span>
<span data-ttu-id="0d8ec-171">Det högsta priset för fakturering av en virtuell dator med en lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-171">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-172">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d8ec-172">-Name</span></span>
<span data-ttu-id="0d8ec-173">Namnet på den virtuella dator resursen.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-173">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-174">-Openports</span><span class="sxs-lookup"><span data-stu-id="0d8ec-174">-OpenPorts</span></span>
<span data-ttu-id="0d8ec-175">En lista över portar som ska öppnas i nätverks säkerhets gruppen (NSG) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-175">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="0d8ec-176">Standardvärdet beror på vilken typ av bild du valt (d.v.s. Windows: 3389, 5985 och Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="0d8ec-176">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-177">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="0d8ec-177">-Priority</span></span>
<span data-ttu-id="0d8ec-178">Prioriteten för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-178">The priority for the virtual machine.</span></span>  <span data-ttu-id="0d8ec-179">Endast värden som stöds är "regular" och "Low".</span><span class="sxs-lookup"><span data-stu-id="0d8ec-179">Only supported values are 'Regular' and 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-180">-ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0d8ec-180">-ProximityPlacementGroup</span></span>
<span data-ttu-id="0d8ec-181">Namn eller resurs-ID för närhets gruppen som ska användas med den här virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-181">The name or resource id of the Proximity Placement Group to use with this VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-182">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="0d8ec-182">-PublicIpAddressName</span></span>
<span data-ttu-id="0d8ec-183">Namnet på en ny (eller befintlig) offentlig IP-adress för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-183">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="0d8ec-184">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-184">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8ec-185">-ResourceGroupName</span></span>
<span data-ttu-id="0d8ec-186">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-186">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-187">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="0d8ec-187">-SecurityGroupName</span></span>
<span data-ttu-id="0d8ec-188">Namnet på en ny (eller befintlig) nätverks säkerhets grupp (NSG) för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-188">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="0d8ec-189">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-189">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-190">-Storlek</span><span class="sxs-lookup"><span data-stu-id="0d8ec-190">-Size</span></span>
<span data-ttu-id="0d8ec-191">Storlek på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-191">The Virtual Machine Size.</span></span>  <span data-ttu-id="0d8ec-192">Standardvärdet är: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-192">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-193">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="0d8ec-193">-SubnetAddressPrefix</span></span>
<span data-ttu-id="0d8ec-194">Adressprefixet för det undernät som kommer att skapas för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-194">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-195">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0d8ec-195">-SubnetName</span></span>
<span data-ttu-id="0d8ec-196">Namnet på ett nytt (eller befintligt) undernät för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-196">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="0d8ec-197">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-197">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-198">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0d8ec-198">-SystemAssignedIdentity</span></span>
<span data-ttu-id="0d8ec-199">Om parametern visas tilldelas den virtuella datorn en hanterad system identitet som genereras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-199">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-200">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0d8ec-200">-Tag</span></span>
<span data-ttu-id="0d8ec-201">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-201">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="0d8ec-202">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-202">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="0d8ec-203">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-203">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-204">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0d8ec-204">-UserAssignedIdentity</span></span>
<span data-ttu-id="0d8ec-205">Namnet på en hanterad tjänst identitet som ska kopplas till den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-205">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-206">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0d8ec-206">-VirtualNetworkName</span></span>
<span data-ttu-id="0d8ec-207">Namnet på ett nytt (eller befintligt) virtuellt nätverk för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-207">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="0d8ec-208">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-208">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-209">-VM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-209">-VM</span></span>
<span data-ttu-id="0d8ec-210">Anger vilken lokal virtuell dator som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-210">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="0d8ec-211">Använd New-AzVMConfig cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-211">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="0d8ec-212">Andra cmdletar kan användas för att konfigurera den virtuella datorn, till exempel set-AzVMOperatingSystem, set-AzVMSourceImage och Add-AzVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-212">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-213">-Zone</span><span class="sxs-lookup"><span data-stu-id="0d8ec-213">-Zone</span></span>
<span data-ttu-id="0d8ec-214">Anger den virtuella datorns zonfil.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-214">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-215">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d8ec-215">-Confirm</span></span>
<span data-ttu-id="0d8ec-216">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-216">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8ec-217">-WhatIf</span></span>
<span data-ttu-id="0d8ec-218">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d8ec-219">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-219">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8ec-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8ec-220">CommonParameters</span></span>
<span data-ttu-id="0d8ec-221">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d8ec-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8ec-222">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d8ec-222">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8ec-223">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d8ec-223">INPUTS</span></span>

### <span data-ttu-id="0d8ec-224">System. String</span><span class="sxs-lookup"><span data-stu-id="0d8ec-224">System.String</span></span>

### <span data-ttu-id="0d8ec-225">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0d8ec-225">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="0d8ec-226">System. string []</span><span class="sxs-lookup"><span data-stu-id="0d8ec-226">System.String[]</span></span>

### <span data-ttu-id="0d8ec-227">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="0d8ec-227">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0d8ec-228">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d8ec-228">OUTPUTS</span></span>

### <span data-ttu-id="0d8ec-229">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0d8ec-229">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="0d8ec-230">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0d8ec-230">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="0d8ec-231">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d8ec-231">NOTES</span></span>

## <span data-ttu-id="0d8ec-232">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d8ec-232">RELATED LINKS</span></span>

[<span data-ttu-id="0d8ec-233">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-233">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0d8ec-234">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-234">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="0d8ec-235">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-235">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="0d8ec-236">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-236">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="0d8ec-237">Stopp-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-237">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="0d8ec-238">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0d8ec-238">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="0d8ec-239">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0d8ec-239">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="0d8ec-240">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0d8ec-240">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="0d8ec-241">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0d8ec-241">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="0d8ec-242">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0d8ec-242">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="0d8ec-243">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="0d8ec-243">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="0d8ec-244">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="0d8ec-244">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)

