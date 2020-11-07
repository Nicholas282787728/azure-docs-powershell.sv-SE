---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: 5f2b2bf738c4e83f8f8f3854e831601ea23c7d8e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929262"
---
# <span data-ttu-id="a4df4-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4df4-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a4df4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4df4-102">SYNOPSIS</span></span>
<span data-ttu-id="a4df4-103">Stoppar en session med pågående paket</span><span class="sxs-lookup"><span data-stu-id="a4df4-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4df4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4df4-104">SYNTAX</span></span>

### <span data-ttu-id="a4df4-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a4df4-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4df4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a4df4-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4df4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4df4-107">DESCRIPTION</span></span>
<span data-ttu-id="a4df4-108">Stop-AzureRmNetworkWatcherPacketCapture stoppar sändningen av en pågående paket.</span><span class="sxs-lookup"><span data-stu-id="a4df4-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="a4df4-109">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4df4-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="a4df4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4df4-110">EXAMPLES</span></span>

### <span data-ttu-id="a4df4-111">---Exempel 1: stoppa en redigeringssession---</span><span class="sxs-lookup"><span data-stu-id="a4df4-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a4df4-112">I det här exemplet stoppar vi en session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="a4df4-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="a4df4-113">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a4df4-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="a4df4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4df4-114">PARAMETERS</span></span>

### <span data-ttu-id="a4df4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4df4-115">-AsJob</span></span>
<span data-ttu-id="a4df4-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4df4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4df4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4df4-117">-DefaultProfile</span></span>
<span data-ttu-id="a4df4-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4df4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4df4-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4df4-119">-NetworkWatcher</span></span>
<span data-ttu-id="a4df4-120">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a4df4-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="a4df4-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a4df4-121">-NetworkWatcherName</span></span>
<span data-ttu-id="a4df4-122">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a4df4-122">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4df4-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a4df4-123">-PacketCaptureName</span></span>
<span data-ttu-id="a4df4-124">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="a4df4-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4df4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4df4-125">-PassThru</span></span>
<span data-ttu-id="a4df4-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a4df4-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a4df4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4df4-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4df4-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4df4-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a4df4-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4df4-129">-Confirm</span></span>
<span data-ttu-id="a4df4-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4df4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4df4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4df4-131">-WhatIf</span></span>
<span data-ttu-id="a4df4-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4df4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4df4-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4df4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4df4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4df4-134">CommonParameters</span></span>
<span data-ttu-id="a4df4-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4df4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4df4-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4df4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4df4-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4df4-137">INPUTS</span></span>

### <span data-ttu-id="a4df4-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4df4-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a4df4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4df4-139">System.String</span></span>

## <span data-ttu-id="a4df4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4df4-140">OUTPUTS</span></span>

### <span data-ttu-id="a4df4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4df4-141">System.Boolean</span></span>

## <span data-ttu-id="a4df4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4df4-142">NOTES</span></span>
<span data-ttu-id="a4df4-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="a4df4-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a4df4-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4df4-144">RELATED LINKS</span></span>

[<span data-ttu-id="a4df4-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4df4-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4df4-146">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a4df4-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a4df4-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4df4-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4df4-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a4df4-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a4df4-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4df4-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a4df4-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4df4-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a4df4-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a4df4-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a4df4-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a4df4-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a4df4-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a4df4-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a4df4-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a4df4-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a4df4-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a4df4-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a4df4-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a4df4-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
