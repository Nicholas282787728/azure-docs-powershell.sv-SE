---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259748"
---
# <span data-ttu-id="1e6c9-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="1e6c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6c9-103">Skapar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="1e6c9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e6c9-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e6c9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="1e6c9-106">Cmdleten **New-AzTrafficManagerProfile** skapar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1e6c9-107">Ange parametern *Name* och nödvändiga inställningar.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="1e6c9-108">Denna cmdlet returnerar ett lokalt objekt som representerar den nya profilen.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="1e6c9-109">Denna cmdlet konfigurerar inte slut punkter för Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="1e6c9-110">Du kan uppdatera det lokala profil objektet med hjälp av Add-AzTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="1e6c9-111">Överför sedan ändringar till Traffic Manager med hjälp av Set-AzTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="1e6c9-112">Du kan också lägga till slut punkter med New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="1e6c9-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e6c9-113">EXAMPLES</span></span>

### <span data-ttu-id="1e6c9-114">Exempel 1: skapa en profil</span><span class="sxs-lookup"><span data-stu-id="1e6c9-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="1e6c9-115">Det här kommandot skapar en Azure Traffic Manager-profil med namnet ContosoProfile i resurs grupp ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="1e6c9-116">DNS FQDN är contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="1e6c9-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e6c9-117">PARAMETERS</span></span>

### <span data-ttu-id="1e6c9-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="1e6c9-118">-CustomHeader</span></span>
<span data-ttu-id="1e6c9-119">Lista över anpassade rubrik namn och värdepar för avsöknings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-120">-DefaultProfile</span></span>
<span data-ttu-id="1e6c9-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="1e6c9-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="1e6c9-123">Lista över förväntade HTTP-statuskod för avsöknings begär Anden.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="1e6c9-124">-MaxReturn</span></span>
<span data-ttu-id="1e6c9-125">Maximalt antal svar som returneras för profiler med en routningsmetod med flera värden.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1e6c9-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="1e6c9-127">Intervallet (i sekunder) som trafik hanteraren kontrollerar tillståndet för varje slut punkt i den här profilen.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="1e6c9-128">Standardvärdet är 30.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="1e6c9-129">-MonitorPath</span></span>
<span data-ttu-id="1e6c9-130">Anger sökvägen som används för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="1e6c9-131">Ange ett värde relativt till slut punkts domän namnet.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="1e6c9-132">Värdet måste börja med ett snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="1e6c9-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="1e6c9-133">-MonitorPort</span></span>
<span data-ttu-id="1e6c9-134">Anger den TCP-port som används för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="1e6c9-135">Giltiga värden är heltal från 1 till 65535.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="1e6c9-136">-MonitorProtocol</span></span>
<span data-ttu-id="1e6c9-137">Anger vilket protokoll som ska användas för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="1e6c9-138">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1e6c9-138">Valid values are:</span></span>

- <span data-ttu-id="1e6c9-139">INKOMMANDE</span><span class="sxs-lookup"><span data-stu-id="1e6c9-139">HTTP</span></span>
- <span data-ttu-id="1e6c9-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="1e6c9-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1e6c9-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="1e6c9-142">Den tid (i sekunder) som trafik hanteraren tillåter slut punkter i den här profilen för att svara på hälso kontrollen.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="1e6c9-143">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="1e6c9-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="1e6c9-145">Antalet misslyckade hälso kontroller på flera nivåer i trafik hanteraren innan en slut punkt i den här profilen deklareras efter nästa misslyckade hälso kontroll.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="1e6c9-146">Standardvärdet är 3.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-147">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e6c9-147">-Name</span></span>
<span data-ttu-id="1e6c9-148">Anger ett namn för Traffic Manager-profilen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="1e6c9-149">-ProfileStatus</span></span>
<span data-ttu-id="1e6c9-150">Anger statusen för profilen.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="1e6c9-151">Giltiga värden är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="1e6c9-152">-RelativeDnsName</span></span>
<span data-ttu-id="1e6c9-153">Anger det relativa DNS-namnet som den här Traffic Manager-profilen ger.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="1e6c9-154">Traffic Manager kombinerar det här värdet och det DNS-domännamn som Azure Traffic Manager använder för att skapa det fullständigt kvalificerade domän namnet (FQDN) för profilen.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6c9-155">-ResourceGroupName</span></span>
<span data-ttu-id="1e6c9-156">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1e6c9-157">Den här cmdleten skapar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-158">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1e6c9-158">-Tag</span></span>
<span data-ttu-id="1e6c9-159">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="1e6c9-160">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="1e6c9-160">For example:</span></span>

<span data-ttu-id="1e6c9-161">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="1e6c9-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="1e6c9-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="1e6c9-163">Anger metoden för trafik cirkulation.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="1e6c9-164">Den här metoden avgör vilken slut punkts Traffic Manager returnerar som svar på inkommande DNS-frågor.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="1e6c9-165">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="1e6c9-165">Valid values are:</span></span>

- <span data-ttu-id="1e6c9-166">Prestandaräknare</span><span class="sxs-lookup"><span data-stu-id="1e6c9-166">Performance</span></span>
- <span data-ttu-id="1e6c9-167">Viktat</span><span class="sxs-lookup"><span data-stu-id="1e6c9-167">Weighted</span></span>
- <span data-ttu-id="1e6c9-168">Ordningen</span><span class="sxs-lookup"><span data-stu-id="1e6c9-168">Priority</span></span>
- <span data-ttu-id="1e6c9-169">Visio</span><span class="sxs-lookup"><span data-stu-id="1e6c9-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="1e6c9-170">-Ttl</span></span>
<span data-ttu-id="1e6c9-171">Anger TTL-värdet (Time to Live) för DNS.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e6c9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e6c9-172">CommonParameters</span></span>
<span data-ttu-id="1e6c9-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e6c9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e6c9-174">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e6c9-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e6c9-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e6c9-175">INPUTS</span></span>

### <span data-ttu-id="1e6c9-176">Ingen</span><span class="sxs-lookup"><span data-stu-id="1e6c9-176">None</span></span>

## <span data-ttu-id="1e6c9-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e6c9-177">OUTPUTS</span></span>

### <span data-ttu-id="1e6c9-178">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1e6c9-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e6c9-179">NOTES</span></span>

## <span data-ttu-id="1e6c9-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e6c9-180">RELATED LINKS</span></span>

[<span data-ttu-id="1e6c9-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1e6c9-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="1e6c9-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="1e6c9-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="1e6c9-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1e6c9-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="1e6c9-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1e6c9-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


