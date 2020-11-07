---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: cf67e27a8f502a753cded74f0cb5bf48ceb2d4ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755596"
---
# <span data-ttu-id="5ca01-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca01-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="5ca01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ca01-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca01-103">Starta en anslutnings övervakare</span><span class="sxs-lookup"><span data-stu-id="5ca01-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ca01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ca01-104">SYNTAX</span></span>

### <span data-ttu-id="5ca01-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="5ca01-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ca01-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5ca01-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca01-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5ca01-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca01-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca01-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca01-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ca01-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca01-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ca01-110">DESCRIPTION</span></span>
<span data-ttu-id="5ca01-111">Den angivna anslutnings övervakaren startas med Start-AzureRmNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ca01-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="5ca01-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ca01-112">EXAMPLES</span></span>

### <span data-ttu-id="5ca01-113">Exempel 1: starta en anslutnings bildskärm</span><span class="sxs-lookup"><span data-stu-id="5ca01-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="5ca01-114">I det här exemplet startas anslutnings övervakaren som anges med namn och nätverks bevakning</span><span class="sxs-lookup"><span data-stu-id="5ca01-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="5ca01-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ca01-115">PARAMETERS</span></span>

### <span data-ttu-id="5ca01-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ca01-116">-AsJob</span></span>
<span data-ttu-id="5ca01-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5ca01-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5ca01-118">-Confirm</span></span>
<span data-ttu-id="5ca01-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5ca01-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca01-120">-DefaultProfile</span></span>
<span data-ttu-id="5ca01-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca01-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca01-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ca01-122">-InputObject</span></span>
<span data-ttu-id="5ca01-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="5ca01-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="5ca01-124">-Location</span></span>
<span data-ttu-id="5ca01-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="5ca01-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ca01-126">-Name</span></span>
<span data-ttu-id="5ca01-127">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="5ca01-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ca01-128">-NetworkWatcher</span></span>
<span data-ttu-id="5ca01-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="5ca01-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="5ca01-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5ca01-130">-NetworkWatcherName</span></span>
<span data-ttu-id="5ca01-131">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="5ca01-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ca01-132">-PassThru</span></span>
<span data-ttu-id="5ca01-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5ca01-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca01-134">-ResourceGroupName</span></span>
<span data-ttu-id="5ca01-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5ca01-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca01-136">-ResourceId</span></span>
<span data-ttu-id="5ca01-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="5ca01-137">Resource ID.</span></span>

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

### <span data-ttu-id="5ca01-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca01-138">-WhatIf</span></span>
<span data-ttu-id="5ca01-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5ca01-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ca01-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5ca01-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca01-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca01-141">CommonParameters</span></span>
<span data-ttu-id="5ca01-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca01-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5ca01-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca01-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca01-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ca01-144">INPUTS</span></span>

### <span data-ttu-id="5ca01-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ca01-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5ca01-146">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="5ca01-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="5ca01-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ca01-147">OUTPUTS</span></span>

### <span data-ttu-id="5ca01-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ca01-148">System.Boolean</span></span>

## <span data-ttu-id="5ca01-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ca01-149">NOTES</span></span>
<span data-ttu-id="5ca01-150">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="5ca01-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="5ca01-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ca01-151">RELATED LINKS</span></span>

[<span data-ttu-id="5ca01-152">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ca01-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="5ca01-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ca01-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="5ca01-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5ca01-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="5ca01-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5ca01-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="5ca01-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5ca01-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="5ca01-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5ca01-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="5ca01-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5ca01-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="5ca01-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ca01-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5ca01-160">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5ca01-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="5ca01-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ca01-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5ca01-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ca01-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5ca01-163">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5ca01-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="5ca01-164">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca01-164">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5ca01-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5ca01-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="5ca01-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca01-166">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5ca01-167">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca01-167">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5ca01-168">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca01-168">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="5ca01-169">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5ca01-169">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
