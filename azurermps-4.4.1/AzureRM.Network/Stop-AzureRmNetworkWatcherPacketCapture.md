---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574562"
---
# <span data-ttu-id="7ab48-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab48-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="7ab48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ab48-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab48-103">Stoppar en session med pågående paket</span><span class="sxs-lookup"><span data-stu-id="7ab48-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ab48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ab48-104">SYNTAX</span></span>

### <span data-ttu-id="7ab48-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="7ab48-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab48-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7ab48-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ab48-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ab48-107">DESCRIPTION</span></span>
<span data-ttu-id="7ab48-108">Stop-AzureRmNetworkWatcherPacketCapture stoppar sändningen av en pågående paket.</span><span class="sxs-lookup"><span data-stu-id="7ab48-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="7ab48-109">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7ab48-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="7ab48-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ab48-110">EXAMPLES</span></span>

### <span data-ttu-id="7ab48-111">---Exempel 1: stoppa en redigeringssession---</span><span class="sxs-lookup"><span data-stu-id="7ab48-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="7ab48-112">I det här exemplet stoppar vi en session med namnet "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="7ab48-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="7ab48-113">När sessionen har stoppats överförs paket registrerings filen till lagring och/eller sparas lokalt på den virtuella datorn, beroende på dess konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7ab48-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="7ab48-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ab48-114">PARAMETERS</span></span>

### <span data-ttu-id="7ab48-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab48-115">-NetworkWatcher</span></span>
<span data-ttu-id="7ab48-116">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="7ab48-116">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab48-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7ab48-117">-NetworkWatcherName</span></span>
<span data-ttu-id="7ab48-118">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="7ab48-118">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab48-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="7ab48-119">-PacketCaptureName</span></span>
<span data-ttu-id="7ab48-120">Paket registrerings namnet.</span><span class="sxs-lookup"><span data-stu-id="7ab48-120">The packet capture name.</span></span>

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

### <span data-ttu-id="7ab48-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ab48-121">-PassThru</span></span>
<span data-ttu-id="7ab48-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7ab48-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7ab48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab48-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ab48-124">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7ab48-124">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab48-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ab48-125">-Confirm</span></span>
<span data-ttu-id="7ab48-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ab48-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab48-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab48-127">-WhatIf</span></span>
<span data-ttu-id="7ab48-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ab48-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ab48-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ab48-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab48-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab48-130">-DefaultProfile</span></span>
<span data-ttu-id="7ab48-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ab48-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab48-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab48-132">CommonParameters</span></span>
<span data-ttu-id="7ab48-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ab48-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab48-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab48-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab48-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ab48-135">INPUTS</span></span>

### <span data-ttu-id="7ab48-136">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab48-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7ab48-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7ab48-137">System.String</span></span>

## <span data-ttu-id="7ab48-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ab48-138">OUTPUTS</span></span>

### <span data-ttu-id="7ab48-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ab48-139">System.Boolean</span></span>

## <span data-ttu-id="7ab48-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ab48-140">NOTES</span></span>
<span data-ttu-id="7ab48-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, paket, upptagning, trafik</span><span class="sxs-lookup"><span data-stu-id="7ab48-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="7ab48-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ab48-142">RELATED LINKS</span></span>

[<span data-ttu-id="7ab48-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab48-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab48-144">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7ab48-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7ab48-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab48-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab48-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7ab48-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7ab48-147">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab48-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7ab48-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab48-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7ab48-149">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7ab48-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7ab48-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7ab48-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7ab48-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7ab48-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7ab48-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7ab48-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7ab48-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7ab48-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7ab48-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7ab48-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
