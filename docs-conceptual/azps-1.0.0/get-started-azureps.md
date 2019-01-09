---
title: Komma igång med Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 10/30/2018
ms.openlocfilehash: 7367648a0a84cd5be5c7501ef4bf743a4290ce0f
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982917"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="c8635-102">Komma igång med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8635-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="c8635-103">Azure PowerShell har utformats för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="c8635-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="c8635-104">Du kan använda Azure PowerShell i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator.</span><span class="sxs-lookup"><span data-stu-id="c8635-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="c8635-105">Den här artikeln hjälper dig att komma igång med Azure PowerShell och du får lära dig grundbegreppen.</span><span class="sxs-lookup"><span data-stu-id="c8635-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="c8635-106">Installera Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8635-106">Install Azure PowerShell</span></span>

<span data-ttu-id="c8635-107">Det första steget är att kontrollera att du har den senaste versionen av Azure PowerShell installerad.</span><span class="sxs-lookup"><span data-stu-id="c8635-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="c8635-108">Information om den senaste versionen finns i [viktig information](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c8635-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="c8635-109">[Installera Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="c8635-109">[Install Azure PowerShell](install-az-ps.md).</span></span>

2. <span data-ttu-id="c8635-110">Kontrollera att installationen lyckades genom att köra `Get-InstalledModule Az -AllVersions` från kommandoraden.</span><span class="sxs-lookup"><span data-stu-id="c8635-110">To verify the installation was successful, run `Get-InstalledModule Az -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="c8635-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="c8635-111">Azure Cloud Shell</span></span>

<span data-ttu-id="c8635-112">Det enklaste sättet att komma igång är att [starta Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="c8635-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="c8635-113">Starta Cloud Shell från det övre navigeringsfältet i Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="c8635-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell-ikon](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="c8635-115">Välj den prenumeration du vill använda och skapa ett lagringskonto.</span><span class="sxs-lookup"><span data-stu-id="c8635-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![skapar ett lagringskonto](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="c8635-117">När du har skapat din lagring öppnar Cloud Shell en PowerShell-session i webbläsaren.</span><span class="sxs-lookup"><span data-stu-id="c8635-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Cloud Shell för PowerShell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a><span data-ttu-id="c8635-119">Logga in på Azure</span><span class="sxs-lookup"><span data-stu-id="c8635-119">Sign in to Azure</span></span>

<span data-ttu-id="c8635-120">Logga in interaktivt:</span><span class="sxs-lookup"><span data-stu-id="c8635-120">Sign on interactively:</span></span>

1. <span data-ttu-id="c8635-121">Skriv `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="c8635-121">Type `Connect-AzAccount`.</span></span> <span data-ttu-id="c8635-122">Med argumentet `-Environment` kan du autentisera för en annan region eller ett annat moln.</span><span class="sxs-lookup"><span data-stu-id="c8635-122">The `-Environment` argument lets you authenticate for a different region or cloud.</span></span> <span data-ttu-id="c8635-123">Om du till exempel vill ansluta till Azure i Kina:</span><span class="sxs-lookup"><span data-stu-id="c8635-123">For example, to connect to Azure China:</span></span>

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. <span data-ttu-id="c8635-124">Du får ett token att använda på https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="c8635-124">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="c8635-125">Öppna den här sidan i webbläsaren och ange token för att logga in med dina Azure-autentiseringsuppgifter och auktorisera Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c8635-125">Open this page in your browser and enter the token to sign in with your Azure credentials, and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="c8635-126">När du har loggat in på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="c8635-126">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span> <span data-ttu-id="c8635-127">Läs mer om inloggningsprocessen och tillgängliga autentiseringsmetoder i [Logga in med Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="c8635-127">To learn more about the sign in process and available authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="c8635-128">Skapa en virtuell Windows-dator med enkla standardinställningar</span><span class="sxs-lookup"><span data-stu-id="c8635-128">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="c8635-129">Cmdleten `New-AzVM` tillhandahåller en förenklad syntax som gör det enkelt att skapa en ny virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="c8635-129">The `New-AzVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="c8635-130">Det är bara två parametervärden du måste ange: namnet på den virtuella datorn och en uppsättning autentiseringsuppgifter för det lokala administratörskontot på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c8635-130">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="c8635-131">Först skapar du autentiseringsobjektet.</span><span class="sxs-lookup"><span data-stu-id="c8635-131">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="c8635-132">Sedan skapar du den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c8635-132">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzVM -Name SampleVM -Credential $cred
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

