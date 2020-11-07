---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: f69910140f2bd7b57a30bd413c74e6f26e646787
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924102"
---
# <span data-ttu-id="10edb-101">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="10edb-101">Stop-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="10edb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10edb-102">SYNOPSIS</span></span>
<span data-ttu-id="10edb-103">Stoppa en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="10edb-103">Stop a connection monitor</span></span>

## <span data-ttu-id="10edb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10edb-104">SYNTAX</span></span>

### <span data-ttu-id="10edb-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="10edb-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="10edb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="10edb-106">SetByName</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="10edb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="10edb-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="10edb-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10edb-108">SetByResourceId</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="10edb-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="10edb-109">SetByInputObject</span></span>
```
Stop-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="10edb-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10edb-110">DESCRIPTION</span></span>
<span data-ttu-id="10edb-111">Stop-AzNetworkWatcherConnectionMonitor cmdlet stoppar den angivna anslutnings skärmen.</span><span class="sxs-lookup"><span data-stu-id="10edb-111">The Stop-AzNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="10edb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10edb-112">EXAMPLES</span></span>

### <span data-ttu-id="10edb-113">---------------Exempel 1: stoppa en anslutnings övervakare---------------</span><span class="sxs-lookup"><span data-stu-id="10edb-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="10edb-114">I det här exemplet stoppar vi anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="10edb-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="10edb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10edb-115">PARAMETERS</span></span>

### <span data-ttu-id="10edb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10edb-116">-AsJob</span></span>
<span data-ttu-id="10edb-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="10edb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10edb-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10edb-118">-Confirm</span></span>
<span data-ttu-id="10edb-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10edb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10edb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10edb-120">-DefaultProfile</span></span>
<span data-ttu-id="10edb-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10edb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10edb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10edb-122">-InputObject</span></span>
<span data-ttu-id="10edb-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="10edb-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="10edb-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="10edb-124">-Location</span></span>
<span data-ttu-id="10edb-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="10edb-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="10edb-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="10edb-126">-Name</span></span>
<span data-ttu-id="10edb-127">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="10edb-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="10edb-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10edb-128">-NetworkWatcher</span></span>
<span data-ttu-id="10edb-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="10edb-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="10edb-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="10edb-130">-NetworkWatcherName</span></span>
<span data-ttu-id="10edb-131">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="10edb-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="10edb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10edb-132">-PassThru</span></span>
<span data-ttu-id="10edb-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="10edb-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="10edb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10edb-134">-ResourceGroupName</span></span>
<span data-ttu-id="10edb-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="10edb-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="10edb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10edb-136">-ResourceId</span></span>
<span data-ttu-id="10edb-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="10edb-137">Resource ID.</span></span>

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

### <span data-ttu-id="10edb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10edb-138">-WhatIf</span></span>
<span data-ttu-id="10edb-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10edb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10edb-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10edb-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="10edb-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10edb-141">INPUTS</span></span>

### <span data-ttu-id="10edb-142">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="10edb-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="10edb-143">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="10edb-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="10edb-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10edb-144">OUTPUTS</span></span>

### <span data-ttu-id="10edb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="10edb-145">System.Boolean</span></span>


## <span data-ttu-id="10edb-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10edb-146">NOTES</span></span>
<span data-ttu-id="10edb-147">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="10edb-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="10edb-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10edb-148">RELATED LINKS</span></span>
<span data-ttu-id="10edb-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="10edb-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="10edb-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="10edb-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="10edb-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="10edb-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="10edb-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="10edb-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>