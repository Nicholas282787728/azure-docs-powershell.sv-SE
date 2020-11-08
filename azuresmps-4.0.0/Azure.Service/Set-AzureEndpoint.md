---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099287"
---
# <span data-ttu-id="4776b-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4776b-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="4776b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4776b-102">SYNOPSIS</span></span>
<span data-ttu-id="4776b-103">Ändrar en slut punkt som tilldelats till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="4776b-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="4776b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4776b-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4776b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4776b-105">DESCRIPTION</span></span>
<span data-ttu-id="4776b-106">Cmdleten **set-AzureEndpoint** ändrar en slut punkt som tilldelats en virtuell Azure-dator.</span><span class="sxs-lookup"><span data-stu-id="4776b-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="4776b-107">Du kan ange ändringar av en slut punkt som inte är bal anse rad.</span><span class="sxs-lookup"><span data-stu-id="4776b-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="4776b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4776b-108">EXAMPLES</span></span>

### <span data-ttu-id="4776b-109">Exempel 1: ändra en slut punkt för att lyssna på en port</span><span class="sxs-lookup"><span data-stu-id="4776b-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="4776b-110">Det här kommandot hämtar konfigurationen för en virtuell dator med namnet VirtualMachine01 med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="4776b-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="4776b-111">Kommandot skickar det till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="4776b-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4776b-112">Denna cmdlet ändrar slut punkten som heter Web för att lyssna på port 443.</span><span class="sxs-lookup"><span data-stu-id="4776b-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="4776b-113">Kommandot skickar det virtuella datorobjektet till cmdleten **Update-AzureVM** som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="4776b-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="4776b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4776b-114">PARAMETERS</span></span>

### <span data-ttu-id="4776b-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="4776b-115">-ACL</span></span>
<span data-ttu-id="4776b-116">Anger en ACL-konfigurationsfil (Access Control List) som denna cmdlet gäller för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4776b-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="4776b-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="4776b-117">-DirectServerReturn</span></span>
<span data-ttu-id="4776b-118">Anger om denna cmdlet aktiverar direkt Server återgång.</span><span class="sxs-lookup"><span data-stu-id="4776b-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="4776b-119">Ange $True som ska aktive ras eller $False inaktivera.</span><span class="sxs-lookup"><span data-stu-id="4776b-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="4776b-120">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4776b-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4776b-121">Anger tids gräns för TCP-timeout i minuter för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4776b-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="4776b-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4776b-122">-InformationAction</span></span>
<span data-ttu-id="4776b-123">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4776b-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4776b-124">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4776b-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4776b-125">Vidare</span><span class="sxs-lookup"><span data-stu-id="4776b-125">Continue</span></span>
- <span data-ttu-id="4776b-126">Över</span><span class="sxs-lookup"><span data-stu-id="4776b-126">Ignore</span></span>
- <span data-ttu-id="4776b-127">Inquire</span><span class="sxs-lookup"><span data-stu-id="4776b-127">Inquire</span></span>
- <span data-ttu-id="4776b-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4776b-128">SilentlyContinue</span></span>
- <span data-ttu-id="4776b-129">Stanna</span><span class="sxs-lookup"><span data-stu-id="4776b-129">Stop</span></span>
- <span data-ttu-id="4776b-130">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4776b-130">Suspend</span></span>

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

### <span data-ttu-id="4776b-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4776b-131">-InformationVariable</span></span>
<span data-ttu-id="4776b-132">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4776b-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4776b-133">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="4776b-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="4776b-134">Anger namnet på intern belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="4776b-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="4776b-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="4776b-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="4776b-136">Anger algoritm för belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="4776b-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="4776b-137">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4776b-137">Valid values are:</span></span> 

- <span data-ttu-id="4776b-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="4776b-138">sourceIP.</span></span>
<span data-ttu-id="4776b-139">Dubbel tupel: käll-IP, mål-IP</span><span class="sxs-lookup"><span data-stu-id="4776b-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="4776b-140">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="4776b-140">sourceIPProtocol.</span></span>
<span data-ttu-id="4776b-141">En par med tre tupler: käll-IP, mål-IP, protokoll</span><span class="sxs-lookup"><span data-stu-id="4776b-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="4776b-142">ingen.</span><span class="sxs-lookup"><span data-stu-id="4776b-142">none.</span></span>
<span data-ttu-id="4776b-143">En fem tuple tillhörighet: käll-IP, källport, mål-IP, målport, protokoll</span><span class="sxs-lookup"><span data-stu-id="4776b-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="4776b-144">Standardvärdet är inget.</span><span class="sxs-lookup"><span data-stu-id="4776b-144">The default value is none.</span></span>

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

### <span data-ttu-id="4776b-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="4776b-145">-LocalPort</span></span>
<span data-ttu-id="4776b-146">Anger den lokala, privata, porten som används av slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4776b-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="4776b-147">Program inom den virtuella datorn lyssnar på den här porten för begär Anden om tjänstens indata för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4776b-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4776b-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="4776b-148">-Name</span></span>
<span data-ttu-id="4776b-149">Anger namnet på slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4776b-149">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4776b-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="4776b-150">-Profile</span></span>
<span data-ttu-id="4776b-151">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4776b-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4776b-152">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4776b-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4776b-153">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4776b-153">-Protocol</span></span>
<span data-ttu-id="4776b-154">Anger slut punktens protokoll.</span><span class="sxs-lookup"><span data-stu-id="4776b-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="4776b-155">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="4776b-155">Valid values are:</span></span> 

- <span data-ttu-id="4776b-156">TCP</span><span class="sxs-lookup"><span data-stu-id="4776b-156">tcp</span></span> 
- <span data-ttu-id="4776b-157">UDP</span><span class="sxs-lookup"><span data-stu-id="4776b-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4776b-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="4776b-158">-PublicPort</span></span>
<span data-ttu-id="4776b-159">Anger den offentliga port som slut punkten använder.</span><span class="sxs-lookup"><span data-stu-id="4776b-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="4776b-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="4776b-160">-VirtualIPName</span></span>
<span data-ttu-id="4776b-161">Anger namnet på en virtuell IP-adress som Azure associeras med till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="4776b-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="4776b-162">Din tjänst kan ha flera virtuella IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="4776b-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="4776b-163">Använd cmdleten **Add-AzureVirtualIP** för att skapa virtuella IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="4776b-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="4776b-164">-VM</span><span class="sxs-lookup"><span data-stu-id="4776b-164">-VM</span></span>
<span data-ttu-id="4776b-165">Anger den virtuella dator där slut punkten hör.</span><span class="sxs-lookup"><span data-stu-id="4776b-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4776b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4776b-166">CommonParameters</span></span>
<span data-ttu-id="4776b-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4776b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4776b-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4776b-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4776b-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4776b-169">INPUTS</span></span>

## <span data-ttu-id="4776b-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4776b-170">OUTPUTS</span></span>

### <span data-ttu-id="4776b-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="4776b-171">System.Object</span></span>

## <span data-ttu-id="4776b-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4776b-172">NOTES</span></span>

## <span data-ttu-id="4776b-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4776b-173">RELATED LINKS</span></span>

[<span data-ttu-id="4776b-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4776b-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="4776b-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="4776b-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="4776b-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4776b-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="4776b-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4776b-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="4776b-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="4776b-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="4776b-179">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4776b-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