<span data-ttu-id="c8635-133">Du kanske undrar vad det är mer som skapas och hur den virtuella datorn konfigureras.</span><span class="sxs-lookup"><span data-stu-id="c8635-133">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="c8635-134">Vi kan först titta på våra resursgrupper.</span><span class="sxs-lookup"><span data-stu-id="c8635-134">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="c8635-135">Resursgruppen **cloud-shell-storage-westus** skapas första gången du använder Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="c8635-135">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="c8635-136">Resursgruppen **SampleVM** skapades av cmdleten `New-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="c8635-136">The **SampleVM** resource group was created by the `New-AzVM` cmdlet.</span></span>

<span data-ttu-id="c8635-137">Vilka andra resurser skapades i den här nya resursgruppen?</span><span class="sxs-lookup"><span data-stu-id="c8635-137">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzResource |
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

<span data-ttu-id="c8635-138">Låt oss ta reda på lite mer om den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c8635-138">Let's get some more details about the VM.</span></span> <span data-ttu-id="c8635-139">Det här exemplet visar hur du hämtar information om operativsystemavbildningen som används för att skapa den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c8635-139">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzVM -Name SampleVM -ResourceGroupName SampleVM |
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

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="c8635-140">Skapa en fullständigt konfigurerad virtuell Linux-dator</span><span class="sxs-lookup"><span data-stu-id="c8635-140">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="c8635-141">I det föregående exemplet användes ett förenklat syntax och parametervärdena som är standard för att skapa en virtuell Windows-dator.</span><span class="sxs-lookup"><span data-stu-id="c8635-141">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="c8635-142">I det här exemplet anger vi värden för alla alternativ för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c8635-142">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="c8635-143">Skapa en resursgrupp</span><span class="sxs-lookup"><span data-stu-id="c8635-143">Create a resource group</span></span>

<span data-ttu-id="c8635-144">I det här exemplet vill vi skapa en resursgrupp.</span><span class="sxs-lookup"><span data-stu-id="c8635-144">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="c8635-145">Resursgrupper i Azure ger ett sätt att hantera flera resurser som du vill gruppera logiskt.</span><span class="sxs-lookup"><span data-stu-id="c8635-145">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="c8635-146">Du kan till exempel skapa en resursgrupp för ett program eller projekt och lägga till en virtuell dator, en databas och en CDN-tjänst inom den.</span><span class="sxs-lookup"><span data-stu-id="c8635-146">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="c8635-147">Vi skapar en resursgrupp med namnet "MyResourceGroup" i regionen uswest2 för Azure.</span><span class="sxs-lookup"><span data-stu-id="c8635-147">Let's create a resource group named "MyResourceGroup" in the uswest2 region of Azure.</span></span> <span data-ttu-id="c8635-148">Ange följande kommando:</span><span class="sxs-lookup"><span data-stu-id="c8635-148">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name 'myResourceGroup' -Location 'westus2'
```

