---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099183"
---
# <span data-ttu-id="77efd-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="77efd-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="77efd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77efd-102">SYNOPSIS</span></span>
<span data-ttu-id="77efd-103">Ändrar alla slut punkter i en belastnings Utjämnings uppsättning i en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="77efd-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="77efd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77efd-104">SYNTAX</span></span>

### <span data-ttu-id="77efd-105">DefaultProbe (standard)</span><span class="sxs-lookup"><span data-stu-id="77efd-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77efd-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="77efd-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="77efd-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="77efd-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="77efd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77efd-108">DESCRIPTION</span></span>
<span data-ttu-id="77efd-109">Cmdleten **set-AzureLoadBalancedEndpoint** ändrar alla slut punkter i en belastnings utjämning som angetts i en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="77efd-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="77efd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77efd-110">EXAMPLES</span></span>

### <span data-ttu-id="77efd-111">Exempel 1: ändra slut punkterna i en belastningsutjämnare</span><span class="sxs-lookup"><span data-stu-id="77efd-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="77efd-112">Det här kommandot ändrar alla slut punkter i belastningsutjämnaren som heter LBSet01 för att använda TCP-protokollet och den privata porten 80.</span><span class="sxs-lookup"><span data-stu-id="77efd-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="77efd-113">Kommandot anger belastningsutjämnaren för belastnings utjämning för att använda TCP-protokollet på Port 8080.</span><span class="sxs-lookup"><span data-stu-id="77efd-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="77efd-114">Exempel 2: Ange en annan virtuell IP-adress</span><span class="sxs-lookup"><span data-stu-id="77efd-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="77efd-115">Det här kommandot ändrar belastningsutjämnaren som har belastningsutjämnaren ange namnet till en virtuell IP-adress som heter Vip01.</span><span class="sxs-lookup"><span data-stu-id="77efd-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="77efd-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77efd-116">PARAMETERS</span></span>

### <span data-ttu-id="77efd-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="77efd-117">-ACL</span></span>
<span data-ttu-id="77efd-118">Anger en ACL-konfigurationsfil (Access Control List) som denna cmdlet gäller för slut punkterna.</span><span class="sxs-lookup"><span data-stu-id="77efd-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="77efd-119">-DirectServerReturn</span></span>
<span data-ttu-id="77efd-120">Anger om denna cmdlet aktiverar direkt Server återgång.</span><span class="sxs-lookup"><span data-stu-id="77efd-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="77efd-121">Ange $True som ska aktive ras eller $False inaktivera.</span><span class="sxs-lookup"><span data-stu-id="77efd-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="77efd-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="77efd-123">Anger tids gräns för TCP-timeout i minuter för slut punkterna.</span><span class="sxs-lookup"><span data-stu-id="77efd-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="77efd-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="77efd-124">-InformationAction</span></span>
<span data-ttu-id="77efd-125">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="77efd-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="77efd-126">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="77efd-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77efd-127">Vidare</span><span class="sxs-lookup"><span data-stu-id="77efd-127">Continue</span></span>
- <span data-ttu-id="77efd-128">Över</span><span class="sxs-lookup"><span data-stu-id="77efd-128">Ignore</span></span>
- <span data-ttu-id="77efd-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="77efd-129">Inquire</span></span>
- <span data-ttu-id="77efd-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="77efd-130">SilentlyContinue</span></span>
- <span data-ttu-id="77efd-131">Stanna</span><span class="sxs-lookup"><span data-stu-id="77efd-131">Stop</span></span>
- <span data-ttu-id="77efd-132">Avbryt</span><span class="sxs-lookup"><span data-stu-id="77efd-132">Suspend</span></span>

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

### <span data-ttu-id="77efd-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="77efd-133">-InformationVariable</span></span>
<span data-ttu-id="77efd-134">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="77efd-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="77efd-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="77efd-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="77efd-136">Anger namnet på intern belastningsutjämnaren som denna cmdlet inkluderar i konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="77efd-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="77efd-137">-LBSetName</span></span>
<span data-ttu-id="77efd-138">Anger namnet på den belastningsutjämnare som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="77efd-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="77efd-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="77efd-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="77efd-140">Anger algoritm för belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="77efd-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="77efd-141">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="77efd-141">Valid values are:</span></span> 

