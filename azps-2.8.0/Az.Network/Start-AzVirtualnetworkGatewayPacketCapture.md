---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 1f0b539e2f5a6e2c387738558fb6db8cbe647457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919446"
---
# <span data-ttu-id="1973d-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1973d-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="1973d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1973d-102">SYNOPSIS</span></span>
<span data-ttu-id="1973d-103">Påbörjar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="1973d-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="1973d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1973d-104">SYNTAX</span></span>

### <span data-ttu-id="1973d-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1973d-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1973d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1973d-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1973d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1973d-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1973d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1973d-108">DESCRIPTION</span></span>
<span data-ttu-id="1973d-109">Påbörjar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="1973d-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="1973d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1973d-110">EXAMPLES</span></span>

### <span data-ttu-id="1973d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1973d-111">Example 1</span></span>
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
### <span data-ttu-id="1973d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1973d-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
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

## <span data-ttu-id="1973d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1973d-113">PARAMETERS</span></span>

### <span data-ttu-id="1973d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1973d-114">-AsJob</span></span>
<span data-ttu-id="1973d-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1973d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1973d-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1973d-116">-Confirm</span></span>
<span data-ttu-id="1973d-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1973d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1973d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1973d-118">-DefaultProfile</span></span>
<span data-ttu-id="1973d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1973d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1973d-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="1973d-120">-FilterData</span></span>
<span data-ttu-id="1973d-121">Filter alternativ för start paket avbildning från virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="1973d-121">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="1973d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1973d-122">-InputObject</span></span>
<span data-ttu-id="1973d-123">Det virtuella nätverkets gateway-objekt där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="1973d-123">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="1973d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1973d-124">-Name</span></span>
<span data-ttu-id="1973d-125">Namnet på den virtuella Nätverksgatewayen där paket hämtningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="1973d-125">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="1973d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1973d-126">-ResourceGroupName</span></span>
<span data-ttu-id="1973d-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1973d-127">The resource group name.</span></span>

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

### <span data-ttu-id="1973d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1973d-128">-ResourceId</span></span>
<span data-ttu-id="1973d-129">Azure Resource ID för den VirtualNetworkGateway där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="1973d-129">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="1973d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1973d-130">-WhatIf</span></span>
<span data-ttu-id="1973d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1973d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1973d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1973d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1973d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1973d-133">CommonParameters</span></span>
<span data-ttu-id="1973d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1973d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1973d-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1973d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1973d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1973d-136">INPUTS</span></span>

### <span data-ttu-id="1973d-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1973d-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1973d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1973d-138">System.String</span></span>

## <span data-ttu-id="1973d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1973d-139">OUTPUTS</span></span>

### <span data-ttu-id="1973d-140">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="1973d-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="1973d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1973d-141">NOTES</span></span>

## <span data-ttu-id="1973d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1973d-142">RELATED LINKS</span></span>
[<span data-ttu-id="1973d-143">Stopp-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1973d-143">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)