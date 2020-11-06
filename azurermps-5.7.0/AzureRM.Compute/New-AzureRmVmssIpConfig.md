---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576602"
---
# <span data-ttu-id="c3167-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c3167-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="c3167-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3167-102">SYNOPSIS</span></span>
<span data-ttu-id="c3167-103">Skapar en IP-konfiguration för ett nätverks gränssnitt för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="c3167-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3167-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3167-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3167-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3167-105">DESCRIPTION</span></span>
<span data-ttu-id="c3167-106">Cmdleten **New-AzureRmVmssIpConfig** skapar ett IP-konfigurationsobjekt för ett nätverks gränssnitt med en virtuell dators skalnings uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c3167-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c3167-107">Ange konfigurationen från den här cmdleten som *IPConfiguration* för Add-AzureRmVmssNetworkInterfaceConfiguration cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3167-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="c3167-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3167-108">EXAMPLES</span></span>

### <span data-ttu-id="c3167-109">Exempel 1: skapa ett IP-konfigurationsobjekt för ett VMSS gränssnitt</span><span class="sxs-lookup"><span data-stu-id="c3167-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="c3167-110">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="c3167-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="c3167-111">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="c3167-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="c3167-112">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning med **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c3167-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="c3167-113">Exempel 2: skapa ett IP-konfigurationsobjekt som innehåller inställningar för NAT-pool</span><span class="sxs-lookup"><span data-stu-id="c3167-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="c3167-114">Det här kommandot skapar ett IP-konfigurationsobjekt med namnet ContosoVmssInterface03 och lagrar det sedan i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="c3167-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="c3167-115">Kommandot använder ett tidigare definierat undernät-ID som lagras i $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="c3167-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="c3167-116">Kommandot lagrar konfigurations inställningarna i $IPConfiguration variabel för senare användning.</span><span class="sxs-lookup"><span data-stu-id="c3167-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="c3167-117">Kommandot anger värden för parametrarna *LoadBalancerInboundNatPoolsId* och *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="c3167-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="c3167-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3167-118">PARAMETERS</span></span>

### <span data-ttu-id="c3167-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="c3167-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="c3167-120">Anger en matris med referenser till Server delens adresspooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c3167-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="c3167-121">Med en skalnings uppsättning kan Server gruppens adresspooler referera till en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c3167-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="c3167-122">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c3167-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="c3167-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="c3167-123">-DnsSetting</span></span>
<span data-ttu-id="c3167-124">De DNS-inställningar som ska tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c3167-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="c3167-125">Domän namns etiketten för DNS-inställningarna för att tillämpas på publicIP-adresser.</span><span class="sxs-lookup"><span data-stu-id="c3167-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="c3167-126">Sammanfogningen av domän namns etiketten och VM-indexet blir domän namns etiketterna för de offentliga IP-adresserna som kommer att skapas.</span><span class="sxs-lookup"><span data-stu-id="c3167-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="c3167-127">-ID</span><span class="sxs-lookup"><span data-stu-id="c3167-127">-Id</span></span>
<span data-ttu-id="c3167-128">Anger ett ID.</span><span class="sxs-lookup"><span data-stu-id="c3167-128">Specifies an ID.</span></span>

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

### <span data-ttu-id="c3167-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="c3167-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="c3167-130">Anger en matris med referenser till inkommande NAT-pooler (Network Address Translation) för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c3167-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="c3167-131">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c3167-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="c3167-132">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c3167-132">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="c3167-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="c3167-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="c3167-134">Anger en matris med referenser till inkommande NAT-pooler för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="c3167-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="c3167-135">En skalnings uppsättning kan referera inkommande NAT-pooler för en offentlig och en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c3167-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="c3167-136">Multiple Scale set kan inte använda samma belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="c3167-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="c3167-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3167-137">-Name</span></span>
<span data-ttu-id="c3167-138">Anger namnet på IP-konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="c3167-138">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="c3167-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="c3167-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="c3167-140">Ange IP-konfigurationen är IPv4 eller IPv6.</span><span class="sxs-lookup"><span data-stu-id="c3167-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="c3167-141">Standard är IPv4.</span><span class="sxs-lookup"><span data-stu-id="c3167-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="c3167-142">Möjliga värden är: IPv4 och IPv6.</span><span class="sxs-lookup"><span data-stu-id="c3167-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="c3167-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="c3167-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="c3167-144">Idle-timeout för den offentliga IP-adressen.</span><span class="sxs-lookup"><span data-stu-id="c3167-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3167-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c3167-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="c3167-146">Konfigurations namnet för publicIP-adressen.</span><span class="sxs-lookup"><span data-stu-id="c3167-146">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="c3167-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c3167-147">-SubnetId</span></span>
<span data-ttu-id="c3167-148">Anger det nätmask-ID som konfigurationen skapar VMSS nätverks gränssnitt för.</span><span class="sxs-lookup"><span data-stu-id="c3167-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="c3167-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3167-149">-Confirm</span></span>
<span data-ttu-id="c3167-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3167-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3167-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3167-151">-WhatIf</span></span>
<span data-ttu-id="c3167-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3167-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3167-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3167-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3167-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3167-154">CommonParameters</span></span>
<span data-ttu-id="c3167-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3167-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3167-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3167-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3167-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3167-157">INPUTS</span></span>

### <span data-ttu-id="c3167-158">Ingen</span><span class="sxs-lookup"><span data-stu-id="c3167-158">None</span></span>
<span data-ttu-id="c3167-159">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c3167-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3167-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3167-160">OUTPUTS</span></span>

## <span data-ttu-id="c3167-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3167-161">NOTES</span></span>

## <span data-ttu-id="c3167-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3167-162">RELATED LINKS</span></span>

[<span data-ttu-id="c3167-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3167-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


