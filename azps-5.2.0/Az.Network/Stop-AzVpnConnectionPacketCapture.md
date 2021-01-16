---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: f80543b245c59cee7261d062c741788489fb5cb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412723"
---
# <span data-ttu-id="ef6c0-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ef6c0-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="ef6c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6c0-103">Stoppar paket registrerings åtgärd på en VPN-anslutning</span><span class="sxs-lookup"><span data-stu-id="ef6c0-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="ef6c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef6c0-104">SYNTAX</span></span>

### <span data-ttu-id="ef6c0-105">ByVpnConnectionName (standard)</span><span class="sxs-lookup"><span data-stu-id="ef6c0-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6c0-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="ef6c0-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6c0-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6c0-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef6c0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef6c0-108">DESCRIPTION</span></span>
<span data-ttu-id="ef6c0-109">Stoppar paket registrerings åtgärden på en VPN-anslutning och laddar upp resultatet på en given SasUrl.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="ef6c0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef6c0-110">EXAMPLES</span></span>

### <span data-ttu-id="ef6c0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef6c0-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="ef6c0-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ef6c0-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="ef6c0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef6c0-113">PARAMETERS</span></span>

### <span data-ttu-id="ef6c0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef6c0-114">-AsJob</span></span>
<span data-ttu-id="ef6c0-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="ef6c0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef6c0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6c0-116">-DefaultProfile</span></span>
<span data-ttu-id="ef6c0-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef6c0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef6c0-118">-InputObject</span></span>
<span data-ttu-id="ef6c0-119">VPN-anslutningsobjektet där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="ef6c0-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="ef6c0-120">-LinkConnectionName</span></span>
<span data-ttu-id="ef6c0-121">Namnen på SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="ef6c0-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef6c0-122">-Name</span></span>
<span data-ttu-id="ef6c0-123">Namnet på den VPN-anslutning där Packet Capture ska startas.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6c0-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="ef6c0-124">-ParentResourceName</span></span>
<span data-ttu-id="ef6c0-125">Namnet på den överordnade resursen.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-125">The parent resource name.</span></span>

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

### <span data-ttu-id="ef6c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef6c0-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-127">The resource group name.</span></span>

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

### <span data-ttu-id="ef6c0-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef6c0-128">-ResourceId</span></span>
<span data-ttu-id="ef6c0-129">Azure Resource ID för den VpnConnection där paket upptagningen ska startas.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="ef6c0-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="ef6c0-130">-SasUrl</span></span>
<span data-ttu-id="ef6c0-131">SAS-URL för stopp paket registrering på VPN.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="ef6c0-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef6c0-132">-Confirm</span></span>
<span data-ttu-id="ef6c0-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6c0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6c0-134">-WhatIf</span></span>
<span data-ttu-id="ef6c0-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef6c0-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef6c0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6c0-137">CommonParameters</span></span>
<span data-ttu-id="ef6c0-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef6c0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6c0-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef6c0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6c0-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef6c0-140">INPUTS</span></span>

### <span data-ttu-id="ef6c0-141">Microsoft. Azure. commands. Networks. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="ef6c0-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="ef6c0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ef6c0-142">System.String</span></span>

## <span data-ttu-id="ef6c0-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef6c0-143">OUTPUTS</span></span>

### <span data-ttu-id="ef6c0-144">Microsoft. Azure. commands. Networks. Models. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="ef6c0-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="ef6c0-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef6c0-145">NOTES</span></span>

## <span data-ttu-id="ef6c0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef6c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="ef6c0-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ef6c0-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)