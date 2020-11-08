---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5b5d7cff963a8f2a5322f67f31cfb31166f75aa9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090824"
---
# <span data-ttu-id="ebf30-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ebf30-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ebf30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebf30-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf30-103">Uppdaterar anslutnings övervaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="ebf30-103">Updates connection monitor resource.</span></span>

## <span data-ttu-id="ebf30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebf30-104">SYNTAX</span></span>

### <span data-ttu-id="ebf30-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="ebf30-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebf30-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ebf30-106">SetByResource</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebf30-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="ebf30-107">SetByResourceV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf30-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="ebf30-108">SetByNameV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf30-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ebf30-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf30-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="ebf30-110">SetByLocationV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf30-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf30-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf30-112">SetByResourceIdV2</span><span class="sxs-lookup"><span data-stu-id="ebf30-112">SetByResourceIdV2</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String>
 -TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>
 -Output <PSNetworkWatcherConnectionMonitorOutputObject[]> -Note <String> -Tag <Hashtable> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebf30-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ebf30-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebf30-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebf30-114">DESCRIPTION</span></span>
<span data-ttu-id="ebf30-115">Set-AzNetworkWatcherConnectionMonitor cmdlet uppdaterar anslutnings övervaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="ebf30-115">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates connection monitor resource.</span></span>

## <span data-ttu-id="ebf30-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebf30-116">EXAMPLES</span></span>

### <span data-ttu-id="ebf30-117">Exempel 1: uppdatera en anslutnings bildskärm</span><span class="sxs-lookup"><span data-stu-id="ebf30-117">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="ebf30-118">I det här exemplet uppdaterar vi den befintliga anslutnings övervakningen genom att ändra destinationAddress och lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="ebf30-118">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="ebf30-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebf30-119">PARAMETERS</span></span>

### <span data-ttu-id="ebf30-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebf30-120">-AsJob</span></span>
<span data-ttu-id="ebf30-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ebf30-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebf30-122">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="ebf30-122">-ConfigureOnly</span></span>
<span data-ttu-id="ebf30-123">Konfigurera anslutnings övervakaren men starta den inte</span><span class="sxs-lookup"><span data-stu-id="ebf30-123">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf30-124">-DefaultProfile</span></span>
<span data-ttu-id="ebf30-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf30-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebf30-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="ebf30-126">-DestinationAddress</span></span>
<span data-ttu-id="ebf30-127">Adress för anslutnings övervakarens destination (IP eller domän namn).</span><span class="sxs-lookup"><span data-stu-id="ebf30-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="ebf30-128">-DestinationPort</span></span>
<span data-ttu-id="ebf30-129">Målport som används av anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="ebf30-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf30-130">-DestinationResourceId</span></span>
<span data-ttu-id="ebf30-131">ID för resursen som används som mål för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="ebf30-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ebf30-132">-Force</span></span>
<span data-ttu-id="ebf30-133">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="ebf30-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ebf30-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebf30-134">-InputObject</span></span>
<span data-ttu-id="ebf30-135">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="ebf30-135">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="ebf30-136">-Location</span></span>
<span data-ttu-id="ebf30-137">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="ebf30-137">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-138">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ebf30-138">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="ebf30-139">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="ebf30-139">Monitoring interval in seconds.</span></span> <span data-ttu-id="ebf30-140">Standardvärdet är 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="ebf30-140">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="ebf30-141">-Name</span></span>
<span data-ttu-id="ebf30-142">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="ebf30-142">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-143">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ebf30-143">-NetworkWatcher</span></span>
<span data-ttu-id="ebf30-144">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="ebf30-144">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-145">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ebf30-145">-NetworkWatcherName</span></span>
<span data-ttu-id="ebf30-146">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="ebf30-146">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-147">-Obs!</span><span class="sxs-lookup"><span data-stu-id="ebf30-147">-Note</span></span>
<span data-ttu-id="ebf30-148">Anteckningar som är kopplade till anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="ebf30-148">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-149">-Utdata</span><span class="sxs-lookup"><span data-stu-id="ebf30-149">-Output</span></span>
<span data-ttu-id="ebf30-150">Beskriver ett mål för att ansluta till en anslutning</span><span class="sxs-lookup"><span data-stu-id="ebf30-150">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf30-151">-ResourceGroupName</span></span>
<span data-ttu-id="ebf30-152">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ebf30-152">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf30-153">-ResourceId</span></span>
<span data-ttu-id="ebf30-154">ConnectionMonitor resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ebf30-154">ConnectionMonitor resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-155">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="ebf30-155">-SourcePort</span></span>
<span data-ttu-id="ebf30-156">Käll porten som används av anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="ebf30-156">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ebf30-157">-SourceResourceId</span></span>
<span data-ttu-id="ebf30-158">ID för resursen som används som källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="ebf30-158">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-159">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ebf30-159">-Tag</span></span>
<span data-ttu-id="ebf30-160">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="ebf30-160">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByResourceId, SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-161">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="ebf30-161">-TestGroup</span></span>
<span data-ttu-id="ebf30-162">Listan med test grupper.</span><span class="sxs-lookup"><span data-stu-id="ebf30-162">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceIdV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf30-163">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ebf30-163">-Confirm</span></span>
<span data-ttu-id="ebf30-164">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ebf30-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebf30-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebf30-165">-WhatIf</span></span>
<span data-ttu-id="ebf30-166">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ebf30-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebf30-167">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ebf30-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebf30-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf30-168">CommonParameters</span></span>
<span data-ttu-id="ebf30-169">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf30-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf30-170">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebf30-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf30-171">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebf30-171">INPUTS</span></span>

### <span data-ttu-id="ebf30-172">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ebf30-172">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ebf30-173">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf30-173">System.String</span></span>

### <span data-ttu-id="ebf30-174">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ebf30-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ebf30-175">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebf30-175">OUTPUTS</span></span>

### <span data-ttu-id="ebf30-176">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="ebf30-176">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="ebf30-177">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="ebf30-177">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="ebf30-178">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebf30-178">NOTES</span></span>

## <span data-ttu-id="ebf30-179">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebf30-179">RELATED LINKS</span></span>