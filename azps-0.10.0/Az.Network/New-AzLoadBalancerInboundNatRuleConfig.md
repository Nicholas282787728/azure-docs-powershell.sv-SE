---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 52aad9586840875cf63a27a8f27ff7296d080bd7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922124"
---
# <span data-ttu-id="09e9a-101">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09e9a-101">New-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="09e9a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="09e9a-103">Skapar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="09e9a-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="09e9a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09e9a-104">SYNTAX</span></span>

### <span data-ttu-id="09e9a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="09e9a-105">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09e9a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="09e9a-106">SetByResource</span></span>
```
New-AzLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09e9a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="09e9a-108">Cmdleten **New-AzLoadBalancerInboundNatRuleConfig** skapar en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="09e9a-108">The **New-AzLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="09e9a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="09e9a-110">Exempel 1: skapa en inkommande NAT-regel för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="09e9a-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="09e9a-111">Det första kommandot skapar en offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="09e9a-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="09e9a-112">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip och lagrar den sedan i $frontend-variabeln.</span><span class="sxs-lookup"><span data-stu-id="09e9a-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="09e9a-113">Det tredje kommandot skapar en inkommande NAT-regel som heter MyInboundNatRule med hjälp av ett frontend-objekt i $frontend.</span><span class="sxs-lookup"><span data-stu-id="09e9a-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="09e9a-114">TCP-protokollet anges och front porten är 3389, samma som Server porten i det här fallet.</span><span class="sxs-lookup"><span data-stu-id="09e9a-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="09e9a-115">Parametrarna *FrontendIpConfiguration* , *Procotol* , *FrontendPort* och *BACKENDPORT* krävs för att skapa en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="09e9a-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="09e9a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09e9a-116">PARAMETERS</span></span>

### <span data-ttu-id="09e9a-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="09e9a-117">-BackendPort</span></span>
<span data-ttu-id="09e9a-118">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09e9a-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e9a-119">-DefaultProfile</span></span>
<span data-ttu-id="09e9a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09e9a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09e9a-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="09e9a-121">-EnableFloatingIP</span></span>
<span data-ttu-id="09e9a-122">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="09e9a-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="09e9a-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="09e9a-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="09e9a-124">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="09e9a-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="09e9a-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="09e9a-126">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="09e9a-126">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="09e9a-127">-FrontendPort</span></span>
<span data-ttu-id="09e9a-128">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="09e9a-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="09e9a-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="09e9a-130">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="09e9a-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="09e9a-131">-Name</span></span>
<span data-ttu-id="09e9a-132">Anger namnet på den regel konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="09e9a-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="09e9a-133">-Protocol</span></span>
<span data-ttu-id="09e9a-134">Anger ett protokoll.</span><span class="sxs-lookup"><span data-stu-id="09e9a-134">Specifies a protocol.</span></span>
<span data-ttu-id="09e9a-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="09e9a-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="09e9a-136">TCP</span><span class="sxs-lookup"><span data-stu-id="09e9a-136">Tcp</span></span>
- <span data-ttu-id="09e9a-137">UDP</span><span class="sxs-lookup"><span data-stu-id="09e9a-137">Udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09e9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e9a-138">CommonParameters</span></span>
<span data-ttu-id="09e9a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e9a-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e9a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e9a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09e9a-141">INPUTS</span></span>

## <span data-ttu-id="09e9a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09e9a-142">OUTPUTS</span></span>

### <span data-ttu-id="09e9a-143">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="09e9a-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="09e9a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09e9a-144">NOTES</span></span>

## <span data-ttu-id="09e9a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09e9a-145">RELATED LINKS</span></span>

[<span data-ttu-id="09e9a-146">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09e9a-146">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="09e9a-147">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09e9a-147">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="09e9a-148">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="09e9a-148">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="09e9a-149">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="09e9a-149">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="09e9a-150">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09e9a-150">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="09e9a-151">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="09e9a-151">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


