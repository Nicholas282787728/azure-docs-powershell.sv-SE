---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260716"
---
# <span data-ttu-id="9eeee-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="9eeee-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="9eeee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9eeee-102">SYNOPSIS</span></span>
<span data-ttu-id="9eeee-103">Skapa en konfiguration för test övervakning.</span><span class="sxs-lookup"><span data-stu-id="9eeee-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="9eeee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9eeee-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9eeee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9eeee-105">DESCRIPTION</span></span>
<span data-ttu-id="9eeee-106">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet skapar en konfiguration för test övervakning.</span><span class="sxs-lookup"><span data-stu-id="9eeee-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="9eeee-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9eeee-107">EXAMPLES</span></span>

### <span data-ttu-id="9eeee-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9eeee-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="9eeee-109">Namn: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443, "metod": "GET", "RequestHeaders": [{\ Name ":" Tillåt "," värde ":" GET "}]," ValidStatusCodeRanges ": [" 2xx "," 300-308 "]," PreferHTTPS ": true} SuccessThreshold: {" ChecksFailedPercent ": 20", "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="9eeee-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="9eeee-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9eeee-110">PARAMETERS</span></span>

### <span data-ttu-id="9eeee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eeee-111">-DefaultProfile</span></span>
<span data-ttu-id="9eeee-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9eeee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eeee-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="9eeee-113">-Name</span></span>
<span data-ttu-id="9eeee-114">Namnet på konfigurationen för test övervakning.</span><span class="sxs-lookup"><span data-stu-id="9eeee-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="9eeee-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="9eeee-115">-PreferredIPVersion</span></span>
<span data-ttu-id="9eeee-116">Önskad IP-version att använda i test utvärdering.</span><span class="sxs-lookup"><span data-stu-id="9eeee-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="9eeee-117">Anslutnings övervakaren kan välja att använda en annan version beroende på andra parametrar.</span><span class="sxs-lookup"><span data-stu-id="9eeee-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="9eeee-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9eeee-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="9eeee-119">De parametrar som används för att utföra testnings utvärdering i vissa protokoll.</span><span class="sxs-lookup"><span data-stu-id="9eeee-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeee-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="9eeee-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="9eeee-121">Den maximala procent andelen misslyckade kontroller som är tillåtna för ett test för utvärdering som lyckat.</span><span class="sxs-lookup"><span data-stu-id="9eeee-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeee-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="9eeee-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="9eeee-123">Den maximala tiden för fördröjning i millisekunder som är tillåtna för ett test för utvärdering som lyckat.</span><span class="sxs-lookup"><span data-stu-id="9eeee-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeee-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="9eeee-124">-TestFrequencySec</span></span>
<span data-ttu-id="9eeee-125">Frekvens för utvärdering av test, i sekunder.</span><span class="sxs-lookup"><span data-stu-id="9eeee-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeee-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9eeee-126">-Confirm</span></span>
<span data-ttu-id="9eeee-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9eeee-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeee-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eeee-128">-WhatIf</span></span>
<span data-ttu-id="9eeee-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9eeee-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eeee-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9eeee-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeee-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eeee-131">CommonParameters</span></span>
<span data-ttu-id="9eeee-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eeee-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eeee-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9eeee-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eeee-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9eeee-134">INPUTS</span></span>

### <span data-ttu-id="9eeee-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="9eeee-135">None</span></span>

## <span data-ttu-id="9eeee-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9eeee-136">OUTPUTS</span></span>

### <span data-ttu-id="9eeee-137">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="9eeee-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="9eeee-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9eeee-138">NOTES</span></span>

## <span data-ttu-id="9eeee-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9eeee-139">RELATED LINKS</span></span>