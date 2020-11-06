---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585752"
---
# <span data-ttu-id="c5b9c-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-101">New-AzureRmVM</span></span>

## <span data-ttu-id="c5b9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b9c-103">Skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5b9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5b9c-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b9c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="c5b9c-106">Cmdleten **New-AzureRmVM** skapar en virtuell dator i Azure.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="c5b9c-107">Denna cmdlet tar ett virtuellt dator objekt som indata.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="c5b9c-108">Använd New-AzureRmVMConfig cmdlet för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="c5b9c-109">Andra cmdletar kan användas för att konfigurera den virtuella datorn, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface och set-AzureRmVMOSDisk.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="c5b9c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5b9c-110">EXAMPLES</span></span>

### <span data-ttu-id="c5b9c-111">Exempel 1: skapa en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="c5b9c-111">Example 1: Create a virtual machine</span></span>
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

<span data-ttu-id="c5b9c-112">Det här exemplet visar hur du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="c5b9c-113">Det här skriptet använder flera andra cmdletar.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="c5b9c-114">Exempel 2: skapa en virtuell dator från en anpassad användar bild</span><span class="sxs-lookup"><span data-stu-id="c5b9c-114">Example 2: Create a virtual machine from a custom user image</span></span>
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

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="c5b9c-115">I det här exemplet används en befintlig sys-prepped, en allmän, anpassad operativ Systems bild och kopplar en datadisk till den, etablerar ett nytt nätverk, distribuerar VHD och kör det.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="c5b9c-116">Det här manuset kan användas för automatisk etablering eftersom det använder den lokala virtuella datorns administratörs inloggnings uppgifter i stället för **att ringa upp** ett användar konto.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="c5b9c-117">Det här skriptet förutsätter att du redan är inloggad på ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="c5b9c-118">Du kan bekräfta din inloggnings status genom att använda cmdleten **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="c5b9c-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="c5b9c-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5b9c-119">PARAMETERS</span></span>

### <span data-ttu-id="c5b9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b9c-120">-DefaultProfile</span></span>
<span data-ttu-id="c5b9c-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5b9c-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="c5b9c-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="c5b9c-123">Anger att denna cmdlet inte installerar **BG info** -tillägget på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="c5b9c-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c5b9c-124">-LicenseType</span></span>
<span data-ttu-id="c5b9c-125">Anger en licens typ, vilket betyder att avbildningen eller disken för den virtuella datorn har licensierats lokalt.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="c5b9c-126">Det här värdet används endast för bilder som innehåller operativ systemet Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="c5b9c-127">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="c5b9c-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c5b9c-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="c5b9c-128">Windows_Client</span></span> 
- <span data-ttu-id="c5b9c-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="c5b9c-129">Windows_Server</span></span>

<span data-ttu-id="c5b9c-130">Detta värde kan inte uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-130">This value cannot be updated.</span></span>
<span data-ttu-id="c5b9c-131">Om du anger den här parametern för en uppdatering måste värdet matcha startvärdet för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b9c-132">-Plats</span><span class="sxs-lookup"><span data-stu-id="c5b9c-132">-Location</span></span>
<span data-ttu-id="c5b9c-133">Anger en plats för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-133">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b9c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b9c-134">-ResourceGroupName</span></span>
<span data-ttu-id="c5b9c-135">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-135">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b9c-136">-Taggar</span><span class="sxs-lookup"><span data-stu-id="c5b9c-136">-Tags</span></span>
<span data-ttu-id="c5b9c-137">Anger att resurser och resurs grupper kan märkas med en uppsättning namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="c5b9c-138">Genom att lägga till taggar till resurser kan du gruppera resurser tillsammans i resurs grupper och skapa egna vyer.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="c5b9c-139">Varje resurs eller resurs grupp kan ha högst 15 taggar.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b9c-140">-VM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-140">-VM</span></span>
<span data-ttu-id="c5b9c-141">Anger vilken lokal virtuell dator som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="c5b9c-142">Använd New-AzureRmVMConfig cmdlet för att få ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="c5b9c-143">Andra cmdletar kan användas för att konfigurera den virtuella datorn, till exempel set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage och Add-AzureRmVMNetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b9c-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="c5b9c-144">-Zone</span></span>
<span data-ttu-id="c5b9c-145">Anger den virtuella datorns zonfil.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-145">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b9c-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5b9c-146">-Confirm</span></span>
<span data-ttu-id="c5b9c-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b9c-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5b9c-148">-WhatIf</span></span>
<span data-ttu-id="c5b9c-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c5b9c-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b9c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b9c-151">CommonParameters</span></span>
<span data-ttu-id="c5b9c-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b9c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b9c-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5b9c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b9c-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5b9c-154">INPUTS</span></span>

## <span data-ttu-id="c5b9c-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5b9c-155">OUTPUTS</span></span>

## <span data-ttu-id="c5b9c-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5b9c-156">NOTES</span></span>

## <span data-ttu-id="c5b9c-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5b9c-157">RELATED LINKS</span></span>

[<span data-ttu-id="c5b9c-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="c5b9c-159">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="c5b9c-160">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="c5b9c-161">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="c5b9c-162">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="c5b9c-163">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c5b9c-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="c5b9c-164">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c5b9c-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="c5b9c-165">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c5b9c-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="c5b9c-166">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="c5b9c-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="c5b9c-167">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c5b9c-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="c5b9c-168">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="c5b9c-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="c5b9c-169">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="c5b9c-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