```output
ResourceGroupName : myResourceGroup
Location          : westus2
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="c8635-149">Den här nya resursgruppen används för att lagra alla resurser som behövs för den nya virtuella datorn som vi skapar.</span><span class="sxs-lookup"><span data-stu-id="c8635-149">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="c8635-150">För att kunna skapa en ny virtuell Linux-dator måste vi först skapa de övriga resurser som krävs och tilldela dem till en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c8635-150">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="c8635-151">Vi kan sedan använda den konfigurationen för att skapa den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="c8635-151">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="c8635-152">Du behöver även ha en offentlig SSH-nyckel med namnet `id_rsa.pub` i `.ssh`-katalogen för din användarprofil.</span><span class="sxs-lookup"><span data-stu-id="c8635-152">Also, you will need to have an SSH public key named `id_rsa.pub` in the `.ssh` directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="c8635-153">Skapa nätverksresurser som krävs</span><span class="sxs-lookup"><span data-stu-id="c8635-153">Create the required network resources</span></span>

<span data-ttu-id="c8635-154">Vi måste först skapa en undernätskonfiguration som ska användas med processen för att skapa virtuella nätverk.</span><span class="sxs-lookup"><span data-stu-id="c8635-154">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="c8635-155">Vi skapar också en offentlig IP-adress så att vi kan ansluta till denna virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="c8635-155">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="c8635-156">Vi skapar en nätverkssäkerhetsgrupp för att säkra åtkomst till den offentliga adressen.</span><span class="sxs-lookup"><span data-stu-id="c8635-156">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="c8635-157">Slutligen skapar vi ett virtuellt nätverkskort med alla föregående resurser.</span><span class="sxs-lookup"><span data-stu-id="c8635-157">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westus2"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="c8635-158">Skapa VM-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="c8635-158">Create the VM configuration</span></span>

<span data-ttu-id="c8635-159">Nu när vi har de nödvändiga resurserna kan vi skapa VM-konfigurationsobjektet.</span><span class="sxs-lookup"><span data-stu-id="c8635-159">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B1s |
  Set-AzVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="c8635-160">Skapa den virtuella datorn</span><span class="sxs-lookup"><span data-stu-id="c8635-160">Create the virtual machine</span></span>

<span data-ttu-id="c8635-161">Vi kan nu skapa den virtuella datorn med VM-konfigurationsobjektet.</span><span class="sxs-lookup"><span data-stu-id="c8635-161">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="c8635-162">Nu när den virtuella datorn har skapats kan du logga in på den nya virtuella Linux-datorn med hjälp av SSH med den offentliga IP-adressen för den virtuella dator du skapade:</span><span class="sxs-lookup"><span data-stu-id="c8635-162">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```powershell-interactive
ssh azureuser@$($publicIp.IpAddress)
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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="c8635-163">Skapa andra resurser i Azure</span><span class="sxs-lookup"><span data-stu-id="c8635-163">Creating other resources in Azure</span></span>

<span data-ttu-id="c8635-164">Vi har nu gått igenom hur du skapar en resursgrupp, en virtuell Linux-dator och en virtuell Windows Server-dator.</span><span class="sxs-lookup"><span data-stu-id="c8635-164">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="c8635-165">Du kan även skapa många andra typer av Azure-resurser.</span><span class="sxs-lookup"><span data-stu-id="c8635-165">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="c8635-166">Om du till exempel vill skapa en lastbalanserare för Azure-nätverk som vi sedan kan koppla till de virtuella datorer vi precis har skapat kan vi använda följande kommando för att skapa:</span><span class="sxs-lookup"><span data-stu-id="c8635-166">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

<span data-ttu-id="c8635-167">Vi kan också skapa ett nytt privat virtuellt nätverk (som ofta kallas ett "VNet" i Azure) för infrastrukturen med följande kommando:</span><span class="sxs-lookup"><span data-stu-id="c8635-167">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="c8635-168">Det som gör Azure och Azure PowerShell så kraftfulla är att vi kan använda dem inte bara för att få molnbaserad infrastruktur, utan också för att skapa hanterade plattformstjänster.</span><span class="sxs-lookup"><span data-stu-id="c8635-168">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="c8635-169">De hanterade plattformstjänsterna kan också kombineras med infrastruktur för att skapa ännu mer kraftfulla lösningar.</span><span class="sxs-lookup"><span data-stu-id="c8635-169">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="c8635-170">Du kan till exempel använda Azure PowerShell för att skapa en Azure AppService.</span><span class="sxs-lookup"><span data-stu-id="c8635-170">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="c8635-171">Azure AppService är en hanterad plattformstjänst som ger ett utmärkt sätt att agera värd för webbappar utan att behöva bekymra sig över infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="c8635-171">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="c8635-172">När du har skapat Azure AppService kan du skapa två nya Azure-webbappar i AppService med hjälp av följande kommandon:</span><span class="sxs-lookup"><span data-stu-id="c8635-172">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="c8635-173">Skapa en lista över distribuerade resurser</span><span class="sxs-lookup"><span data-stu-id="c8635-173">Listing deployed resources</span></span>

