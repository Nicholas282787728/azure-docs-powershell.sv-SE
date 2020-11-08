---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 914d942620eea7517b2bac635399fd7d1b3c1307
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091401"
---
# <span data-ttu-id="ddd77-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-101">New-AzVmss</span></span>

## <span data-ttu-id="ddd77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddd77-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd77-103">Skapar en VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd77-103">Creates a VMSS.</span></span>

## <span data-ttu-id="ddd77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddd77-104">SYNTAX</span></span>

### <span data-ttu-id="ddd77-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="ddd77-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddd77-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddd77-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd77-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddd77-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd77-108">Cmdleten **New-AzVmss** skapar en skal uppsättning för virtuell dator (VMSS) i Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd77-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="ddd77-109">Använd den enkla parameter uppsättningen ( `SimpleParameterSet` ) för att snabbt skapa en fördefinierad VMSS och tillhör ande resurser.</span><span class="sxs-lookup"><span data-stu-id="ddd77-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="ddd77-110">Använd standard parameter uppsättningen ( `DefaultParameter` ) för mer avancerade scenarier när du måste konfigurera varje komponent i VMSS och var och en av de associerade resurserna innan du skapar den.</span><span class="sxs-lookup"><span data-stu-id="ddd77-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="ddd77-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddd77-111">EXAMPLES</span></span>

### <span data-ttu-id="ddd77-112">Exempel 1: skapa en VMSS med hjälp av **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="ddd77-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="ddd77-113">Kommandot här skapar följande med namnet `$vmssName` :</span><span class="sxs-lookup"><span data-stu-id="ddd77-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="ddd77-114">En resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ddd77-114">A Resource Group</span></span>
* <span data-ttu-id="ddd77-115">Ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="ddd77-115">A virtual network</span></span>
* <span data-ttu-id="ddd77-116">En belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="ddd77-116">A load balancer</span></span>
* <span data-ttu-id="ddd77-117">En offentlig IP-adress</span><span class="sxs-lookup"><span data-stu-id="ddd77-117">A public IP</span></span>
* <span data-ttu-id="ddd77-118">VMSS med två instanser</span><span class="sxs-lookup"><span data-stu-id="ddd77-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="ddd77-119">Standard avbildningen som valts för de virtuella datorerna i VMSS är `2016-Datacenter Windows Server` och SKU är `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="ddd77-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="ddd77-120">Exempel 2: skapa en VMSS med hjälp av **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="ddd77-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="ddd77-121">Det komplexa exemplet ovan skapar en VMSS, nedan följer en beskrivning av vad som händer:</span><span class="sxs-lookup"><span data-stu-id="ddd77-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="ddd77-122">Det första kommandot skapar en resurs grupp med angivet namn och plats.</span><span class="sxs-lookup"><span data-stu-id="ddd77-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="ddd77-123">Det andra kommandot använder cmdleten **New-AzStorageAccount** för att skapa ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ddd77-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="ddd77-124">Det tredje kommandot använder sedan cmdleten **Get-AzStorageAccount** för att hämta lagrings kontot som skapats i det andra kommandot och lagrar resultatet i $STOAccount variabel.</span><span class="sxs-lookup"><span data-stu-id="ddd77-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="ddd77-125">Det femte kommandot använder cmdleten **New-AzVirtualNetworkSubnetConfig** för att skapa ett undernät och lagrar resultatet i variabeln som heter $SubNet.</span><span class="sxs-lookup"><span data-stu-id="ddd77-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="ddd77-126">I sjätte kommandot används cmdleten **New-AzVirtualNetwork** för att skapa ett virtuellt nätverk och det lagrar resultatet i variabeln som heter $VNet.</span><span class="sxs-lookup"><span data-stu-id="ddd77-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="ddd77-127">Det sjunde kommandot använder funktionen **Get-AzVirtualNetwork** för att få information om det virtuella nätverk som skapats i sjätte kommandot och lagrar informationen i variabeln som heter $VNet.</span><span class="sxs-lookup"><span data-stu-id="ddd77-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="ddd77-128">Det åttonde och nionde kommandot använder den **nya-AzPublicIpAddress** och **AzureRmPublicIpAddress** för att skapa och få information från den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="ddd77-129">I kommandona lagras informationen i variabeln som heter $PubIP.</span><span class="sxs-lookup"><span data-stu-id="ddd77-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="ddd77-130">Det tionde kommandot använder cmdleten **New-AzureRmLoadBalancerFrontendIpConfig** för att skapa en uppladdnings enhet och lagrar resultatet i variabeln som heter $frontend.</span><span class="sxs-lookup"><span data-stu-id="ddd77-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="ddd77-131">Det elfte kommandot använder den **nya-AzLoadBalancerBackendAddressPoolConfig** för att skapa en konfiguration för en server dels adresspool och lagrar resultatet i variabeln som heter $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="ddd77-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="ddd77-132">Det tolfte kommandot använder **New-AzLoadBalancerProbeConfig** för att skapa en sond och lagrar sondens information i variabeln som heter $PROBE.</span><span class="sxs-lookup"><span data-stu-id="ddd77-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="ddd77-133">I det trettonde kommandot används cmdleten **New-AzLoadBalancerInboundNatPoolConfig** för att skapa en konfiguration för inkommande NAT-adresspool (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="ddd77-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="ddd77-134">I Fourteenth-kommandot används den **nya AzLoadBalancerRuleConfig** för att skapa en regel konfiguration för belastnings utjämning och det lagrar resultatet i variabeln som heter $LBRule.</span><span class="sxs-lookup"><span data-stu-id="ddd77-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="ddd77-135">Det femtonde kommandot använder cmdleten **New-AzLoadBalancer** för att skapa en belastnings utjämning och lagrar resultatet i variabeln som heter $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="ddd77-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="ddd77-136">Kommandot Sixteenth använder funktionen **Get-AzLoadBalancer** för att få information om belastningsutjämnaren som har skapats i det femtonde kommandot och lagrar informationen i variabeln som heter $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="ddd77-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="ddd77-137">Kommandot seventeenth använder cmdlet **New-AzVmssIPConfig** för att skapa en VMSS IP-konfiguration och lagrar informationen i variabeln som heter $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="ddd77-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="ddd77-138">I åttonde-kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd77-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="ddd77-139">I av-kommandot används cmdleten **New-AzVmss** för att skapa VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd77-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="ddd77-140">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddd77-140">PARAMETERS</span></span>

