---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 87d875881ce6086f033353dd4b37ba8a8098a96c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758373"
---
# <span data-ttu-id="f05f3-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f05f3-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="f05f3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f05f3-102">SYNOPSIS</span></span>
<span data-ttu-id="f05f3-103">Uppdaterar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f05f3-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f05f3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f05f3-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f05f3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f05f3-105">DESCRIPTION</span></span>
<span data-ttu-id="f05f3-106">Set-AzureRmApplicationGatewayBackendHttpSettings cmdleten uppdaterar serverns HTTP-inställningar (backend Hypertext Transfer Protocol) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f05f3-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="f05f3-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i en pool.</span><span class="sxs-lookup"><span data-stu-id="f05f3-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="f05f3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f05f3-108">EXAMPLES</span></span>

### <span data-ttu-id="f05f3-109">Exempel 1: uppdatera backend-HTTP-inställningarna för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="f05f3-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="f05f3-110">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="f05f3-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f05f3-111">Det andra kommandot uppdaterar HTTP-inställningarna för programgatewayen i $AppGw variabel för att använda port 88, HTTP-protokollet och aktiverar cookie-baserad tillhörighet.</span><span class="sxs-lookup"><span data-stu-id="f05f3-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="f05f3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f05f3-112">PARAMETERS</span></span>

### <span data-ttu-id="f05f3-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="f05f3-113">-AffinityCookieName</span></span>
<span data-ttu-id="f05f3-114">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="f05f3-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="f05f3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05f3-115">-ApplicationGateway</span></span>
<span data-ttu-id="f05f3-116">Anger ett Application Gateway-objekt med vilket denna cmdlet kopplar backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="f05f3-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f05f3-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="f05f3-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="f05f3-118">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f05f3-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="f05f3-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="f05f3-119">-ConnectionDraining</span></span>
<span data-ttu-id="f05f3-120">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="f05f3-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="f05f3-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="f05f3-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="f05f3-122">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för Server delen.</span><span class="sxs-lookup"><span data-stu-id="f05f3-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="f05f3-123">De acceptabla värdena för den här parametern är: inaktiverade eller aktiverade.</span><span class="sxs-lookup"><span data-stu-id="f05f3-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="f05f3-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="f05f3-124">-HostName</span></span>
<span data-ttu-id="f05f3-125">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="f05f3-125">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="f05f3-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f05f3-126">-Name</span></span>
<span data-ttu-id="f05f3-127">Anger namnet på backend-objektet HTTP Settings.</span><span class="sxs-lookup"><span data-stu-id="f05f3-127">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="f05f3-128">-Path</span><span class="sxs-lookup"><span data-stu-id="f05f3-128">-Path</span></span>
<span data-ttu-id="f05f3-129">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="f05f3-129">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="f05f3-130">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="f05f3-130">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="f05f3-131">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="f05f3-131">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="f05f3-132">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="f05f3-132">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="f05f3-133">-Port</span><span class="sxs-lookup"><span data-stu-id="f05f3-133">-Port</span></span>
<span data-ttu-id="f05f3-134">Anger vilken port som ska användas för varje server i backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="f05f3-134">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="f05f3-135">-Sond</span><span class="sxs-lookup"><span data-stu-id="f05f3-135">-Probe</span></span>
<span data-ttu-id="f05f3-136">Anger den avsökning som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="f05f3-136">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f05f3-137">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="f05f3-137">-ProbeEnabled</span></span>
<span data-ttu-id="f05f3-138">Flagga om Avsök är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="f05f3-138">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="f05f3-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="f05f3-139">-ProbeId</span></span>
<span data-ttu-id="f05f3-140">Anger ID för den sond som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="f05f3-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="f05f3-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f05f3-141">-Protocol</span></span>
<span data-ttu-id="f05f3-142">Anger vilket protokoll som ska användas för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="f05f3-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="f05f3-143">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="f05f3-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="f05f3-144">Den här parametern är Skift läges känslig.</span><span class="sxs-lookup"><span data-stu-id="f05f3-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="f05f3-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="f05f3-145">-RequestTimeout</span></span>
<span data-ttu-id="f05f3-146">Anger ett timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="f05f3-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="f05f3-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05f3-147">-DefaultProfile</span></span>
<span data-ttu-id="f05f3-148">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f05f3-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f05f3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05f3-149">CommonParameters</span></span>
<span data-ttu-id="f05f3-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f05f3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05f3-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f05f3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05f3-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f05f3-152">INPUTS</span></span>

### <span data-ttu-id="f05f3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f05f3-153">System.String</span></span>

## <span data-ttu-id="f05f3-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f05f3-154">OUTPUTS</span></span>

### <span data-ttu-id="f05f3-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f05f3-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f05f3-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f05f3-156">NOTES</span></span>

## <span data-ttu-id="f05f3-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f05f3-157">RELATED LINKS</span></span>

[<span data-ttu-id="f05f3-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f05f3-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="f05f3-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f05f3-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="f05f3-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f05f3-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="f05f3-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f05f3-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()
