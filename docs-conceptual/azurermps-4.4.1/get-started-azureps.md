---
title: Komma igång med Azure PowerShell | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 0897e8fc3a50a58ac8945bd95722736526f63e19
ms.sourcegitcommit: 990f82648b0aa2e970f96c02466a7134077c8c56
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/11/2018
ms.locfileid: "38100162"
---
# <a name="getting-started-with-azure-powershell"></a>Komma igång med Azure PowerShell

Azure PowerShell har utformats för att hantera och administrera Azure-resurser från kommandoraden och för att skapa automatiseringsskript som fungerar mot Azure Resource Manager. Du kan använda det i webbläsaren med [Azure Cloud Shell](/azure/cloud-shell/overview) eller installera det på din lokala dator och använda det i PowerShell-sessioner. Den här artikeln hjälper dig att komma igång med att använda det och lär dig grundbegreppen bakom.

## <a name="connect"></a>Anslut

Det enklaste sättet att komma igång är att [starta Cloud Shell](/azure/cloud-shell/quickstart).

1. Starta Cloud Shell från det övre navigeringsfältet i Azure Portal.

   ![Shell-ikon](~/media/get-started-azureps/shell-icon.png)

2. Välj den prenumeration du vill använda och skapa ett lagringskonto.

   ![skapar ett lagringskonto](~/media/get-started-azureps/storage-prompt.png)

När du har skapat din lagring öppnar Cloud Shell en PowerShell-session i webbläsaren.

