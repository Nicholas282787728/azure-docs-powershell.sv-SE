---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093459"
---
# <span data-ttu-id="513f2-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="513f2-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="513f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="513f2-102">SYNOPSIS</span></span>
<span data-ttu-id="513f2-103">Lägger till en slut punkt till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="513f2-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="513f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="513f2-104">SYNTAX</span></span>

### <span data-ttu-id="513f2-105">NoLB (standard)</span><span class="sxs-lookup"><span data-stu-id="513f2-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="513f2-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="513f2-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="513f2-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="513f2-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="513f2-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="513f2-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="513f2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="513f2-109">DESCRIPTION</span></span>
<span data-ttu-id="513f2-110">Cmdleten **Add-AzureEndpoint** lägger till en slut punkt till ett objekt i Azure Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="513f2-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="513f2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="513f2-111">EXAMPLES</span></span>

### <span data-ttu-id="513f2-112">Exempel 1: lägga till en slut punkt</span><span class="sxs-lookup"><span data-stu-id="513f2-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="513f2-113">Det här kommandot hämtar konfigurationen för en virtuell dator med namnet VirtualMachine01 med hjälp av cmdleten **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="513f2-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="513f2-114">Kommandot skickar det till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="513f2-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="513f2-115">Denna cmdlet lägger till en slut punkt med namnet Httpin.</span><span class="sxs-lookup"><span data-stu-id="513f2-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="513f2-116">Slut punkten har en offentlig port 80 och lokal port 8080.</span><span class="sxs-lookup"><span data-stu-id="513f2-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="513f2-117">Kommandot skickar det virtuella datorobjektet till cmdleten **Update-AzureVM** som implementerar dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="513f2-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="513f2-118">Exempel 2: lägga till en slut punkt som tillhör en belastningsutjämnad grupp</span><span class="sxs-lookup"><span data-stu-id="513f2-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="513f2-119">Det här kommandot hämtar konfigurationen för en virtuell dator med namnet VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="513f2-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="513f2-120">Den aktuella cmdleten lägger till en slut punkt som heter Httpin.</span><span class="sxs-lookup"><span data-stu-id="513f2-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="513f2-121">Slut punkten har en offentlig port 80 och lokal port 8080.</span><span class="sxs-lookup"><span data-stu-id="513f2-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="513f2-122">Slut punkten tillhör den delade belastningsutjämnade gruppen webb grupp.</span><span class="sxs-lookup"><span data-stu-id="513f2-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="513f2-123">En HTTP PROBE på port 80 med sökvägen "/" övervakar slut punktens tillgänglighet.</span><span class="sxs-lookup"><span data-stu-id="513f2-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="513f2-124">Kommandot verkställer dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="513f2-124">The command implements your changes.</span></span>

### <span data-ttu-id="513f2-125">Exempel 3: koppla en virtuell IP-adress till en slut punkt</span><span class="sxs-lookup"><span data-stu-id="513f2-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="513f2-126">Det här kommandot hämtar konfigurationen för en virtuell dator med namnet VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="513f2-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="513f2-127">Den aktuella cmdleten lägger till en slut punkt som heter Httpin.</span><span class="sxs-lookup"><span data-stu-id="513f2-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="513f2-128">Slut punkten har en offentlig port 80 och lokal port 8080.</span><span class="sxs-lookup"><span data-stu-id="513f2-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="513f2-129">Det här kommandot associerar en virtuell IP-adress till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="513f2-130">Kommandot verkställer dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="513f2-130">The command implements your changes.</span></span>

## <span data-ttu-id="513f2-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="513f2-131">PARAMETERS</span></span>

