---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924094"
---
# <span data-ttu-id="c98a7-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c98a7-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="c98a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c98a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c98a7-103">Stoppar en session med pågående paket</span><span class="sxs-lookup"><span data-stu-id="c98a7-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="c98a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c98a7-104">SYNTAX</span></span>

### <span data-ttu-id="c98a7-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="c98a7-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c98a7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c98a7-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c98a7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c98a7-107">DESCRIPTION</span></span>
<span data-ttu-id="c98a7-108">Stop-AzNetworkWatcherPacketCapture stoppar sändningen av en pågående paket.</span><span class="sxs-lookup"><span data-stu-id="c98a7-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="c98a7-109">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c98a7-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c98a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c98a7-110">EXAMPLES</span></span>

### <span data-ttu-id="c98a7-111">---Exempel 1: stoppa en redigeringssession---</span><span class="sxs-lookup"><span data-stu-id="c98a7-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="c98a7-112">I det här exemplet stoppar vi en session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="c98a7-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="c98a7-113">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c98a7-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="c98a7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c98a7-114">PARAMETERS</span></span>

### <span data-ttu-id="c98a7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c98a7-115">-AsJob</span></span>
<span data-ttu-id="c98a7-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c98a7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c98a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c98a7-117">-DefaultProfile</span></span>
<span data-ttu-id="c98a7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c98a7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c98a7-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c98a7-119">-NetworkWatcher</span></span>
<span data-ttu-id="c98a7-120">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="c98a7-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="c98a7-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c98a7-121">-NetworkWatcherName</span></span>
<span data-ttu-id="c98a7-122">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="c98a7-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="c98a7-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="c98a7-123">-PacketCaptureName</span></span>
<span data-ttu-id="c98a7-124">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="c98a7-124">The packet capture name.</span></span>

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

### <span data-ttu-id="c98a7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c98a7-125">-PassThru</span></span>
<span data-ttu-id="c98a7-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c98a7-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c98a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c98a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="c98a7-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c98a7-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c98a7-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c98a7-129">-Confirm</span></span>
<span data-ttu-id="c98a7-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c98a7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c98a7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c98a7-131">-WhatIf</span></span>
<span data-ttu-id="c98a7-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c98a7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c98a7-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c98a7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c98a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98a7-134">CommonParameters</span></span>
<span data-ttu-id="c98a7-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98a7-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98a7-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98a7-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c98a7-137">INPUTS</span></span>

### <span data-ttu-id="c98a7-138">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c98a7-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c98a7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c98a7-139">System.String</span></span>

## <span data-ttu-id="c98a7-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c98a7-140">OUTPUTS</span></span>

### <span data-ttu-id="c98a7-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c98a7-141">System.Boolean</span></span>

## <span data-ttu-id="c98a7-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c98a7-142">NOTES</span></span>
<span data-ttu-id="c98a7-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="c98a7-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="c98a7-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c98a7-144">RELATED LINKS</span></span>

[<span data-ttu-id="c98a7-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c98a7-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c98a7-146">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c98a7-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c98a7-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c98a7-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c98a7-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c98a7-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c98a7-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c98a7-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c98a7-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c98a7-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c98a7-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c98a7-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c98a7-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c98a7-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c98a7-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c98a7-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c98a7-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c98a7-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c98a7-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c98a7-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c98a7-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c98a7-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
