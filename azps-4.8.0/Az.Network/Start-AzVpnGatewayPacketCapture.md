---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258128"
---
# <span data-ttu-id="57a4b-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57a4b-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="57a4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="57a4b-103">Påbörjar paket registrerings åtgärd på en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="57a4b-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="57a4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57a4b-104">SYNTAX</span></span>

### <span data-ttu-id="57a4b-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="57a4b-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a4b-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="57a4b-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57a4b-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="57a4b-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57a4b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="57a4b-109">Påbörjar paket registrerings åtgärd på en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="57a4b-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="57a4b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="57a4b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="57a4b-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="57a4b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="57a4b-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="57a4b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57a4b-113">PARAMETERS</span></span>

### <span data-ttu-id="57a4b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57a4b-114">-AsJob</span></span>
<span data-ttu-id="57a4b-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="57a4b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57a4b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57a4b-116">-DefaultProfile</span></span>
<span data-ttu-id="57a4b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57a4b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="57a4b-118">-FilterData</span></span>
<span data-ttu-id="57a4b-119">Filter alternativ för start paket avbildning på VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="57a4b-119">Filter options for start packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57a4b-120">-InputObject</span></span>
<span data-ttu-id="57a4b-121">VPN gateway-objekt där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="57a4b-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="57a4b-122">-Name</span></span>
<span data-ttu-id="57a4b-123">Namnet på den VPN-gateway där Packet Capture ska startas.</span><span class="sxs-lookup"><span data-stu-id="57a4b-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57a4b-124">-ResourceGroupName</span></span>
<span data-ttu-id="57a4b-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="57a4b-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57a4b-126">-ResourceId</span></span>
<span data-ttu-id="57a4b-127">Azure Resource ID för den VpnGateway där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="57a4b-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57a4b-128">-Confirm</span></span>
<span data-ttu-id="57a4b-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57a4b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57a4b-130">-WhatIf</span></span>
<span data-ttu-id="57a4b-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57a4b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57a4b-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57a4b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a4b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a4b-133">CommonParameters</span></span>
<span data-ttu-id="57a4b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a4b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a4b-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57a4b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a4b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57a4b-136">INPUTS</span></span>

### <span data-ttu-id="57a4b-137">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="57a4b-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="57a4b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="57a4b-138">System.String</span></span>

## <span data-ttu-id="57a4b-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57a4b-139">OUTPUTS</span></span>

### <span data-ttu-id="57a4b-140">Microsoft. Azure. commands. Networks. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="57a4b-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="57a4b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57a4b-141">NOTES</span></span>

## <span data-ttu-id="57a4b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57a4b-142">RELATED LINKS</span></span>

[<span data-ttu-id="57a4b-143">Stopp-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="57a4b-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)