### <span data-ttu-id="513f2-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="513f2-132">-ACL</span></span>
<span data-ttu-id="513f2-133">Anger en ACL-konfigurationsfil (Access Control List) för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="513f2-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="513f2-134">-DefaultProbe</span></span>
<span data-ttu-id="513f2-135">Anger att denna cmdlet använder standardinställningen för avsökning.</span><span class="sxs-lookup"><span data-stu-id="513f2-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="513f2-136">-DirectServerReturn</span></span>
<span data-ttu-id="513f2-137">Anger om denna cmdlet aktiverar direkt Server återgång.</span><span class="sxs-lookup"><span data-stu-id="513f2-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="513f2-138">Ange $True som ska aktive ras eller $False inaktivera.</span><span class="sxs-lookup"><span data-stu-id="513f2-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="513f2-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="513f2-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="513f2-140">Anger tids gräns för TCP-timeout i minuter för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="513f2-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="513f2-141">-InformationAction</span></span>
<span data-ttu-id="513f2-142">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="513f2-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="513f2-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="513f2-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="513f2-144">Vidare</span><span class="sxs-lookup"><span data-stu-id="513f2-144">Continue</span></span>
- <span data-ttu-id="513f2-145">Över</span><span class="sxs-lookup"><span data-stu-id="513f2-145">Ignore</span></span>
- <span data-ttu-id="513f2-146">Inquire</span><span class="sxs-lookup"><span data-stu-id="513f2-146">Inquire</span></span>
- <span data-ttu-id="513f2-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="513f2-147">SilentlyContinue</span></span>
- <span data-ttu-id="513f2-148">Stanna</span><span class="sxs-lookup"><span data-stu-id="513f2-148">Stop</span></span>
- <span data-ttu-id="513f2-149">Avbryt</span><span class="sxs-lookup"><span data-stu-id="513f2-149">Suspend</span></span>

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

### <span data-ttu-id="513f2-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="513f2-150">-InformationVariable</span></span>
<span data-ttu-id="513f2-151">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="513f2-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="513f2-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="513f2-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="513f2-153">Anger namnet på intern belastningsutjämnaren.</span><span class="sxs-lookup"><span data-stu-id="513f2-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="513f2-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="513f2-154">-LBSetName</span></span>
<span data-ttu-id="513f2-155">Anger namnet på den belastningsutjämnare som angetts för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="513f2-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="513f2-157">Anger algoritm för belastnings fördelning.</span><span class="sxs-lookup"><span data-stu-id="513f2-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="513f2-158">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="513f2-158">Valid values are:</span></span> 

- <span data-ttu-id="513f2-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="513f2-159">sourceIP.</span></span>
<span data-ttu-id="513f2-160">Dubbel tupel: käll-IP, mål-IP</span><span class="sxs-lookup"><span data-stu-id="513f2-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="513f2-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="513f2-161">sourceIPProtocol.</span></span>
<span data-ttu-id="513f2-162">En par med tre tupler: käll-IP, mål-IP, protokoll</span><span class="sxs-lookup"><span data-stu-id="513f2-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="513f2-163">ingen.</span><span class="sxs-lookup"><span data-stu-id="513f2-163">none.</span></span>
<span data-ttu-id="513f2-164">En fem tuple tillhörighet: käll-IP, källport, mål-IP, målport, protokoll</span><span class="sxs-lookup"><span data-stu-id="513f2-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="513f2-165">Standardvärdet är inget.</span><span class="sxs-lookup"><span data-stu-id="513f2-165">The default value is none.</span></span>

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

### <span data-ttu-id="513f2-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="513f2-166">-LocalPort</span></span>
<span data-ttu-id="513f2-167">Anger den lokala, privata, porten som används av slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="513f2-168">Program inom den virtuella datorn lyssnar på den här porten för begär Anden om tjänstens indata för den här slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-169">-Namn</span><span class="sxs-lookup"><span data-stu-id="513f2-169">-Name</span></span>
<span data-ttu-id="513f2-170">Anger ett namn för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-170">Specifies a name for the endpoint.</span></span>

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

