---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 54ddf9527abcb1f94a4d8c262f9c0f22e18ea1ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585739"
---
# <span data-ttu-id="082b8-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="082b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="082b8-102">SYNOPSIS</span></span>
<span data-ttu-id="082b8-103">Skapar en VMSS.</span><span class="sxs-lookup"><span data-stu-id="082b8-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="082b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="082b8-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="082b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="082b8-105">DESCRIPTION</span></span>
<span data-ttu-id="082b8-106">Cmdleten **New-AzureRmVmss** skapar en skal uppsättning för virtuell dator (VMSS) i Azure.</span><span class="sxs-lookup"><span data-stu-id="082b8-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="082b8-107">Denna cmdlet tar ett **VirtualMachineScaleSet** -objekt som inmatning.</span><span class="sxs-lookup"><span data-stu-id="082b8-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="082b8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="082b8-108">EXAMPLES</span></span>

### <span data-ttu-id="082b8-109">Exempel 1: skapa en VMSS</span><span class="sxs-lookup"><span data-stu-id="082b8-109">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="082b8-110">I följande komplexa exempel skapas en VMSS.</span><span class="sxs-lookup"><span data-stu-id="082b8-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="082b8-111">Det första kommandot skapar en resurs grupp med angivet namn och plats.</span><span class="sxs-lookup"><span data-stu-id="082b8-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="082b8-112">Det andra kommandot använder cmdleten **New-AzureRmStorageAccount** för att skapa ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="082b8-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="082b8-113">Det tredje kommandot använder sedan cmdleten **Get-AzureRmStorageAccount** för att hämta lagrings kontot som skapats i det andra kommandot och lagrar resultatet i $STOAccount variabel.</span><span class="sxs-lookup"><span data-stu-id="082b8-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="082b8-114">Det femte kommandot använder cmdleten **New-AzureRmVirtualNetworkSubnetConfig** för att skapa ett undernät och lagrar resultatet i variabeln som heter $SubNet.</span><span class="sxs-lookup"><span data-stu-id="082b8-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="082b8-115">I sjätte kommandot används cmdleten **New-AzureRmVirtualNetwork** för att skapa ett virtuellt nätverk och det lagrar resultatet i variabeln som heter $VNet.</span><span class="sxs-lookup"><span data-stu-id="082b8-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="082b8-116">Det sjunde kommandot använder funktionen **Get-AzureRmVirtualNetwork** för att få information om det virtuella nätverk som skapats i sjätte kommandot och lagrar informationen i variabeln som heter $VNet.</span><span class="sxs-lookup"><span data-stu-id="082b8-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="082b8-117">Det åttonde och nionde kommandot använder den **nya-AzureRmPublicIpAddress** och **AzureRmPublicIpAddress** för att skapa och få information från den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="082b8-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="082b8-118">I kommandona lagras informationen i variabeln som heter $PubIP.</span><span class="sxs-lookup"><span data-stu-id="082b8-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="082b8-119">Det tionde kommandot använder cmdleten **New-AzureRmLoadBalancerFrontendIpConfig** för att skapa en uppladdnings enhet och lagrar resultatet i variabeln som heter $frontend.</span><span class="sxs-lookup"><span data-stu-id="082b8-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="082b8-120">Det elfte kommandot använder den **nya-AzureRmLoadBalancerBackendAddressPoolConfig** för att skapa en konfiguration för en server dels adresspool och lagrar resultatet i variabeln som heter $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="082b8-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="082b8-121">Det tolfte kommandot använder **New-AzureRmLoadBalancerProbeConfig** för att skapa en sond och lagrar sondens information i variabeln som heter $PROBE.</span><span class="sxs-lookup"><span data-stu-id="082b8-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="082b8-122">I det trettonde kommandot används cmdleten **New-AzureRmLoadBalancerInboundNatPoolConfig** för att skapa en konfiguration för inkommande NAT-adresspool (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="082b8-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="082b8-123">I Fourteenth-kommandot används den **nya AzureRmLoadBalancerRuleConfig** för att skapa en regel konfiguration för belastnings utjämning och det lagrar resultatet i variabeln som heter $LBRule.</span><span class="sxs-lookup"><span data-stu-id="082b8-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="082b8-124">Det femtonde kommandot använder cmdleten **New-AzureRmLoadBalancer** för att skapa en belastnings utjämning och lagrar resultatet i variabeln som heter $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="082b8-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="082b8-125">Kommandot Sixteenth använder funktionen **Get-AzureRmLoadBalancer** för att få information om belastningsutjämnaren som har skapats i det femtonde kommandot och lagrar informationen i variabeln som heter $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="082b8-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="082b8-126">Kommandot seventeenth använder cmdlet **New-AzureRmVmssIPConfig** för att skapa en VMSS IP-konfiguration och lagrar informationen i variabeln som heter $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="082b8-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="082b8-127">I åttonde-kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="082b8-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="082b8-128">I av-kommandot används cmdleten **New-AzureRmVmss** för att skapa VMSS.</span><span class="sxs-lookup"><span data-stu-id="082b8-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="082b8-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="082b8-129">PARAMETERS</span></span>

### <span data-ttu-id="082b8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="082b8-130">-DefaultProfile</span></span>
<span data-ttu-id="082b8-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="082b8-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="082b8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="082b8-132">-ResourceGroupName</span></span>
<span data-ttu-id="082b8-133">Anger namnet på resurs gruppen för VMSS.</span><span class="sxs-lookup"><span data-stu-id="082b8-133">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="082b8-134">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="082b8-134">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="082b8-135">Anger det **VirtualMachineScaleSet** -objekt som innehåller egenskaperna för det VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="082b8-135">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="082b8-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="082b8-136">-VMScaleSetName</span></span>
<span data-ttu-id="082b8-137">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="082b8-137">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="082b8-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="082b8-138">-Confirm</span></span>
<span data-ttu-id="082b8-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="082b8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="082b8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="082b8-140">-WhatIf</span></span>
<span data-ttu-id="082b8-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="082b8-141">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="082b8-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="082b8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="082b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="082b8-143">CommonParameters</span></span>
<span data-ttu-id="082b8-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="082b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="082b8-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="082b8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="082b8-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="082b8-146">INPUTS</span></span>

## <span data-ttu-id="082b8-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="082b8-147">OUTPUTS</span></span>

### <span data-ttu-id="082b8-148">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="082b8-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="082b8-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="082b8-149">NOTES</span></span>

## <span data-ttu-id="082b8-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="082b8-150">RELATED LINKS</span></span>

[<span data-ttu-id="082b8-151">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="082b8-152">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="082b8-153">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="082b8-154">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="082b8-155">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="082b8-156">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="082b8-157">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="082b8-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


