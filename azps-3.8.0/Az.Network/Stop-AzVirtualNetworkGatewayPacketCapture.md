---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088373"
---
# <span data-ttu-id="d11ef-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d11ef-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="d11ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d11ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d11ef-103">Stoppar paket registrerings åtgärd på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="d11ef-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="d11ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d11ef-104">SYNTAX</span></span>

### <span data-ttu-id="d11ef-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="d11ef-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d11ef-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d11ef-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d11ef-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d11ef-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d11ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d11ef-108">DESCRIPTION</span></span>
<span data-ttu-id="d11ef-109">Stoppar paket registrerings åtgärden på en virtuell nätverksgateway och laddar upp resultatet på angiven SasUrl.</span><span class="sxs-lookup"><span data-stu-id="d11ef-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="d11ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d11ef-110">EXAMPLES</span></span>

### <span data-ttu-id="d11ef-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d11ef-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="d11ef-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d11ef-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="d11ef-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d11ef-113">PARAMETERS</span></span>

### <span data-ttu-id="d11ef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d11ef-114">-AsJob</span></span>
<span data-ttu-id="d11ef-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d11ef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d11ef-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d11ef-116">-Confirm</span></span>
<span data-ttu-id="d11ef-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d11ef-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d11ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11ef-118">-DefaultProfile</span></span>
<span data-ttu-id="d11ef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d11ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d11ef-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d11ef-120">-InputObject</span></span>
<span data-ttu-id="d11ef-121">Det virtuella nätverkets gateway-objekt där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="d11ef-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d11ef-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="d11ef-122">-Name</span></span>
<span data-ttu-id="d11ef-123">Namnet på den virtuella Nätverksgatewayen där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="d11ef-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="d11ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="d11ef-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d11ef-125">The resource group name.</span></span>

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

### <span data-ttu-id="d11ef-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d11ef-126">-ResourceId</span></span>
<span data-ttu-id="d11ef-127">Azure Resource ID för den VirtualNetworkGateway där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="d11ef-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="d11ef-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="d11ef-128">-SasUrl</span></span>
<span data-ttu-id="d11ef-129">SAS URL-paketfiltrering från virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="d11ef-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="d11ef-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d11ef-130">-WhatIf</span></span>
<span data-ttu-id="d11ef-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d11ef-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d11ef-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d11ef-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d11ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11ef-133">CommonParameters</span></span>
<span data-ttu-id="d11ef-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11ef-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d11ef-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11ef-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d11ef-136">INPUTS</span></span>

### <span data-ttu-id="d11ef-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d11ef-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d11ef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d11ef-138">System.String</span></span>

## <span data-ttu-id="d11ef-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d11ef-139">OUTPUTS</span></span>

### <span data-ttu-id="d11ef-140">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d11ef-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d11ef-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d11ef-141">NOTES</span></span>

## <span data-ttu-id="d11ef-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d11ef-142">RELATED LINKS</span></span>
[<span data-ttu-id="d11ef-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d11ef-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
