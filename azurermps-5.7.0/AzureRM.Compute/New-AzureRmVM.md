---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574353"
---
# <span data-ttu-id="e29ab-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-101">New-AzureRmVM</span></span>

## <span data-ttu-id="e29ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e29ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e29ab-103">Skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e29ab-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e29ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e29ab-104">SYNTAX</span></span>

### <span data-ttu-id="e29ab-105">SimpleParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e29ab-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29ab-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29ab-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29ab-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e29ab-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29ab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e29ab-108">DESCRIPTION</span></span>
<span data-ttu-id="e29ab-109">Cmdleten **New-AzureRmVM** skapar en virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="e29ab-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="e29ab-110">Denna cmdlet tar ett virtuellt dator objekt som indata.</span><span class="sxs-lookup"><span data-stu-id="e29ab-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="e29ab-111">Använd New-AzureRmVMConfig cmdlet för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e29ab-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="e29ab-112">Andra cmdletar kan användas för att konfigurera den virtuella datorn, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface och set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e29ab-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="e29ab-113">Med `SimpleParameterSet` är det enkelt att skapa en virtuell dator med de vanligaste argumenten för att skapa virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="e29ab-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="e29ab-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e29ab-114">EXAMPLES</span></span>

### <span data-ttu-id="e29ab-115">Exempel 1: skapa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e29ab-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="e29ab-116">Det här exemplet visar hur du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e29ab-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="e29ab-117">Skriptet frågar efter den virtuella datorns användar namn och lösen ord.</span><span class="sxs-lookup"><span data-stu-id="e29ab-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="e29ab-118">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="e29ab-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="e29ab-119">Exempel 2: skapa en virtuell dator från en anpassad användar bild</span><span class="sxs-lookup"><span data-stu-id="e29ab-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="e29ab-120">I det här exemplet används en befintlig sys-prepped, en allmän, anpassad operativ Systems bild och kopplar en datadisk till den, etablerar ett nytt nätverk, distribuerar VHD och kör det.</span><span class="sxs-lookup"><span data-stu-id="e29ab-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="e29ab-121">Det här manuset kan användas för automatisk etablering eftersom det använder den lokala virtuella datorns administratörs inloggnings uppgifter i stället för **att ringa upp** ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="e29ab-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="e29ab-122">Det här skriptet förutsätter att du redan är inloggad på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="e29ab-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="e29ab-123">Du kan bekräfta din inloggnings status genom att använda cmdleten **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="e29ab-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="e29ab-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e29ab-124">PARAMETERS</span></span>

