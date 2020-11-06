---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 9c49fd381e1f63d60332eb42759cfb9dd187fbf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575279"
---
# <span data-ttu-id="8174a-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8174a-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="8174a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8174a-102">SYNOPSIS</span></span>
<span data-ttu-id="8174a-103">Skapar en IP-konfiguration för ett nätverks gränssnitt för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="8174a-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8174a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8174a-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8174a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8174a-105">DESCRIPTION</span></span>
<span data-ttu-id="8174a-106">Cmdleten **New-AzureRmVmssIpConfig** skapar ett IP-konfigurationsobjekt för ett nätverks gränssnitt med en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8174a-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8174a-107">Ange konfigurationen från den här cmdleten som *IPConfiguration* för Add-AzureRmVmssNetworkInterfaceConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8174a-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="8174a-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8174a-108">EXAMPLES</span></span>

### <span data-ttu-id="8174a-109">Exempel 1: skapa ett IP-konfigurationsobjekt för ett VMSS gränssnitt</span><span class="sxs-lookup"><span data-stu-id="8174a-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="8174a-110">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="8174a-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="8174a-111">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="8174a-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8174a-112">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning med **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8174a-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="8174a-113">Exempel 2: skapa ett IP-konfigurationsobjekt som innehåller inställningar för NAT-pool</span><span class="sxs-lookup"><span data-stu-id="8174a-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="8174a-114">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface03 och lagrar det sedan i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="8174a-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8174a-115">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="8174a-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8174a-116">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="8174a-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8174a-117">Kommandot anger värden för parametrarna *LoadBalancerInboundNatPoolsId* och *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="8174a-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="8174a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8174a-118">PARAMETERS</span></span>

### <span data-ttu-id="8174a-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8174a-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="8174a-120">Anger en matris med referenser till Server delens adresspooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8174a-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="8174a-121">Med en skalnings uppsättning kan Server gruppens adresspooler referera till en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8174a-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8174a-122">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8174a-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8174a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8174a-123">-DefaultProfile</span></span>
<span data-ttu-id="8174a-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8174a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8174a-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="8174a-125">-DnsSetting</span></span>
<span data-ttu-id="8174a-126">De DNS-inställningar som ska tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="8174a-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8174a-127">Domän namns etiketten för DNS-inställningarna för att tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="8174a-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8174a-128">Sammanfogningen av domän namns etiketten och VM-indexet blir domän namns etiketterna för de offentliga IP-adresserna som kommer att skapas.</span><span class="sxs-lookup"><span data-stu-id="8174a-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-129">-ID</span><span class="sxs-lookup"><span data-stu-id="8174a-129">-Id</span></span>
<span data-ttu-id="8174a-130">Anger ett ID.</span><span class="sxs-lookup"><span data-stu-id="8174a-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="8174a-131">-IpTag</span></span>
<span data-ttu-id="8174a-132">Anger en matris med IP-taggnamn.</span><span class="sxs-lookup"><span data-stu-id="8174a-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8174a-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="8174a-134">Anger en matris med referenser till inkommande NAT-pooler (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8174a-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="8174a-135">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8174a-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8174a-136">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8174a-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="8174a-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="8174a-138">Anger en matris med referenser till inkommande NAT-pooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8174a-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="8174a-139">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8174a-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8174a-140">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8174a-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="8174a-141">-Name</span></span>
<span data-ttu-id="8174a-142">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8174a-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-143">-Primär</span><span class="sxs-lookup"><span data-stu-id="8174a-143">-Primary</span></span>
<span data-ttu-id="8174a-144">Anger primär IP-konfiguration om nätverks gränssnittet har mer än en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8174a-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="8174a-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8174a-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="8174a-146">Ange IP-konfigurationen är IPv4 eller IPv6.</span><span class="sxs-lookup"><span data-stu-id="8174a-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="8174a-147">Standard är IPv4.</span><span class="sxs-lookup"><span data-stu-id="8174a-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="8174a-148">Möjliga värden är: IPv4 och IPv6.</span><span class="sxs-lookup"><span data-stu-id="8174a-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8174a-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="8174a-150">Idle-timeout för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="8174a-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8174a-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="8174a-152">Konfigurations namnet för publicIP-adressen.</span><span class="sxs-lookup"><span data-stu-id="8174a-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="8174a-153">-PublicIPPrefix</span></span>
<span data-ttu-id="8174a-154">ID för offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="8174a-154">The ID of Public IP Prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8174a-155">-SubnetId</span></span>
<span data-ttu-id="8174a-156">Anger det nätmask-ID som konfigurationen skapar VMSS nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="8174a-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8174a-157">-Confirm</span></span>
<span data-ttu-id="8174a-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8174a-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8174a-159">-WhatIf</span></span>
<span data-ttu-id="8174a-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8174a-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8174a-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8174a-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8174a-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8174a-162">CommonParameters</span></span>
<span data-ttu-id="8174a-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8174a-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8174a-164">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8174a-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8174a-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8174a-165">INPUTS</span></span>

### <span data-ttu-id="8174a-166">System. String</span><span class="sxs-lookup"><span data-stu-id="8174a-166">System.String</span></span>

### <span data-ttu-id="8174a-167">System. string []</span><span class="sxs-lookup"><span data-stu-id="8174a-167">System.String[]</span></span>

### <span data-ttu-id="8174a-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8174a-168">System.Int32</span></span>

### <span data-ttu-id="8174a-169">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="8174a-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="8174a-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8174a-170">OUTPUTS</span></span>

### <span data-ttu-id="8174a-171">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8174a-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="8174a-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8174a-172">NOTES</span></span>

## <span data-ttu-id="8174a-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8174a-173">RELATED LINKS</span></span>

[<span data-ttu-id="8174a-174">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8174a-174">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


