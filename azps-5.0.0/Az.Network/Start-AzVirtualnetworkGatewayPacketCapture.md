---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325698"
---
# <span data-ttu-id="6e519-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e519-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="6e519-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e519-102">SYNOPSIS</span></span>
<span data-ttu-id="6e519-103">Påbörjar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6e519-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="6e519-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e519-104">SYNTAX</span></span>

### <span data-ttu-id="6e519-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="6e519-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e519-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e519-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e519-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e519-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e519-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e519-108">DESCRIPTION</span></span>
<span data-ttu-id="6e519-109">Påbörjar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6e519-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="6e519-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e519-110">EXAMPLES</span></span>

### <span data-ttu-id="6e519-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6e519-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="6e519-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6e519-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="6e519-113">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="6e519-113">Example 3</span></span>
<span data-ttu-id="6e519-114">Exempel på Packet-insamling för att fånga alla inre och yttre paket</span><span class="sxs-lookup"><span data-stu-id="6e519-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="6e519-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e519-115">PARAMETERS</span></span>

### <span data-ttu-id="6e519-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e519-116">-AsJob</span></span>
<span data-ttu-id="6e519-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6e519-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e519-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6e519-118">-Confirm</span></span>
<span data-ttu-id="6e519-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6e519-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e519-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e519-120">-DefaultProfile</span></span>
<span data-ttu-id="6e519-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e519-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e519-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="6e519-122">-FilterData</span></span>
<span data-ttu-id="6e519-123">Filter alternativ för start paket avbildning från virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6e519-123">Filter options for start packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e519-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e519-124">-InputObject</span></span>
<span data-ttu-id="6e519-125">Det virtuella nätverkets gateway-objekt där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="6e519-125">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e519-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="6e519-126">-Name</span></span>
<span data-ttu-id="6e519-127">Namnet på den virtuella Nätverksgatewayen där paket hämtningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="6e519-127">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e519-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e519-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e519-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6e519-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e519-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e519-130">-ResourceId</span></span>
<span data-ttu-id="6e519-131">Azure Resource ID för den VirtualNetworkGateway där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="6e519-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e519-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e519-132">-WhatIf</span></span>
<span data-ttu-id="6e519-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6e519-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e519-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6e519-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e519-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e519-135">CommonParameters</span></span>
<span data-ttu-id="6e519-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e519-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e519-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e519-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e519-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e519-138">INPUTS</span></span>

### <span data-ttu-id="6e519-139">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="6e519-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="6e519-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6e519-140">System.String</span></span>

## <span data-ttu-id="6e519-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e519-141">OUTPUTS</span></span>

### <span data-ttu-id="6e519-142">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="6e519-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="6e519-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e519-143">NOTES</span></span>

## <span data-ttu-id="6e519-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e519-144">RELATED LINKS</span></span>
[<span data-ttu-id="6e519-145">Stopp-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6e519-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)