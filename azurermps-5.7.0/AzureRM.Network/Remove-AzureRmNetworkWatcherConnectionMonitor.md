---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 10582a0e81fdb9c86902c7a2580ad31fe84f3bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757410"
---
# <span data-ttu-id="28199-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28199-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="28199-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28199-102">SYNOPSIS</span></span>
<span data-ttu-id="28199-103">Ta bort anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="28199-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28199-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28199-104">SYNTAX</span></span>

### <span data-ttu-id="28199-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="28199-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28199-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="28199-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28199-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="28199-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28199-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="28199-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28199-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="28199-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28199-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28199-110">DESCRIPTION</span></span>
<span data-ttu-id="28199-111">Cmdleten Remove-AzureRmNetworkWatcherConnectionMonitor tar bort den angivna anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="28199-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="28199-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28199-112">EXAMPLES</span></span>

### <span data-ttu-id="28199-113">Exempel 1: ta bort den angivna anslutnings övervakaren</span><span class="sxs-lookup"><span data-stu-id="28199-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="28199-114">I det här exemplet tar vi bort anslutnings övervakaren som anges av plats och namn.</span><span class="sxs-lookup"><span data-stu-id="28199-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="28199-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28199-115">PARAMETERS</span></span>

### <span data-ttu-id="28199-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28199-116">-AsJob</span></span>
<span data-ttu-id="28199-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="28199-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28199-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28199-118">-Confirm</span></span>
<span data-ttu-id="28199-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28199-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28199-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28199-120">-DefaultProfile</span></span>
<span data-ttu-id="28199-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28199-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28199-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28199-122">-InputObject</span></span>
<span data-ttu-id="28199-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="28199-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="28199-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="28199-124">-Location</span></span>
<span data-ttu-id="28199-125">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="28199-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="28199-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="28199-126">-Name</span></span>
<span data-ttu-id="28199-127">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="28199-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="28199-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28199-128">-NetworkWatcher</span></span>
<span data-ttu-id="28199-129">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="28199-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="28199-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="28199-130">-NetworkWatcherName</span></span>
<span data-ttu-id="28199-131">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="28199-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="28199-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28199-132">-PassThru</span></span>
<span data-ttu-id="28199-133">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="28199-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="28199-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28199-134">-ResourceGroupName</span></span>
<span data-ttu-id="28199-135">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="28199-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="28199-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28199-136">-ResourceId</span></span>
<span data-ttu-id="28199-137">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="28199-137">Resource ID.</span></span>

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

### <span data-ttu-id="28199-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28199-138">-WhatIf</span></span>
<span data-ttu-id="28199-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28199-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28199-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28199-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28199-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28199-141">CommonParameters</span></span>
<span data-ttu-id="28199-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28199-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="28199-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28199-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28199-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28199-144">INPUTS</span></span>

### <span data-ttu-id="28199-145">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28199-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="28199-146">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="28199-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="28199-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28199-147">OUTPUTS</span></span>

### <span data-ttu-id="28199-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28199-148">System.Boolean</span></span>

## <span data-ttu-id="28199-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28199-149">NOTES</span></span>
<span data-ttu-id="28199-150">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="28199-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="28199-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28199-151">RELATED LINKS</span></span>

[<span data-ttu-id="28199-152">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28199-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="28199-153">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28199-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="28199-154">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="28199-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="28199-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="28199-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="28199-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="28199-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="28199-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="28199-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="28199-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="28199-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="28199-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28199-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="28199-160">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="28199-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="28199-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28199-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="28199-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28199-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="28199-163">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="28199-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="28199-164">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28199-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="28199-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="28199-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="28199-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="28199-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()
