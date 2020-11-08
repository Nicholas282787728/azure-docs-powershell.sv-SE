---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093450"
---
# <span data-ttu-id="2f29f-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f29f-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="2f29f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f29f-102">SYNOPSIS</span></span>
<span data-ttu-id="2f29f-103">Lägger till en intern belastningsutjämnare till en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="2f29f-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="2f29f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f29f-104">SYNTAX</span></span>

### <span data-ttu-id="2f29f-105">ServiceAndSlot (standard)</span><span class="sxs-lookup"><span data-stu-id="2f29f-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f29f-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="2f29f-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2f29f-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="2f29f-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2f29f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f29f-108">DESCRIPTION</span></span>
<span data-ttu-id="2f29f-109">Cmdleten **Add-AzureInternalLoadBalancer** lägger till en intern belastningsutjämnare-konfiguration i en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="2f29f-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="2f29f-110">För ett virtuellt nätverk kan du ange ett undernät eller IP-adressen för den interna belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="2f29f-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="2f29f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f29f-111">EXAMPLES</span></span>

### <span data-ttu-id="2f29f-112">Exempel 1: lägga till en intern belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="2f29f-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="2f29f-113">Det här kommandot lägger till en intern belastningsutjämnare som heter ContosoILB till tjänsten ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="2f29f-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="2f29f-114">Exempel 2: lägga till en intern belastningsutjämnare för ett angivet undernät</span><span class="sxs-lookup"><span data-stu-id="2f29f-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="2f29f-115">Det här kommandot lägger till en intern belastningsutjämnare som heter ContosoILB till tjänsten ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="2f29f-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="2f29f-116">Kommandot anger det undernät som heter FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="2f29f-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="2f29f-117">Exempel 3: lägga till en intern belastningsutjämnare för ett angivet undernät och en viss adress</span><span class="sxs-lookup"><span data-stu-id="2f29f-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="2f29f-118">Det här kommandot lägger till en intern belastningsutjämnare som heter ContosoILB till tjänsten ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="2f29f-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="2f29f-119">Kommandot anger det undernät som heter FrontEndSubnet och den statiska adressen för det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="2f29f-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="2f29f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f29f-120">PARAMETERS</span></span>

### <span data-ttu-id="2f29f-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2f29f-121">-InformationAction</span></span>
<span data-ttu-id="2f29f-122">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="2f29f-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2f29f-123">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2f29f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2f29f-124">Vidare</span><span class="sxs-lookup"><span data-stu-id="2f29f-124">Continue</span></span>
- <span data-ttu-id="2f29f-125">Över</span><span class="sxs-lookup"><span data-stu-id="2f29f-125">Ignore</span></span>
- <span data-ttu-id="2f29f-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="2f29f-126">Inquire</span></span>
- <span data-ttu-id="2f29f-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2f29f-127">SilentlyContinue</span></span>
- <span data-ttu-id="2f29f-128">Stanna</span><span class="sxs-lookup"><span data-stu-id="2f29f-128">Stop</span></span>
- <span data-ttu-id="2f29f-129">Avbryt</span><span class="sxs-lookup"><span data-stu-id="2f29f-129">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2f29f-130">-InformationVariable</span></span>
<span data-ttu-id="2f29f-131">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="2f29f-131">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="2f29f-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="2f29f-133">Anger namnet på intern belastningsutjämnaren som läggs till i cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f29f-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="2f29f-134">-Profile</span></span>
<span data-ttu-id="2f29f-135">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2f29f-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2f29f-136">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2f29f-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2f29f-137">-ServiceName</span></span>
<span data-ttu-id="2f29f-138">Anger namnet på den tjänst där denna cmdlet lägger till en intern belastningsutjämnare.</span><span class="sxs-lookup"><span data-stu-id="2f29f-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="2f29f-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="2f29f-140">Anger virtuell nätverks-IP-adress för en intern belastningsutjämnare som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="2f29f-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="2f29f-141">-SubnetName</span></span>
<span data-ttu-id="2f29f-142">Anger namnet på under nätet för en intern belastningsutjämnare som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="2f29f-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f29f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f29f-143">CommonParameters</span></span>
<span data-ttu-id="2f29f-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f29f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f29f-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f29f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f29f-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f29f-146">INPUTS</span></span>

## <span data-ttu-id="2f29f-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f29f-147">OUTPUTS</span></span>

### <span data-ttu-id="2f29f-148">Microsoft. WindowsAzure. commands. Utilitiess. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="2f29f-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="2f29f-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f29f-149">NOTES</span></span>

## <span data-ttu-id="2f29f-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f29f-150">RELATED LINKS</span></span>

[<span data-ttu-id="2f29f-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f29f-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="2f29f-152">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="2f29f-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="2f29f-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f29f-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="2f29f-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2f29f-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


