---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525745"
---
# <span data-ttu-id="b2977-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2977-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="b2977-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2977-102">SYNOPSIS</span></span>
<span data-ttu-id="b2977-103">Påbörjar paket registrerings åtgärd på en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="b2977-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="b2977-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2977-104">SYNTAX</span></span>

### <span data-ttu-id="b2977-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="b2977-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2977-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="b2977-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2977-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="b2977-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2977-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2977-108">DESCRIPTION</span></span>
<span data-ttu-id="b2977-109">Påbörjar paket registrerings åtgärd på en VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="b2977-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="b2977-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2977-110">EXAMPLES</span></span>

### <span data-ttu-id="b2977-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2977-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="b2977-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b2977-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="b2977-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2977-113">PARAMETERS</span></span>

### <span data-ttu-id="b2977-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2977-114">-AsJob</span></span>
<span data-ttu-id="b2977-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b2977-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2977-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2977-116">-DefaultProfile</span></span>
<span data-ttu-id="b2977-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2977-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2977-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="b2977-118">-FilterData</span></span>
<span data-ttu-id="b2977-119">Filter alternativ för start paket upptagning på VPN-anslutning.</span><span class="sxs-lookup"><span data-stu-id="b2977-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="b2977-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2977-120">-InputObject</span></span>
<span data-ttu-id="b2977-121">VPN-anslutningsobjektet där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="b2977-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="b2977-122">-LinkConnectionName</span></span>
<span data-ttu-id="b2977-123">Namnen på SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="b2977-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="b2977-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2977-124">-Name</span></span>
<span data-ttu-id="b2977-125">Namnet på den VPN-anslutning där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="b2977-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="b2977-126">-ParentResourceName</span></span>
<span data-ttu-id="b2977-127">Namnet på den överordnade Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="b2977-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2977-128">-ResourceGroupName</span></span>
<span data-ttu-id="b2977-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b2977-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2977-130">-ResourceId</span></span>
<span data-ttu-id="b2977-131">Azure Resource ID för den VpnConnection där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="b2977-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2977-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b2977-132">-Confirm</span></span>
<span data-ttu-id="b2977-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b2977-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2977-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2977-134">-WhatIf</span></span>
<span data-ttu-id="b2977-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b2977-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2977-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b2977-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2977-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2977-137">CommonParameters</span></span>
<span data-ttu-id="b2977-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2977-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2977-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2977-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2977-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2977-140">INPUTS</span></span>

### <span data-ttu-id="b2977-141">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="b2977-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="b2977-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b2977-142">System.String</span></span>

## <span data-ttu-id="b2977-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2977-143">OUTPUTS</span></span>

### <span data-ttu-id="b2977-144">Microsoft. Azure. commands. Networks. Models. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="b2977-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="b2977-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2977-145">NOTES</span></span>

## <span data-ttu-id="b2977-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2977-146">RELATED LINKS</span></span>

[<span data-ttu-id="b2977-147">Stopp-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b2977-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)