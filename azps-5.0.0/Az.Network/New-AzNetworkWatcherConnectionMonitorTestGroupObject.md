---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324576"
---
# <span data-ttu-id="48681-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="48681-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="48681-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48681-102">SYNOPSIS</span></span>
<span data-ttu-id="48681-103">Skapa en test grupp för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="48681-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="48681-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48681-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48681-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48681-105">DESCRIPTION</span></span>
<span data-ttu-id="48681-106">Med cmdleten New-AzNetworkWatcherConnectionMonitorTestGroupObject skapar du en test grupp för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="48681-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="48681-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48681-107">EXAMPLES</span></span>

### <span data-ttu-id="48681-108">Exempel 1: skapa en test grupp med 2 testConfigurations, w Source och 2 mål slut punkter</span><span class="sxs-lookup"><span data-stu-id="48681-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="48681-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48681-109">PARAMETERS</span></span>

### <span data-ttu-id="48681-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48681-110">-DefaultProfile</span></span>
<span data-ttu-id="48681-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48681-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48681-112">-Mål</span><span class="sxs-lookup"><span data-stu-id="48681-112">-Destination</span></span>
<span data-ttu-id="48681-113">Lista över mål slut punkter.</span><span class="sxs-lookup"><span data-stu-id="48681-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48681-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="48681-114">-Disable</span></span>
<span data-ttu-id="48681-115">Flagga som anger om test gruppen är inaktive rad.</span><span class="sxs-lookup"><span data-stu-id="48681-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="48681-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="48681-116">-Name</span></span>
<span data-ttu-id="48681-117">Test gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="48681-117">The test group name.</span></span>

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

### <span data-ttu-id="48681-118">-Källa</span><span class="sxs-lookup"><span data-stu-id="48681-118">-Source</span></span>
<span data-ttu-id="48681-119">Lista över käll slut punkter.</span><span class="sxs-lookup"><span data-stu-id="48681-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48681-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="48681-120">-TestConfiguration</span></span>
<span data-ttu-id="48681-121">Lista över test konfiguration.</span><span class="sxs-lookup"><span data-stu-id="48681-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48681-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48681-122">-Confirm</span></span>
<span data-ttu-id="48681-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48681-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48681-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48681-124">-WhatIf</span></span>
<span data-ttu-id="48681-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="48681-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48681-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="48681-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48681-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48681-127">CommonParameters</span></span>
<span data-ttu-id="48681-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48681-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48681-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48681-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48681-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48681-130">INPUTS</span></span>

### <span data-ttu-id="48681-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="48681-131">None</span></span>

## <span data-ttu-id="48681-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48681-132">OUTPUTS</span></span>

### <span data-ttu-id="48681-133">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="48681-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="48681-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48681-134">NOTES</span></span>

## <span data-ttu-id="48681-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48681-135">RELATED LINKS</span></span>
