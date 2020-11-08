---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: e3dc6589ae3ba72140e0fa95ceec98ab280937f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092568"
---
# <span data-ttu-id="2bcc2-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2bcc2-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="2bcc2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bcc2-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcc2-103">Skapar backend HTTP-inställning för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="2bcc2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bcc2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bcc2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bcc2-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcc2-106">New-AzApplicationGatewayBackendHttpSetting cmdlet skapar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="2bcc2-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i en pool.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="2bcc2-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bcc2-108">EXAMPLES</span></span>

### <span data-ttu-id="2bcc2-109">Exempel 1: skapa backend HTTP-inställningar</span><span class="sxs-lookup"><span data-stu-id="2bcc2-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="2bcc2-110">Det här kommandot skapar backend HTTP-inställningar med namnet Setting01 på port 80, med HTTP-protokoll med cookie-baserad tillhörighet avaktiverad.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="2bcc2-111">Inställningarna lagras i variabeln $Setting.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="2bcc2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bcc2-112">PARAMETERS</span></span>

### <span data-ttu-id="2bcc2-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="2bcc2-113">-AffinityCookieName</span></span>
<span data-ttu-id="2bcc2-114">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="2bcc2-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="2bcc2-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2bcc2-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="2bcc2-116">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2bcc2-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2bcc2-117">-ConnectionDraining</span></span>
<span data-ttu-id="2bcc2-118">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="2bcc2-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="2bcc2-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="2bcc2-120">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="2bcc2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcc2-121">-DefaultProfile</span></span>
<span data-ttu-id="2bcc2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bcc2-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="2bcc2-123">-HostName</span></span>
<span data-ttu-id="2bcc2-124">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="2bcc2-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bcc2-125">-Name</span></span>
<span data-ttu-id="2bcc2-126">Anger namnet på de HTTP-inställningar som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2bcc2-127">-Path</span><span class="sxs-lookup"><span data-stu-id="2bcc2-127">-Path</span></span>
<span data-ttu-id="2bcc2-128">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="2bcc2-129">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="2bcc2-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="2bcc2-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="2bcc2-131">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="2bcc2-132">-Port</span><span class="sxs-lookup"><span data-stu-id="2bcc2-132">-Port</span></span>
<span data-ttu-id="2bcc2-133">Anger backend-serverns port.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="2bcc2-134">-Sond</span><span class="sxs-lookup"><span data-stu-id="2bcc2-134">-Probe</span></span>
<span data-ttu-id="2bcc2-135">Anger en sond som ska kopplas till backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="2bcc2-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="2bcc2-136">-ProbeId</span></span>
<span data-ttu-id="2bcc2-137">Anger ID för den sond som ska kopplas till backend-serverns pool.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="2bcc2-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2bcc2-138">-Protocol</span></span>
<span data-ttu-id="2bcc2-139">Anger vilket protokoll som ska användas för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="2bcc2-140">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="2bcc2-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="2bcc2-141">-RequestTimeout</span></span>
<span data-ttu-id="2bcc2-142">Anger ett timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="2bcc2-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2bcc2-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="2bcc2-144">Betrodda rot certifikat för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="2bcc2-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="2bcc2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcc2-145">CommonParameters</span></span>
<span data-ttu-id="2bcc2-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bcc2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcc2-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bcc2-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcc2-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bcc2-148">INPUTS</span></span>

### <span data-ttu-id="2bcc2-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="2bcc2-149">None</span></span>

## <span data-ttu-id="2bcc2-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bcc2-150">OUTPUTS</span></span>

### <span data-ttu-id="2bcc2-151">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2bcc2-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2bcc2-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bcc2-152">NOTES</span></span>

## <span data-ttu-id="2bcc2-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bcc2-153">RELATED LINKS</span></span>

[<span data-ttu-id="2bcc2-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2bcc2-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2bcc2-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2bcc2-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2bcc2-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2bcc2-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2bcc2-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2bcc2-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

