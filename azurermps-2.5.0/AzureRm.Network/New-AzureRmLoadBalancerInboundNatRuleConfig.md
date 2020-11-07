---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: bcf937c0da7adfd0accafcd943de24744eb4a5ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931254"
---
# <span data-ttu-id="8013c-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8013c-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="8013c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8013c-102">SYNOPSIS</span></span>
<span data-ttu-id="8013c-103">Skapar en inkommande NAT-regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8013c-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8013c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8013c-104">SYNTAX</span></span>

### <span data-ttu-id="8013c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8013c-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8013c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8013c-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8013c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8013c-107">DESCRIPTION</span></span>
<span data-ttu-id="8013c-108">Cmdleten **New-AzureRmLoadBalancerInboundNatRuleConfig** skapar en inkommande NAT-regel (Network Address Translation) för en Azure-belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="8013c-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8013c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8013c-109">EXAMPLES</span></span>

### <span data-ttu-id="8013c-110">Exempel 1: skapa en inkommande NAT-regel för belastnings utjämning</span><span class="sxs-lookup"><span data-stu-id="8013c-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="8013c-111">Det första kommandot skapar en offentlig IP-adress med namnet MyPublicIP i resurs gruppen som heter MyResourceGroup och lagrar den sedan i $publicip variabel.</span><span class="sxs-lookup"><span data-stu-id="8013c-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="8013c-112">Det andra kommandot skapar en front-IP-konfiguration som heter FrontendIpConfig01 med den offentliga IP-adressen i $publicip och lagrar den sedan i $frontend-variabeln.</span><span class="sxs-lookup"><span data-stu-id="8013c-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="8013c-113">Det tredje kommandot skapar en inkommande NAT-regel som heter MyInboundNatRule med hjälp av ett frontend-objekt i $frontend.</span><span class="sxs-lookup"><span data-stu-id="8013c-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="8013c-114">TCP-protokollet anges och front porten är 3389, samma som Server porten i det här fallet.</span><span class="sxs-lookup"><span data-stu-id="8013c-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="8013c-115">Parametrarna *FrontendIpConfiguration* , *Procotol* , *FrontendPort* och *BACKENDPORT* krävs för att skapa en inkommande NAT-regel.</span><span class="sxs-lookup"><span data-stu-id="8013c-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="8013c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8013c-116">PARAMETERS</span></span>

### <span data-ttu-id="8013c-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="8013c-117">-BackendPort</span></span>
<span data-ttu-id="8013c-118">Anger Server dels porten för trafik som matchas av denna regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8013c-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="8013c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8013c-119">-DefaultProfile</span></span>
<span data-ttu-id="8013c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8013c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8013c-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="8013c-121">-EnableFloatingIP</span></span>
<span data-ttu-id="8013c-122">Anger att denna cmdlet aktiverar en flytande IP-adress för en regel konfiguration.</span><span class="sxs-lookup"><span data-stu-id="8013c-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="8013c-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="8013c-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="8013c-124">Anger en lista över de front-IP-adresser som är associerade med en regel konfiguration för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8013c-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8013c-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8013c-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="8013c-126">Anger ID för en front-IP-adresskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="8013c-126">Specifies the ID for a front-end IP address configuration.</span></span>

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

### <span data-ttu-id="8013c-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8013c-127">-FrontendPort</span></span>
<span data-ttu-id="8013c-128">Anger front porten som matchas av en regel för belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8013c-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="8013c-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="8013c-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="8013c-130">Anger hur lång tid, i minuter, som status för konversationer ska behållas i en belastnings utjämning.</span><span class="sxs-lookup"><span data-stu-id="8013c-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="8013c-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="8013c-131">-Name</span></span>
<span data-ttu-id="8013c-132">Anger namnet på den regel konfiguration som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="8013c-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8013c-133">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="8013c-133">-Protocol</span></span>
<span data-ttu-id="8013c-134">Anger ett protokoll.</span><span class="sxs-lookup"><span data-stu-id="8013c-134">Specifies a protocol.</span></span>
<span data-ttu-id="8013c-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8013c-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8013c-136">TCP</span><span class="sxs-lookup"><span data-stu-id="8013c-136">Tcp</span></span>
- <span data-ttu-id="8013c-137">UDP</span><span class="sxs-lookup"><span data-stu-id="8013c-137">Udp</span></span>

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

### <span data-ttu-id="8013c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8013c-138">CommonParameters</span></span>
<span data-ttu-id="8013c-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8013c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8013c-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8013c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8013c-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8013c-141">INPUTS</span></span>

## <span data-ttu-id="8013c-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8013c-142">OUTPUTS</span></span>

### <span data-ttu-id="8013c-143">Microsoft. Azure. commands. Networks. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="8013c-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="8013c-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8013c-144">NOTES</span></span>

## <span data-ttu-id="8013c-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8013c-145">RELATED LINKS</span></span>

[<span data-ttu-id="8013c-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8013c-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8013c-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8013c-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8013c-148">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8013c-148">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8013c-149">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8013c-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="8013c-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8013c-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="8013c-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8013c-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


