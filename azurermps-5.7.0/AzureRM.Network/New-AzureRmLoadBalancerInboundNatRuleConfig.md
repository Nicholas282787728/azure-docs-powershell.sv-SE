---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 0b974d1d79be82f3c16f1052abe0eecc7fa9ba30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756488"
---
# <span data-ttu-id="1dbd8-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dbd8-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="1dbd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbd8-103">Skapar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dbd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dbd8-104">SYNTAX</span></span>

### <span data-ttu-id="1dbd8-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1dbd8-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbd8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1dbd8-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbd8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dbd8-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbd8-108">Cmdleten **New-AzureRmLoadBalancerInboundNatRuleConfig** skapar en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1dbd8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dbd8-109">EXAMPLES</span></span>

### <span data-ttu-id="1dbd8-110">Exempel 1: skapa en inkommande NAT-regel för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="1dbd8-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="1dbd8-111">Det första kommandot skapar en offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="1dbd8-112">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip och lagrar den sedan i $frontend-variabeln.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="1dbd8-113">Det tredje kommandot skapar en inkommande NAT-regel som heter MyInboundNatRule med hjälp av ett frontend-objekt i $frontend.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="1dbd8-114">TCP-protokollet anges och front porten är 3389, samma som Server porten i det här fallet.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="1dbd8-115">Parametrarna *FrontendIpConfiguration* , *Procotol* , *FrontendPort* och *BACKENDPORT* krävs för att skapa en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="1dbd8-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dbd8-116">PARAMETERS</span></span>

### <span data-ttu-id="1dbd8-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="1dbd8-117">-BackendPort</span></span>
<span data-ttu-id="1dbd8-118">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="1dbd8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbd8-119">-DefaultProfile</span></span>
<span data-ttu-id="1dbd8-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbd8-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="1dbd8-121">-EnableFloatingIP</span></span>
<span data-ttu-id="1dbd8-122">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="1dbd8-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dbd8-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="1dbd8-124">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1dbd8-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1dbd8-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="1dbd8-126">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="1dbd8-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1dbd8-127">-FrontendPort</span></span>
<span data-ttu-id="1dbd8-128">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="1dbd8-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1dbd8-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="1dbd8-130">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="1dbd8-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dbd8-131">-Name</span></span>
<span data-ttu-id="1dbd8-132">Anger namnet på den regel konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1dbd8-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1dbd8-133">-Protocol</span></span>
<span data-ttu-id="1dbd8-134">Anger ett protokoll.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-134">Specifies a protocol.</span></span>
<span data-ttu-id="1dbd8-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1dbd8-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1dbd8-136">TCP</span><span class="sxs-lookup"><span data-stu-id="1dbd8-136">Tcp</span></span>
- <span data-ttu-id="1dbd8-137">UDP</span><span class="sxs-lookup"><span data-stu-id="1dbd8-137">Udp</span></span>

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

### <span data-ttu-id="1dbd8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbd8-138">CommonParameters</span></span>
<span data-ttu-id="1dbd8-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbd8-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbd8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbd8-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dbd8-141">INPUTS</span></span>

### <span data-ttu-id="1dbd8-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="1dbd8-142">None</span></span>
<span data-ttu-id="1dbd8-143">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="1dbd8-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1dbd8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dbd8-144">OUTPUTS</span></span>

### <span data-ttu-id="1dbd8-145">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="1dbd8-145">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="1dbd8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dbd8-146">NOTES</span></span>

## <span data-ttu-id="1dbd8-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dbd8-147">RELATED LINKS</span></span>

[<span data-ttu-id="1dbd8-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dbd8-148">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1dbd8-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dbd8-149">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1dbd8-150">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dbd8-150">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="1dbd8-151">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="1dbd8-151">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="1dbd8-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dbd8-152">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1dbd8-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1dbd8-153">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


