---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 3696b33b18314d58e950fa9786e1febac5c3d22c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924281"
---
# <span data-ttu-id="cfa3d-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cfa3d-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="cfa3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfa3d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa3d-103">Uppdaterar backend HTTP-inställningar för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="cfa3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfa3d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa3d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfa3d-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa3d-106">Set-AzApplicationGatewayBackendHttpSetting cmdleten uppdaterar serverns HTTP-inställningar (backend Hypertext Transfer Protocol) för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="cfa3d-107">Backend-HTTP-inställningar tillämpas på alla backend-servrar i en pool.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="cfa3d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfa3d-108">EXAMPLES</span></span>

### <span data-ttu-id="cfa3d-109">Exempel 1: uppdatera backend-HTTP-inställningarna för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="cfa3d-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="cfa3d-110">Det första kommandot hämtar den Programgateway som heter ApplicationGateway01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar den i $AppGw variabeln.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="cfa3d-111">Det andra kommandot uppdaterar HTTP-inställningarna för programgatewayen i $AppGw variabel för att använda port 88, HTTP-protokollet och aktiverar cookie-baserad tillhörighet.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="cfa3d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfa3d-112">PARAMETERS</span></span>

### <span data-ttu-id="cfa3d-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="cfa3d-113">-AffinityCookieName</span></span>
<span data-ttu-id="cfa3d-114">Cookie-namn som ska användas för tillhörighets-cookien</span><span class="sxs-lookup"><span data-stu-id="cfa3d-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="cfa3d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfa3d-115">-ApplicationGateway</span></span>
<span data-ttu-id="cfa3d-116">Anger ett Application Gateway-objekt med vilket denna cmdlet kopplar backend HTTP-inställningar.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="cfa3d-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="cfa3d-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="cfa3d-118">Anger autentiseringscertifikat för programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="cfa3d-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cfa3d-119">-ConnectionDraining</span></span>
<span data-ttu-id="cfa3d-120">Anslutningen avsluts till resursens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="cfa3d-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="cfa3d-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="cfa3d-122">Anger om cookie-baserad tillhörighet ska aktive ras eller inaktive ras för Server delen.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="cfa3d-123">De acceptabla värdena för den här parametern är: inaktiverade eller aktiverade.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="cfa3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa3d-124">-DefaultProfile</span></span>
<span data-ttu-id="cfa3d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa3d-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="cfa3d-126">-HostName</span></span>
<span data-ttu-id="cfa3d-127">Anger att värd huvudet ska skickas till backend-servrarna.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="cfa3d-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfa3d-128">-Name</span></span>
<span data-ttu-id="cfa3d-129">Anger namnet på backend-objektet HTTP Settings.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="cfa3d-130">-Path</span><span class="sxs-lookup"><span data-stu-id="cfa3d-130">-Path</span></span>
<span data-ttu-id="cfa3d-131">Sökväg som ska användas som prefix för alla HTTP-begäranden.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="cfa3d-132">Om det inte finns något värde för den här parametern används ingen sökväg för fast.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="cfa3d-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="cfa3d-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="cfa3d-134">Flagga om värd huvudet ska hämtas från Server delens värdnamn.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="cfa3d-135">-Port</span><span class="sxs-lookup"><span data-stu-id="cfa3d-135">-Port</span></span>
<span data-ttu-id="cfa3d-136">Anger vilken port som ska användas för varje server i backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="cfa3d-137">-Sond</span><span class="sxs-lookup"><span data-stu-id="cfa3d-137">-Probe</span></span>
<span data-ttu-id="cfa3d-138">Anger den avsökning som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="cfa3d-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="cfa3d-139">-ProbeEnabled</span></span>
<span data-ttu-id="cfa3d-140">Flagga om Avsök är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="cfa3d-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="cfa3d-141">-ProbeId</span></span>
<span data-ttu-id="cfa3d-142">Anger ID för den sond som ska kopplas till backend HTTP-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="cfa3d-143">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="cfa3d-143">-Protocol</span></span>
<span data-ttu-id="cfa3d-144">Anger vilket protokoll som ska användas för kommunikation mellan Application Gateway och backend-servrar.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="cfa3d-145">De acceptabla värdena för den här parametern är: http och https.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="cfa3d-146">Den här parametern är Skift läges känslig.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="cfa3d-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="cfa3d-147">-RequestTimeout</span></span>
<span data-ttu-id="cfa3d-148">Anger ett timeout-värde för en begäran.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="cfa3d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa3d-149">CommonParameters</span></span>
<span data-ttu-id="cfa3d-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfa3d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa3d-151">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa3d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa3d-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfa3d-152">INPUTS</span></span>

### <span data-ttu-id="cfa3d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="cfa3d-153">System.String</span></span>

## <span data-ttu-id="cfa3d-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfa3d-154">OUTPUTS</span></span>

### <span data-ttu-id="cfa3d-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfa3d-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cfa3d-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfa3d-156">NOTES</span></span>

## <span data-ttu-id="cfa3d-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfa3d-157">RELATED LINKS</span></span>

[<span data-ttu-id="cfa3d-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cfa3d-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="cfa3d-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cfa3d-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="cfa3d-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cfa3d-160">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="cfa3d-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="cfa3d-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

