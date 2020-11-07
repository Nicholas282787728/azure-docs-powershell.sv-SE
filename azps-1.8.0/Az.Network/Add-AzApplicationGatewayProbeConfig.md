---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 25db1c941975111cdf000ce142519e90f08cd101
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753969"
---
# <span data-ttu-id="fad61-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad61-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fad61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fad61-102">SYNOPSIS</span></span>
<span data-ttu-id="fad61-103">Lägger till en hälso sökning i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fad61-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="fad61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fad61-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fad61-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fad61-105">DESCRIPTION</span></span>
<span data-ttu-id="fad61-106">Add-AzApplicationGatewayProbeConfig cmdlet lägger till en hälso sökning i en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fad61-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="fad61-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fad61-107">EXAMPLES</span></span>

### <span data-ttu-id="fad61-108">Exempel 1: lägga till en hälso kontroll i en Programgateway</span><span class="sxs-lookup"><span data-stu-id="fad61-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="fad61-109">Det här kommandot lägger till en hälso sökning med namnet Probe01 för programgatewayen med namnet Gateway.</span><span class="sxs-lookup"><span data-stu-id="fad61-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="fad61-110">Kommandot anger också tröskelvärdet för fel till 8 försök och timeout efter 120 sekunder.</span><span class="sxs-lookup"><span data-stu-id="fad61-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="fad61-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fad61-111">PARAMETERS</span></span>

### <span data-ttu-id="fad61-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad61-112">-ApplicationGateway</span></span>
<span data-ttu-id="fad61-113">Anger den Programgateway som denna cmdlet lägger till en sond för.</span><span class="sxs-lookup"><span data-stu-id="fad61-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="fad61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad61-114">-DefaultProfile</span></span>
<span data-ttu-id="fad61-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fad61-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fad61-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="fad61-116">-HostName</span></span>
<span data-ttu-id="fad61-117">Anger det värdnamn som den här cmdleten skickar sonden till.</span><span class="sxs-lookup"><span data-stu-id="fad61-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="fad61-118">-Intervall</span><span class="sxs-lookup"><span data-stu-id="fad61-118">-Interval</span></span>
<span data-ttu-id="fad61-119">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="fad61-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="fad61-120">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="fad61-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="fad61-121">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="fad61-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fad61-122">-Passa</span><span class="sxs-lookup"><span data-stu-id="fad61-122">-Match</span></span>
<span data-ttu-id="fad61-123">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="fad61-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="fad61-124">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="fad61-124">Default value is empty</span></span>

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

### <span data-ttu-id="fad61-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="fad61-125">-MinServers</span></span>
<span data-ttu-id="fad61-126">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="fad61-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="fad61-127">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="fad61-127">Default value is 0</span></span>

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

### <span data-ttu-id="fad61-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="fad61-128">-Name</span></span>
<span data-ttu-id="fad61-129">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="fad61-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="fad61-130">-Path</span><span class="sxs-lookup"><span data-stu-id="fad61-130">-Path</span></span>
<span data-ttu-id="fad61-131">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="fad61-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="fad61-132">Giltig sökväg börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="fad61-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="fad61-133">Avsökningen skickas till \< protokoll \> :// \< värd \> : \< port \> \< Sök väg \> .</span><span class="sxs-lookup"><span data-stu-id="fad61-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="fad61-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fad61-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="fad61-135">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="fad61-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="fad61-136">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="fad61-136">Default value is false</span></span>

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

### <span data-ttu-id="fad61-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="fad61-137">-Protocol</span></span>
<span data-ttu-id="fad61-138">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="fad61-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="fad61-139">Denna cmdlet stöder endast HTTP.</span><span class="sxs-lookup"><span data-stu-id="fad61-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="fad61-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="fad61-140">-Timeout</span></span>
<span data-ttu-id="fad61-141">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="fad61-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="fad61-142">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="fad61-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="fad61-143">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="fad61-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="fad61-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="fad61-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="fad61-145">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="fad61-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="fad61-146">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="fad61-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="fad61-147">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="fad61-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="fad61-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad61-148">CommonParameters</span></span>
<span data-ttu-id="fad61-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad61-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad61-150">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad61-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad61-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fad61-151">INPUTS</span></span>

### <span data-ttu-id="fad61-152">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad61-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fad61-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fad61-153">OUTPUTS</span></span>

### <span data-ttu-id="fad61-154">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fad61-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fad61-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fad61-155">NOTES</span></span>

## <span data-ttu-id="fad61-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fad61-156">RELATED LINKS</span></span>

[<span data-ttu-id="fad61-157">Lägga till en sond i en befintlig Application Gateway</span><span class="sxs-lookup"><span data-stu-id="fad61-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="fad61-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad61-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fad61-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad61-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fad61-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad61-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fad61-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fad61-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)
