---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: f394d5aadb743f4439f3bda4cd5522f26f719516
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089517"
---
# <span data-ttu-id="0e138-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="0e138-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="0e138-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e138-102">SYNOPSIS</span></span>
<span data-ttu-id="0e138-103">Skapa en konfiguration för test övervakning.</span><span class="sxs-lookup"><span data-stu-id="0e138-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="0e138-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e138-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Int32>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e138-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e138-105">DESCRIPTION</span></span>
<span data-ttu-id="0e138-106">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet skapar en konfiguration för test övervakning.</span><span class="sxs-lookup"><span data-stu-id="0e138-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="0e138-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e138-107">EXAMPLES</span></span>

### <span data-ttu-id="0e138-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e138-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="0e138-109">Namn: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443, "metod": "GET", "RequestHeaders": [{\ Name ":" Tillåt "," värde ":" GET "}]," ValidStatusCodeRanges ": [" 2xx "," 300-308 "]," PreferHTTPS ": true} SuccessThreshold: {" ChecksFailedPercent ": 20", "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="0e138-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="0e138-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e138-110">PARAMETERS</span></span>

### <span data-ttu-id="0e138-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e138-111">-DefaultProfile</span></span>
<span data-ttu-id="0e138-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e138-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e138-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e138-113">-Name</span></span>
<span data-ttu-id="0e138-114">Namnet på konfigurationen för test övervakning.</span><span class="sxs-lookup"><span data-stu-id="0e138-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="0e138-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="0e138-115">-PreferredIPVersion</span></span>
<span data-ttu-id="0e138-116">Önskad IP-version att använda i test utvärdering.</span><span class="sxs-lookup"><span data-stu-id="0e138-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="0e138-117">Anslutnings övervakaren kan välja att använda en annan version beroende på andra parametrar.</span><span class="sxs-lookup"><span data-stu-id="0e138-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="0e138-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e138-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="0e138-119">De parametrar som används för att utföra testnings utvärdering i vissa protokoll.</span><span class="sxs-lookup"><span data-stu-id="0e138-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="0e138-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="0e138-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="0e138-121">Den maximala procent andelen misslyckade kontroller som är tillåtna för ett test för utvärdering som lyckat.</span><span class="sxs-lookup"><span data-stu-id="0e138-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="0e138-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="0e138-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="0e138-123">Den maximala tiden för fördröjning i millisekunder som är tillåtna för ett test för utvärdering som lyckat.</span><span class="sxs-lookup"><span data-stu-id="0e138-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="0e138-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="0e138-124">-TestFrequencySec</span></span>
<span data-ttu-id="0e138-125">Frekvens för utvärdering av test, i sekunder.</span><span class="sxs-lookup"><span data-stu-id="0e138-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="0e138-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e138-126">-Confirm</span></span>
<span data-ttu-id="0e138-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e138-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e138-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e138-128">-WhatIf</span></span>
<span data-ttu-id="0e138-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e138-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e138-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e138-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e138-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e138-131">CommonParameters</span></span>
<span data-ttu-id="0e138-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e138-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e138-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e138-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e138-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e138-134">INPUTS</span></span>

### <span data-ttu-id="0e138-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="0e138-135">None</span></span>

## <span data-ttu-id="0e138-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e138-136">OUTPUTS</span></span>

### <span data-ttu-id="0e138-137">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="0e138-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="0e138-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e138-138">NOTES</span></span>

## <span data-ttu-id="0e138-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e138-139">RELATED LINKS</span></span>
