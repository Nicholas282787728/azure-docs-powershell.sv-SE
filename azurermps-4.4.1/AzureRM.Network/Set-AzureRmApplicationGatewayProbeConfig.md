---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 212e418c3fdaf8ba7f67ebdae0565d5d230daa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577624"
---
# <span data-ttu-id="b6a8b-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b6a8b-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b6a8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b6a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a8b-103">Ställer in Health PROBE-konfigurationen för en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b6a8b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6a8b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b6a8b-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a8b-106">Den Set-AzureRmApplicationGatewayProbeConfig cmdleten ställer in Health PROBE-konfigurationen på en befintlig Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="b6a8b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b6a8b-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a8b-108">Exempel 1: Ange konfiguration för en hälso sökning på en Programgateway</span><span class="sxs-lookup"><span data-stu-id="b6a8b-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="b6a8b-109">Det här kommandot anger konfigurationen för en hälso sökning med namnet Probe05 för programgatewayen med namnet Gateway.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="b6a8b-110">Kommandot anger också tröskelvärdet för fel till 8 försök och timeout efter 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="b6a8b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b6a8b-111">PARAMETERS</span></span>

### <span data-ttu-id="b6a8b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6a8b-112">-ApplicationGateway</span></span>
<span data-ttu-id="b6a8b-113">Anger den Programgateway som denna cmdlet skickar en sökning till.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="b6a8b-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="b6a8b-114">-HostName</span></span>
<span data-ttu-id="b6a8b-115">Anger det värdnamn som den här cmdleten skickar sonden till.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="b6a8b-116">-Intervall</span><span class="sxs-lookup"><span data-stu-id="b6a8b-116">-Interval</span></span>
<span data-ttu-id="b6a8b-117">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="b6a8b-118">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="b6a8b-119">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="b6a8b-120">-Passa</span><span class="sxs-lookup"><span data-stu-id="b6a8b-120">-Match</span></span>
<span data-ttu-id="b6a8b-121">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="b6a8b-122">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="b6a8b-122">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a8b-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="b6a8b-123">-MinServers</span></span>
<span data-ttu-id="b6a8b-124">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="b6a8b-125">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="b6a8b-125">Default value is 0</span></span>

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

### <span data-ttu-id="b6a8b-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b6a8b-126">-Name</span></span>
<span data-ttu-id="b6a8b-127">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="b6a8b-128">-Path</span><span class="sxs-lookup"><span data-stu-id="b6a8b-128">-Path</span></span>
<span data-ttu-id="b6a8b-129">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="b6a8b-130">Giltiga sökvägar börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="b6a8b-130">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="b6a8b-131">Avsökningen skickas till \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="b6a8b-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="b6a8b-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b6a8b-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="b6a8b-133">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="b6a8b-134">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="b6a8b-134">Default value is false</span></span>

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

### <span data-ttu-id="b6a8b-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b6a8b-135">-Protocol</span></span>
<span data-ttu-id="b6a8b-136">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-136">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="b6a8b-137">-Timeout</span><span class="sxs-lookup"><span data-stu-id="b6a8b-137">-Timeout</span></span>
<span data-ttu-id="b6a8b-138">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-138">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="b6a8b-139">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-139">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="b6a8b-140">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-140">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="b6a8b-141">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="b6a8b-141">-UnhealthyThreshold</span></span>
<span data-ttu-id="b6a8b-142">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-142">Specifies the probe retry count.</span></span>
<span data-ttu-id="b6a8b-143">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-143">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="b6a8b-144">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-144">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="b6a8b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a8b-145">-DefaultProfile</span></span>
<span data-ttu-id="b6a8b-146">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a8b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a8b-147">CommonParameters</span></span>
<span data-ttu-id="b6a8b-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a8b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a8b-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a8b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a8b-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b6a8b-150">INPUTS</span></span>

### <span data-ttu-id="b6a8b-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6a8b-151">PSApplicationGateway</span></span>
<span data-ttu-id="b6a8b-152">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="b6a8b-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b6a8b-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b6a8b-153">OUTPUTS</span></span>

### <span data-ttu-id="b6a8b-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6a8b-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6a8b-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b6a8b-155">NOTES</span></span>

## <span data-ttu-id="b6a8b-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b6a8b-156">RELATED LINKS</span></span>

[<span data-ttu-id="b6a8b-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b6a8b-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b6a8b-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b6a8b-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b6a8b-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b6a8b-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b6a8b-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b6a8b-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

