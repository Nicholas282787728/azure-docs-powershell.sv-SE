---
title: Komma igång med Azure PowerShell
description: ''
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 474fd0cbabf3967f13b7f60e02158fc2c9a106cc
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523333"
---
# <a name="get-started-with-azure-powershell"></a>Komma igång med Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell har utformats för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager. Du kan använda Azure PowerShell i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator. Den här artikeln hjälper dig att komma igång med Azure PowerShell och du får lära dig grundbegreppen.

## <a name="install-azure-powershell"></a>Installera Azure PowerShell

Det första steget är att kontrollera att du har den senaste versionen av Azure PowerShell installerad. Information om den senaste versionen finns i [viktig information](./release-notes-azureps.md).

1. [Installera Azure PowerShell](install-azurerm-ps.md).

2. Kontrollera att installationen lyckades genom att köra `Get-InstalledModule AzureRM -AllVersions` från kommandoraden.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

Det enklaste sättet att komma igång är att [starta Cloud Shell](/azure/cloud-shell/quickstart).

1. Starta Cloud Shell från det övre navigeringsfältet i Azure Portal.

   ![Shell-ikon](~/media/get-started-azureps/shell-icon.png)

2. Välj den prenumeration du vill använda och skapa ett lagringskonto.

   ![skapar ett lagringskonto](~/media/get-started-azureps/storage-prompt.png)

När du har skapat din lagring öppnar Cloud Shell en PowerShell-session i webbläsaren.