### <span data-ttu-id="ddd77-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="ddd77-141">-AllocationMethod</span></span>
<span data-ttu-id="ddd77-142">Tilldelnings metod för den offentliga IP-adressen för skalan (statisk eller dynamisk).</span><span class="sxs-lookup"><span data-stu-id="ddd77-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="ddd77-143">Om inget värde anges kommer tilldelningen att vara statisk.</span><span class="sxs-lookup"><span data-stu-id="ddd77-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddd77-144">-AsJob</span></span>
<span data-ttu-id="ddd77-145">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="ddd77-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ddd77-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="ddd77-146">-BackendPoolName</span></span>
<span data-ttu-id="ddd77-147">Namnet på backend-adresspoolen som ska användas i belastningsutjämnaren för den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="ddd77-148">Om inget värde anges skapas en ny backend-pool, med samma namn som den inställda skalan.</span><span class="sxs-lookup"><span data-stu-id="ddd77-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="ddd77-149">-BackendPort</span></span>
<span data-ttu-id="ddd77-150">Server dels port nummer som används av skal uppsättningens belastningsutjämnare för att kommunicera med virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="ddd77-151">Om inga värden anges används portarna 3389 och 5985 för Windows-VMS och port 22 används för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="ddd77-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-152">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="ddd77-152">-Credential</span></span>
<span data-ttu-id="ddd77-153">Administratörs uppgifterna (användar namn och lösen ord) för virtuella datorer i den här skalan.</span><span class="sxs-lookup"><span data-stu-id="ddd77-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="ddd77-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="ddd77-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="ddd77-155">Anger storleken på data diskarna i GB.</span><span class="sxs-lookup"><span data-stu-id="ddd77-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd77-156">-DefaultProfile</span></span>
<span data-ttu-id="ddd77-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd77-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddd77-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ddd77-158">-DomainNameLabel</span></span>
<span data-ttu-id="ddd77-159">Domän namns etiketten för det offentliga Fully-Qualified domän namnet (FQDN) för den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="ddd77-160">Det här är den första komponenten i domän namnet som automatiskt tilldelas till skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="ddd77-161">Automatiskt tilldelade domän namn Använd formuläret ( <DomainNameLabel> . <Location> .. cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ddd77-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="ddd77-162">Om inget värde anges blir standard etiketten för domän namn sammanfogningen av <ScaleSetName> och <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="ddd77-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="ddd77-163">-EnableUltraSSD</span></span>
<span data-ttu-id="ddd77-164">Använd UltraSSD-diskar för datorerna i skalan.</span><span class="sxs-lookup"><span data-stu-id="ddd77-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd77-165">-EvictionPolicy</span></span>
<span data-ttu-id="ddd77-166">Borttagnings princip för skalan för den virtuella datorns lågprioriterade.</span><span class="sxs-lookup"><span data-stu-id="ddd77-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="ddd77-167">Endast värden som stöds är "frigör" och "ta bort".</span><span class="sxs-lookup"><span data-stu-id="ddd77-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="ddd77-168">-FrontendPoolName</span></span>
<span data-ttu-id="ddd77-169">Namnet på den frontend-adresspool som ska användas i belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="ddd77-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="ddd77-170">Om inget värde anges skapas en ny klient delens adresspool med samma namn som den inställda skalan.</span><span class="sxs-lookup"><span data-stu-id="ddd77-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ddd77-171">-ImageName</span></span>
<span data-ttu-id="ddd77-172">Namnet på bilden för virtuella datorer i den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="ddd77-173">Om inget värde anges används "Windows Server 2016 Data Center"-bilden.</span><span class="sxs-lookup"><span data-stu-id="ddd77-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="ddd77-174">-InstanceCount</span></span>
<span data-ttu-id="ddd77-175">Antalet virtuella dator bilder i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="ddd77-176">Om inget värde anges skapas två instanser.</span><span class="sxs-lookup"><span data-stu-id="ddd77-176">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="ddd77-177">-LoadBalancerName</span></span>
<span data-ttu-id="ddd77-178">Namnet på belastningsutjämnaren som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="ddd77-179">En ny belastningsutjämnare med samma namn som skal uppsättning skapas om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="ddd77-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-180">-Plats</span><span class="sxs-lookup"><span data-stu-id="ddd77-180">-Location</span></span>
<span data-ttu-id="ddd77-181">Den Azure-plats där den här skalnings uppsättningen skapas.</span><span class="sxs-lookup"><span data-stu-id="ddd77-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="ddd77-182">Om inget värde anges härleds platsen från platsen för andra resurser som refereras till i parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ddd77-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="ddd77-183">-MaxPrice</span></span>
<span data-ttu-id="ddd77-184">Max priset för fakturering av en skala för en virtuell dator med en lägre prioritet.</span><span class="sxs-lookup"><span data-stu-id="ddd77-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="ddd77-185">-NatBackendPort</span></span>
<span data-ttu-id="ddd77-186">Backend-port för inkommande NAT.</span><span class="sxs-lookup"><span data-stu-id="ddd77-186">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-187">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="ddd77-187">-Priority</span></span>
<span data-ttu-id="ddd77-188">Prioriteten för den virtuella datorn i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-188">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="ddd77-189">Endast värden som stöds är "regular", "dekor" och "Low".</span><span class="sxs-lookup"><span data-stu-id="ddd77-189">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="ddd77-190">' Regular ' är för vanlig virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ddd77-190">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="ddd77-191">"Plats" gäller för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ddd77-191">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="ddd77-192">"Low" är också för en virtuell dator, men ersätts med ' dekor ".</span><span class="sxs-lookup"><span data-stu-id="ddd77-192">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="ddd77-193">Använd "plats" istället för "Low".</span><span class="sxs-lookup"><span data-stu-id="ddd77-193">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-194">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="ddd77-194">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="ddd77-195">Resurs-ID för närhets gruppen som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-195">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-196">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="ddd77-196">-PublicIpAddressName</span></span>
<span data-ttu-id="ddd77-197">Namnet på den offentliga IP-adressen som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-197">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="ddd77-198">En ny offentlig IP-adress med samma namn som skal uppsättningen skapas om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="ddd77-198">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd77-199">-ResourceGroupName</span></span>
<span data-ttu-id="ddd77-200">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="ddd77-200">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="ddd77-201">Om inget värde anges skapas en ny ResourceGroup med samma namn som skalan.</span><span class="sxs-lookup"><span data-stu-id="ddd77-201">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-202">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd77-202">-ScaleInPolicy</span></span>
<span data-ttu-id="ddd77-203">De regler som ska användas vid skalning-i en virtuell dators skala uppsättning.</span><span class="sxs-lookup"><span data-stu-id="ddd77-203">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="ddd77-204">Möjliga värden är: ' default ', ' OldestVM ' och ' NewestVM '.</span><span class="sxs-lookup"><span data-stu-id="ddd77-204">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="ddd77-205">"Standard" när en skala för virtuell dator skal för änd ras i, fördelas skalnings uppsättningen först över zoner om den är en Zonal skala.</span><span class="sxs-lookup"><span data-stu-id="ddd77-205">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="ddd77-206">Då kommer den att bal anse ras i så stor utsträckning som möjligt.</span><span class="sxs-lookup"><span data-stu-id="ddd77-206">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="ddd77-207">De virtuella datorerna som valts för borttagning är de nyaste som inte skyddas från Scale-in i varje fel domän.</span><span class="sxs-lookup"><span data-stu-id="ddd77-207">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="ddd77-208">' OldestVM ' när en virtuell dators Scale-uppsättning skal för änd ras-in väljs de äldsta virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="ddd77-208">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ddd77-209">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="ddd77-209">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ddd77-210">Inom varje zon kommer de äldsta virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="ddd77-210">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="ddd77-211">' NewestVM ' när en virtuell dators skal uppsättning skal för änd ras-in väljs de senaste virtuella datorerna som inte skyddas från Scale-in att tas bort.</span><span class="sxs-lookup"><span data-stu-id="ddd77-211">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="ddd77-212">För Zonal för virtuell dator fördelas skalnings uppsättningen först över zoner.</span><span class="sxs-lookup"><span data-stu-id="ddd77-212">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="ddd77-213">Inom varje zon kommer de senaste virtuella datorerna som inte skyddas att väljas för borttagning.</span><span class="sxs-lookup"><span data-stu-id="ddd77-213">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-214">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd77-214">-SecurityGroupName</span></span>
<span data-ttu-id="ddd77-215">Namnet på nätverks säkerhets gruppen som ska användas för den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-215">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="ddd77-216">Om inget värde anges skapas en standard grupp för nätverks säkerhet med samma namn som skal uppsättningen och tillämpas på skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-216">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-217">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ddd77-217">-SinglePlacementGroup</span></span>
<span data-ttu-id="ddd77-218">Använd det här alternativet om du vill skapa en skal uppsättning i en enda placerings grupp, som standard är flera grupper</span><span class="sxs-lookup"><span data-stu-id="ddd77-218">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-219">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="ddd77-219">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="ddd77-220">Anger att tilläggen inte körs på de extra överetablerade datorerna.</span><span class="sxs-lookup"><span data-stu-id="ddd77-220">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-221">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ddd77-221">-SubnetAddressPrefix</span></span>
<span data-ttu-id="ddd77-222">Adressprefixet för det undernät som denna ScaleSet kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="ddd77-222">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="ddd77-223">Standardinställningarna för undernät (192.168.1.0/24) tillämpas om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="ddd77-223">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-224">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ddd77-224">-SubnetName</span></span>
<span data-ttu-id="ddd77-225">Namnet på det undernät som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-225">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="ddd77-226">Ett nytt undernät skapas med samma namn som skalan om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="ddd77-226">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-227">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ddd77-227">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ddd77-228">Om parametern är angiven är den eller de virtuella datorerna i skalnings uppsättningen (kallas) för en hanterad system identitet som genereras automatiskt.</span><span class="sxs-lookup"><span data-stu-id="ddd77-228">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ddd77-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="ddd77-230">Uppgraderings princip läget för virtuella dator instanser i den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-230">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="ddd77-231">Uppgraderings princip kan ange automatiska, manuella eller rullande uppgraderingar.</span><span class="sxs-lookup"><span data-stu-id="ddd77-231">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-232">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ddd77-232">-UserAssignedIdentity</span></span>
<span data-ttu-id="ddd77-233">Namnet på ett hanterat tjänst-ID som ska kopplas till de virtuella datorerna i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-233">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd77-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ddd77-235">Anger det **VirtualMachineScaleSet** -objekt som innehåller egenskaperna för det VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ddd77-235">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-236">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ddd77-236">-VirtualNetworkName</span></span>
<span data-ttu-id="ddd77-237">Namnet till det virtuella nätverk som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-237">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="ddd77-238">Om inget värde anges skapas ett nytt virtuellt nätverk med samma namn som skal uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-238">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-239">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ddd77-239">-VMScaleSetName</span></span>
<span data-ttu-id="ddd77-240">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="ddd77-240">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-241">-VmSize</span><span class="sxs-lookup"><span data-stu-id="ddd77-241">-VmSize</span></span>
<span data-ttu-id="ddd77-242">Storleken på virtuella dator instanser i den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-242">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="ddd77-243">En standard storlek (Standard_DS1_v2) används om ingen storlek har angetts.</span><span class="sxs-lookup"><span data-stu-id="ddd77-243">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-244">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="ddd77-244">-VnetAddressPrefix</span></span>
<span data-ttu-id="ddd77-245">Adressprefixet för det virtuella nätverk som används med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="ddd77-245">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="ddd77-246">Standardvärden för virtuella nätverks adressprefix (192.168.0.0/16) används om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="ddd77-246">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-247">-Zone</span><span class="sxs-lookup"><span data-stu-id="ddd77-247">-Zone</span></span>
<span data-ttu-id="ddd77-248">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="ddd77-248">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd77-249">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddd77-249">-Confirm</span></span>
<span data-ttu-id="ddd77-250">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddd77-250">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd77-251">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd77-251">-WhatIf</span></span>
<span data-ttu-id="ddd77-252">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddd77-252">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd77-253">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddd77-253">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd77-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd77-254">CommonParameters</span></span>
<span data-ttu-id="ddd77-255">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd77-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd77-256">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddd77-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd77-257">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddd77-257">INPUTS</span></span>

### <span data-ttu-id="ddd77-258">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd77-258">System.String</span></span>

### <span data-ttu-id="ddd77-259">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd77-259">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="ddd77-260">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ddd77-260">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ddd77-261">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddd77-261">OUTPUTS</span></span>

### <span data-ttu-id="ddd77-262">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ddd77-262">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ddd77-263">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddd77-263">NOTES</span></span>

## <span data-ttu-id="ddd77-264">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddd77-264">RELATED LINKS</span></span>

[<span data-ttu-id="ddd77-265">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-265">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="ddd77-266">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-266">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="ddd77-267">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-267">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="ddd77-268">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-268">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="ddd77-269">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-269">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="ddd77-270">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-270">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="ddd77-271">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ddd77-271">Update-AzVmss</span></span>](./Update-AzVmss.md)


