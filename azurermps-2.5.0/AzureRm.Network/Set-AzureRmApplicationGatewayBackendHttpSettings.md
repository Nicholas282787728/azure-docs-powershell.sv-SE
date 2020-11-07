---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: c20faf9ca89892d952d553d0f85cfa28b90ac590
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929678"
---
# <span data-ttu-id="73378-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73378-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="73378-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73378-102">SYNOPSIS</span></span>
<span data-ttu-id="73378-103">Uppdaterar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="73378-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73378-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73378-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73378-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73378-105">DESCRIPTION</span></span>
<span data-ttu-id="73378-106">Set-AzureRmApplicationGatewayBackendHttpSettings cmdleten uppdaterar serverns HTTP-inställningar (backend Hypertext Transfer Protocol) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="73378-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="73378-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i en pool.</span><span class="sxs-lookup"><span data-stu-id="73378-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="73378-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73378-108">EXAMPLES</span></span>

### <span data-ttu-id="73378-109">Exempel 1: uppdatera backend-HTTP-inställningarna för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="73378-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="73378-110">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="73378-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="73378-111">Det andra kommandot uppdaterar HTTP-inställningarna för programgatewayen i $AppGw variabel för att använda port 88, HTTP-protokollet och aktiverar cookie-baserad tillhörighet.</span><span class="sxs-lookup"><span data-stu-id="73378-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="73378-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73378-112">PARAMETERS</span></span>

### <span data-ttu-id="73378-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="73378-113">-AffinityCookieName</span></span>
<span data-ttu-id="73378-114">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="73378-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="73378-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73378-115">-ApplicationGateway</span></span>
<span data-ttu-id="73378-116">Anger ett Application Gateway-objekt med vilket denna cmdlet kopplar backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="73378-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="73378-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="73378-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="73378-118">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="73378-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="73378-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="73378-119">-ConnectionDraining</span></span>
<span data-ttu-id="73378-120">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="73378-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="73378-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="73378-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="73378-122">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för Server delen.</span><span class="sxs-lookup"><span data-stu-id="73378-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="73378-123">De acceptabla värdena för den här parametern är: inaktiverade eller aktiverade.</span><span class="sxs-lookup"><span data-stu-id="73378-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="73378-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73378-124">-DefaultProfile</span></span>
<span data-ttu-id="73378-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73378-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73378-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="73378-126">-HostName</span></span>
<span data-ttu-id="73378-127">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="73378-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="73378-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="73378-128">-Name</span></span>
<span data-ttu-id="73378-129">Anger namnet på backend-objektet HTTP Settings.</span><span class="sxs-lookup"><span data-stu-id="73378-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="73378-130">-Path</span><span class="sxs-lookup"><span data-stu-id="73378-130">-Path</span></span>
<span data-ttu-id="73378-131">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="73378-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="73378-132">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="73378-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="73378-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="73378-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="73378-134">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="73378-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="73378-135">-Port</span><span class="sxs-lookup"><span data-stu-id="73378-135">-Port</span></span>
<span data-ttu-id="73378-136">Anger vilken port som ska användas för varje server i backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="73378-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="73378-137">-Sond</span><span class="sxs-lookup"><span data-stu-id="73378-137">-Probe</span></span>
<span data-ttu-id="73378-138">Anger den avsökning som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="73378-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="73378-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="73378-139">-ProbeEnabled</span></span>
<span data-ttu-id="73378-140">Flagga om Avsök är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="73378-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="73378-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="73378-141">-ProbeId</span></span>
<span data-ttu-id="73378-142">Anger ID för den sond som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="73378-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="73378-143">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="73378-143">-Protocol</span></span>
<span data-ttu-id="73378-144">Anger vilket protokoll som ska användas för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="73378-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="73378-145">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="73378-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="73378-146">Den här parametern är Skift läges känslig.</span><span class="sxs-lookup"><span data-stu-id="73378-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="73378-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="73378-147">-RequestTimeout</span></span>
<span data-ttu-id="73378-148">Anger ett timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="73378-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="73378-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73378-149">CommonParameters</span></span>
<span data-ttu-id="73378-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73378-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73378-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73378-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73378-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73378-152">INPUTS</span></span>

### <span data-ttu-id="73378-153">System. String</span><span class="sxs-lookup"><span data-stu-id="73378-153">System.String</span></span>

## <span data-ttu-id="73378-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73378-154">OUTPUTS</span></span>

### <span data-ttu-id="73378-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73378-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73378-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73378-156">NOTES</span></span>

## <span data-ttu-id="73378-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73378-157">RELATED LINKS</span></span>

[<span data-ttu-id="73378-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73378-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="73378-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73378-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="73378-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73378-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="73378-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="73378-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

