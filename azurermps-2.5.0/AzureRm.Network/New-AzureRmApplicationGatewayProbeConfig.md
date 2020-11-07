---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 0e3c0c9a3f1c47163a28dc1732ef488f87014c63
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928734"
---
# <span data-ttu-id="48375-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48375-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="48375-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48375-102">SYNOPSIS</span></span>
<span data-ttu-id="48375-103">Skapar en hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="48375-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48375-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48375-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48375-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48375-105">DESCRIPTION</span></span>
<span data-ttu-id="48375-106">New-AzureRmApplicationGatewayProbeConfig cmdlet skapar en hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="48375-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="48375-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48375-107">EXAMPLES</span></span>

### <span data-ttu-id="48375-108">Example1: skapa en hälso kontroll</span><span class="sxs-lookup"><span data-stu-id="48375-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="48375-109">Det här kommandot skapar en hälso Avsök med namnet Probe03, med HTTP-protokoll, ett 30 sekunder, timeout på 120 sekunder och en fel tröskel på 8 försök.</span><span class="sxs-lookup"><span data-stu-id="48375-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="48375-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48375-110">PARAMETERS</span></span>

### <span data-ttu-id="48375-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48375-111">-DefaultProfile</span></span>
<span data-ttu-id="48375-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48375-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48375-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="48375-113">-HostName</span></span>
<span data-ttu-id="48375-114">Anger värd namnet som den här cmdleten skickar.</span><span class="sxs-lookup"><span data-stu-id="48375-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="48375-115">-Intervall</span><span class="sxs-lookup"><span data-stu-id="48375-115">-Interval</span></span>
<span data-ttu-id="48375-116">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="48375-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="48375-117">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="48375-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="48375-118">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48375-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="48375-119">-Passa</span><span class="sxs-lookup"><span data-stu-id="48375-119">-Match</span></span>
<span data-ttu-id="48375-120">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="48375-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="48375-121">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="48375-121">Default value is empty</span></span>

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

### <span data-ttu-id="48375-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="48375-122">-MinServers</span></span>
<span data-ttu-id="48375-123">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="48375-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="48375-124">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="48375-124">Default value is 0</span></span>

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

### <span data-ttu-id="48375-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="48375-125">-Name</span></span>
<span data-ttu-id="48375-126">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="48375-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="48375-127">-Path</span><span class="sxs-lookup"><span data-stu-id="48375-127">-Path</span></span>
<span data-ttu-id="48375-128">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="48375-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="48375-129">Giltiga sökvägar börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="48375-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="48375-130">Avsökningen skickas till \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="48375-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="48375-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="48375-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="48375-132">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="48375-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="48375-133">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="48375-133">Default value is false</span></span>

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

### <span data-ttu-id="48375-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="48375-134">-Protocol</span></span>
<span data-ttu-id="48375-135">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="48375-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="48375-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="48375-136">-Timeout</span></span>
<span data-ttu-id="48375-137">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="48375-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="48375-138">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="48375-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="48375-139">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48375-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="48375-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="48375-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="48375-141">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="48375-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="48375-142">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="48375-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="48375-143">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="48375-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="48375-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48375-144">CommonParameters</span></span>
<span data-ttu-id="48375-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48375-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48375-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48375-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48375-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48375-147">INPUTS</span></span>

## <span data-ttu-id="48375-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48375-148">OUTPUTS</span></span>

### <span data-ttu-id="48375-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="48375-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="48375-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48375-150">NOTES</span></span>

## <span data-ttu-id="48375-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48375-151">RELATED LINKS</span></span>

[<span data-ttu-id="48375-152">Skapa anpassad avsökning för Application Gateway med PowerShell för Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="48375-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="48375-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48375-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="48375-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48375-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="48375-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48375-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="48375-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="48375-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

