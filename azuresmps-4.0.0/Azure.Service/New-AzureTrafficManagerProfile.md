---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099432"
---
# <span data-ttu-id="b61ae-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b61ae-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="b61ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b61ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b61ae-103">Skapar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="b61ae-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="b61ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b61ae-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b61ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b61ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b61ae-106">Cmdleten **New-AzureTrafficManagerProfile** skapar en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="b61ae-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b61ae-107">När du har skapat en profil där du ställer in *LoadBalancingMethod* -värdet till "failover" kan du bestämma failover-ordningen för de slut punkter som du lägger till i din profil med Add-AzureTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b61ae-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="b61ae-108">Mer information finns i exempel 2 nedan.</span><span class="sxs-lookup"><span data-stu-id="b61ae-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="b61ae-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b61ae-109">EXAMPLES</span></span>

### <span data-ttu-id="b61ae-110">Exempel 1: skapa en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="b61ae-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="b61ae-111">Det här kommandot skapar en Traffic Manager-profil med namnet min profil i den angivna Traffic Manager-domänen med en Round Robin-metod, ett TTL-värde på 30 sekunder, HTTP Monitoring Protocol, övervaknings port 80 och med den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="b61ae-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="b61ae-112">Exempel 2: ändra ordning på slut punkter till önskad redundansväxling</span><span class="sxs-lookup"><span data-stu-id="b61ae-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="b61ae-113">I det här exemplet ordnas de slut punkter som läggs till i min profil i den önskade failover-ordningen.</span><span class="sxs-lookup"><span data-stu-id="b61ae-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="b61ae-114">Det första kommandot får Traffic Manager-Profile-objektet som heter min profil och lagrar objektet i $Profile variabel.</span><span class="sxs-lookup"><span data-stu-id="b61ae-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="b61ae-115">Det andra kommandot ändrar änd punkterna från matrisen slut punkter till den ordning som redundans ska utföras.</span><span class="sxs-lookup"><span data-stu-id="b61ae-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="b61ae-116">Det senaste kommandot uppdaterar Traffic Manager-profilen som lagras i $Profile med den nya slut punkts ordningen.</span><span class="sxs-lookup"><span data-stu-id="b61ae-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="b61ae-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b61ae-117">PARAMETERS</span></span>

### <span data-ttu-id="b61ae-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="b61ae-118">-DomainName</span></span>
<span data-ttu-id="b61ae-119">Anger domän namnet för Traffic Manager-profilen.</span><span class="sxs-lookup"><span data-stu-id="b61ae-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="b61ae-120">Det måste vara en under domän till trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="b61ae-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="b61ae-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="b61ae-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="b61ae-122">Anger den metod för belastnings utjämning som ska användas för att distribuera anslutningen.</span><span class="sxs-lookup"><span data-stu-id="b61ae-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="b61ae-123">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b61ae-123">Valid values are:</span></span> 

- <span data-ttu-id="b61ae-124">Prestandaräknare</span><span class="sxs-lookup"><span data-stu-id="b61ae-124">Performance</span></span>
- <span data-ttu-id="b61ae-125">Återställning</span><span class="sxs-lookup"><span data-stu-id="b61ae-125">Failover</span></span>
- <span data-ttu-id="b61ae-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="b61ae-126">RoundRobin</span></span>

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

### <span data-ttu-id="b61ae-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="b61ae-127">-MonitorPort</span></span>
<span data-ttu-id="b61ae-128">Anger vilken port som används för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="b61ae-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="b61ae-129">Giltiga värden är heltal som är större än 0 och mindre än eller lika med 65 535.</span><span class="sxs-lookup"><span data-stu-id="b61ae-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61ae-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="b61ae-130">-MonitorProtocol</span></span>
<span data-ttu-id="b61ae-131">Anger vilket protokoll som ska användas för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="b61ae-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="b61ae-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="b61ae-132">Valid values are:</span></span> 

- <span data-ttu-id="b61ae-133">Inkommande</span><span class="sxs-lookup"><span data-stu-id="b61ae-133">Http</span></span>

- <span data-ttu-id="b61ae-134">Https</span><span class="sxs-lookup"><span data-stu-id="b61ae-134">Https</span></span>

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

### <span data-ttu-id="b61ae-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="b61ae-135">-MonitorRelativePath</span></span>
<span data-ttu-id="b61ae-136">Anger sökvägen i förhållande till slut punktens domän namn till Avsök för hälso tillstånd.</span><span class="sxs-lookup"><span data-stu-id="b61ae-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="b61ae-137">Sökvägen måste uppfylla följande begränsningar:</span><span class="sxs-lookup"><span data-stu-id="b61ae-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="b61ae-138">Sökvägen måste vara mellan 1 och 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="b61ae-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="b61ae-139">Det måste börja med ett snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="b61ae-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="b61ae-140">Det får inte innehålla XML-element, \<\> .</span><span class="sxs-lookup"><span data-stu-id="b61ae-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="b61ae-141">Det får inte innehålla dubbla snedstreck,//.</span><span class="sxs-lookup"><span data-stu-id="b61ae-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="b61ae-142">Det får inte innehålla några ogiltiga HTML-escape-tecken.</span><span class="sxs-lookup"><span data-stu-id="b61ae-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="b61ae-143">Till exempel% XY.</span><span class="sxs-lookup"><span data-stu-id="b61ae-143">For example, %XY.</span></span>

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

### <span data-ttu-id="b61ae-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="b61ae-144">-Name</span></span>
<span data-ttu-id="b61ae-145">Anger namnet på den Traffic Manager-profil som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b61ae-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b61ae-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="b61ae-146">-Profile</span></span>
<span data-ttu-id="b61ae-147">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b61ae-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b61ae-148">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b61ae-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b61ae-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="b61ae-149">-Ttl</span></span>
<span data-ttu-id="b61ae-150">Anger det TTL-värde (Time to Live) för DNS som informerar den lokala DNS-matcharen hur länge DNS-posterna ska cachelagras.</span><span class="sxs-lookup"><span data-stu-id="b61ae-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="b61ae-151">Giltiga värden är heltal mellan 30 och 999 999.</span><span class="sxs-lookup"><span data-stu-id="b61ae-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b61ae-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61ae-152">CommonParameters</span></span>
<span data-ttu-id="b61ae-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61ae-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61ae-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61ae-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61ae-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b61ae-155">INPUTS</span></span>

## <span data-ttu-id="b61ae-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b61ae-156">OUTPUTS</span></span>

### <span data-ttu-id="b61ae-157">Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="b61ae-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="b61ae-158">Denna cmdlet skapar ett profil objekt för Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="b61ae-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="b61ae-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b61ae-159">NOTES</span></span>

## <span data-ttu-id="b61ae-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b61ae-160">RELATED LINKS</span></span>

[<span data-ttu-id="b61ae-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b61ae-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b61ae-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b61ae-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b61ae-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b61ae-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b61ae-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b61ae-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b61ae-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b61ae-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


