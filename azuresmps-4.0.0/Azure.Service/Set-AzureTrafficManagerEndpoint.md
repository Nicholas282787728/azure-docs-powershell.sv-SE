---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093160"
---
# <span data-ttu-id="f6dae-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6dae-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f6dae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6dae-102">SYNOPSIS</span></span>
<span data-ttu-id="f6dae-103">Uppdaterar egenskaperna för en slut punkt i en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="f6dae-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="f6dae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6dae-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6dae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6dae-105">DESCRIPTION</span></span>
<span data-ttu-id="f6dae-106">Cmdleten **set-AzureTrafficManagerEndpoint** uppdaterar egenskaperna för en slut punkt i en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="f6dae-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f6dae-107">Om slut punkten inte finns i den aktuella profilen skapar den här cmdlet den.</span><span class="sxs-lookup"><span data-stu-id="f6dae-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="f6dae-108">När du har lagt till en slut punkt skickar du resultatet till cmdleten **set-AzureTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f6dae-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f6dae-109">Denna cmdlet ansluter till Azure för att spara dina ändringar.</span><span class="sxs-lookup"><span data-stu-id="f6dae-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="f6dae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6dae-110">EXAMPLES</span></span>

### <span data-ttu-id="f6dae-111">Exempel 1: uppdatera en slut punkt för en profil</span><span class="sxs-lookup"><span data-stu-id="f6dae-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="f6dae-112">Det första kommandot använder cmdleten **Get-AzureTrafficManagerProfile** för att hämta profilen med namnet ContosoProfile och lagrar den sedan i $TrafficManagerProfile variabel.</span><span class="sxs-lookup"><span data-stu-id="f6dae-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f6dae-113">Det andra kommandot uppdaterar slut punkten i Traffic Manager-profilen som lagras i $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f6dae-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f6dae-114">Slut punkten har domän namnet ContosoApp02.cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="f6dae-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="f6dae-115">Kommandot anger också slut punktens status, typ, vikt och plats.</span><span class="sxs-lookup"><span data-stu-id="f6dae-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="f6dae-116">Kommandot skickar den ändrade profilen till cmdleten **set-AzureTrafficManagerProfile** för att ansluta till Azure för att spara ändringarna.</span><span class="sxs-lookup"><span data-stu-id="f6dae-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="f6dae-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6dae-117">PARAMETERS</span></span>

### <span data-ttu-id="f6dae-118">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="f6dae-118">-DomainName</span></span>
<span data-ttu-id="f6dae-119">Anger domän namnet för slut punkten som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="f6dae-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="f6dae-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="f6dae-120">-Location</span></span>
<span data-ttu-id="f6dae-121">Anger platsen för slut punkten som cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="f6dae-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="f6dae-122">Det måste vara en Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="f6dae-122">This must be an Azure location.</span></span>

<span data-ttu-id="f6dae-123">Den här parametern måste innehålla ett värde för slut punkter av typen "any" eller av typen "TrafficManager" i en profil som har metod för belastnings utjämning angiven till "prestanda".</span><span class="sxs-lookup"><span data-stu-id="f6dae-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="f6dae-124">De möjliga värdena är namnen på Azure-regionen, som finns på  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="f6dae-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="f6dae-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="f6dae-125">-MinChildEndpoints</span></span>
<span data-ttu-id="f6dae-126">Anger det minsta antalet slut punkter som den kapslade profilen måste ha för att den här slut punkten ska kunna anses vara online.</span><span class="sxs-lookup"><span data-stu-id="f6dae-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="f6dae-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="f6dae-127">-Profile</span></span>
<span data-ttu-id="f6dae-128">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="f6dae-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f6dae-129">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="f6dae-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f6dae-130">-Status</span><span class="sxs-lookup"><span data-stu-id="f6dae-130">-Status</span></span>
<span data-ttu-id="f6dae-131">Anger statusen för övervaknings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="f6dae-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="f6dae-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f6dae-132">Valid values are:</span></span> 

- <span data-ttu-id="f6dae-133">Aktiverat</span><span class="sxs-lookup"><span data-stu-id="f6dae-133">Enabled</span></span>
- <span data-ttu-id="f6dae-134">Aktiv</span><span class="sxs-lookup"><span data-stu-id="f6dae-134">Disabled</span></span>

<span data-ttu-id="f6dae-135">Om du anger ett värde för aktive rad övervakar trafik hanteraren slut punkten och belastnings Utjämnings metoden när trafiken hanteras.</span><span class="sxs-lookup"><span data-stu-id="f6dae-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="f6dae-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6dae-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="f6dae-137">Anger den Traffic Manager-profil som du vill ändra slut punkten för.</span><span class="sxs-lookup"><span data-stu-id="f6dae-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="f6dae-138">– Skriv</span><span class="sxs-lookup"><span data-stu-id="f6dae-138">-Type</span></span>
<span data-ttu-id="f6dae-139">Anger typen av slut punkt.</span><span class="sxs-lookup"><span data-stu-id="f6dae-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="f6dae-140">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="f6dae-140">Valid values are:</span></span> 

- <span data-ttu-id="f6dae-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="f6dae-141">CloudService</span></span>
- <span data-ttu-id="f6dae-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f6dae-142">AzureWebsite</span></span>
- <span data-ttu-id="f6dae-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f6dae-143">TrafficManager</span></span>

- <span data-ttu-id="f6dae-144">Eventuell</span><span class="sxs-lookup"><span data-stu-id="f6dae-144">Any</span></span> 

<span data-ttu-id="f6dae-145">Om det finns fler än en AzureWebsite-slutpunkt måste slut punkterna finnas i olika data Center.</span><span class="sxs-lookup"><span data-stu-id="f6dae-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="f6dae-146">-Vikt</span><span class="sxs-lookup"><span data-stu-id="f6dae-146">-Weight</span></span>
<span data-ttu-id="f6dae-147">Anger vikten för slut punkten som cmdleten lägger till.</span><span class="sxs-lookup"><span data-stu-id="f6dae-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="f6dae-148">Det giltiga värde intervallet är \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="f6dae-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="f6dae-149">Den här parametern används endast för principer för belastnings utjämning på RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="f6dae-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="f6dae-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6dae-150">CommonParameters</span></span>
<span data-ttu-id="f6dae-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6dae-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6dae-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6dae-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6dae-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6dae-153">INPUTS</span></span>

## <span data-ttu-id="f6dae-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6dae-154">OUTPUTS</span></span>

### <span data-ttu-id="f6dae-155">Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="f6dae-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="f6dae-156">Denna cmdlet skapar ett profil objekt för Traffic Manager, som innehåller information om den uppdaterade profilen.</span><span class="sxs-lookup"><span data-stu-id="f6dae-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="f6dae-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6dae-157">NOTES</span></span>

## <span data-ttu-id="f6dae-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6dae-158">RELATED LINKS</span></span>

[<span data-ttu-id="f6dae-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6dae-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="f6dae-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6dae-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="f6dae-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6dae-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f6dae-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6dae-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


