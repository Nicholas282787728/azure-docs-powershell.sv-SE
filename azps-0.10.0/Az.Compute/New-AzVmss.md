---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: fc788d40cbcd807ef05be4ab43fcda4371aaa084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925037"
---
# <span data-ttu-id="6f57d-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-101">New-AzVmss</span></span>

## <span data-ttu-id="6f57d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f57d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f57d-103">Skapar en VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f57d-103">Creates a VMSS.</span></span>

## <span data-ttu-id="6f57d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f57d-104">SYNTAX</span></span>

### <span data-ttu-id="6f57d-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="6f57d-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f57d-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f57d-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f57d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f57d-107">DESCRIPTION</span></span>
<span data-ttu-id="6f57d-108">Cmdleten **New-AzVmss** skapar en skal uppsättning för virtuell dator (VMSS) i Azure.</span><span class="sxs-lookup"><span data-stu-id="6f57d-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="6f57d-109">Denna cmdlet tar ett **VirtualMachineScaleSet** -objekt som inmatning.</span><span class="sxs-lookup"><span data-stu-id="6f57d-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="6f57d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f57d-110">EXAMPLES</span></span>

### <span data-ttu-id="6f57d-111">Exempel 1: skapa en VMSS</span><span class="sxs-lookup"><span data-stu-id="6f57d-111">Example 1: Create a VMSS</span></span>
```
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

<span data-ttu-id="6f57d-112">I följande komplexa exempel skapas en VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f57d-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="6f57d-113">Det första kommandot skapar en resurs grupp med angivet namn och plats.</span><span class="sxs-lookup"><span data-stu-id="6f57d-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="6f57d-114">Det andra kommandot använder cmdleten **New-AzStorageAccount** för att skapa ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6f57d-114">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="6f57d-115">Det tredje kommandot använder sedan cmdleten **Get-AzStorageAccount** för att hämta lagrings kontot som skapats i det andra kommandot och lagrar resultatet i $STOAccount variabel.</span><span class="sxs-lookup"><span data-stu-id="6f57d-115">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="6f57d-116">Det femte kommandot använder cmdleten **New-AzVirtualNetworkSubnetConfig** för att skapa ett undernät och lagrar resultatet i variabeln som heter $SubNet.</span><span class="sxs-lookup"><span data-stu-id="6f57d-116">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="6f57d-117">I sjätte kommandot används cmdleten **New-AzVirtualNetwork** för att skapa ett virtuellt nätverk och det lagrar resultatet i variabeln som heter $VNet.</span><span class="sxs-lookup"><span data-stu-id="6f57d-117">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="6f57d-118">Det sjunde kommandot använder funktionen **Get-AzVirtualNetwork** för att få information om det virtuella nätverk som skapats i sjätte kommandot och lagrar informationen i variabeln som heter $VNet.</span><span class="sxs-lookup"><span data-stu-id="6f57d-118">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="6f57d-119">Det åttonde och nionde kommandot använder den **nya-AzPublicIpAddress** och **AzureRmPublicIpAddress** för att skapa och få information från den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-119">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="6f57d-120">I kommandona lagras informationen i variabeln som heter $PubIP.</span><span class="sxs-lookup"><span data-stu-id="6f57d-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="6f57d-121">Det tionde kommandot använder cmdleten **New-AzureRmLoadBalancerFrontendIpConfig** för att skapa en uppladdnings enhet och lagrar resultatet i variabeln som heter $frontend.</span><span class="sxs-lookup"><span data-stu-id="6f57d-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="6f57d-122">Det elfte kommandot använder den **nya-AzLoadBalancerBackendAddressPoolConfig** för att skapa en konfiguration för en server dels adresspool och lagrar resultatet i variabeln som heter $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="6f57d-122">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="6f57d-123">Det tolfte kommandot använder **New-AzLoadBalancerProbeConfig** för att skapa en sond och lagrar sondens information i variabeln som heter $PROBE.</span><span class="sxs-lookup"><span data-stu-id="6f57d-123">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="6f57d-124">I det trettonde kommandot används cmdleten **New-AzLoadBalancerInboundNatPoolConfig** för att skapa en konfiguration för inkommande NAT-adresspool (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="6f57d-124">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="6f57d-125">I Fourteenth-kommandot används den **nya AzLoadBalancerRuleConfig** för att skapa en regel konfiguration för belastnings utjämning och det lagrar resultatet i variabeln som heter $LBRule.</span><span class="sxs-lookup"><span data-stu-id="6f57d-125">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="6f57d-126">Det femtonde kommandot använder cmdleten **New-AzLoadBalancer** för att skapa en belastnings utjämning och lagrar resultatet i variabeln som heter $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="6f57d-126">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="6f57d-127">Kommandot Sixteenth använder funktionen **Get-AzLoadBalancer** för att få information om belastningsutjämnaren som har skapats i det femtonde kommandot och lagrar informationen i variabeln som heter $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="6f57d-127">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="6f57d-128">Kommandot seventeenth använder cmdlet **New-AzVmssIPConfig** för att skapa en VMSS IP-konfiguration och lagrar informationen i variabeln som heter $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="6f57d-128">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="6f57d-129">I åttonde-kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f57d-129">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="6f57d-130">I av-kommandot används cmdleten **New-AzVmss** för att skapa VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f57d-130">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="6f57d-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f57d-131">PARAMETERS</span></span>

### <span data-ttu-id="6f57d-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="6f57d-132">-AllocationMethod</span></span>
<span data-ttu-id="6f57d-133">Tilldelnings metod för den offentliga IP-adressen för skalan (statisk eller dynamisk).</span><span class="sxs-lookup"><span data-stu-id="6f57d-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="6f57d-134">Om inget värde anges kommer tilldelningen att vara statisk.</span><span class="sxs-lookup"><span data-stu-id="6f57d-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f57d-135">-AsJob</span></span>
<span data-ttu-id="6f57d-136">Kör cmdlet i bakgrunden och returnera ett jobb för att spåra förloppet.</span><span class="sxs-lookup"><span data-stu-id="6f57d-136">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6f57d-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="6f57d-137">-BackendPoolName</span></span>
<span data-ttu-id="6f57d-138">Namnet på backend-adresspoolen som ska användas i belastningsutjämnaren för den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="6f57d-139">Om inget värde anges skapas en ny backend-pool, med samma namn som den inställda skalan.</span><span class="sxs-lookup"><span data-stu-id="6f57d-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="6f57d-140">-BackendPort</span></span>
<span data-ttu-id="6f57d-141">Server dels port nummer som används av skal uppsättningens belastningsutjämnare för att kommunicera med virtuella datorer i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="6f57d-142">Om inga värden anges används portarna 3389 och 5985 för Windows-VMS och port 22 används för virtuella Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="6f57d-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-143">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="6f57d-143">-Credential</span></span>
<span data-ttu-id="6f57d-144">Administratörs uppgifterna (användar namn och lösen ord) för virtuella datorer i den här skalan.</span><span class="sxs-lookup"><span data-stu-id="6f57d-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="6f57d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f57d-145">-DefaultProfile</span></span>
<span data-ttu-id="6f57d-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f57d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f57d-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="6f57d-147">-DomainNameLabel</span></span>
<span data-ttu-id="6f57d-148">Domän namns etiketten för det offentliga Fully-Qualified domän namnet (FQDN) för den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="6f57d-149">Det här är den första komponenten i domän namnet som automatiskt assiged till skalan.</span><span class="sxs-lookup"><span data-stu-id="6f57d-149">This is the first component of the domain name that is automatically assiged to the Scale Set.</span></span> <span data-ttu-id="6f57d-150">Automatiskt tilldelade domän namn Använd formuläret ( <DomainNameLabel> . <Location> .. cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="6f57d-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="6f57d-151">Om inget värde anges blir standard etiketten för domän namn sammanfogningen av <ScaleSetName> och <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="6f57d-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="6f57d-152">-FrontendPoolName</span></span>
<span data-ttu-id="6f57d-153">Namnet på frontend-adresspoolen som useIn skalnings locad.</span><span class="sxs-lookup"><span data-stu-id="6f57d-153">The name of the frontend address pool to usein the Scale Set locad balancer.</span></span>  <span data-ttu-id="6f57d-154">Om inget värde anges skapas en ny klient delens adresspool med samma namn som den inställda skalan.</span><span class="sxs-lookup"><span data-stu-id="6f57d-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6f57d-155">-ImageName</span></span>
<span data-ttu-id="6f57d-156">Namnet på bilden för virtuella datorer i den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="6f57d-157">Om inget värde anges används "Windows Server 2016 Data Center"-bilden.</span><span class="sxs-lookup"><span data-stu-id="6f57d-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="6f57d-158">-InstanceCount</span></span>
<span data-ttu-id="6f57d-159">Antalet virtuella dator bilder i skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="6f57d-160">Om inget värde anges skapas två instanser.</span><span class="sxs-lookup"><span data-stu-id="6f57d-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="6f57d-161">-LoadBalancerName</span></span>
<span data-ttu-id="6f57d-162">Namnet på belastningsutjämnaren som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="6f57d-163">En ny belastningsutjämnare med samma namn som skal uppsättning skapas om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="6f57d-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-164">-Plats</span><span class="sxs-lookup"><span data-stu-id="6f57d-164">-Location</span></span>
<span data-ttu-id="6f57d-165">Den Azure-plats där den här skalnings uppsättningen skapas.</span><span class="sxs-lookup"><span data-stu-id="6f57d-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="6f57d-166">Om inget värde anges härleds platsen från platsen för andra resurser som refereras till i parametrarna.</span><span class="sxs-lookup"><span data-stu-id="6f57d-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="6f57d-167">-NatBackendPort</span></span>
<span data-ttu-id="6f57d-168">Backend-port för inkommande NAT.</span><span class="sxs-lookup"><span data-stu-id="6f57d-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="6f57d-169">-PublicIpAddressName</span></span>
<span data-ttu-id="6f57d-170">Namnet på den offentliga IP-adressen som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="6f57d-171">En ny offentlig IP-adress med samma namn som skal uppsättningen skapas om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="6f57d-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f57d-172">-ResourceGroupName</span></span>
<span data-ttu-id="6f57d-173">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="6f57d-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="6f57d-174">Om inget värde anges skapas en ny ResourceGroup med samma namn som skalan.</span><span class="sxs-lookup"><span data-stu-id="6f57d-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="6f57d-175">-SecurityGroupName</span></span>
<span data-ttu-id="6f57d-176">Namnet på nätverks säkerhets gruppen som ska användas för den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="6f57d-177">Om inget värde anges skapas en standard grupp för nätverks säkerhet med samma namn som skal uppsättningen och tillämpas på skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6f57d-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="6f57d-179">Adressprefixet för det undernät som denna ScaleSet kommer att använda.</span><span class="sxs-lookup"><span data-stu-id="6f57d-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="6f57d-180">Standardinställningarna för undernät (192.168.1.0/24) tillämpas om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="6f57d-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="6f57d-181">-SubnetName</span></span>
<span data-ttu-id="6f57d-182">Namnet på det undernät som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="6f57d-183">Ett nytt undernät skapas med samma namn som skalan om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="6f57d-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="6f57d-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="6f57d-185">Uppgraderings princip läget för virtuella dator instanser i den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="6f57d-186">Uppgraderings princip kan ange automatiska, manuella eller rullande uppgraderingar.</span><span class="sxs-lookup"><span data-stu-id="6f57d-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6f57d-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6f57d-188">Anger det **VirtualMachineScaleSet** -objekt som innehåller egenskaperna för det VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="6f57d-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="6f57d-189">-VirtualNetworkName</span></span>
<span data-ttu-id="6f57d-190">Namnet till det virtuella nätverk som ska användas med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="6f57d-191">Om inget värde anges skapas ett nytt virtuellt nätverk med samma namn som skal uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6f57d-192">-VMScaleSetName</span></span>
<span data-ttu-id="6f57d-193">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="6f57d-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="6f57d-194">-VmSize</span></span>
<span data-ttu-id="6f57d-195">Storleken på virtuella dator instanser i den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="6f57d-196">En standard storlek (Standard_DS1_v2) används om ingen storlek har angetts.</span><span class="sxs-lookup"><span data-stu-id="6f57d-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="6f57d-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="6f57d-198">Adressprefixet för det virtuella nätverk som används med den här skalnings uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="6f57d-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="6f57d-199">Standardvärden för virtuella nätverks adressprefix (192.168.0.0/16) används om inget värde anges.</span><span class="sxs-lookup"><span data-stu-id="6f57d-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f57d-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="6f57d-200">-Zone</span></span>
<span data-ttu-id="6f57d-201">En lista över tillgänglighets zoner som betecknar den IP som tilldelats resursen måste komma från.</span><span class="sxs-lookup"><span data-stu-id="6f57d-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="6f57d-202">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f57d-202">-Confirm</span></span>
<span data-ttu-id="6f57d-203">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f57d-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f57d-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f57d-204">-WhatIf</span></span>
<span data-ttu-id="6f57d-205">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f57d-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6f57d-206">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f57d-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f57d-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f57d-207">CommonParameters</span></span>
<span data-ttu-id="6f57d-208">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f57d-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f57d-209">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f57d-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f57d-210">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f57d-210">INPUTS</span></span>

### <span data-ttu-id="6f57d-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6f57d-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="6f57d-212">Parametern ' VirtualMachineScaleSet ' godkänner värdet av typen ' VirtualMachineScaleSet ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="6f57d-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="6f57d-213">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f57d-213">OUTPUTS</span></span>

### <span data-ttu-id="6f57d-214">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="6f57d-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6f57d-215">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f57d-215">NOTES</span></span>

## <span data-ttu-id="6f57d-216">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f57d-216">RELATED LINKS</span></span>

[<span data-ttu-id="6f57d-217">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-217">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="6f57d-218">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-218">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="6f57d-219">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-219">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="6f57d-220">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-220">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="6f57d-221">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-221">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="6f57d-222">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-222">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="6f57d-223">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6f57d-223">Update-AzVmss</span></span>](./Update-AzVmss.md)


