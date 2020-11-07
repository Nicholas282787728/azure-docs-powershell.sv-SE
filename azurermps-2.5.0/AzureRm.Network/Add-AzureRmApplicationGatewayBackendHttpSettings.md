---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f283b40e7e40285a221eb436495d54820884003f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930222"
---
# <span data-ttu-id="955d6-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="955d6-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="955d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="955d6-102">SYNOPSIS</span></span>
<span data-ttu-id="955d6-103">Lägger till backend HTTP-inställningar till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="955d6-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="955d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="955d6-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="955d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="955d6-105">DESCRIPTION</span></span>
<span data-ttu-id="955d6-106">Med den här Add-AzureRmApplicationGatewayBackendHttpSettings cmdleten läggs Server-HTTP-inställningar till i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="955d6-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="955d6-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i poolen.</span><span class="sxs-lookup"><span data-stu-id="955d6-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="955d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="955d6-108">EXAMPLES</span></span>

### <span data-ttu-id="955d6-109">Exempel 1: lägga till backend HTTP-inställningar till en Programgateway</span><span class="sxs-lookup"><span data-stu-id="955d6-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="955d6-110">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln. Det andra kommandot lägger till backend-HTTP-inställningar för programgatewayen, vilket ger porten värdet 88 och protokollet till HTTP, samt namnen inställningar Setting02.</span><span class="sxs-lookup"><span data-stu-id="955d6-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="955d6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="955d6-111">PARAMETERS</span></span>

### <span data-ttu-id="955d6-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="955d6-112">-AffinityCookieName</span></span>
<span data-ttu-id="955d6-113">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="955d6-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="955d6-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="955d6-114">-ApplicationGateway</span></span>
<span data-ttu-id="955d6-115">Anger namnet på den Programgateway för vilken denna cmdlet lägger till inställningar.</span><span class="sxs-lookup"><span data-stu-id="955d6-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="955d6-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="955d6-117">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="955d6-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="955d6-118">-ConnectionDraining</span></span>
<span data-ttu-id="955d6-119">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="955d6-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="955d6-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="955d6-121">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för Server delen.</span><span class="sxs-lookup"><span data-stu-id="955d6-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="955d6-122">De acceptabla värdena för den här parametern är: inaktiverade.</span><span class="sxs-lookup"><span data-stu-id="955d6-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955d6-123">-DefaultProfile</span></span>
<span data-ttu-id="955d6-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="955d6-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="955d6-125">-HostName</span></span>
<span data-ttu-id="955d6-126">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="955d6-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="955d6-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="955d6-127">-Name</span></span>
<span data-ttu-id="955d6-128">Anger namnet på de HTTP-inställningar som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="955d6-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="955d6-129">-Path</span><span class="sxs-lookup"><span data-stu-id="955d6-129">-Path</span></span>
<span data-ttu-id="955d6-130">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="955d6-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="955d6-131">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="955d6-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="955d6-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="955d6-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="955d6-133">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="955d6-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-134">-Port</span><span class="sxs-lookup"><span data-stu-id="955d6-134">-Port</span></span>
<span data-ttu-id="955d6-135">Anger backend-serverns port.</span><span class="sxs-lookup"><span data-stu-id="955d6-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="955d6-136">-Sond</span><span class="sxs-lookup"><span data-stu-id="955d6-136">-Probe</span></span>
<span data-ttu-id="955d6-137">Anger den avsökning som ska kopplas till backend-servern.</span><span class="sxs-lookup"><span data-stu-id="955d6-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="955d6-138">-ProbeEnabled</span></span>
<span data-ttu-id="955d6-139">Flagga om Avsök är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="955d6-139">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-140">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="955d6-140">-ProbeId</span></span>
<span data-ttu-id="955d6-141">Anger ID för den sond som ska kopplas till backend-servern.</span><span class="sxs-lookup"><span data-stu-id="955d6-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="955d6-142">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="955d6-142">-Protocol</span></span>
<span data-ttu-id="955d6-143">Anger protokollet för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="955d6-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="955d6-144">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="955d6-144">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955d6-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="955d6-145">-RequestTimeout</span></span>
<span data-ttu-id="955d6-146">Anger timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="955d6-146">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="955d6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955d6-147">CommonParameters</span></span>
<span data-ttu-id="955d6-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955d6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955d6-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="955d6-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955d6-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="955d6-150">INPUTS</span></span>

### <span data-ttu-id="955d6-151">System. String</span><span class="sxs-lookup"><span data-stu-id="955d6-151">System.String</span></span>

## <span data-ttu-id="955d6-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="955d6-152">OUTPUTS</span></span>

### <span data-ttu-id="955d6-153">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="955d6-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="955d6-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="955d6-154">NOTES</span></span>

## <span data-ttu-id="955d6-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="955d6-155">RELATED LINKS</span></span>

[<span data-ttu-id="955d6-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="955d6-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="955d6-157">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="955d6-157">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="955d6-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="955d6-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="955d6-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="955d6-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

