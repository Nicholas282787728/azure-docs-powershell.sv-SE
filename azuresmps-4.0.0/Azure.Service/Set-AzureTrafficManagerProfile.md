---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099024"
---
# <span data-ttu-id="45d72-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="45d72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45d72-102">SYNOPSIS</span></span>
<span data-ttu-id="45d72-103">Uppdaterar egenskaperna för en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="45d72-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="45d72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45d72-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="45d72-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45d72-105">DESCRIPTION</span></span>
<span data-ttu-id="45d72-106">Cmdleten **set-AzureTrafficManagerProfile** uppdaterar egenskaperna för en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="45d72-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="45d72-107">För profiler för vilka du har angett *LoadBalancingMethod* -värdet till "failover" kan du bestämma växlings ordningen för slut punkter som du har lagt till i din profil med Add-AzureTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45d72-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="45d72-108">Mer information finns i exempel 3 nedan.</span><span class="sxs-lookup"><span data-stu-id="45d72-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="45d72-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45d72-109">EXAMPLES</span></span>

### <span data-ttu-id="45d72-110">Exempel 1: ange TTL för en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="45d72-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="45d72-111">Det här kommandot anger TTL till 60 sekunder för Traffic Manager-MyTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="45d72-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="45d72-112">Exempel 2: ange flera värden för en profil</span><span class="sxs-lookup"><span data-stu-id="45d72-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="45d72-113">Det här kommandot får en Traffic Manager-profil med namnet min profil med cmdleten **Get-AzureTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="45d72-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="45d72-114">Profilen använder belastnings Utjämnings metoden RoundRobin, ett TTL-värde på 30 sekunder, Monitor Protocol HTTP, Monitor port och den relativa sökvägen för en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="45d72-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="45d72-115">Exempel 3: ändra ordning på slut punkter till önskad redundansväxling</span><span class="sxs-lookup"><span data-stu-id="45d72-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="45d72-116">I det här exemplet ordnas de slut punkter som läggs till i min profil i den önskade failover-ordningen.</span><span class="sxs-lookup"><span data-stu-id="45d72-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="45d72-117">Det första kommandot får Traffic Manager-Profile-objektet som heter min profil och lagrar objektet i $Profile variabel.</span><span class="sxs-lookup"><span data-stu-id="45d72-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="45d72-118">Det andra kommandot ändrar änd punkterna från matrisen slut punkter till den ordning som redundans ska utföras.</span><span class="sxs-lookup"><span data-stu-id="45d72-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="45d72-119">Det senaste kommandot uppdaterar Traffic Manager-profilen som lagras i $Profile med den nya slut punkts ordningen.</span><span class="sxs-lookup"><span data-stu-id="45d72-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="45d72-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45d72-120">PARAMETERS</span></span>

### <span data-ttu-id="45d72-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="45d72-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="45d72-122">Anger den metod för belastnings utjämning som ska användas för att distribuera anslutningen.</span><span class="sxs-lookup"><span data-stu-id="45d72-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="45d72-123">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="45d72-123">Valid values are:</span></span> 

- <span data-ttu-id="45d72-124">Prestandaräknare</span><span class="sxs-lookup"><span data-stu-id="45d72-124">Performance</span></span>
- <span data-ttu-id="45d72-125">Återställning</span><span class="sxs-lookup"><span data-stu-id="45d72-125">Failover</span></span>
- <span data-ttu-id="45d72-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="45d72-126">RoundRobin</span></span>

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

### <span data-ttu-id="45d72-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="45d72-127">-MonitorPort</span></span>
<span data-ttu-id="45d72-128">Anger vilken port som används för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="45d72-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="45d72-129">Giltiga värden är heltal som är större än 0 och mindre än eller lika med 65 535.</span><span class="sxs-lookup"><span data-stu-id="45d72-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="45d72-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="45d72-130">-MonitorProtocol</span></span>
<span data-ttu-id="45d72-131">Anger vilket protokoll som ska användas för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="45d72-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="45d72-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="45d72-132">Valid values are:</span></span> 

- <span data-ttu-id="45d72-133">Inkommande</span><span class="sxs-lookup"><span data-stu-id="45d72-133">Http</span></span>
- <span data-ttu-id="45d72-134">Https</span><span class="sxs-lookup"><span data-stu-id="45d72-134">Https</span></span>

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

### <span data-ttu-id="45d72-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="45d72-135">-MonitorRelativePath</span></span>
<span data-ttu-id="45d72-136">Anger sökvägen i förhållande till slut punktens domän namn till Avsök för hälso tillstånd.</span><span class="sxs-lookup"><span data-stu-id="45d72-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="45d72-137">Sökvägen måste uppfylla följande begränsningar:</span><span class="sxs-lookup"><span data-stu-id="45d72-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="45d72-138">Sökvägen måste vara mellan 1 och 1000 tecken.</span><span class="sxs-lookup"><span data-stu-id="45d72-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="45d72-139">Det måste börja med ett snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="45d72-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="45d72-140">Det får inte innehålla XML-element, \<\> .</span><span class="sxs-lookup"><span data-stu-id="45d72-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="45d72-141">Det får inte innehålla dubbla snedstreck,//.</span><span class="sxs-lookup"><span data-stu-id="45d72-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="45d72-142">Det får inte innehålla några ogiltiga HTML-escape-tecken.</span><span class="sxs-lookup"><span data-stu-id="45d72-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="45d72-143">Till exempel% XY.</span><span class="sxs-lookup"><span data-stu-id="45d72-143">For example, %XY.</span></span>

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

### <span data-ttu-id="45d72-144">-Namn</span><span class="sxs-lookup"><span data-stu-id="45d72-144">-Name</span></span>
<span data-ttu-id="45d72-145">Anger namnet på den Traffic Manager-profil som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="45d72-145">Specifies the name of the Traffic Manager profile to update.</span></span>

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

### <span data-ttu-id="45d72-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="45d72-146">-Profile</span></span>
<span data-ttu-id="45d72-147">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="45d72-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="45d72-148">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="45d72-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="45d72-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="45d72-150">Anger den Traffic Manager-profil som du använder för att ange profilen.</span><span class="sxs-lookup"><span data-stu-id="45d72-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45d72-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="45d72-151">-Ttl</span></span>
<span data-ttu-id="45d72-152">Anger det TTL-värde (Time to Live) för DNS som informerar den lokala DNS-matcharen hur länge DNS-posterna ska cachelagras.</span><span class="sxs-lookup"><span data-stu-id="45d72-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="45d72-153">Giltiga värden är ett heltal mellan 30 och 999 999.</span><span class="sxs-lookup"><span data-stu-id="45d72-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="45d72-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d72-154">CommonParameters</span></span>
<span data-ttu-id="45d72-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d72-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d72-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d72-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d72-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45d72-157">INPUTS</span></span>

## <span data-ttu-id="45d72-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45d72-158">OUTPUTS</span></span>

### <span data-ttu-id="45d72-159">Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="45d72-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="45d72-160">Denna cmdlet skapar ett profil objekt för Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="45d72-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="45d72-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45d72-161">NOTES</span></span>

## <span data-ttu-id="45d72-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45d72-162">RELATED LINKS</span></span>

[<span data-ttu-id="45d72-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="45d72-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="45d72-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="45d72-166">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="45d72-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="45d72-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