![Cloud Shell för PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Du kan även installera Azure PowerShell och använda det lokalt i en PowerShell-session.

## <a name="install-azure-powershell"></a>Installera Azure PowerShell

Det första steget är att kontrollera att du har den senaste versionen av Azure PowerShell installerad. Information om den senaste versionen finns i [viktig information](./release-notes-azureps.md).

1. [Installera Azure PowerShell](install-azurerm-ps.md).

2. Kontrollera att installationen lyckades genom att köra `Get-Module AzureRM -ListAvailable` från kommandoraden.

## <a name="sign-in-to-azure"></a>Logga in på Azure

Logga in interaktivt:

1. Skriv `Login-AzureRmAccount`. En dialogruta som frågar efter dina Azure-autentiseringsuppgifter visas. Med alternativet "-EnvironmentName" kan du autentisera dig i Azure Kina eller Azure Tyskland.

   t.ex. Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Ange e-postadressen och lösenordet som är kopplade till ditt konto. Azure autentiserar och sparar autentiseringsuppgifterna och stänger sedan fönstret.

När du har loggat in på ett Azure-konto kan du använda Azure PowerShell-cmdletar för att komma åt och hantera resurserna i prenumerationen.

## <a name="create-a-resource-group"></a>Skapa en resursgrupp

Nu när allt har konfigurerats ska vi använda Azure PowerShell för att skapa resurser i Azure.

Skapa först en resursgrupp. Resursgrupper i Azure ger ett sätt att hantera flera resurser som du vill gruppera logiskt. Du kan till exempel skapa en resursgrupp för ett program eller projekt och lägga till en virtuell dator, en databas och en CDN-tjänst inom den.

Vi ska skapa en resursgrupp med namnet "MyResourceGroup" i den västeuropeiska regionen för Azure. Ange följande kommando:

```powershell
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Skapa en virtuell Windows-dator

Nu när vi har en resursgrupp kan vi skapa en virtuell Windows-dator i den. För att kunna skapa en ny virtuell dator måste vi först skapa de övriga resurser som krävs och tilldela dem till en konfiguration. Vi kan sedan använda den konfigurationen för att skapa den virtuella datorn.

### <a name="create-the-required-network-resources"></a>Skapa nätverksresurser som krävs

Vi måste först skapa en undernätskonfiguration som ska användas med processen för att skapa virtuella nätverk. Vi skapar också en offentlig IP-adress så att vi kan ansluta till denna virtuella dator. Vi skapar en nätverkssäkerhetsgrupp för att säkra åtkomst till den offentliga adressen. Slutligen skapar vi ett virtuellt nätverkskort med alla föregående resurser.

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Skapa den virtuella datorn

Vi måste först ha en uppsättning autentiseringsuppgifter för operativsystemet.

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Nu när vi har de nödvändiga resurserna kan vi skapa den virtuella datorn. För detta steg skapar vi ett VM-konfigurationsobjekt och sedan använder vi konfigurationen för att skapa den virtuella datorn.

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Kommandot `New-AzureRmVM` ger resultat när den virtuella datorn har skapats färdigt och är redo att användas.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Logga nu in på den virtuella Windows Server-dator som har skapats med hjälp av Fjärrskrivbord och den virtuella datorns offentliga IP-adress. Följande kommando visar den offentliga IP-adress som skapades i föregående skript.

```powershell
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Om du använder ett Windows-baserat system kan du göra detta från kommandoraden med mstsc-kommandot:

```powershell
mstsc /v:xx.xxx.xx.xxx
```

Ange samma kombination av användarnamn/lösenord för att logga in som du använde när du skapade den virtuella datorn.

## <a name="create-a-linux-virtual-machine"></a>Skapa en virtuell Linux-dator

För att kunna skapa en ny virtuell Linux-dator måste vi först skapa de övriga resurser som krävs och tilldela dem till en konfiguration. Vi kan sedan använda den konfigurationen för att skapa den virtuella datorn. Detta förutsätter att du redan har skapat resursgruppen på det sätt som visats tidigare. Du behöver även ha en offentlig SSH-nyckel med namnet `id_rsa.pub` i .ssh-katalogen för din användarprofil.

### <a name="create-the-required-network-resources"></a>Skapa nätverksresurser som krävs

Vi måste först skapa en undernätskonfiguration som ska användas med processen för att skapa virtuella nätverk. Vi skapar också en offentlig IP-adress så att vi kan ansluta till denna virtuella dator. Vi skapar en nätverkssäkerhetsgrupp för att säkra åtkomst till den offentliga adressen. Slutligen skapar vi ett virtuellt nätverkskort med alla föregående resurser.

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
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

### <a name="create-the-virtual-machine"></a>Skapa den virtuella datorn

Nu när vi har de nödvändiga resurserna kan vi skapa den virtuella datorn. För detta steg skapar vi ett VM-konfigurationsobjekt och sedan använder vi konfigurationen för att skapa den virtuella datorn.

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Nu när den virtuella datorn har skapats kan du logga in på den nya virtuella Linux-datorn med hjälp av SSH med den offentliga IP-adressen för den virtuella dator du skapade:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

Om du till exempel vill skapa en belastningsutjämnare för Azure-nätverk som vi sedan kan koppla till de virtuella datorer vi precis har skapat kan vi använda följande kommando för att skapa:

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Vi kan också skapa ett nytt privat virtuellt nätverk (som ofta kallas ett "VNet" i Azure) för infrastrukturen med följande kommando:

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Det som gör Azure och Azure PowerShell så kraftfulla är att vi kan använda dem inte bara för att få molnbaserad infrastruktur, utan också för att skapa hanterade plattformstjänster. De hanterade plattformstjänsterna kan också kombineras med infrastruktur för att skapa ännu mer kraftfulla lösningar.

Du kan till exempel använda Azure PowerShell för att skapa en Azure AppService. Azure AppService är en hanterad plattformstjänst som ger ett utmärkt sätt att agera värd för webbappar utan att behöva bekymra sig över infrastruktur. När du har skapat Azure AppService kan du skapa två nya Azure-webbappar i AppService med hjälp av följande kommandon:

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Skapa en lista över distribuerade resurser

Du kan använda cmdleten `Get-AzureRmResource` för att få fram en lista över de resurser som körs i Azure. I följande exempel visas resurserna som vi nyss skapade i den nya resursgruppen.

```powershell
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
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

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Du uppmanas att bekräfta att du vill ta bort resursen.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Du kan också ta bort många resurser i taget. Följande kommando tar till exempel bort hela resursgruppen "MyResourceGroup" som vi har använt för alla exempel i denna handledning. Detta tar bort resursgruppen och alla resurser i den.

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Det kan ta flera minuter att slutföra.

## <a name="get-samples"></a>Hämta exempel

Om du vill lära dig mer om att använda Azure PowerShell kan du ta en titt på våra vanligaste skript för [virtuella Linux-datorer](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [virtuella Windows-datorer](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [webbappar](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) och [SQL-databaser](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Nästa steg

* [Logga in med Azure PowerShell](authenticate-azureps.md)
* [Hantera Azure-prenumerationer med Azure PowerShell](manage-subscriptions-azureps.md)
* [Skapa tjänstens huvudnamn i Azure med Azure PowerShell](create-azure-service-principal-azureps.md)
* Läs den viktiga informationen om hur du migrerar från en äldre version: [ https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes ](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Få hjälp från communityn:
  * [Azure-forumet på MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
