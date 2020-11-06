---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582348"
---
# <span data-ttu-id="75934-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75934-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="75934-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75934-102">SYNOPSIS</span></span>
<span data-ttu-id="75934-103">Lägger till en hälso sökning i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="75934-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75934-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75934-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75934-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75934-105">DESCRIPTION</span></span>
<span data-ttu-id="75934-106">Add-AzureRmApplicationGatewayProbeConfig cmdlet lägger till en hälso sökning i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="75934-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="75934-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75934-107">EXAMPLES</span></span>

### <span data-ttu-id="75934-108">Exempel 1: lägga till en hälso kontroll i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="75934-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="75934-109">Det här kommandot lägger till en hälso sökning med namnet Probe01 för programgatewayen med namnet Gateway.</span><span class="sxs-lookup"><span data-stu-id="75934-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="75934-110">Kommandot anger också tröskelvärdet för fel till 8 försök och timeout efter 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75934-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="75934-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75934-111">PARAMETERS</span></span>

### <span data-ttu-id="75934-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75934-112">-ApplicationGateway</span></span>
<span data-ttu-id="75934-113">Anger den Programgateway som denna cmdlet lägger till en sond för.</span><span class="sxs-lookup"><span data-stu-id="75934-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="75934-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="75934-114">-HostName</span></span>
<span data-ttu-id="75934-115">Anger det värdnamn som den här cmdleten skickar sonden till.</span><span class="sxs-lookup"><span data-stu-id="75934-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="75934-116">-Intervall</span><span class="sxs-lookup"><span data-stu-id="75934-116">-Interval</span></span>
<span data-ttu-id="75934-117">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="75934-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="75934-118">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="75934-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="75934-119">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75934-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="75934-120">-Passa</span><span class="sxs-lookup"><span data-stu-id="75934-120">-Match</span></span>
<span data-ttu-id="75934-121">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="75934-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="75934-122">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="75934-122">Default value is empty</span></span>

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

### <span data-ttu-id="75934-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="75934-123">-MinServers</span></span>
<span data-ttu-id="75934-124">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="75934-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="75934-125">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="75934-125">Default value is 0</span></span>

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

### <span data-ttu-id="75934-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="75934-126">-Name</span></span>
<span data-ttu-id="75934-127">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="75934-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="75934-128">-Path</span><span class="sxs-lookup"><span data-stu-id="75934-128">-Path</span></span>
<span data-ttu-id="75934-129">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="75934-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="75934-130">Giltig sökväg börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="75934-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="75934-131">Avsökningen skickas till \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="75934-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="75934-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="75934-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="75934-133">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="75934-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="75934-134">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="75934-134">Default value is false</span></span>

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

### <span data-ttu-id="75934-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="75934-135">-Protocol</span></span>
<span data-ttu-id="75934-136">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="75934-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="75934-137">Denna cmdlet stöder endast HTTP.</span><span class="sxs-lookup"><span data-stu-id="75934-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="75934-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="75934-138">-Timeout</span></span>
<span data-ttu-id="75934-139">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="75934-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="75934-140">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="75934-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="75934-141">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75934-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="75934-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="75934-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="75934-143">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="75934-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="75934-144">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="75934-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="75934-145">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="75934-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="75934-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75934-146">-DefaultProfile</span></span>
<span data-ttu-id="75934-147">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75934-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75934-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75934-148">CommonParameters</span></span>
<span data-ttu-id="75934-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75934-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75934-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75934-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75934-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75934-151">INPUTS</span></span>

### <span data-ttu-id="75934-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75934-152">PSApplicationGateway</span></span>
<span data-ttu-id="75934-153">Parametern ' ApplicationGateway ' godkänner värdet av typen ' PSApplicationGateway ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="75934-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="75934-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75934-154">OUTPUTS</span></span>

### <span data-ttu-id="75934-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75934-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75934-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75934-156">NOTES</span></span>

## <span data-ttu-id="75934-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75934-157">RELATED LINKS</span></span>

[<span data-ttu-id="75934-158">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="75934-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="75934-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75934-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="75934-160">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75934-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="75934-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75934-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="75934-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="75934-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

