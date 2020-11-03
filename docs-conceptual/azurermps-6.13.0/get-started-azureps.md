---
title: Komma igång med Azure PowerShell
description: ''
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: cbb07ce6711616c1cabe5ab2108015ea78fd28e9
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523180"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="457a3-102">Komma igång med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="457a3-102">Get started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="457a3-103">Azure PowerShell har utformats för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="457a3-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="457a3-104">Du kan använda Azure PowerShell i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator.</span><span class="sxs-lookup"><span data-stu-id="457a3-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="457a3-105">Den här artikeln hjälper dig att komma igång med Azure PowerShell och du får lära dig grundbegreppen.</span><span class="sxs-lookup"><span data-stu-id="457a3-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="457a3-106">Installera Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="457a3-106">Install Azure PowerShell</span></span>

<span data-ttu-id="457a3-107">Det första steget är att kontrollera att du har den senaste versionen av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="457a3-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="457a3-108">Information om den senaste versionen finns i [viktig information](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="457a3-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="457a3-109">[Installera Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="457a3-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="457a3-110">Kontrollera att installationen lyckades genom att köra `Get-InstalledModule AzureRM -AllVersions` från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="457a3-110">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="457a3-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="457a3-111">Azure Cloud Shell</span></span>

<span data-ttu-id="457a3-112">Det enklaste sättet att komma igång är att [starta Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="457a3-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="457a3-113">Starta Cloud Shell från det övre navigeringsfältet i Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="457a3-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell-ikon](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="457a3-115">Välj den prenumeration du vill använda och skapa ett lagringskonto.</span><span class="sxs-lookup"><span data-stu-id="457a3-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![skapar ett lagringskonto](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="457a3-117">När du har skapat din lagring öppnar Cloud Shell en PowerShell-session i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="457a3-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell för PowerShell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="457a3-119">Du kan även installera Azure PowerShell och använda det lokalt i en PowerShell-session.</span><span class="sxs-lookup"><span data-stu-id="457a3-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="457a3-120">Logga in på Azure</span><span class="sxs-lookup"><span data-stu-id="457a3-120">Sign in to Azure</span></span>

<span data-ttu-id="457a3-121">Logga in interaktivt:</span><span class="sxs-lookup"><span data-stu-id="457a3-121">Sign on interactively:</span></span>

1. <span data-ttu-id="457a3-122">Skriv `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="457a3-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="457a3-123">En dialogruta som frågar efter dina Azure-autentiseringsuppgifter visas.</span><span class="sxs-lookup"><span data-stu-id="457a3-123">You'll get a dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="457a3-124">Med alternativet "-Environment" kan du autentisera dig i Azure Kina eller Azure Tyskland.</span><span class="sxs-lookup"><span data-stu-id="457a3-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="457a3-125">till exempel Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="457a3-125">for example, Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="457a3-126">Ange e-postadressen och lösenordet som är kopplade till ditt konto.</span><span class="sxs-lookup"><span data-stu-id="457a3-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="457a3-127">Azure autentiserar och sparar autentiseringsuppgifterna och stänger sedan fönstret.</span><span class="sxs-lookup"><span data-stu-id="457a3-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="457a3-128">När du har loggat in på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="457a3-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="457a3-129">Skapa en virtuell Windows-dator med enkla standardinställningar</span><span class="sxs-lookup"><span data-stu-id="457a3-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="457a3-130">Cmdleten `New-AzureRmVM` tillhandahåller en förenklad syntax som gör det enkelt att skapa en ny virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="457a3-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="457a3-131">Det är bara två parametervärden du måste ange: namnet på den virtuella datorn och en uppsättning autentiseringsuppgifter för det lokala administratörskontot på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="457a3-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="457a3-132">Först skapar du autentiseringsobjektet.</span><span class="sxs-lookup"><span data-stu-id="457a3-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="457a3-133">Sedan skapar du den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="457a3-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="457a3-134">Du kanske undrar vad det är mer som skapas och hur den virtuella datorn konfigureras.</span><span class="sxs-lookup"><span data-stu-id="457a3-134">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="457a3-135">Vi kan först titta på våra resursgrupper.</span><span class="sxs-lookup"><span data-stu-id="457a3-135">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="457a3-136">Resursgruppen **cloud-shell-storage-westus** skapas första gången du använder Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="457a3-136">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="457a3-137">Resursgruppen **SampleVM** skapades av cmdleten `New-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="457a3-137">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="457a3-138">Vilka andra resurser skapades i den här nya resursgruppen?</span><span class="sxs-lookup"><span data-stu-id="457a3-138">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="457a3-139">Låt oss ta reda på lite mer om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="457a3-139">Let's get some more details about the VM.</span></span> <span data-ttu-id="457a3-140">Det här exemplet visar hur du hämtar information om operativsystemavbildningen som används för att skapa den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="457a3-140">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="457a3-141">Skapa en fullständigt konfigurerad virtuell Linux-dator</span><span class="sxs-lookup"><span data-stu-id="457a3-141">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="457a3-142">I det föregående exemplet användes ett förenklat syntax och parametervärdena som är standard för att skapa en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="457a3-142">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="457a3-143">I det här exemplet anger vi värden för alla alternativ för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="457a3-143">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="457a3-144">Skapa en resursgrupp</span><span class="sxs-lookup"><span data-stu-id="457a3-144">Create a resource group</span></span>

<span data-ttu-id="457a3-145">I det här exemplet vill vi skapa en resursgrupp.</span><span class="sxs-lookup"><span data-stu-id="457a3-145">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="457a3-146">Resursgrupper i Azure ger ett sätt att hantera flera resurser som du vill gruppera logiskt.</span><span class="sxs-lookup"><span data-stu-id="457a3-146">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="457a3-147">Du kan till exempel skapa en resursgrupp för ett program eller projekt och lägga till en virtuell dator, en databas och en CDN-tjänst inom den.</span><span class="sxs-lookup"><span data-stu-id="457a3-147">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="457a3-148">Vi ska skapa en resursgrupp med namnet "MyResourceGroup" i den västeuropeiska regionen för Azure.</span><span class="sxs-lookup"><span data-stu-id="457a3-148">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="457a3-149">Ange följande kommando:</span><span class="sxs-lookup"><span data-stu-id="457a3-149">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="457a3-150">Den här nya resursgruppen används för att lagra alla resurser som behövs för den nya virtuella datorn som vi skapar.</span><span class="sxs-lookup"><span data-stu-id="457a3-150">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="457a3-151">För att kunna skapa en ny virtuell Linux-dator måste vi först skapa de övriga resurser som krävs och tilldela dem till en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="457a3-151">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="457a3-152">Vi kan sedan använda den konfigurationen för att skapa den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="457a3-152">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="457a3-153">Du behöver även ha en offentlig SSH-nyckel med namnet `id_rsa.pub` i .ssh-katalogen för din användarprofil.</span><span class="sxs-lookup"><span data-stu-id="457a3-153">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="457a3-154">Skapa nätverksresurser som krävs</span><span class="sxs-lookup"><span data-stu-id="457a3-154">Create the required network resources</span></span>

<span data-ttu-id="457a3-155">Vi måste först skapa en undernätskonfiguration som ska användas med processen för att skapa virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="457a3-155">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="457a3-156">Vi skapar också en offentlig IP-adress så att vi kan ansluta till denna virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="457a3-156">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="457a3-157">Vi skapar en nätverkssäkerhetsgrupp för att säkra åtkomst till den offentliga adressen.</span><span class="sxs-lookup"><span data-stu-id="457a3-157">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="457a3-158">Slutligen skapar vi ett virtuellt nätverkskort med alla föregående resurser.</span><span class="sxs-lookup"><span data-stu-id="457a3-158">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="457a3-159">Skapa VM-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="457a3-159">Create the VM configuration</span></span>

<span data-ttu-id="457a3-160">Nu när vi har de nödvändiga resurserna kan vi skapa VM-konfigurationsobjektet.</span><span class="sxs-lookup"><span data-stu-id="457a3-160">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="457a3-161">Skapa den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="457a3-161">Create the virtual machine</span></span>

<span data-ttu-id="457a3-162">Vi kan nu skapa den virtuella datorn med VM-konfigurationsobjektet.</span><span class="sxs-lookup"><span data-stu-id="457a3-162">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="457a3-163">Nu när den virtuella datorn har skapats kan du logga in på den nya virtuella Linux-datorn med hjälp av SSH med den offentliga IP-adressen för den virtuella dator du skapade:</span><span class="sxs-lookup"><span data-stu-id="457a3-163">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="457a3-164">Skapa andra resurser i Azure</span><span class="sxs-lookup"><span data-stu-id="457a3-164">Creating other resources in Azure</span></span>

<span data-ttu-id="457a3-165">Vi har nu gått igenom hur du skapar en resursgrupp, en virtuell Linux-dator och en virtuell Windows Server-dator.</span><span class="sxs-lookup"><span data-stu-id="457a3-165">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="457a3-166">Du kan även skapa många andra typer av Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="457a3-166">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="457a3-167">Om du till exempel vill skapa en lastbalanserare för Azure-nätverk som vi sedan kan koppla till de virtuella datorer vi precis har skapat kan vi använda följande kommando för att skapa:</span><span class="sxs-lookup"><span data-stu-id="457a3-167">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="457a3-168">Vi kan också skapa ett nytt privat virtuellt nätverk (som ofta kallas ett "VNet" i Azure) för infrastrukturen med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="457a3-168">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="457a3-169">Det som gör Azure och Azure PowerShell så kraftfulla är att vi kan använda dem inte bara för att få molnbaserad infrastruktur, utan också för att skapa hanterade plattformstjänster.</span><span class="sxs-lookup"><span data-stu-id="457a3-169">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="457a3-170">De hanterade plattformstjänsterna kan också kombineras med infrastruktur för att skapa ännu mer kraftfulla lösningar.</span><span class="sxs-lookup"><span data-stu-id="457a3-170">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="457a3-171">Du kan till exempel använda Azure PowerShell för att skapa en Azure AppService.</span><span class="sxs-lookup"><span data-stu-id="457a3-171">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="457a3-172">Azure AppService är en hanterad plattformstjänst som ger ett utmärkt sätt att agera värd för webbappar utan att behöva bekymra sig över infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="457a3-172">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="457a3-173">När du har skapat Azure AppService kan du skapa två nya Azure-webbappar i AppService med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="457a3-173">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="457a3-174">Skapa en lista över distribuerade resurser</span><span class="sxs-lookup"><span data-stu-id="457a3-174">Listing deployed resources</span></span>

<span data-ttu-id="457a3-175">Du kan använda cmdleten `Get-AzureRmResource` för att få fram en lista över de resurser som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="457a3-175">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="457a3-176">I följande exempel visas resurserna som vi skapade i den nya resursgruppen.</span><span class="sxs-lookup"><span data-stu-id="457a3-176">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="457a3-177">Ta bort resurser</span><span class="sxs-lookup"><span data-stu-id="457a3-177">Deleting resources</span></span>

<span data-ttu-id="457a3-178">Om du vill rensa i Azure-kontot kan du ta bort de resurser vi skapade i detta exempel.</span><span class="sxs-lookup"><span data-stu-id="457a3-178">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="457a3-179">Du kan använda cmdletarna `Remove-AzureRm*` för att ta bort de resurser du inte längre behöver.</span><span class="sxs-lookup"><span data-stu-id="457a3-179">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="457a3-180">Använd följande kommando om du vill ta bort den virtuella Windows-dator vi skapade:</span><span class="sxs-lookup"><span data-stu-id="457a3-180">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="457a3-181">Du uppmanas att bekräfta att du vill ta bort resursen.</span><span class="sxs-lookup"><span data-stu-id="457a3-181">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="457a3-182">Du kan också ta bort många resurser på samma gång.</span><span class="sxs-lookup"><span data-stu-id="457a3-182">You can also delete many resources at once.</span></span> <span data-ttu-id="457a3-183">Följande kommando tar till exempel bort resursgruppen "MyResourceGroup" som vi har använt för alla exempel hittills.</span><span class="sxs-lookup"><span data-stu-id="457a3-183">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="457a3-184">Alla resurser i gruppen tas också bort.</span><span class="sxs-lookup"><span data-stu-id="457a3-184">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="457a3-185">Uppgiften kan ta flera minuter att slutföra, beroende på antal och typ av resurser.</span><span class="sxs-lookup"><span data-stu-id="457a3-185">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="457a3-186">Hämta exempel</span><span class="sxs-lookup"><span data-stu-id="457a3-186">Get samples</span></span>

<span data-ttu-id="457a3-187">Om du vill lära dig mer om att använda Azure PowerShell kan du ta en titt på våra vanligaste skript för [virtuella Linux-datorer](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuella Windows-datorer](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [webbappar](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) och [SQL-databaser](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="457a3-187">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="457a3-188">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="457a3-188">Next steps</span></span>

* [<span data-ttu-id="457a3-189">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="457a3-189">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="457a3-190">Hantera Azure-prenumerationer med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="457a3-190">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="457a3-191">Skapa tjänstens huvudnamn i Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="457a3-191">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="457a3-192">Läs [den viktiga informationen](./release-notes-azureps.md) om hur du migrerar från en äldre version.</span><span class="sxs-lookup"><span data-stu-id="457a3-192">Read the [Release notes](./release-notes-azureps.md) about migrating from an older release.</span></span>
* <span data-ttu-id="457a3-193">Få hjälp från communityn:</span><span class="sxs-lookup"><span data-stu-id="457a3-193">Get help from the community:</span></span>
  * [<span data-ttu-id="457a3-194">Azure-forumet på MSDN</span><span class="sxs-lookup"><span data-stu-id="457a3-194">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="457a3-195">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="457a3-195">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
