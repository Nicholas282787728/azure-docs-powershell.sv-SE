---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272426"
---
# <span data-ttu-id="d7f4d-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="d7f4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f4d-103">Uppdaterar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-103">Updates a network interface.</span></span>

## <span data-ttu-id="d7f4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7f4d-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7f4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f4d-106">**Set-AzNetworkInterface** uppdaterar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="d7f4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f4d-108">Exempel 1: Konfigurera ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d7f4d-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="d7f4d-109">Det här exemplet konfigurerar ett nätverks gränssnitt.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-109">This example configures a network interface.</span></span>
<span data-ttu-id="d7f4d-110">Det första kommandot får ett nätverks gränssnitt som heter NetworkInterface1 i ResourceGroup1 för resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="d7f4d-111">Med det andra kommandot anges IP-konfigurationens privata IP-adress.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="d7f4d-112">Det tredje kommandot ställer in den privata IP-tilldelnings metoden till statisk.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="d7f4d-113">Det fjärde kommandot anger en tagg i nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="d7f4d-114">Det femte kommandot använder informationen som lagras i $Nic variabel för att ange nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="d7f4d-115">Exempel 2: ändra DNS-inställningar i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d7f4d-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="d7f4d-116">Det första kommandot får ett nätverks gränssnitt med namnet NetworkInterface1 som finns i resurs grupp ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="d7f4d-117">Det andra kommandot lägger till DNS-192.168.1.100 till det här gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="d7f4d-118">Det tredje kommandot tillämpar dessa ändringar i nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="d7f4d-119">Om du vill ta bort en DNS-Server följer du kommandona ovan, men Ersätt ". Lägg till "med". Ta bort "i det andra kommandot.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="d7f4d-120">Exempel 3: aktivera IP-vidarebefordran i ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d7f4d-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="d7f4d-121">Det första kommandot får ett befintligt nätverks gränssnitt med namnet NetworkInterface1 och lagrar det i $nic variabeln.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="d7f4d-122">Det andra kommandot ändrar värdet för IP-vidarekoppling till sant.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="d7f4d-123">Dessutom tillämpar det tredje kommandot ändringarna i nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="d7f4d-124">Om du vill inaktivera IP-vidarebefordran i ett nätverks gränssnitt följer du exempel exempel på att ändra det andra kommandot till "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="d7f4d-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="d7f4d-125">Exempel 4: ändra undernät för ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d7f4d-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="d7f4d-126">Det första kommandot får nätverks gränssnittet NetworkInterface1 och lagrar det i $nic variabel.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="d7f4d-127">Det andra kommandot hämtar det virtuella nätverk som är kopplat till det undernät som nätverks gränssnittet ska kopplas till.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="d7f4d-128">Det andra kommandot hämtar under nätet och lagrar det i variabeln $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="d7f4d-129">Det tredje kommandot associerade den primära privata IP-adressen för nätverks gränssnittet med det nya under nätet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="d7f4d-130">Slutligen användes de här ändringarna i nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="d7f4d-131">IP-konfigurationerna måste vara dynamiska innan du kan ändra under nätet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="d7f4d-132">Om du har statiska IP-konfigurationer måste du ändra till dynamisk innan du fortsätter.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="d7f4d-133">Om nätverks gränssnittet har flera IP-konfigurationer måste kommandot tillbaka utföras för alla dessa IP-konfigurationer innan kommandot Set-AzNetworkInterface körs.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="d7f4d-134">Det kan du göra på det sätt som gäller, men genom att ersätta "0" med rätt nummer.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="d7f4d-135">Om ett nätverks gränssnitt har N IP-konfigurationer måste N-1 av dessa kommandon finnas.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="d7f4d-136">Exempel 5: associera/koppla bort en nätverks säkerhets grupp till ett nätverks gränssnitt</span><span class="sxs-lookup"><span data-stu-id="d7f4d-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="d7f4d-137">Det första kommandot får ett befintligt nätverks gränssnitt med namnet NetworkInterface1 och lagrar det i $nic variabeln.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="d7f4d-138">Det andra kommandot får en befintlig nätverks säkerhets grupp som heter MyNSG och lagrar den i $nsg variabeln.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="d7f4d-139">Det tredje kommandot tilldelar $nsg till $nic.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="d7f4d-140">Slutligen tillämpas kommandot på nätverks gränssnittet.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="d7f4d-141">Om du vill koppla från nätverks säkerhets grupper från ett nätverks gränssnitt kan du enkelt ersätta $nsg i det tredje kommandot med $null.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="d7f4d-142">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7f4d-142">PARAMETERS</span></span>

### <span data-ttu-id="d7f4d-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7f4d-143">-AsJob</span></span>
<span data-ttu-id="d7f4d-144">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d7f4d-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7f4d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f4d-145">-DefaultProfile</span></span>
<span data-ttu-id="d7f4d-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7f4d-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-147">-NetworkInterface</span></span>
<span data-ttu-id="d7f4d-148">Anger ett objekt som representerar det tillstånd som nätverks gränssnittet ska anges i.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f4d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f4d-149">CommonParameters</span></span>
<span data-ttu-id="d7f4d-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f4d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f4d-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f4d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f4d-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7f4d-152">INPUTS</span></span>

### <span data-ttu-id="d7f4d-153">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d7f4d-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7f4d-154">OUTPUTS</span></span>

### <span data-ttu-id="d7f4d-155">Microsoft. Azure. commands. Networks. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d7f4d-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7f4d-156">NOTES</span></span>

## <span data-ttu-id="d7f4d-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7f4d-157">RELATED LINKS</span></span>

[<span data-ttu-id="d7f4d-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="d7f4d-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="d7f4d-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="d7f4d-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d7f4d-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)