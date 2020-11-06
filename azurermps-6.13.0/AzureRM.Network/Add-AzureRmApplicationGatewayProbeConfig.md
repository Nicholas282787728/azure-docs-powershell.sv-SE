---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 3942705083c6181ae3ddc7eb9961eb3580fa97bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576920"
---
# <span data-ttu-id="48ca8-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48ca8-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="48ca8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="48ca8-103">Lägger till en hälso sökning i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="48ca8-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48ca8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48ca8-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48ca8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48ca8-105">DESCRIPTION</span></span>
<span data-ttu-id="48ca8-106">Add-AzureRmApplicationGatewayProbeConfig cmdlet lägger till en hälso sökning i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="48ca8-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="48ca8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48ca8-107">EXAMPLES</span></span>

### <span data-ttu-id="48ca8-108">Exempel 1: lägga till en hälso kontroll i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="48ca8-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="48ca8-109">Det här kommandot lägger till en hälso sökning med namnet Probe01 för programgatewayen med namnet Gateway.</span><span class="sxs-lookup"><span data-stu-id="48ca8-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="48ca8-110">Kommandot anger också tröskelvärdet för fel till 8 försök och timeout efter 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="48ca8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48ca8-111">PARAMETERS</span></span>

### <span data-ttu-id="48ca8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48ca8-112">-ApplicationGateway</span></span>
<span data-ttu-id="48ca8-113">Anger den Programgateway som denna cmdlet lägger till en sond för.</span><span class="sxs-lookup"><span data-stu-id="48ca8-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="48ca8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ca8-114">-DefaultProfile</span></span>
<span data-ttu-id="48ca8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48ca8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48ca8-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="48ca8-116">-HostName</span></span>
<span data-ttu-id="48ca8-117">Anger det värdnamn som den här cmdleten skickar sonden till.</span><span class="sxs-lookup"><span data-stu-id="48ca8-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="48ca8-118">-Intervall</span><span class="sxs-lookup"><span data-stu-id="48ca8-118">-Interval</span></span>
<span data-ttu-id="48ca8-119">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="48ca8-120">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="48ca8-121">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="48ca8-122">-Passa</span><span class="sxs-lookup"><span data-stu-id="48ca8-122">-Match</span></span>
<span data-ttu-id="48ca8-123">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="48ca8-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="48ca8-124">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="48ca8-124">Default value is empty</span></span>

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

### <span data-ttu-id="48ca8-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="48ca8-125">-MinServers</span></span>
<span data-ttu-id="48ca8-126">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="48ca8-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="48ca8-127">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="48ca8-127">Default value is 0</span></span>

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

### <span data-ttu-id="48ca8-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="48ca8-128">-Name</span></span>
<span data-ttu-id="48ca8-129">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="48ca8-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="48ca8-130">-Path</span><span class="sxs-lookup"><span data-stu-id="48ca8-130">-Path</span></span>
<span data-ttu-id="48ca8-131">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="48ca8-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="48ca8-132">Giltig sökväg börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="48ca8-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="48ca8-133">Avsökningen skickas till \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="48ca8-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="48ca8-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="48ca8-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="48ca8-135">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="48ca8-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="48ca8-136">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="48ca8-136">Default value is false</span></span>

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

### <span data-ttu-id="48ca8-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="48ca8-137">-Protocol</span></span>
<span data-ttu-id="48ca8-138">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="48ca8-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="48ca8-139">Denna cmdlet stöder endast HTTP.</span><span class="sxs-lookup"><span data-stu-id="48ca8-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="48ca8-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="48ca8-140">-Timeout</span></span>
<span data-ttu-id="48ca8-141">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="48ca8-142">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="48ca8-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="48ca8-143">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="48ca8-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="48ca8-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="48ca8-145">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="48ca8-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="48ca8-146">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="48ca8-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="48ca8-147">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48ca8-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="48ca8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ca8-148">CommonParameters</span></span>
<span data-ttu-id="48ca8-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ca8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ca8-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48ca8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ca8-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48ca8-151">INPUTS</span></span>

### <span data-ttu-id="48ca8-152">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48ca8-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="48ca8-153">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48ca8-153">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="48ca8-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48ca8-154">OUTPUTS</span></span>

### <span data-ttu-id="48ca8-155">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48ca8-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48ca8-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48ca8-156">NOTES</span></span>

## <span data-ttu-id="48ca8-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48ca8-157">RELATED LINKS</span></span>

[<span data-ttu-id="48ca8-158">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="48ca8-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="48ca8-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48ca8-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="48ca8-160">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48ca8-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="48ca8-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48ca8-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="48ca8-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48ca8-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