![Cloud Shell för PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Du kan även installera Azure PowerShell och använda det lokalt i en PowerShell-session.

## <a name="sign-in-to-azure"></a>Logga in på Azure

Logga in interaktivt:

1. Skriv `Connect-AzureRmAccount`. En dialogruta som frågar efter dina Azure-autentiseringsuppgifter visas. Med alternativet "-Environment" kan du tillåtas att logga in i Azure Kina eller Azure Tyskland.

   t.ex. Connect-AzureRmAccount -Environment AzureChinaCloud

2. Ange e-postadressen och lösenordet som är kopplade till ditt konto. Azure autentiserar och sparar autentiseringsuppgifterna och stänger sedan fönstret.

När du har loggat in på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Skapa en virtuell Windows-dator med enkla standardinställningar

Cmdleten `New-AzureRmVM` tillhandahåller en förenklad syntax som gör det enkelt att skapa en ny virtuell dator. Det är bara två parametervärden du måste ange: namnet på den virtuella datorn och en uppsättning autentiseringsuppgifter för det lokala administratörskontot på den virtuella datorn.

Först skapar du autentiseringsobjektet.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Sedan skapar du den virtuella datorn.

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

Det var enkelt. Men du kanske undrar vad det är mer som skapas och hur den virtuella datorn konfigureras. Vi kan först titta på våra resursgrupper.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

Resursgruppen **cloud-shell-storage-westus** skapas första gången du använder Cloud Shell. Resursgruppen **SampleVM** skapades av cmdleten `New-AzureRmVM`.

Vilka andra resurser skapades i den här nya resursgruppen?

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

Låt oss ta reda på lite mer om den virtuella datorn. De här exemplen visar hur du hämtar information om operativsystemavbildningen som används för att skapa den virtuella datorn.

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Skapa en fullständigt konfigurerad virtuell Linux-dator

I det föregående exemplet användes ett förenklat syntax och parametervärdena som är standard för att skapa en virtuell Windows-dator. I det här exemplet anger vi värden för alla alternativ för den virtuella datorn.

### <a name="create-a-resource-group"></a>Skapa en resursgrupp

I det här exemplet vill vi skapa en resursgrupp. Resursgrupper i Azure ger ett sätt att hantera flera resurser som du vill gruppera logiskt. Du kan till exempel skapa en resursgrupp för ett program eller projekt och lägga till en virtuell dator, en databas och en CDN-tjänst inom den.

Vi ska skapa en resursgrupp med namnet "MyResourceGroup" i den västeuropeiska regionen för Azure. Ange följande kommando:

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

Den här nya resursgruppen används för att lagra alla resurser som behövs för den nya virtuella datorn som vi skapar. För att kunna skapa en ny virtuell Linux-dator måste vi först skapa de övriga resurser som krävs och tilldela dem till en konfiguration. Vi kan sedan använda den konfigurationen för att skapa den virtuella datorn. Du behöver även ha en offentlig SSH-nyckel med namnet `id_rsa.pub` i .ssh-katalogen för din användarprofil.

#### <a name="create-the-required-network-resources"></a>Skapa nätverksresurser som krävs

Vi måste först skapa en undernätskonfiguration som ska användas med processen för att skapa virtuella nätverk. Vi skapar också en offentlig IP-adress så att vi kan ansluta till denna virtuella dator. Vi skapar en nätverkssäkerhetsgrupp för att säkra åtkomst till den offentliga adressen. Slutligen skapar vi ett virtuellt nätverkskort med alla föregående resurser.

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

### <a name="create-the-vm-configuration"></a>Skapa VM-konfigurationen

Nu när vi har de nödvändiga resurserna kan vi skapa VM-konfigurationsobjektet.

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

### <a name="create-the-virtual-machine"></a>Skapa den virtuella datorn

Vi kan nu skapa den virtuella datorn med VM-konfigurationsobjektet.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Nu när den virtuella datorn har skapats kan du logga in på den nya virtuella Linux-datorn med hjälp av SSH med den offentliga IP-adressen för den virtuella dator du skapade:

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

## <a name="creating-other-resources-in-azure"></a>Skapa andra resurser i Azure

Vi har nu gått igenom hur du skapar en resursgrupp, en virtuell Linux-dator och en virtuell Windows Server-dator. Du kan även skapa många andra typer av Azure-resurser.

Om du till exempel vill skapa en lastbalanserare för Azure-nätverk som vi sedan kan koppla till de virtuella datorer vi precis har skapat kan vi använda följande kommando för att skapa:

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Vi kan också skapa ett nytt privat virtuellt nätverk (som ofta kallas ett "VNet" i Azure) för infrastrukturen med följande kommando:

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Det som gör Azure och Azure PowerShell så kraftfulla är att vi kan använda dem inte bara för att få molnbaserad infrastruktur, utan också för att skapa hanterade plattformstjänster. De hanterade plattformstjänsterna kan också kombineras med infrastruktur för att skapa ännu mer kraftfulla lösningar.

Du kan till exempel använda Azure PowerShell för att skapa en Azure AppService. Azure AppService är en hanterad plattformstjänst som ger ett utmärkt sätt att agera värd för webbappar utan att behöva bekymra sig över infrastruktur. När du har skapat Azure AppService kan du skapa två nya Azure-webbappar i AppService med hjälp av följande kommandon:

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Skapa en lista över distribuerade resurser

Du kan använda cmdleten `Get-AzureRmResource` för att få fram en lista över de resurser som körs i Azure. I följande exempel visas resurserna som vi nyss skapade i den nya resursgruppen.

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

## <a name="deleting-resources"></a>Ta bort resurser

Om du vill rensa i Azure-kontot kan du ta bort de resurser vi skapade i detta exempel. Du kan använda cmdletarna `Remove-AzureRm*` för att ta bort de resurser du inte längre behöver. Använd följande kommando om du vill ta bort den virtuella Windows-dator vi skapade:

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Du uppmanas att bekräfta att du vill ta bort resursen.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Du kan också ta bort många resurser i taget. Följande kommando tar till exempel bort hela resursgruppen "MyResourceGroup" som vi har använt för alla exempel i denna handledning. Detta tar bort resursgruppen och alla resurser i den.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Det kan ta flera minuter att slutföra.

## <a name="get-samples"></a>Hämta exempel

Om du vill lära dig mer om att använda Azure PowerShell kan du ta en titt på våra vanligaste skript för [virtuella Linux-datorer](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuella Windows-datorer](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [webbappar](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) och [SQL-databaser](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Nästa steg

* [Logga in med Azure PowerShell](authenticate-azureps.md)
* [Hantera Azure-prenumerationer med Azure PowerShell](manage-subscriptions-azureps.md)
* [Skapa tjänstens huvudnamn i Azure med Azure PowerShell](create-azure-service-principal-azureps.md)
* Läs [den viktiga informationen](./release-notes-azureps.md) om hur du migrerar från en äldre version.
* Få hjälp från communityn:
  * [Azure-forumet på MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](https://go.microsoft.com/fwlink/?LinkId=320213)
