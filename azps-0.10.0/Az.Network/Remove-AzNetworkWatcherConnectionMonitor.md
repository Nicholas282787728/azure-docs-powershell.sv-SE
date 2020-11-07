---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 2f2ca6c4b9174248074cb3863c7be7de45c170c6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924382"
---
# <span data-ttu-id="1e6ec-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1e6ec-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="1e6ec-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e6ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1e6ec-103">Ta bort anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-103">Remove connection monitor.</span></span>

## <span data-ttu-id="1e6ec-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e6ec-104">SYNTAX</span></span>

### <span data-ttu-id="1e6ec-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="1e6ec-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1e6ec-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1e6ec-106">SetByName</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1e6ec-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1e6ec-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1e6ec-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e6ec-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1e6ec-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e6ec-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1e6ec-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e6ec-110">DESCRIPTION</span></span>
<span data-ttu-id="1e6ec-111">Cmdleten Remove-AzNetworkWatcherConnectionMonitor tar bort den angivna anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="1e6ec-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e6ec-112">EXAMPLES</span></span>

### <span data-ttu-id="1e6ec-113">---------------Exempel 1: ta bort den angivna anslutnings övervakaren---------------</span><span class="sxs-lookup"><span data-stu-id="1e6ec-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="1e6ec-114">I det här exemplet tar vi bort anslutnings övervakaren som anges av plats och namn.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="1e6ec-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e6ec-115">PARAMETERS</span></span>

### <span data-ttu-id="1e6ec-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e6ec-116">-AsJob</span></span>
<span data-ttu-id="1e6ec-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1e6ec-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e6ec-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e6ec-118">-Confirm</span></span>
<span data-ttu-id="1e6ec-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e6ec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e6ec-120">-DefaultProfile</span></span>
<span data-ttu-id="1e6ec-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e6ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e6ec-122">-InputObject</span></span>
<span data-ttu-id="1e6ec-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="1e6ec-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="1e6ec-124">-Location</span></span>
<span data-ttu-id="1e6ec-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1e6ec-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e6ec-126">-Name</span></span>
<span data-ttu-id="1e6ec-127">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="1e6ec-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e6ec-128">-NetworkWatcher</span></span>
<span data-ttu-id="1e6ec-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="1e6ec-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1e6ec-130">-NetworkWatcherName</span></span>
<span data-ttu-id="1e6ec-131">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="1e6ec-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e6ec-132">-PassThru</span></span>
<span data-ttu-id="1e6ec-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1e6ec-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1e6ec-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e6ec-134">-ResourceGroupName</span></span>
<span data-ttu-id="1e6ec-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1e6ec-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e6ec-136">-ResourceId</span></span>
<span data-ttu-id="1e6ec-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-137">Resource ID.</span></span>

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

### <span data-ttu-id="1e6ec-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e6ec-138">-WhatIf</span></span>
<span data-ttu-id="1e6ec-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e6ec-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e6ec-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="1e6ec-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e6ec-141">INPUTS</span></span>

### <span data-ttu-id="1e6ec-142">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e6ec-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1e6ec-143">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="1e6ec-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="1e6ec-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e6ec-144">OUTPUTS</span></span>

### <span data-ttu-id="1e6ec-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e6ec-145">System.Boolean</span></span>


## <span data-ttu-id="1e6ec-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e6ec-146">NOTES</span></span>
<span data-ttu-id="1e6ec-147">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="1e6ec-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="1e6ec-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e6ec-148">RELATED LINKS</span></span>
<span data-ttu-id="1e6ec-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="1e6ec-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="1e6ec-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="1e6ec-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="1e6ec-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="1e6ec-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="1e6ec-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="1e6ec-152">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>

