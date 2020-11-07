---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 50f54d258e6b5575983d8cd35f487783ea922eb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924262"
---
# <span data-ttu-id="0004a-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0004a-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0004a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0004a-102">SYNOPSIS</span></span>
<span data-ttu-id="0004a-103">Ställer in Health PROBE-konfigurationen för en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0004a-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="0004a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0004a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0004a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0004a-105">DESCRIPTION</span></span>
<span data-ttu-id="0004a-106">Den Set-AzApplicationGatewayProbeConfig cmdleten ställer in Health PROBE-konfigurationen på en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="0004a-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="0004a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0004a-107">EXAMPLES</span></span>

### <span data-ttu-id="0004a-108">Exempel 1: Ange konfiguration för en hälso sökning på en Programgateway</span><span class="sxs-lookup"><span data-stu-id="0004a-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="0004a-109">Det här kommandot anger konfigurationen för en hälso sökning med namnet Probe05 för programgatewayen med namnet Gateway.</span><span class="sxs-lookup"><span data-stu-id="0004a-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="0004a-110">Kommandot anger också tröskelvärdet för fel till 8 försök och timeout efter 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0004a-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="0004a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0004a-111">PARAMETERS</span></span>

### <span data-ttu-id="0004a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0004a-112">-ApplicationGateway</span></span>
<span data-ttu-id="0004a-113">Anger den Programgateway som denna cmdlet skickar en sökning till.</span><span class="sxs-lookup"><span data-stu-id="0004a-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="0004a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0004a-114">-DefaultProfile</span></span>
<span data-ttu-id="0004a-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0004a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0004a-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="0004a-116">-HostName</span></span>
<span data-ttu-id="0004a-117">Anger det värdnamn som den här cmdleten skickar sonden till.</span><span class="sxs-lookup"><span data-stu-id="0004a-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="0004a-118">-Intervall</span><span class="sxs-lookup"><span data-stu-id="0004a-118">-Interval</span></span>
<span data-ttu-id="0004a-119">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0004a-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="0004a-120">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="0004a-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="0004a-121">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0004a-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0004a-122">-Passa</span><span class="sxs-lookup"><span data-stu-id="0004a-122">-Match</span></span>
<span data-ttu-id="0004a-123">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="0004a-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="0004a-124">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="0004a-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0004a-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="0004a-125">-MinServers</span></span>
<span data-ttu-id="0004a-126">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="0004a-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="0004a-127">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="0004a-127">Default value is 0</span></span>

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

### <span data-ttu-id="0004a-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="0004a-128">-Name</span></span>
<span data-ttu-id="0004a-129">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="0004a-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0004a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="0004a-130">-Path</span></span>
<span data-ttu-id="0004a-131">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="0004a-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="0004a-132">Giltiga sökvägar börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="0004a-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="0004a-133">Avsökningen skickas till \< protokoll \> :// \< värd \> : \< port \> \< Sök väg \> .</span><span class="sxs-lookup"><span data-stu-id="0004a-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="0004a-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0004a-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="0004a-135">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="0004a-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="0004a-136">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="0004a-136">Default value is false</span></span>

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

### <span data-ttu-id="0004a-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0004a-137">-Protocol</span></span>
<span data-ttu-id="0004a-138">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="0004a-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="0004a-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="0004a-139">-Timeout</span></span>
<span data-ttu-id="0004a-140">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0004a-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="0004a-141">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="0004a-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="0004a-142">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0004a-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0004a-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="0004a-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="0004a-144">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="0004a-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="0004a-145">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="0004a-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="0004a-146">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0004a-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="0004a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0004a-147">CommonParameters</span></span>
<span data-ttu-id="0004a-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0004a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0004a-149">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0004a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0004a-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0004a-150">INPUTS</span></span>

### <span data-ttu-id="0004a-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0004a-151">PSApplicationGateway</span></span>
<span data-ttu-id="0004a-152">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="0004a-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="0004a-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0004a-153">OUTPUTS</span></span>

### <span data-ttu-id="0004a-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0004a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0004a-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0004a-155">NOTES</span></span>

## <span data-ttu-id="0004a-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0004a-156">RELATED LINKS</span></span>

[<span data-ttu-id="0004a-157">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0004a-157">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0004a-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0004a-158">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0004a-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0004a-159">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0004a-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0004a-160">Remove-AzApplicationGatewayProbeConfig</span></span>]()