### <span data-ttu-id="e29ab-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e29ab-125">-AddressPrefix</span></span>
<span data-ttu-id="e29ab-126">Adressprefixet för det virtuella nätverk som kommer att skapas för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="e29ab-127">-AllocationMethod</span></span>
<span data-ttu-id="e29ab-128">Metod för IP-tilldelning för den offentliga IP-adressen som skapas för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e29ab-129">-AsJob</span></span>
<span data-ttu-id="e29ab-130">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="e29ab-130">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="e29ab-131">-AvailabilitySetName</span></span>
<span data-ttu-id="e29ab-132">Anger ett namn för tillgänglighets uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e29ab-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-133">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="e29ab-133">-Credential</span></span>
<span data-ttu-id="e29ab-134">Administratörs uppgifterna för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-134">The administrator credentials for the VM.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="e29ab-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="e29ab-136">Anger storleken på data diskarna i GB.</span><span class="sxs-lookup"><span data-stu-id="e29ab-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29ab-137">-DefaultProfile</span></span>
<span data-ttu-id="e29ab-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e29ab-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e29ab-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="e29ab-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="e29ab-140">Anger att denna cmdlet inte installerar **BG info** -tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-141">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="e29ab-141">-DiskFile</span></span>
<span data-ttu-id="e29ab-142">Den lokala sökvägen till den virtuella hård disk filen laddas upp till molnet och för att skapa den virtuella datorn, och den måste ha ". VHD" som dess suffix.</span><span class="sxs-lookup"><span data-stu-id="e29ab-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="e29ab-143">-DomainNameLabel</span></span>
<span data-ttu-id="e29ab-144">Etiketten för under domänen för det fullständigt kvalificerade domän namnet (FQDN) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="e29ab-145">Det här tar formuläret `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="e29ab-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e29ab-146">-ImageName</span></span>
<span data-ttu-id="e29ab-147">Det eget namn på den virtuella datorn som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e29ab-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="e29ab-148">Dessa inkluderar: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, Corei, Debian, openSUSE-skottår, RHEL, SLES.</span><span class="sxs-lookup"><span data-stu-id="e29ab-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e29ab-149">-LicenseType</span></span>
<span data-ttu-id="e29ab-150">Anger en licens typ, vilket betyder att avbildningen eller disken för den virtuella datorn har licensierats lokalt.</span><span class="sxs-lookup"><span data-stu-id="e29ab-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="e29ab-151">Det här värdet används endast för bilder som innehåller operativ systemet Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e29ab-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="e29ab-152">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e29ab-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e29ab-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="e29ab-153">Windows_Client</span></span>
- <span data-ttu-id="e29ab-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="e29ab-154">Windows_Server</span></span>

<span data-ttu-id="e29ab-155">Detta värde kan inte uppdateras.</span><span class="sxs-lookup"><span data-stu-id="e29ab-155">This value cannot be updated.</span></span>
<span data-ttu-id="e29ab-156">Om du anger den här parametern för en uppdatering måste värdet matcha startvärdet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="e29ab-157">-Linux</span></span>
<span data-ttu-id="e29ab-158">Anger om disk filen är för Linux VM, om den anges; eller Windows, om det inte anges som standard.</span><span class="sxs-lookup"><span data-stu-id="e29ab-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-159">-Plats</span><span class="sxs-lookup"><span data-stu-id="e29ab-159">-Location</span></span>
<span data-ttu-id="e29ab-160">Anger en plats för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-161">-Namn</span><span class="sxs-lookup"><span data-stu-id="e29ab-161">-Name</span></span>
<span data-ttu-id="e29ab-162">Namnet på den virtuella dator resursen.</span><span class="sxs-lookup"><span data-stu-id="e29ab-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-163">-Openports</span><span class="sxs-lookup"><span data-stu-id="e29ab-163">-OpenPorts</span></span>
<span data-ttu-id="e29ab-164">En lista över portar som ska öppnas i nätverks säkerhets gruppen (NSG) för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="e29ab-165">Standardvärdet beror på vilken typ av bild du valt (d.v.s. Windows: 3389, 5985 och Linux: 22).</span><span class="sxs-lookup"><span data-stu-id="e29ab-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="e29ab-166">-PublicIpAddressName</span></span>
<span data-ttu-id="e29ab-167">Namnet på en ny (eller befintlig) offentlig IP-adress för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e29ab-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="e29ab-168">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29ab-169">-ResourceGroupName</span></span>
<span data-ttu-id="e29ab-170">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e29ab-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="e29ab-171">-SecurityGroupName</span></span>
<span data-ttu-id="e29ab-172">Namnet på en ny (eller befintlig) nätverks säkerhets grupp (NSG) för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e29ab-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="e29ab-173">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-174">-Storlek</span><span class="sxs-lookup"><span data-stu-id="e29ab-174">-Size</span></span>
<span data-ttu-id="e29ab-175">Storlek på virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e29ab-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="e29ab-176">Standardvärdet är: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="e29ab-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="e29ab-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="e29ab-178">Adressprefixet för det undernät som kommer att skapas för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e29ab-179">-SubnetName</span></span>
<span data-ttu-id="e29ab-180">Namnet på ett nytt (eller befintligt) undernät för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e29ab-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="e29ab-181">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-182">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e29ab-182">-Tag</span></span>
<span data-ttu-id="e29ab-183">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="e29ab-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="e29ab-184">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="e29ab-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="e29ab-185">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="e29ab-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e29ab-186">-VirtualNetworkName</span></span>
<span data-ttu-id="e29ab-187">Namnet på ett nytt (eller befintligt) virtuellt nätverk för den virtuella dator som ska användas.</span><span class="sxs-lookup"><span data-stu-id="e29ab-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="e29ab-188">Om inget anges genereras ett namn.</span><span class="sxs-lookup"><span data-stu-id="e29ab-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-189">-VM</span><span class="sxs-lookup"><span data-stu-id="e29ab-189">-VM</span></span>
<span data-ttu-id="e29ab-190">Anger vilken lokal virtuell dator som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e29ab-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="e29ab-191">Använd New-AzureRmVMConfig cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e29ab-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="e29ab-192">Andra cmdletar kan användas för att konfigurera den virtuella datorn, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage och Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="e29ab-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-193">-Zone</span><span class="sxs-lookup"><span data-stu-id="e29ab-193">-Zone</span></span>
<span data-ttu-id="e29ab-194">Anger den virtuella datorns zonfil.</span><span class="sxs-lookup"><span data-stu-id="e29ab-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-195">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e29ab-195">-Confirm</span></span>
<span data-ttu-id="e29ab-196">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e29ab-196">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29ab-197">-WhatIf</span></span>
<span data-ttu-id="e29ab-198">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e29ab-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e29ab-199">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e29ab-199">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29ab-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29ab-200">CommonParameters</span></span>
<span data-ttu-id="e29ab-201">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29ab-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29ab-202">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29ab-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29ab-203">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e29ab-203">INPUTS</span></span>

### <span data-ttu-id="e29ab-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e29ab-204">PSVirtualMachine</span></span>
<span data-ttu-id="e29ab-205">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e29ab-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="e29ab-206">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e29ab-206">OUTPUTS</span></span>

### <span data-ttu-id="e29ab-207">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e29ab-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e29ab-208">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e29ab-208">NOTES</span></span>

## <span data-ttu-id="e29ab-209">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e29ab-209">RELATED LINKS</span></span>

[<span data-ttu-id="e29ab-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="e29ab-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="e29ab-212">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="e29ab-213">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="e29ab-214">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="e29ab-215">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="e29ab-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="e29ab-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e29ab-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="e29ab-217">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e29ab-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="e29ab-218">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="e29ab-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="e29ab-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e29ab-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="e29ab-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="e29ab-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="e29ab-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e29ab-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


