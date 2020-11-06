---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: a41daa12a126e768a4cc7842a72b031d4ca7a759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583247"
---
# <span data-ttu-id="0ab27-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0ab27-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0ab27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ab27-102">SYNOPSIS</span></span>
<span data-ttu-id="0ab27-103">Skapar en hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="0ab27-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ab27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ab27-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ab27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ab27-105">DESCRIPTION</span></span>
<span data-ttu-id="0ab27-106">New-AzureRmApplicationGatewayProbeConfig cmdlet skapar en hälso sökning.</span><span class="sxs-lookup"><span data-stu-id="0ab27-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="0ab27-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ab27-107">EXAMPLES</span></span>

### <span data-ttu-id="0ab27-108">Example1: skapa en hälso kontroll</span><span class="sxs-lookup"><span data-stu-id="0ab27-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="0ab27-109">Det här kommandot skapar en hälso Avsök med namnet Probe03, med HTTP-protokoll, ett 30 sekunder, timeout på 120 sekunder och en fel tröskel på 8 försök.</span><span class="sxs-lookup"><span data-stu-id="0ab27-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="0ab27-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ab27-110">PARAMETERS</span></span>

### <span data-ttu-id="0ab27-111">-HostName</span><span class="sxs-lookup"><span data-stu-id="0ab27-111">-HostName</span></span>
<span data-ttu-id="0ab27-112">Anger värd namnet som den här cmdleten skickar.</span><span class="sxs-lookup"><span data-stu-id="0ab27-112">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="0ab27-113">-Intervall</span><span class="sxs-lookup"><span data-stu-id="0ab27-113">-Interval</span></span>
<span data-ttu-id="0ab27-114">Anger avsöknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0ab27-114">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="0ab27-115">Det här är tidsintervallet mellan två efterföljande sonder.</span><span class="sxs-lookup"><span data-stu-id="0ab27-115">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="0ab27-116">Värdet är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0ab27-116">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0ab27-117">-Passa</span><span class="sxs-lookup"><span data-stu-id="0ab27-117">-Match</span></span>
<span data-ttu-id="0ab27-118">Brödtext som måste ingå i sjukvården.</span><span class="sxs-lookup"><span data-stu-id="0ab27-118">Body that must be contained in the health response.</span></span>
<span data-ttu-id="0ab27-119">Standardvärdet är inte ifyllt</span><span class="sxs-lookup"><span data-stu-id="0ab27-119">Default value is empty</span></span>

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

### <span data-ttu-id="0ab27-120">-MinServers</span><span class="sxs-lookup"><span data-stu-id="0ab27-120">-MinServers</span></span>
<span data-ttu-id="0ab27-121">Minsta antal servrar som alltid har marker ATS som friska.</span><span class="sxs-lookup"><span data-stu-id="0ab27-121">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="0ab27-122">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="0ab27-122">Default value is 0</span></span>

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

### <span data-ttu-id="0ab27-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ab27-123">-Name</span></span>
<span data-ttu-id="0ab27-124">Anger namnet på sonden.</span><span class="sxs-lookup"><span data-stu-id="0ab27-124">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0ab27-125">-Path</span><span class="sxs-lookup"><span data-stu-id="0ab27-125">-Path</span></span>
<span data-ttu-id="0ab27-126">Anger den relativa sökvägen för sonden.</span><span class="sxs-lookup"><span data-stu-id="0ab27-126">Specifies the relative path of probe.</span></span>
<span data-ttu-id="0ab27-127">Giltiga sökvägar börjar med snedstreck (/).</span><span class="sxs-lookup"><span data-stu-id="0ab27-127">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="0ab27-128">Avsökningen skickas till \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="0ab27-128">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="0ab27-129">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0ab27-129">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="0ab27-130">Om värd huvudet ska hämtas från Server delens http-inställningar.</span><span class="sxs-lookup"><span data-stu-id="0ab27-130">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="0ab27-131">Standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="0ab27-131">Default value is false</span></span>

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

### <span data-ttu-id="0ab27-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0ab27-132">-Protocol</span></span>
<span data-ttu-id="0ab27-133">Anger det protokoll som används för att skicka avsökning.</span><span class="sxs-lookup"><span data-stu-id="0ab27-133">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="0ab27-134">-Timeout</span><span class="sxs-lookup"><span data-stu-id="0ab27-134">-Timeout</span></span>
<span data-ttu-id="0ab27-135">Anger timeout för avsökning i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0ab27-135">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="0ab27-136">Denna cmdlet markerar avsökningen som misslyckad om ett giltigt svar inte tas emot med denna tids gräns.</span><span class="sxs-lookup"><span data-stu-id="0ab27-136">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="0ab27-137">Giltiga värden är mellan 1 sekund och 86400 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0ab27-137">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0ab27-138">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="0ab27-138">-UnhealthyThreshold</span></span>
<span data-ttu-id="0ab27-139">Anger antal försök för avsökning.</span><span class="sxs-lookup"><span data-stu-id="0ab27-139">Specifies the probe retry count.</span></span>
<span data-ttu-id="0ab27-140">Backend-servern är avmarkerad efter att det efterföljande avsöknings felet når fel tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="0ab27-140">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="0ab27-141">Giltiga värden är mellan 1 och 20 sekunder.</span><span class="sxs-lookup"><span data-stu-id="0ab27-141">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="0ab27-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ab27-142">-DefaultProfile</span></span>
<span data-ttu-id="0ab27-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ab27-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ab27-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ab27-144">CommonParameters</span></span>
<span data-ttu-id="0ab27-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ab27-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ab27-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ab27-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ab27-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ab27-147">INPUTS</span></span>

## <span data-ttu-id="0ab27-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ab27-148">OUTPUTS</span></span>

### <span data-ttu-id="0ab27-149">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="0ab27-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="0ab27-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ab27-150">NOTES</span></span>

## <span data-ttu-id="0ab27-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ab27-151">RELATED LINKS</span></span>

[<span data-ttu-id="0ab27-152">Skapa anpassad avsökning för Application Gateway med PowerShell för Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="0ab27-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="0ab27-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0ab27-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0ab27-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0ab27-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0ab27-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0ab27-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0ab27-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0ab27-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

