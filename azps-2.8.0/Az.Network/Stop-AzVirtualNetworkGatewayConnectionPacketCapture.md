---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 791b6d74049aeec24e67ca29f5fae990f511908d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919441"
---
# <span data-ttu-id="5cd6d-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5cd6d-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="5cd6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5cd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd6d-103">Stoppar paket registrerings åtgärd för en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="5cd6d-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="5cd6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5cd6d-104">SYNTAX</span></span>

### <span data-ttu-id="5cd6d-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="5cd6d-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd6d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5cd6d-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd6d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cd6d-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd6d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5cd6d-108">DESCRIPTION</span></span>
<span data-ttu-id="5cd6d-109">Stoppar paket registrerings åtgärden på en anslutning till en virtuell nätverksgateway och laddar upp resultatet på en given SasUrl.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="5cd6d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5cd6d-110">EXAMPLES</span></span>

### <span data-ttu-id="5cd6d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5cd6d-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="5cd6d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5cd6d-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="5cd6d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5cd6d-113">PARAMETERS</span></span>

### <span data-ttu-id="5cd6d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5cd6d-114">-AsJob</span></span>
<span data-ttu-id="5cd6d-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5cd6d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cd6d-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5cd6d-116">-Confirm</span></span>
<span data-ttu-id="5cd6d-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd6d-118">-DefaultProfile</span></span>
<span data-ttu-id="5cd6d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cd6d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cd6d-120">-InputObject</span></span>
<span data-ttu-id="5cd6d-121">Connection-objektet för den virtuella Nätverksgatewayen där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="5cd6d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5cd6d-122">-Name</span></span>
<span data-ttu-id="5cd6d-123">Namnet på den virtuella Nätverksgatewayen där paket hämtningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5cd6d-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-125">The resource group name.</span></span>

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

### <span data-ttu-id="5cd6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cd6d-126">-ResourceId</span></span>
<span data-ttu-id="5cd6d-127">Azure Resource ID för den VirtualNetworkGatewayConnection där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="5cd6d-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="5cd6d-128">-SasUrl</span></span>
<span data-ttu-id="5cd6d-129">SAS-URL för upptagning av stopp paket i virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="5cd6d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd6d-130">-WhatIf</span></span>
<span data-ttu-id="5cd6d-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd6d-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd6d-133">CommonParameters</span></span>
<span data-ttu-id="5cd6d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd6d-135">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cd6d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd6d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5cd6d-136">INPUTS</span></span>

### <span data-ttu-id="5cd6d-137">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="5cd6d-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="5cd6d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5cd6d-138">System.String</span></span>

## <span data-ttu-id="5cd6d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5cd6d-139">OUTPUTS</span></span>

### <span data-ttu-id="5cd6d-140">Microsoft. Azure. commands. Networks. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5cd6d-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="5cd6d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5cd6d-141">NOTES</span></span>

## <span data-ttu-id="5cd6d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5cd6d-142">RELATED LINKS</span></span>
[<span data-ttu-id="5cd6d-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5cd6d-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)