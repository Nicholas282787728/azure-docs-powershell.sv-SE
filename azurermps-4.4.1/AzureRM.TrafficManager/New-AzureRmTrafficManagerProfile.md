---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 8b88ee761ab9ee136777fb29e7726a2f72110553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757978"
---
# <span data-ttu-id="e7a85-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="e7a85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7a85-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a85-103">Skapar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="e7a85-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7a85-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7a85-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7a85-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a85-106">Cmdleten **New-AzureRmTrafficManagerProfile** skapar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="e7a85-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="e7a85-107">Ange parametern *Name* och nödvändiga inställningar.</span><span class="sxs-lookup"><span data-stu-id="e7a85-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="e7a85-108">Denna cmdlet returnerar ett lokalt objekt som representerar den nya profilen.</span><span class="sxs-lookup"><span data-stu-id="e7a85-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="e7a85-109">Denna cmdlet konfigurerar inte slut punkter för Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="e7a85-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="e7a85-110">Du kan uppdatera det lokala profil objektet med hjälp av Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a85-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="e7a85-111">Överför sedan ändringar till Traffic Manager med hjälp av Set-AzureRmTrafficManagerProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a85-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="e7a85-112">Du kan också lägga till slut punkter med New-AzureRmTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a85-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e7a85-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7a85-113">EXAMPLES</span></span>

### <span data-ttu-id="e7a85-114">Exempel 1: skapa en profil</span><span class="sxs-lookup"><span data-stu-id="e7a85-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="e7a85-115">Det här kommandot skapar en Azure Traffic Manager-profil med namnet ContosoProfile i resurs grupp ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e7a85-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="e7a85-116">DNS FQDN är contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="e7a85-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="e7a85-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7a85-117">PARAMETERS</span></span>

### <span data-ttu-id="e7a85-118">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e7a85-118">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="e7a85-119">Intervallet (i sekunder) som trafik hanteraren kontrollerar tillståndet för varje slut punkt i den här profilen.</span><span class="sxs-lookup"><span data-stu-id="e7a85-119">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="e7a85-120">Standardvärdet är 30.</span><span class="sxs-lookup"><span data-stu-id="e7a85-120">The default is 30.</span></span>

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

### <span data-ttu-id="e7a85-121">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="e7a85-121">-MonitorPath</span></span>
<span data-ttu-id="e7a85-122">Anger sökvägen som används för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="e7a85-122">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="e7a85-123">Ange ett värde relativt till slut punkts domän namnet.</span><span class="sxs-lookup"><span data-stu-id="e7a85-123">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="e7a85-124">Värdet måste börja med ett snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="e7a85-124">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="e7a85-125">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="e7a85-125">-MonitorPort</span></span>
<span data-ttu-id="e7a85-126">Anger den TCP-port som används för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="e7a85-126">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="e7a85-127">Giltiga värden är heltal från 1 till 65535.</span><span class="sxs-lookup"><span data-stu-id="e7a85-127">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="e7a85-128">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="e7a85-128">-MonitorProtocol</span></span>
<span data-ttu-id="e7a85-129">Anger vilket protokoll som ska användas för att övervaka slut punktens status.</span><span class="sxs-lookup"><span data-stu-id="e7a85-129">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="e7a85-130">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e7a85-130">Valid values are:</span></span>

- <span data-ttu-id="e7a85-131">INKOMMANDE</span><span class="sxs-lookup"><span data-stu-id="e7a85-131">HTTP</span></span>
- <span data-ttu-id="e7a85-132">HTTPS</span><span class="sxs-lookup"><span data-stu-id="e7a85-132">HTTPS</span></span>

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

### <span data-ttu-id="e7a85-133">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="e7a85-133">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="e7a85-134">Den tid (i sekunder) som trafik hanteraren tillåter slut punkter i den här profilen för att svara på hälso kontrollen.</span><span class="sxs-lookup"><span data-stu-id="e7a85-134">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="e7a85-135">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="e7a85-135">The default is 10.</span></span>

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

### <span data-ttu-id="e7a85-136">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="e7a85-136">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="e7a85-137">Antalet misslyckade hälso kontroller på flera nivåer i trafik hanteraren innan en slut punkt i den här profilen deklareras efter nästa misslyckade hälso kontroll.</span><span class="sxs-lookup"><span data-stu-id="e7a85-137">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="e7a85-138">Standardvärdet är 3.</span><span class="sxs-lookup"><span data-stu-id="e7a85-138">The default is 3.</span></span>

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

