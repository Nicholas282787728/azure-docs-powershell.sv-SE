---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: f355d011bbd810fa309cd8b7d64ed95090a00ea6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925810"
---
# <span data-ttu-id="2289d-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2289d-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="2289d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2289d-102">SYNOPSIS</span></span>
<span data-ttu-id="2289d-103">Skapar en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="2289d-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="2289d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2289d-104">SYNTAX</span></span>

### <span data-ttu-id="2289d-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2289d-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2289d-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="2289d-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2289d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2289d-107">DESCRIPTION</span></span>
<span data-ttu-id="2289d-108">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="2289d-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="2289d-109">Cmdleten **New-AzLocalNetworkGateway** skapar objektet som representerar din lokala-gateway baserat på gatewayens namn, resurs gruppens namn, plats och IP-adress, samt adressprefixet för det lokala nätverket som ansluter till Azure.</span><span class="sxs-lookup"><span data-stu-id="2289d-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="2289d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2289d-110">EXAMPLES</span></span>

### <span data-ttu-id="2289d-111">1: skapa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="2289d-111">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="2289d-112">Skapar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG" i plats "West" med IP-adressen "23.99.221.164" och adressprefixet "10.5.51.0/24" på-lokala.</span><span class="sxs-lookup"><span data-stu-id="2289d-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="2289d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2289d-113">PARAMETERS</span></span>

### <span data-ttu-id="2289d-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2289d-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2289d-115">-AsJob</span></span>
<span data-ttu-id="2289d-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2289d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2289d-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="2289d-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="2289d-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2289d-119">-DefaultProfile</span></span>
<span data-ttu-id="2289d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2289d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2289d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2289d-121">-Force</span></span>
<span data-ttu-id="2289d-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2289d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2289d-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2289d-123">-Fqdn</span></span>
<span data-ttu-id="2289d-124">FQDN för lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="2289d-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="2289d-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="2289d-126">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="2289d-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="2289d-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2289d-129">-ResourceGroupName</span></span>
<span data-ttu-id="2289d-130">Anger den resurs grupp som den lokala nät portens Gateway tillhör.</span><span class="sxs-lookup"><span data-stu-id="2289d-130">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2289d-131">-Tag</span></span>
<span data-ttu-id="2289d-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="2289d-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2289d-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="2289d-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2289d-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2289d-134">-Confirm</span></span>
<span data-ttu-id="2289d-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2289d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2289d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2289d-136">-WhatIf</span></span>
<span data-ttu-id="2289d-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2289d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2289d-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2289d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2289d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2289d-139">CommonParameters</span></span>
<span data-ttu-id="2289d-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2289d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2289d-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2289d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2289d-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2289d-142">INPUTS</span></span>

### <span data-ttu-id="2289d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2289d-143">System.String</span></span>

### <span data-ttu-id="2289d-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="2289d-144">System.String[]</span></span>

### <span data-ttu-id="2289d-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2289d-145">System.UInt32</span></span>

### <span data-ttu-id="2289d-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2289d-146">System.Int32</span></span>

### <span data-ttu-id="2289d-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="2289d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2289d-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2289d-148">OUTPUTS</span></span>

### <span data-ttu-id="2289d-149">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2289d-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="2289d-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2289d-150">NOTES</span></span>

## <span data-ttu-id="2289d-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2289d-151">RELATED LINKS</span></span>

[<span data-ttu-id="2289d-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2289d-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="2289d-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2289d-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="2289d-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2289d-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
