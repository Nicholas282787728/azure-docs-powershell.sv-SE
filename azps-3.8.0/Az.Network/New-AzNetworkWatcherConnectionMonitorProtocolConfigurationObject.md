---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088744"
---
# <span data-ttu-id="20690-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="20690-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="20690-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20690-102">SYNOPSIS</span></span>
<span data-ttu-id="20690-103">Skapa protokoll konfiguration som används för testnings utvärdering via TCP, HTTP eller ICMP.</span><span class="sxs-lookup"><span data-stu-id="20690-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="20690-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20690-104">SYNTAX</span></span>

### <span data-ttu-id="20690-105">TCP</span><span class="sxs-lookup"><span data-stu-id="20690-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20690-106">INKOMMANDE</span><span class="sxs-lookup"><span data-stu-id="20690-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20690-107">ICMP</span><span class="sxs-lookup"><span data-stu-id="20690-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20690-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20690-108">DESCRIPTION</span></span>
<span data-ttu-id="20690-109">Den New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdleten skapar en protokoll konfiguration som används för att utföra testnings utvärdering via TCP, HTTP eller ICMP.</span><span class="sxs-lookup"><span data-stu-id="20690-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="20690-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20690-110">EXAMPLES</span></span>

### <span data-ttu-id="20690-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20690-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="20690-112">Port: 80 DisableTraceRoute: false</span><span class="sxs-lookup"><span data-stu-id="20690-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="20690-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20690-113">PARAMETERS</span></span>

### <span data-ttu-id="20690-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20690-114">-DefaultProfile</span></span>
<span data-ttu-id="20690-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20690-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20690-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="20690-116">-DisableTraceRoute</span></span>
<span data-ttu-id="20690-117">Värde som anger om Sök vägs utvärdering med spårnings flöde ska inaktive ras.</span><span class="sxs-lookup"><span data-stu-id="20690-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="20690-118">-HttpProtocol</span></span>
<span data-ttu-id="20690-119">HTTP Protocol-växel</span><span class="sxs-lookup"><span data-stu-id="20690-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="20690-120">-IcmpProtocol</span></span>
<span data-ttu-id="20690-121">ICMP Protocol switch.</span><span class="sxs-lookup"><span data-stu-id="20690-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-122">-Metod</span><span class="sxs-lookup"><span data-stu-id="20690-122">-Method</span></span>
<span data-ttu-id="20690-123">Den HTTP-metod som ska användas.</span><span class="sxs-lookup"><span data-stu-id="20690-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-124">-Path</span><span class="sxs-lookup"><span data-stu-id="20690-124">-Path</span></span>
<span data-ttu-id="20690-125">Sökvägen till URI: n.</span><span class="sxs-lookup"><span data-stu-id="20690-125">The path component of the URI.</span></span> <span data-ttu-id="20690-126">Till exempel \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="20690-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-127">-Port</span><span class="sxs-lookup"><span data-stu-id="20690-127">-Port</span></span>
<span data-ttu-id="20690-128">Porten att ansluta till.</span><span class="sxs-lookup"><span data-stu-id="20690-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="20690-129">-PreferHTTPS</span></span>
<span data-ttu-id="20690-130">Värde som anger om HTTPS är önskat framför HTTP om valet inte är explicit.</span><span class="sxs-lookup"><span data-stu-id="20690-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="20690-131">-RequestHeader</span></span>
<span data-ttu-id="20690-132">HTTP-huvuden för överföring med begäran.</span><span class="sxs-lookup"><span data-stu-id="20690-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="20690-133">-TcpProtocol</span></span>
<span data-ttu-id="20690-134">TCP Protocol switch.</span><span class="sxs-lookup"><span data-stu-id="20690-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="20690-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="20690-136">Om HTTP-status är korrekta.</span><span class="sxs-lookup"><span data-stu-id="20690-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="20690-137">\"2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="20690-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20690-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20690-138">CommonParameters</span></span>
<span data-ttu-id="20690-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20690-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20690-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20690-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20690-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20690-141">INPUTS</span></span>

### <span data-ttu-id="20690-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="20690-142">None</span></span>

## <span data-ttu-id="20690-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20690-143">OUTPUTS</span></span>

### <span data-ttu-id="20690-144">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="20690-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="20690-145">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="20690-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="20690-146">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="20690-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="20690-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20690-147">NOTES</span></span>

## <span data-ttu-id="20690-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20690-148">RELATED LINKS</span></span>
