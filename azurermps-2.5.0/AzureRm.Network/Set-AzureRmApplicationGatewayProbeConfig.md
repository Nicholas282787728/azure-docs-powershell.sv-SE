---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 7fb8a30986c31659b49a08b261062e150ebe7e09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928686"
---
# <span data-ttu-id="75cc3-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75cc3-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="75cc3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="75cc3-103">Ställer in Health PROBE-konfigurationen för en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="75cc3-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75cc3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75cc3-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75cc3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="75cc3-106">Den Set-AzureRmApplicationGatewayProbeConfig cmdleten ställer in Health PROBE-konfigurationen på en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="75cc3-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="75cc3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75cc3-107">EXAMPLES</span></span>

### <span data-ttu-id="75cc3-108">Exempel 1: Ange konfiguration för en hälso sökning på en Programgateway</span><span class="sxs-lookup"><span data-stu-id="75cc3-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="75cc3-109">Det här kommandot anger konfigurationen för en hälso sökning med namnet Probe05 för programgatewayen med namnet Gateway.</span><span class="sxs-lookup"><span data-stu-id="75cc3-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="75cc3-110">Kommandot anger också tröskelvärdet för fel till 8 försök och timeout efter 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="75cc3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75cc3-111">PARAMETERS</span></span>

### <span data-ttu-id="75cc3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75cc3-112">-ApplicationGateway</span></span>
<span data-ttu-id="75cc3-113">Anger den Programgateway som denna cmdlet skickar en sökning till.</span><span class="sxs-lookup"><span data-stu-id="75cc3-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="75cc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cc3-114">-DefaultProfile</span></span>
<span data-ttu-id="75cc3-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75cc3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75cc3-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="75cc3-116">-HostName</span></span>
<span data-ttu-id="75cc3-117">Anger det värdnamn som den här cmdleten skickar sonden till.</span><span class="sxs-lookup"><span data-stu-id="75cc3-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="75cc3-118">-Intervall</span><span class="sxs-lookup"><span data-stu-id="75cc3-118">-Interval</span></span>
<span data-ttu-id="75cc3-119">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="75cc3-120">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="75cc3-121">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="75cc3-122">-Passa</span><span class="sxs-lookup"><span data-stu-id="75cc3-122">-Match</span></span>
<span data-ttu-id="75cc3-123">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="75cc3-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="75cc3-124">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="75cc3-124">Default value is empty</span></span>

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

### <span data-ttu-id="75cc3-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="75cc3-125">-MinServers</span></span>
<span data-ttu-id="75cc3-126">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="75cc3-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="75cc3-127">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="75cc3-127">Default value is 0</span></span>

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

### <span data-ttu-id="75cc3-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="75cc3-128">-Name</span></span>
<span data-ttu-id="75cc3-129">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="75cc3-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="75cc3-130">-Path</span><span class="sxs-lookup"><span data-stu-id="75cc3-130">-Path</span></span>
<span data-ttu-id="75cc3-131">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="75cc3-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="75cc3-132">Giltiga sökvägar börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="75cc3-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="75cc3-133">Avsökningen skickas till \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="75cc3-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="75cc3-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="75cc3-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="75cc3-135">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="75cc3-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="75cc3-136">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="75cc3-136">Default value is false</span></span>

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

### <span data-ttu-id="75cc3-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="75cc3-137">-Protocol</span></span>
<span data-ttu-id="75cc3-138">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="75cc3-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="75cc3-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="75cc3-139">-Timeout</span></span>
<span data-ttu-id="75cc3-140">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="75cc3-141">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="75cc3-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="75cc3-142">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="75cc3-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="75cc3-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="75cc3-144">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="75cc3-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="75cc3-145">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="75cc3-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="75cc3-146">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75cc3-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="75cc3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cc3-147">CommonParameters</span></span>
<span data-ttu-id="75cc3-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cc3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cc3-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75cc3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cc3-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75cc3-150">INPUTS</span></span>

### <span data-ttu-id="75cc3-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75cc3-151">PSApplicationGateway</span></span>
<span data-ttu-id="75cc3-152">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="75cc3-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="75cc3-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75cc3-153">OUTPUTS</span></span>

### <span data-ttu-id="75cc3-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75cc3-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75cc3-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75cc3-155">NOTES</span></span>

## <span data-ttu-id="75cc3-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75cc3-156">RELATED LINKS</span></span>

[<span data-ttu-id="75cc3-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75cc3-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="75cc3-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75cc3-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="75cc3-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75cc3-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="75cc3-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75cc3-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

