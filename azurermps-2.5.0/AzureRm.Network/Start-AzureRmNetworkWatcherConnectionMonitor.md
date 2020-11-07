---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929277"
---
# <span data-ttu-id="91aa0-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91aa0-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="91aa0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91aa0-102">SYNOPSIS</span></span>
<span data-ttu-id="91aa0-103">Starta en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="91aa0-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91aa0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91aa0-104">SYNTAX</span></span>

### <span data-ttu-id="91aa0-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="91aa0-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91aa0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="91aa0-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91aa0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="91aa0-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91aa0-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="91aa0-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="91aa0-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="91aa0-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="91aa0-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91aa0-110">DESCRIPTION</span></span>
<span data-ttu-id="91aa0-111">Den angivna anslutnings övervakaren startas med Start-AzureRmNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91aa0-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="91aa0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91aa0-112">EXAMPLES</span></span>

### <span data-ttu-id="91aa0-113">---------------Exempel 1: starta en anslutnings övervakare---------------</span><span class="sxs-lookup"><span data-stu-id="91aa0-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="91aa0-114">I det här exemplet startas anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="91aa0-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="91aa0-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91aa0-115">PARAMETERS</span></span>

### <span data-ttu-id="91aa0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91aa0-116">-AsJob</span></span>
<span data-ttu-id="91aa0-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="91aa0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91aa0-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91aa0-118">-Confirm</span></span>
<span data-ttu-id="91aa0-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91aa0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91aa0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91aa0-120">-DefaultProfile</span></span>
<span data-ttu-id="91aa0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91aa0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91aa0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91aa0-122">-InputObject</span></span>
<span data-ttu-id="91aa0-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="91aa0-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="91aa0-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="91aa0-124">-Location</span></span>
<span data-ttu-id="91aa0-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="91aa0-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="91aa0-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="91aa0-126">-Name</span></span>
<span data-ttu-id="91aa0-127">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="91aa0-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="91aa0-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91aa0-128">-NetworkWatcher</span></span>
<span data-ttu-id="91aa0-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="91aa0-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="91aa0-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="91aa0-130">-NetworkWatcherName</span></span>
<span data-ttu-id="91aa0-131">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="91aa0-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="91aa0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91aa0-132">-PassThru</span></span>
<span data-ttu-id="91aa0-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="91aa0-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="91aa0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91aa0-134">-ResourceGroupName</span></span>
<span data-ttu-id="91aa0-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="91aa0-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="91aa0-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91aa0-136">-ResourceId</span></span>
<span data-ttu-id="91aa0-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="91aa0-137">Resource ID.</span></span>

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

### <span data-ttu-id="91aa0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91aa0-138">-WhatIf</span></span>
<span data-ttu-id="91aa0-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91aa0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91aa0-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91aa0-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="91aa0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91aa0-141">INPUTS</span></span>

### <span data-ttu-id="91aa0-142">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91aa0-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="91aa0-143">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="91aa0-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="91aa0-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91aa0-144">OUTPUTS</span></span>

### <span data-ttu-id="91aa0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="91aa0-145">System.Boolean</span></span>


## <span data-ttu-id="91aa0-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91aa0-146">NOTES</span></span>
<span data-ttu-id="91aa0-147">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="91aa0-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="91aa0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91aa0-148">RELATED LINKS</span></span>
<span data-ttu-id="91aa0-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="91aa0-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="91aa0-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="91aa0-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="91aa0-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="91aa0-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="91aa0-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Stopp-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="91aa0-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
