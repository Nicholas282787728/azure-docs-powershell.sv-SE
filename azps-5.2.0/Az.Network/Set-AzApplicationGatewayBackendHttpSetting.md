---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389271"
---
# <span data-ttu-id="353e5-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="353e5-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="353e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="353e5-102">SYNOPSIS</span></span>
<span data-ttu-id="353e5-103">Uppdaterar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="353e5-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="353e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="353e5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="353e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="353e5-105">DESCRIPTION</span></span>
<span data-ttu-id="353e5-106">Set-AzApplicationGatewayBackendHttpSetting cmdleten uppdaterar serverns HTTP-inställningar (backend Hypertext Transfer Protocol) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="353e5-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="353e5-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i en pool.</span><span class="sxs-lookup"><span data-stu-id="353e5-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="353e5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="353e5-108">EXAMPLES</span></span>

### <span data-ttu-id="353e5-109">Exempel 1: uppdatera backend-HTTP-inställningarna för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="353e5-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="353e5-110">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="353e5-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="353e5-111">Det andra kommandot uppdaterar HTTP-inställningarna för programgatewayen i $AppGw variabel för att använda port 88, HTTP-protokollet och aktiverar cookie-baserad tillhörighet.</span><span class="sxs-lookup"><span data-stu-id="353e5-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="353e5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="353e5-112">PARAMETERS</span></span>

### <span data-ttu-id="353e5-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="353e5-113">-AffinityCookieName</span></span>
<span data-ttu-id="353e5-114">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="353e5-114">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="353e5-115">-ApplicationGateway</span></span>
<span data-ttu-id="353e5-116">Anger ett Application Gateway-objekt med vilket denna cmdlet kopplar backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="353e5-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="353e5-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="353e5-118">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="353e5-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="353e5-119">-ConnectionDraining</span></span>
<span data-ttu-id="353e5-120">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="353e5-120">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="353e5-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="353e5-122">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för Server delen.</span><span class="sxs-lookup"><span data-stu-id="353e5-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="353e5-123">De acceptabla värdena för den här parametern är: inaktiverade eller aktiverade.</span><span class="sxs-lookup"><span data-stu-id="353e5-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353e5-124">-DefaultProfile</span></span>
<span data-ttu-id="353e5-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="353e5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="353e5-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="353e5-126">-HostName</span></span>
<span data-ttu-id="353e5-127">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="353e5-127">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="353e5-128">-Name</span></span>
<span data-ttu-id="353e5-129">Anger namnet på backend-objektet HTTP Settings.</span><span class="sxs-lookup"><span data-stu-id="353e5-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="353e5-130">-Path</span><span class="sxs-lookup"><span data-stu-id="353e5-130">-Path</span></span>
<span data-ttu-id="353e5-131">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="353e5-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="353e5-132">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="353e5-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="353e5-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="353e5-134">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="353e5-134">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-135">-Port</span><span class="sxs-lookup"><span data-stu-id="353e5-135">-Port</span></span>
<span data-ttu-id="353e5-136">Anger vilken port som ska användas för varje server i backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="353e5-136">Specifies the port to use for each server in the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-137">-Sond</span><span class="sxs-lookup"><span data-stu-id="353e5-137">-Probe</span></span>
<span data-ttu-id="353e5-138">Anger den avsökning som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="353e5-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="353e5-139">-ProbeId</span></span>
<span data-ttu-id="353e5-140">Anger ID för den sond som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="353e5-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="353e5-141">-Protocol</span></span>
<span data-ttu-id="353e5-142">Anger vilket protokoll som ska användas för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="353e5-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="353e5-143">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="353e5-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="353e5-144">Den här parametern är Skift läges känslig.</span><span class="sxs-lookup"><span data-stu-id="353e5-144">This parameter is case-sensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="353e5-145">-RequestTimeout</span></span>
<span data-ttu-id="353e5-146">Anger ett timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="353e5-146">Specifies a request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="353e5-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="353e5-148">Betrodda rot certifikat för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="353e5-148">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="353e5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353e5-149">CommonParameters</span></span>
<span data-ttu-id="353e5-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353e5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353e5-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353e5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353e5-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="353e5-152">INPUTS</span></span>

### <span data-ttu-id="353e5-153">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="353e5-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="353e5-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="353e5-154">OUTPUTS</span></span>

### <span data-ttu-id="353e5-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="353e5-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="353e5-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="353e5-156">NOTES</span></span>

## <span data-ttu-id="353e5-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="353e5-157">RELATED LINKS</span></span>

[<span data-ttu-id="353e5-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="353e5-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="353e5-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="353e5-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="353e5-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="353e5-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="353e5-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="353e5-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

