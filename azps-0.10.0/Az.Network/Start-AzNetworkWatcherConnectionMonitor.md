---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 61b23db6cfc634b318aa0070b5f784ad7067a234
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924117"
---
# <span data-ttu-id="6be90-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6be90-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6be90-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6be90-102">SYNOPSIS</span></span>
<span data-ttu-id="6be90-103">Starta en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="6be90-103">Start a connection monitor</span></span>

## <span data-ttu-id="6be90-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6be90-104">SYNTAX</span></span>

### <span data-ttu-id="6be90-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="6be90-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6be90-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6be90-106">SetByName</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6be90-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6be90-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6be90-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6be90-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="6be90-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6be90-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="6be90-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6be90-110">DESCRIPTION</span></span>
<span data-ttu-id="6be90-111">Den angivna anslutnings övervakaren startas med Start-AzNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6be90-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="6be90-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6be90-112">EXAMPLES</span></span>

### <span data-ttu-id="6be90-113">---------------Exempel 1: starta en anslutnings övervakare---------------</span><span class="sxs-lookup"><span data-stu-id="6be90-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="6be90-114">I det här exemplet startas anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="6be90-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="6be90-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6be90-115">PARAMETERS</span></span>

### <span data-ttu-id="6be90-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6be90-116">-AsJob</span></span>
<span data-ttu-id="6be90-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6be90-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6be90-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6be90-118">-Confirm</span></span>
<span data-ttu-id="6be90-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6be90-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6be90-120">-DefaultProfile</span></span>
<span data-ttu-id="6be90-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6be90-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6be90-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6be90-122">-InputObject</span></span>
<span data-ttu-id="6be90-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="6be90-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="6be90-124">-Location</span></span>
<span data-ttu-id="6be90-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="6be90-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="6be90-126">-Name</span></span>
<span data-ttu-id="6be90-127">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="6be90-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6be90-128">-NetworkWatcher</span></span>
<span data-ttu-id="6be90-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="6be90-129">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6be90-130">-NetworkWatcherName</span></span>
<span data-ttu-id="6be90-131">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="6be90-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6be90-132">-PassThru</span></span>
<span data-ttu-id="6be90-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6be90-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6be90-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6be90-134">-ResourceGroupName</span></span>
<span data-ttu-id="6be90-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6be90-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6be90-136">-ResourceId</span></span>
<span data-ttu-id="6be90-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="6be90-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6be90-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6be90-138">-WhatIf</span></span>
<span data-ttu-id="6be90-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6be90-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6be90-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6be90-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="6be90-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6be90-141">INPUTS</span></span>

### <span data-ttu-id="6be90-142">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6be90-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6be90-143">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6be90-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="6be90-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6be90-144">OUTPUTS</span></span>

### <span data-ttu-id="6be90-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6be90-145">System.Boolean</span></span>


## <span data-ttu-id="6be90-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6be90-146">NOTES</span></span>
<span data-ttu-id="6be90-147">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="6be90-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6be90-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6be90-148">RELATED LINKS</span></span>
<span data-ttu-id="6be90-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="6be90-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="6be90-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="6be90-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="6be90-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="6be90-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="6be90-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Stopp-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="6be90-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span></span>