### <span data-ttu-id="513f2-171">-Noprobe</span><span class="sxs-lookup"><span data-stu-id="513f2-171">-NoProbe</span></span>
<span data-ttu-id="513f2-172">Anger att denna cmdlet använder inställningen ingen avsökning.</span><span class="sxs-lookup"><span data-stu-id="513f2-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="513f2-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="513f2-174">Anger avsöknings intervall för avsökning i sekunder för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="513f2-175">-ProbePath</span></span>
<span data-ttu-id="513f2-176">Anger den relativa sökvägen till HTTP PROBE.</span><span class="sxs-lookup"><span data-stu-id="513f2-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="513f2-177">-ProbePort</span></span>
<span data-ttu-id="513f2-178">Anger vilken port som används för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="513f2-179">-ProbeProtocol</span></span>
<span data-ttu-id="513f2-180">Anger port protokoll.</span><span class="sxs-lookup"><span data-stu-id="513f2-180">Specifies the port protocol.</span></span>
<span data-ttu-id="513f2-181">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="513f2-181">Valid values are:</span></span> 

- <span data-ttu-id="513f2-182">TCP</span><span class="sxs-lookup"><span data-stu-id="513f2-182">tcp</span></span> 
- <span data-ttu-id="513f2-183">inkommande</span><span class="sxs-lookup"><span data-stu-id="513f2-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="513f2-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="513f2-185">Anger tids gräns för avsöknings perioden i sekunder.</span><span class="sxs-lookup"><span data-stu-id="513f2-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-186">-Profil</span><span class="sxs-lookup"><span data-stu-id="513f2-186">-Profile</span></span>
<span data-ttu-id="513f2-187">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="513f2-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="513f2-188">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="513f2-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="513f2-189">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="513f2-189">-Protocol</span></span>
<span data-ttu-id="513f2-190">Anger slut punktens protokoll.</span><span class="sxs-lookup"><span data-stu-id="513f2-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="513f2-191">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="513f2-191">Valid values are:</span></span> 

- <span data-ttu-id="513f2-192">TCP</span><span class="sxs-lookup"><span data-stu-id="513f2-192">tcp</span></span> 
- <span data-ttu-id="513f2-193">UDP</span><span class="sxs-lookup"><span data-stu-id="513f2-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="513f2-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="513f2-194">-PublicPort</span></span>
<span data-ttu-id="513f2-195">Anger den offentliga port som slut punkten använder.</span><span class="sxs-lookup"><span data-stu-id="513f2-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="513f2-196">Om du inte anger något värde tilldelar Azure en tillgänglig port.</span><span class="sxs-lookup"><span data-stu-id="513f2-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="513f2-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="513f2-197">-VirtualIPName</span></span>
<span data-ttu-id="513f2-198">Anger namnet på en virtuell IP-adress som Azure associeras med till slut punkten.</span><span class="sxs-lookup"><span data-stu-id="513f2-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="513f2-199">Din tjänst kan ha flera virtuella IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="513f2-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="513f2-200">Använd cmdleten **Add-AzureVirtualIP** för att skapa virtuella IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="513f2-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="513f2-201">-VM</span><span class="sxs-lookup"><span data-stu-id="513f2-201">-VM</span></span>
<span data-ttu-id="513f2-202">Anger den virtuella dator där slut punkten hör.</span><span class="sxs-lookup"><span data-stu-id="513f2-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="513f2-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513f2-203">CommonParameters</span></span>
<span data-ttu-id="513f2-204">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513f2-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513f2-205">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513f2-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513f2-206">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="513f2-206">INPUTS</span></span>

## <span data-ttu-id="513f2-207">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="513f2-207">OUTPUTS</span></span>

### <span data-ttu-id="513f2-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="513f2-208">System.Object</span></span>

## <span data-ttu-id="513f2-209">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="513f2-209">NOTES</span></span>

## <span data-ttu-id="513f2-210">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="513f2-210">RELATED LINKS</span></span>

[<span data-ttu-id="513f2-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="513f2-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="513f2-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="513f2-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="513f2-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="513f2-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="513f2-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="513f2-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="513f2-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="513f2-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="513f2-216">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="513f2-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


