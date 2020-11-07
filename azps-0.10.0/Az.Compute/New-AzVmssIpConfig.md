---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 41b176d5952e9a33d0d0868b97fc71a14d6b43d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93925029"
---
# <span data-ttu-id="18953-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="18953-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="18953-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18953-102">SYNOPSIS</span></span>
<span data-ttu-id="18953-103">Skapar en IP-konfiguration för ett nätverks gränssnitt för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="18953-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="18953-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18953-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18953-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18953-105">DESCRIPTION</span></span>
<span data-ttu-id="18953-106">Cmdleten **New-AzVmssIpConfig** skapar ett IP-konfigurationsobjekt för ett nätverks gränssnitt med en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="18953-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="18953-107">Ange konfigurationen från den här cmdleten som *IPConfiguration* för Add-AzVmssNetworkInterfaceConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18953-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="18953-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18953-108">EXAMPLES</span></span>

### <span data-ttu-id="18953-109">Exempel 1: skapa ett IP-konfigurationsobjekt för ett VMSS gränssnitt</span><span class="sxs-lookup"><span data-stu-id="18953-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="18953-110">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="18953-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="18953-111">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="18953-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="18953-112">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning med **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="18953-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="18953-113">Exempel 2: skapa ett IP-konfigurationsobjekt som innehåller inställningar för NAT-pool</span><span class="sxs-lookup"><span data-stu-id="18953-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="18953-114">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface03 och lagrar det sedan i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="18953-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="18953-115">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="18953-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="18953-116">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="18953-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="18953-117">Kommandot anger värden för parametrarna *LoadBalancerInboundNatPoolsId* och *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="18953-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="18953-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18953-118">PARAMETERS</span></span>

### <span data-ttu-id="18953-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="18953-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="18953-120">Anger en matris med referenser till Server delens adresspooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="18953-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="18953-121">Med en skalnings uppsättning kan Server gruppens adresspooler referera till en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="18953-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="18953-122">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="18953-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18953-123">-DefaultProfile</span></span>
<span data-ttu-id="18953-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18953-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18953-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="18953-125">-DnsSetting</span></span>
<span data-ttu-id="18953-126">De DNS-inställningar som ska tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="18953-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="18953-127">Domän namns etiketten för DNS-inställningarna för att tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="18953-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="18953-128">Sammanfogningen av domän namns etiketten och VM-indexet blir domän namns etiketterna för de offentliga IP-adresserna som kommer att skapas.</span><span class="sxs-lookup"><span data-stu-id="18953-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-129">-ID</span><span class="sxs-lookup"><span data-stu-id="18953-129">-Id</span></span>
<span data-ttu-id="18953-130">Anger ett ID.</span><span class="sxs-lookup"><span data-stu-id="18953-130">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-131">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="18953-131">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="18953-132">Anger en matris med referenser till inkommande NAT-pooler (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="18953-132">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="18953-133">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="18953-133">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="18953-134">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="18953-134">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-135">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="18953-135">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="18953-136">Anger en matris med referenser till inkommande NAT-pooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="18953-136">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="18953-137">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="18953-137">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="18953-138">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="18953-138">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="18953-139">-Name</span></span>
<span data-ttu-id="18953-140">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="18953-140">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-141">-Primär</span><span class="sxs-lookup"><span data-stu-id="18953-141">-Primary</span></span>
<span data-ttu-id="18953-142">Anger primär IP-konfiguration om nätverks gränssnittet har mer än en IP-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="18953-142">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="18953-143">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="18953-143">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="18953-144">Ange IP-konfigurationen är IPv4 eller IPv6.</span><span class="sxs-lookup"><span data-stu-id="18953-144">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="18953-145">Standard är IPv4.</span><span class="sxs-lookup"><span data-stu-id="18953-145">Default is taken as IPv4.</span></span>  <span data-ttu-id="18953-146">Möjliga värden är: IPv4 och IPv6.</span><span class="sxs-lookup"><span data-stu-id="18953-146">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="18953-147">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="18953-148">Idle-timeout för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="18953-148">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-149">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="18953-149">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="18953-150">Konfigurations namnet för publicIP-adressen.</span><span class="sxs-lookup"><span data-stu-id="18953-150">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-151">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="18953-151">-SubnetId</span></span>
<span data-ttu-id="18953-152">Anger det nätmask-ID som konfigurationen skapar VMSS nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="18953-152">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18953-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18953-153">-Confirm</span></span>
<span data-ttu-id="18953-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18953-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18953-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18953-155">-WhatIf</span></span>
<span data-ttu-id="18953-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18953-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18953-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18953-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18953-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18953-158">CommonParameters</span></span>
<span data-ttu-id="18953-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18953-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18953-160">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18953-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18953-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18953-161">INPUTS</span></span>

### <span data-ttu-id="18953-162">Ingen</span><span class="sxs-lookup"><span data-stu-id="18953-162">None</span></span>
<span data-ttu-id="18953-163">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="18953-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18953-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18953-164">OUTPUTS</span></span>

### <span data-ttu-id="18953-165">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="18953-165">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="18953-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18953-166">NOTES</span></span>

## <span data-ttu-id="18953-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18953-167">RELATED LINKS</span></span>

[<span data-ttu-id="18953-168">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="18953-168">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