<span data-ttu-id="c8635-174">Du kan använda cmdleten `Get-AzResource` för att få fram en lista över de resurser som körs i Azure.</span><span class="sxs-lookup"><span data-stu-id="c8635-174">You can use the `Get-AzResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="c8635-175">I följande exempel visas resurserna som vi skapade i den nya resursgruppen.</span><span class="sxs-lookup"><span data-stu-id="c8635-175">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westus2 Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westus2 Microsoft.Compute/disks
myLinuxVM                                             westus2 Microsoft.Compute/virtualMachines
myWindowsVM                                           westus2 Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westus2 Microsoft.Compute/virtualMachines/extensions
myNic1                                                westus2 Microsoft.Network/networkInterfaces
myNic2                                                westus2 Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westus2 Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westus2 Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westus2 Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westus2 Microsoft.Network/publicIPAddresses
MYvNET1                                               westus2 Microsoft.Network/virtualNetworks
MYvNET2                                               westus2 Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westus2 Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="c8635-176">Ta bort resurser</span><span class="sxs-lookup"><span data-stu-id="c8635-176">Deleting resources</span></span>

<span data-ttu-id="c8635-177">Om du vill rensa i Azure-kontot kan du ta bort de resurser vi skapade i detta exempel.</span><span class="sxs-lookup"><span data-stu-id="c8635-177">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="c8635-178">Du kan använda cmdletarna `Remove-Az*` för att ta bort de resurser du inte längre behöver.</span><span class="sxs-lookup"><span data-stu-id="c8635-178">You can use the `Remove-Az*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="c8635-179">Använd följande kommando om du vill ta bort den virtuella Windows-dator vi skapade:</span><span class="sxs-lookup"><span data-stu-id="c8635-179">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="c8635-180">Du uppmanas att bekräfta att du vill ta bort resursen.</span><span class="sxs-lookup"><span data-stu-id="c8635-180">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c8635-181">Du kan också ta bort många resurser på samma gång.</span><span class="sxs-lookup"><span data-stu-id="c8635-181">You can also delete many resources at once.</span></span> <span data-ttu-id="c8635-182">Följande kommando tar till exempel bort resursgruppen "MyResourceGroup" som vi har använt för alla exempel hittills.</span><span class="sxs-lookup"><span data-stu-id="c8635-182">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="c8635-183">Alla resurser i gruppen tas också bort.</span><span class="sxs-lookup"><span data-stu-id="c8635-183">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c8635-184">Uppgiften kan ta flera minuter att slutföra, beroende på antal och typ av resurser.</span><span class="sxs-lookup"><span data-stu-id="c8635-184">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="c8635-185">Hämta exempel</span><span class="sxs-lookup"><span data-stu-id="c8635-185">Get samples</span></span>

<span data-ttu-id="c8635-186">Om du vill lära dig mer om att använda Azure PowerShell kan du ta en titt på våra vanligaste skript för [virtuella Linux-datorer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuella Windows-datorer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [webbappar](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) och [SQL-databaser](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c8635-186">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="c8635-187">Nästa steg</span><span class="sxs-lookup"><span data-stu-id="c8635-187">Next steps</span></span>

* [<span data-ttu-id="c8635-188">Logga in med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8635-188">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="c8635-189">Hantera Azure-prenumerationer med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8635-189">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="c8635-190">Skapa tjänstens huvudnamn i Azure med Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c8635-190">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="c8635-191">Få hjälp från communityn:</span><span class="sxs-lookup"><span data-stu-id="c8635-191">Get help from the community:</span></span>
  * [<span data-ttu-id="c8635-192">Azure-forumet på MSDN</span><span class="sxs-lookup"><span data-stu-id="c8635-192">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="c8635-193">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="c8635-193">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
