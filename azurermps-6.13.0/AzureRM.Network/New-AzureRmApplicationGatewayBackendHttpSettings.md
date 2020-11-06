---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 3b292b70e96c8da57a87834ecc4c095c9ca3f55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575207"
---
# <span data-ttu-id="c605b-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c605b-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c605b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c605b-102">SYNOPSIS</span></span>
<span data-ttu-id="c605b-103">Skapar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c605b-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c605b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c605b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c605b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c605b-105">DESCRIPTION</span></span>
<span data-ttu-id="c605b-106">New-AzureRmApplicationGatewayBackendHttpSettings cmdlet skapar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="c605b-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="c605b-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i en pool.</span><span class="sxs-lookup"><span data-stu-id="c605b-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="c605b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c605b-108">EXAMPLES</span></span>

### <span data-ttu-id="c605b-109">Exempel 1: skapa backend HTTP-inställningar</span><span class="sxs-lookup"><span data-stu-id="c605b-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="c605b-110">Det här kommandot skapar backend HTTP-inställningar med namnet Setting01 på port 80, med HTTP-protokoll med cookie-baserad tillhörighet avaktiverad.</span><span class="sxs-lookup"><span data-stu-id="c605b-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="c605b-111">Inställningarna lagras i variabeln $Setting.</span><span class="sxs-lookup"><span data-stu-id="c605b-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="c605b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c605b-112">PARAMETERS</span></span>

### <span data-ttu-id="c605b-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="c605b-113">-AffinityCookieName</span></span>
<span data-ttu-id="c605b-114">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="c605b-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="c605b-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="c605b-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="c605b-116">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="c605b-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="c605b-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c605b-117">-ConnectionDraining</span></span>
<span data-ttu-id="c605b-118">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="c605b-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="c605b-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="c605b-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="c605b-120">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="c605b-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="c605b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c605b-121">-DefaultProfile</span></span>
<span data-ttu-id="c605b-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c605b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c605b-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="c605b-123">-HostName</span></span>
<span data-ttu-id="c605b-124">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="c605b-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="c605b-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="c605b-125">-Name</span></span>
<span data-ttu-id="c605b-126">Anger namnet på de HTTP-inställningar som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="c605b-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c605b-127">-Path</span><span class="sxs-lookup"><span data-stu-id="c605b-127">-Path</span></span>
<span data-ttu-id="c605b-128">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="c605b-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="c605b-129">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="c605b-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="c605b-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c605b-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="c605b-131">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="c605b-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="c605b-132">-Port</span><span class="sxs-lookup"><span data-stu-id="c605b-132">-Port</span></span>
<span data-ttu-id="c605b-133">Anger backend-serverns port.</span><span class="sxs-lookup"><span data-stu-id="c605b-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="c605b-134">-Sond</span><span class="sxs-lookup"><span data-stu-id="c605b-134">-Probe</span></span>
<span data-ttu-id="c605b-135">Anger en sond som ska kopplas till backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="c605b-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="c605b-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c605b-136">-ProbeId</span></span>
<span data-ttu-id="c605b-137">Anger ID för den sond som ska kopplas till backend-serverns pool.</span><span class="sxs-lookup"><span data-stu-id="c605b-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="c605b-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c605b-138">-Protocol</span></span>
<span data-ttu-id="c605b-139">Anger vilket protokoll som ska användas för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="c605b-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="c605b-140">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="c605b-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="c605b-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="c605b-141">-RequestTimeout</span></span>
<span data-ttu-id="c605b-142">Anger ett timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="c605b-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="c605b-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c605b-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="c605b-144">Betrodda rot certifikat för Application Gateway</span><span class="sxs-lookup"><span data-stu-id="c605b-144">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c605b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c605b-145">CommonParameters</span></span>
<span data-ttu-id="c605b-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c605b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c605b-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c605b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c605b-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c605b-148">INPUTS</span></span>

### <span data-ttu-id="c605b-149">Ingen</span><span class="sxs-lookup"><span data-stu-id="c605b-149">None</span></span>

## <span data-ttu-id="c605b-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c605b-150">OUTPUTS</span></span>

### <span data-ttu-id="c605b-151">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c605b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c605b-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c605b-152">NOTES</span></span>

## <span data-ttu-id="c605b-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c605b-153">RELATED LINKS</span></span>

[<span data-ttu-id="c605b-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c605b-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c605b-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c605b-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c605b-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c605b-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c605b-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c605b-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