- <span data-ttu-id="77efd-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="77efd-142">sourceIP.</span></span>
<span data-ttu-id="77efd-143">Dubbel tupel: käll-IP, mål-IP</span><span class="sxs-lookup"><span data-stu-id="77efd-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="77efd-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="77efd-144">sourceIPProtocol.</span></span>
<span data-ttu-id="77efd-145">En par med tre tupler: käll-IP, mål-IP, protokoll</span><span class="sxs-lookup"><span data-stu-id="77efd-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="77efd-146">ingen.</span><span class="sxs-lookup"><span data-stu-id="77efd-146">none.</span></span>
<span data-ttu-id="77efd-147">En fem tuple tillhörighet: käll-IP, källport, mål-IP, målport, protokoll</span><span class="sxs-lookup"><span data-stu-id="77efd-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="77efd-148">Standardvärdet är inget.</span><span class="sxs-lookup"><span data-stu-id="77efd-148">The default value is none.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="77efd-149">-LocalPort</span></span>
<span data-ttu-id="77efd-150">Anger den lokala, privata, porten som dessa slut punkter använder.</span><span class="sxs-lookup"><span data-stu-id="77efd-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="77efd-151">Program på den virtuella datorn lyssnar på den här porten för begär Anden om tjänstens indata för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="77efd-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="77efd-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="77efd-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="77efd-153">Anger avsöknings intervall för avsökning, i sekunder, för slut punkterna.</span><span class="sxs-lookup"><span data-stu-id="77efd-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="77efd-154">-ProbePath</span></span>
<span data-ttu-id="77efd-155">Anger den relativa sökvägen för HTTP PROBE.</span><span class="sxs-lookup"><span data-stu-id="77efd-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="77efd-156">-ProbePort</span></span>
<span data-ttu-id="77efd-157">Anger vilken port som används för belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="77efd-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="77efd-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="77efd-159">Anger att belastningsutjämnaren för belastnings utjämning använder en HTTP-avsökning.</span><span class="sxs-lookup"><span data-stu-id="77efd-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="77efd-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="77efd-161">Anger att belastningsutjämnaren för belastnings utjämning använder en TCP-sond.</span><span class="sxs-lookup"><span data-stu-id="77efd-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="77efd-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="77efd-163">Anger timeout för Avsök-avslut i sekunder.</span><span class="sxs-lookup"><span data-stu-id="77efd-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-164">-Profil</span><span class="sxs-lookup"><span data-stu-id="77efd-164">-Profile</span></span>
<span data-ttu-id="77efd-165">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="77efd-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77efd-166">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="77efd-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="77efd-167">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="77efd-167">-Protocol</span></span>
<span data-ttu-id="77efd-168">Anger protokollet för slut punkterna.</span><span class="sxs-lookup"><span data-stu-id="77efd-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="77efd-169">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="77efd-169">Valid values are:</span></span> 

- <span data-ttu-id="77efd-170">TCP</span><span class="sxs-lookup"><span data-stu-id="77efd-170">TCP</span></span> 
- <span data-ttu-id="77efd-171">UDP</span><span class="sxs-lookup"><span data-stu-id="77efd-171">UDP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="77efd-172">-PublicPort</span></span>
<span data-ttu-id="77efd-173">Anger den offentliga port som slut punkten använder.</span><span class="sxs-lookup"><span data-stu-id="77efd-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="77efd-174">Om du inte anger något värde tilldelar Azure en tillgänglig port.</span><span class="sxs-lookup"><span data-stu-id="77efd-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="77efd-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77efd-175">-ServiceName</span></span>
<span data-ttu-id="77efd-176">Anger namnet på den Azure-tjänst som innehåller slut punkterna som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="77efd-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="77efd-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="77efd-177">-VirtualIPName</span></span>
<span data-ttu-id="77efd-178">Anger namnet på en virtuell IP-adress som Azure associeras med till slut punkterna.</span><span class="sxs-lookup"><span data-stu-id="77efd-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="77efd-179">Använd cmdleten **Add-AzureVirtualIP** för att lägga till virtuella IP-adresser i din tjänst.</span><span class="sxs-lookup"><span data-stu-id="77efd-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77efd-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77efd-180">CommonParameters</span></span>
<span data-ttu-id="77efd-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77efd-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77efd-182">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77efd-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77efd-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77efd-183">INPUTS</span></span>

## <span data-ttu-id="77efd-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77efd-184">OUTPUTS</span></span>

## <span data-ttu-id="77efd-185">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77efd-185">NOTES</span></span>

## <span data-ttu-id="77efd-186">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77efd-186">RELATED LINKS</span></span>

[<span data-ttu-id="77efd-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="77efd-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="77efd-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77efd-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