### <span data-ttu-id="e7a85-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7a85-139">-Name</span></span>
<span data-ttu-id="e7a85-140">Anger ett namn för Traffic Manager-profilen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="e7a85-140">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e7a85-141">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="e7a85-141">-ProfileStatus</span></span>
<span data-ttu-id="e7a85-142">Anger statusen för profilen.</span><span class="sxs-lookup"><span data-stu-id="e7a85-142">Specifies the status of the profile.</span></span>
<span data-ttu-id="e7a85-143">Giltiga värden är: Enabled och disabled.</span><span class="sxs-lookup"><span data-stu-id="e7a85-143">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="e7a85-144">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="e7a85-144">-RelativeDnsName</span></span>
<span data-ttu-id="e7a85-145">Anger det relativa DNS-namnet som den här Traffic Manager-profilen ger.</span><span class="sxs-lookup"><span data-stu-id="e7a85-145">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="e7a85-146">Traffic Manager kombinerar det här värdet och det DNS-domännamn som Azure Traffic Manager använder för att skapa det fullständigt kvalificerade domän namnet (FQDN) för profilen.</span><span class="sxs-lookup"><span data-stu-id="e7a85-146">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="e7a85-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a85-147">-ResourceGroupName</span></span>
<span data-ttu-id="e7a85-148">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e7a85-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e7a85-149">Den här cmdleten skapar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e7a85-149">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e7a85-150">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e7a85-150">-Tag</span></span>
<span data-ttu-id="e7a85-151">Par med nyckelord i en hash-tabell som taggar på servern.</span><span class="sxs-lookup"><span data-stu-id="e7a85-151">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="e7a85-152">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="e7a85-152">For example:</span></span>

<span data-ttu-id="e7a85-153">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="e7a85-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e7a85-154">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="e7a85-154">-TrafficRoutingMethod</span></span>
<span data-ttu-id="e7a85-155">Anger metoden för trafik cirkulation.</span><span class="sxs-lookup"><span data-stu-id="e7a85-155">Specifies the traffic routing method.</span></span>
<span data-ttu-id="e7a85-156">Den här metoden avgör vilken slut punkts Traffic Manager returnerar som svar på inkommande DNS-frågor.</span><span class="sxs-lookup"><span data-stu-id="e7a85-156">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="e7a85-157">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="e7a85-157">Valid values are:</span></span>

- <span data-ttu-id="e7a85-158">Prestandaräknare</span><span class="sxs-lookup"><span data-stu-id="e7a85-158">Performance</span></span>
- <span data-ttu-id="e7a85-159">Viktat</span><span class="sxs-lookup"><span data-stu-id="e7a85-159">Weighted</span></span>
- <span data-ttu-id="e7a85-160">Ordningen</span><span class="sxs-lookup"><span data-stu-id="e7a85-160">Priority</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a85-161">-TTL</span><span class="sxs-lookup"><span data-stu-id="e7a85-161">-Ttl</span></span>
<span data-ttu-id="e7a85-162">Anger TTL-värdet (Time to Live) för DNS.</span><span class="sxs-lookup"><span data-stu-id="e7a85-162">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="e7a85-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-163">-DefaultProfile</span></span>
<span data-ttu-id="e7a85-164">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a85-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a85-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a85-165">CommonParameters</span></span>
<span data-ttu-id="e7a85-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a85-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a85-167">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a85-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a85-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7a85-168">INPUTS</span></span>

## <span data-ttu-id="e7a85-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7a85-169">OUTPUTS</span></span>

### <span data-ttu-id="e7a85-170">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-170">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="e7a85-171">Denna cmdlet returnerar ett nytt TrafficManagerProfile-objekt.</span><span class="sxs-lookup"><span data-stu-id="e7a85-171">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="e7a85-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7a85-172">NOTES</span></span>

## <span data-ttu-id="e7a85-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7a85-173">RELATED LINKS</span></span>

[<span data-ttu-id="e7a85-174">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="e7a85-174">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="e7a85-175">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-175">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e7a85-176">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-176">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e7a85-177">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-177">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e7a85-178">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-178">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="e7a85-179">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e7a85-179">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


