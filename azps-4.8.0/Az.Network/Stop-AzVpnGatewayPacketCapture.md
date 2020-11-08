---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258113"
---
# <span data-ttu-id="2e531-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e531-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="2e531-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e531-102">SYNOPSIS</span></span>
<span data-ttu-id="2e531-103">Stoppar paket registrerings åtgärd på en VPN-gateway.</span><span class="sxs-lookup"><span data-stu-id="2e531-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="2e531-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e531-104">SYNTAX</span></span>

### <span data-ttu-id="2e531-105">ByVpnGatewayName (standard)</span><span class="sxs-lookup"><span data-stu-id="2e531-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e531-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="2e531-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e531-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="2e531-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e531-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e531-108">DESCRIPTION</span></span>
<span data-ttu-id="2e531-109">Stoppar paket registrerings åtgärden på en VPN-gateway och laddar upp resultatet på angiven SasUrl.</span><span class="sxs-lookup"><span data-stu-id="2e531-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="2e531-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e531-110">EXAMPLES</span></span>

### <span data-ttu-id="2e531-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2e531-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="2e531-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2e531-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="2e531-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e531-113">PARAMETERS</span></span>

### <span data-ttu-id="2e531-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e531-114">-AsJob</span></span>
<span data-ttu-id="2e531-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2e531-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e531-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e531-116">-DefaultProfile</span></span>
<span data-ttu-id="2e531-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e531-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e531-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e531-118">-InputObject</span></span>
<span data-ttu-id="2e531-119">VPN gateway-objekt där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="2e531-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="2e531-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e531-120">-Name</span></span>
<span data-ttu-id="2e531-121">Namnet på den VPN-gateway där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="2e531-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="2e531-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e531-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e531-123">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2e531-123">The resource group name.</span></span>

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

### <span data-ttu-id="2e531-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e531-124">-ResourceId</span></span>
<span data-ttu-id="2e531-125">Azure Resource ID för den VpnGateway där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="2e531-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="2e531-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="2e531-126">-SasUrl</span></span>
<span data-ttu-id="2e531-127">SAS URL-paketfiltrering på VPN gateway.</span><span class="sxs-lookup"><span data-stu-id="2e531-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="2e531-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e531-128">-Confirm</span></span>
<span data-ttu-id="2e531-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e531-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e531-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e531-130">-WhatIf</span></span>
<span data-ttu-id="2e531-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e531-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e531-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e531-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e531-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e531-133">CommonParameters</span></span>
<span data-ttu-id="2e531-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e531-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e531-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e531-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e531-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e531-136">INPUTS</span></span>

### <span data-ttu-id="2e531-137">Microsoft. Azure. commands. Networks. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="2e531-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="2e531-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2e531-138">System.String</span></span>

## <span data-ttu-id="2e531-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e531-139">OUTPUTS</span></span>

### <span data-ttu-id="2e531-140">Microsoft. Azure. commands. Networks. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2e531-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2e531-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e531-141">NOTES</span></span>

## <span data-ttu-id="2e531-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e531-142">RELATED LINKS</span></span>

[<span data-ttu-id="2e531-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e531-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)