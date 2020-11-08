---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099606"
---
# <span data-ttu-id="6a3cc-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a3cc-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="6a3cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a3cc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3cc-103">Lägger till en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="6a3cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a3cc-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a3cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a3cc-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3cc-106">Cmdleten **Add-AzureTrafficManagerEndpoint** lägger till en slut punkt till en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6a3cc-107">När du har lagt till en slut punkt skickar du resultatet till cmdleten **set-AzureTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6a3cc-108">Denna cmdlet ansluter till Azure för att spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="6a3cc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a3cc-109">EXAMPLES</span></span>

### <span data-ttu-id="6a3cc-110">Exempel 1: lägga till en slut punkt för en profil</span><span class="sxs-lookup"><span data-stu-id="6a3cc-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="6a3cc-111">Det första kommandot använder cmdleten **Get-AzureTrafficManagerProfile** för att hämta profilen med namnet ContosoProfile och lagrar den sedan i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="6a3cc-112">Det andra kommandot lägger till en slut punkt till Traffic Manager-profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6a3cc-113">Slut punkten har domän namnet Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="6a3cc-114">Kommandot anger också om den är aktive rad och dess typ.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="6a3cc-115">Kommandot skickar Profile-objektet till cmdleten **set-AzureTrafficManagerProfile** för att ansluta till Azure för att spara ändringarna.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="6a3cc-116">Exempel 2: lägga till en slut punkt med en angiven plats och vikt</span><span class="sxs-lookup"><span data-stu-id="6a3cc-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="6a3cc-117">Det här kommandot lägger till en slut punkt till en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="6a3cc-118">Slut punkten har domän namnet Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="6a3cc-119">Kommandot anger också om den är aktive rad och dess typ.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="6a3cc-120">Kommandot anger också tjocklek och plats för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="6a3cc-121">Kommandot skickar profil objekt till **set-AzureTrafficManagerProfile** för att kunna spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="6a3cc-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a3cc-122">PARAMETERS</span></span>

### <span data-ttu-id="6a3cc-123">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="6a3cc-123">-DomainName</span></span>
<span data-ttu-id="6a3cc-124">Anger domän namnet för slut punkten som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="6a3cc-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="6a3cc-125">-Location</span></span>
<span data-ttu-id="6a3cc-126">Anger platsen för slut punkten som cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="6a3cc-127">Det måste vara en Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-127">This must be an Azure location.</span></span>

<span data-ttu-id="6a3cc-128">Den här parametern måste innehålla ett värde för slut punkter av typen "any" eller av typen "TrafficManager" i en profil som har metod för belastnings utjämning angiven till "prestanda".</span><span class="sxs-lookup"><span data-stu-id="6a3cc-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="6a3cc-129">De möjliga värdena är namnen på Azure-regionen, som finns på https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="6a3cc-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="6a3cc-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="6a3cc-130">-MinChildEndpoints</span></span>
<span data-ttu-id="6a3cc-131">Anger det minsta antalet slut punkter som den kapslade profilen måste ha för att den här slut punkten ska kunna anses vara online.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="6a3cc-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a3cc-132">-Profile</span></span>
<span data-ttu-id="6a3cc-133">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6a3cc-134">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a3cc-135">-Status</span><span class="sxs-lookup"><span data-stu-id="6a3cc-135">-Status</span></span>
<span data-ttu-id="6a3cc-136">Anger statusen för övervaknings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="6a3cc-137">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="6a3cc-137">Valid values are:</span></span> 

- <span data-ttu-id="6a3cc-138">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="6a3cc-138">Enabled</span></span>
- <span data-ttu-id="6a3cc-139">Aktiv</span><span class="sxs-lookup"><span data-stu-id="6a3cc-139">Disabled</span></span>

<span data-ttu-id="6a3cc-140">Om du anger ett värde för aktive rad övervakar trafik hanteraren slut punkten och belastnings Utjämnings metoden när trafiken hanteras.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="6a3cc-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a3cc-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="6a3cc-142">Anger den Traffic Manager-profil som du vill lägga till slut punkten för.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="6a3cc-143">– Skriv</span><span class="sxs-lookup"><span data-stu-id="6a3cc-143">-Type</span></span>
<span data-ttu-id="6a3cc-144">Anger typen av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="6a3cc-145">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="6a3cc-145">Valid values are:</span></span> 

- <span data-ttu-id="6a3cc-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="6a3cc-146">CloudService</span></span>
- <span data-ttu-id="6a3cc-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6a3cc-147">AzureWebsite</span></span>
- <span data-ttu-id="6a3cc-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="6a3cc-148">TrafficManager</span></span>

- <span data-ttu-id="6a3cc-149">Eventuell</span><span class="sxs-lookup"><span data-stu-id="6a3cc-149">Any</span></span> 

<span data-ttu-id="6a3cc-150">Om det finns fler än en AzureWebsite-slutpunkt måste slut punkterna finnas i olika data Center.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="6a3cc-151">-Vikt</span><span class="sxs-lookup"><span data-stu-id="6a3cc-151">-Weight</span></span>
<span data-ttu-id="6a3cc-152">Anger vikten för slut punkten som cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="6a3cc-153">Det giltiga värde intervallet är \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="6a3cc-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="6a3cc-154">Den här parametern används endast för principer för belastnings utjämning på RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="6a3cc-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3cc-155">CommonParameters</span></span>
<span data-ttu-id="6a3cc-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3cc-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3cc-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3cc-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a3cc-158">INPUTS</span></span>

## <span data-ttu-id="6a3cc-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a3cc-159">OUTPUTS</span></span>

### <span data-ttu-id="6a3cc-160">Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="6a3cc-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="6a3cc-161">Denna cmdlet skapar ett profil objekt för Traffic Manager, som innehåller information om den uppdaterade profilen.</span><span class="sxs-lookup"><span data-stu-id="6a3cc-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="6a3cc-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a3cc-162">NOTES</span></span>

## <span data-ttu-id="6a3cc-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a3cc-163">RELATED LINKS</span></span>

[<span data-ttu-id="6a3cc-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a3cc-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="6a3cc-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a3cc-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="6a3cc-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a3cc-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="6a3cc-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a3cc-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


