---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 3a1d9c2f415d56263529fcd66aa1ee9535823bbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919447"
---
# <span data-ttu-id="8b33b-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b33b-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="8b33b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8b33b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b33b-103">Påbörjar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="8b33b-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="8b33b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8b33b-104">SYNTAX</span></span>

### <span data-ttu-id="8b33b-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="8b33b-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b33b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8b33b-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b33b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b33b-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b33b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8b33b-108">DESCRIPTION</span></span>
<span data-ttu-id="8b33b-109">Påbörjar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="8b33b-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="8b33b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8b33b-110">EXAMPLES</span></span>

### <span data-ttu-id="8b33b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8b33b-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="8b33b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8b33b-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="8b33b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8b33b-113">PARAMETERS</span></span>

### <span data-ttu-id="8b33b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b33b-114">-AsJob</span></span>
<span data-ttu-id="8b33b-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8b33b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b33b-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8b33b-116">-Confirm</span></span>
<span data-ttu-id="8b33b-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8b33b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b33b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b33b-118">-DefaultProfile</span></span>
<span data-ttu-id="8b33b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8b33b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b33b-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="8b33b-120">-FilterData</span></span>
<span data-ttu-id="8b33b-121">Filter alternativ för att hämta start paket från anslutningar för virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="8b33b-121">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="8b33b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b33b-122">-InputObject</span></span>
<span data-ttu-id="8b33b-123">Connection-objektet för den virtuella Nätverksgatewayen där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="8b33b-123">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b33b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="8b33b-124">-Name</span></span>
<span data-ttu-id="8b33b-125">Namnet på den virtuella Nätverksgatewayen där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="8b33b-125">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b33b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b33b-126">-ResourceGroupName</span></span>
<span data-ttu-id="8b33b-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8b33b-127">The resource group name.</span></span>

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

### <span data-ttu-id="8b33b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b33b-128">-ResourceId</span></span>
<span data-ttu-id="8b33b-129">Azure Resource ID för den VirtualNetworkGatewayConnection där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="8b33b-129">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="8b33b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b33b-130">-WhatIf</span></span>
<span data-ttu-id="8b33b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8b33b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b33b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8b33b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b33b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b33b-133">CommonParameters</span></span>
<span data-ttu-id="8b33b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b33b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b33b-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b33b-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b33b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8b33b-136">INPUTS</span></span>

### <span data-ttu-id="8b33b-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8b33b-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="8b33b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8b33b-138">System.String</span></span>

## <span data-ttu-id="8b33b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8b33b-139">OUTPUTS</span></span>

### <span data-ttu-id="8b33b-140">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8b33b-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="8b33b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8b33b-141">NOTES</span></span>

## <span data-ttu-id="8b33b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8b33b-142">RELATED LINKS</span></span>
[<span data-ttu-id="8b33b-143">Stopp-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b33b-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)