---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 271d4c9d9fd4a7eb34d4ced4b32dc3929a32b31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745070"
---
# <span data-ttu-id="8509b-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8509b-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="8509b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8509b-102">SYNOPSIS</span></span>
<span data-ttu-id="8509b-103">Skapar en IP-konfiguration för ett nätverks gränssnitt för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="8509b-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="8509b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8509b-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8509b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8509b-105">DESCRIPTION</span></span>
<span data-ttu-id="8509b-106">Cmdleten **New-AzVmssIpConfig** skapar ett IP-konfigurationsobjekt för ett nätverks gränssnitt med en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="8509b-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="8509b-107">Ange konfigurationen från den här cmdleten som *IPConfiguration* för Add-AzVmssNetworkInterfaceConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8509b-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="8509b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8509b-108">EXAMPLES</span></span>

### <span data-ttu-id="8509b-109">Exempel 1: skapa ett IP-konfigurationsobjekt för ett VMSS gränssnitt</span><span class="sxs-lookup"><span data-stu-id="8509b-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="8509b-110">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="8509b-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="8509b-111">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="8509b-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8509b-112">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning med **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="8509b-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="8509b-113">Exempel 2: skapa ett IP-konfigurationsobjekt som innehåller inställningar för NAT-pool</span><span class="sxs-lookup"><span data-stu-id="8509b-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="8509b-114">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface03 och lagrar det sedan i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="8509b-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8509b-115">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="8509b-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="8509b-116">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="8509b-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="8509b-117">Kommandot anger värden för parametrarna *LoadBalancerInboundNatPoolsId* och *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="8509b-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="8509b-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8509b-118">PARAMETERS</span></span>

### <span data-ttu-id="8509b-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8509b-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="8509b-120">Anger en matris med referenser till Server delens adresspooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8509b-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="8509b-121">Med en skalnings uppsättning kan Server gruppens adresspooler referera till en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8509b-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8509b-122">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8509b-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8509b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8509b-123">-DefaultProfile</span></span>
<span data-ttu-id="8509b-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8509b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8509b-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="8509b-125">-DnsSetting</span></span>
<span data-ttu-id="8509b-126">De DNS-inställningar som ska tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="8509b-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8509b-127">Domän namns etiketten för DNS-inställningarna för att tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="8509b-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="8509b-128">Sammanfogningen av domän namns etiketten och VM-indexet blir domän namns etiketterna för de offentliga IP-adresserna som kommer att skapas.</span><span class="sxs-lookup"><span data-stu-id="8509b-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="8509b-129">-ID</span><span class="sxs-lookup"><span data-stu-id="8509b-129">-Id</span></span>
<span data-ttu-id="8509b-130">Anger ett ID.</span><span class="sxs-lookup"><span data-stu-id="8509b-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="8509b-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="8509b-131">-IpTag</span></span>
<span data-ttu-id="8509b-132">Anger en matris med IP-taggnamn.</span><span class="sxs-lookup"><span data-stu-id="8509b-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="8509b-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="8509b-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="8509b-134">Anger en matris med referenser till inkommande NAT-pooler (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8509b-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="8509b-135">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8509b-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8509b-136">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8509b-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8509b-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="8509b-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="8509b-138">Anger en matris med referenser till inkommande NAT-pooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8509b-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="8509b-139">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8509b-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="8509b-140">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8509b-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="8509b-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="8509b-141">-Name</span></span>
<span data-ttu-id="8509b-142">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8509b-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="8509b-143">-Primär</span><span class="sxs-lookup"><span data-stu-id="8509b-143">-Primary</span></span>
<span data-ttu-id="8509b-144">Anger primär IP-konfiguration om nätverks gränssnittet har mer än en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8509b-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="8509b-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8509b-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="8509b-146">Ange IP-konfigurationen är IPv4 eller IPv6.</span><span class="sxs-lookup"><span data-stu-id="8509b-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="8509b-147">Standard är IPv4.</span><span class="sxs-lookup"><span data-stu-id="8509b-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="8509b-148">Möjliga värden är: IPv4 och IPv6.</span><span class="sxs-lookup"><span data-stu-id="8509b-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="8509b-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8509b-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="8509b-150">Idle-timeout för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="8509b-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="8509b-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8509b-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="8509b-152">Konfigurations namnet för publicIP-adressen.</span><span class="sxs-lookup"><span data-stu-id="8509b-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="8509b-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="8509b-153">-PublicIPPrefix</span></span>
<span data-ttu-id="8509b-154">ID för offentlig IP-prefix</span><span class="sxs-lookup"><span data-stu-id="8509b-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="8509b-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8509b-155">-SubnetId</span></span>
<span data-ttu-id="8509b-156">Anger det nätmask-ID som konfigurationen skapar VMSS nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="8509b-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="8509b-157">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8509b-157">-Confirm</span></span>
<span data-ttu-id="8509b-158">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8509b-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8509b-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8509b-159">-WhatIf</span></span>
<span data-ttu-id="8509b-160">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8509b-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8509b-161">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8509b-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8509b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8509b-162">CommonParameters</span></span>
<span data-ttu-id="8509b-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8509b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8509b-164">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8509b-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8509b-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8509b-165">INPUTS</span></span>

### <span data-ttu-id="8509b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="8509b-166">System.String</span></span>

### <span data-ttu-id="8509b-167">System. string []</span><span class="sxs-lookup"><span data-stu-id="8509b-167">System.String[]</span></span>

### <span data-ttu-id="8509b-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8509b-168">System.Int32</span></span>

### <span data-ttu-id="8509b-169">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="8509b-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="8509b-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8509b-170">OUTPUTS</span></span>

### <span data-ttu-id="8509b-171">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8509b-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="8509b-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8509b-172">NOTES</span></span>

## <span data-ttu-id="8509b-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8509b-173">RELATED LINKS</span></span>

[<span data-ttu-id="8509b-174">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8509b-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


