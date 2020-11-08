---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 7f4a7568139cc41827e94c5bf538d11e2aa3dee4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262552"
---
# <span data-ttu-id="00fb3-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="00fb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="00fb3-102">SYNOPSIS</span></span>
<span data-ttu-id="00fb3-103">Skapar en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="00fb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="00fb3-104">SYNTAX</span></span>

### <span data-ttu-id="00fb3-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="00fb3-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fb3-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="00fb3-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00fb3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="00fb3-107">DESCRIPTION</span></span>
<span data-ttu-id="00fb3-108">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="00fb3-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="00fb3-109">Cmdleten **New-AzLocalNetworkGateway** skapar objektet som representerar din lokala-gateway baserat på gatewayens namn, resurs gruppens namn, plats och IP-adress, samt adressprefixet för det lokala nätverket som ansluter till Azure.</span><span class="sxs-lookup"><span data-stu-id="00fb3-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="00fb3-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="00fb3-110">EXAMPLES</span></span>

### <span data-ttu-id="00fb3-111">Exempel 1: skapa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="00fb3-112">Skapar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG" i plats "West" med IP-adressen "23.99.221.164" och adressprefixet "10.5.51.0/24" på-lokala.</span><span class="sxs-lookup"><span data-stu-id="00fb3-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="00fb3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="00fb3-113">PARAMETERS</span></span>

### <span data-ttu-id="00fb3-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="00fb3-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="00fb3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00fb3-115">-AsJob</span></span>
<span data-ttu-id="00fb3-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="00fb3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00fb3-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="00fb3-117">-Asn</span></span>
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

### <span data-ttu-id="00fb3-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="00fb3-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="00fb3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fb3-119">-DefaultProfile</span></span>
<span data-ttu-id="00fb3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="00fb3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00fb3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="00fb3-121">-Force</span></span>
<span data-ttu-id="00fb3-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="00fb3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00fb3-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="00fb3-123">-Fqdn</span></span>
<span data-ttu-id="00fb3-124">FQDN för lokal nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="00fb3-124">FQDN of local network gateway.</span></span>

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

### <span data-ttu-id="00fb3-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="00fb3-125">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="00fb3-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="00fb3-126">-Location</span></span>
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

### <span data-ttu-id="00fb3-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="00fb3-127">-Name</span></span>
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

### <span data-ttu-id="00fb3-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="00fb3-128">-PeerWeight</span></span>
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

### <span data-ttu-id="00fb3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fb3-129">-ResourceGroupName</span></span>
<span data-ttu-id="00fb3-130">Anger den resurs grupp som den lokala nät portens Gateway tillhör.</span><span class="sxs-lookup"><span data-stu-id="00fb3-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="00fb3-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="00fb3-131">-Tag</span></span>
<span data-ttu-id="00fb3-132">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="00fb3-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="00fb3-133">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="00fb3-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="00fb3-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="00fb3-134">-Confirm</span></span>
<span data-ttu-id="00fb3-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="00fb3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fb3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fb3-136">-WhatIf</span></span>
<span data-ttu-id="00fb3-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="00fb3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fb3-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="00fb3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fb3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fb3-139">CommonParameters</span></span>
<span data-ttu-id="00fb3-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fb3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fb3-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00fb3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fb3-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="00fb3-142">INPUTS</span></span>

### <span data-ttu-id="00fb3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="00fb3-143">System.String</span></span>

### <span data-ttu-id="00fb3-144">System. string []</span><span class="sxs-lookup"><span data-stu-id="00fb3-144">System.String[]</span></span>

### <span data-ttu-id="00fb3-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="00fb3-145">System.UInt32</span></span>

### <span data-ttu-id="00fb3-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="00fb3-146">System.Int32</span></span>

### <span data-ttu-id="00fb3-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="00fb3-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="00fb3-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="00fb3-148">OUTPUTS</span></span>

### <span data-ttu-id="00fb3-149">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="00fb3-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="00fb3-150">NOTES</span></span>

## <span data-ttu-id="00fb3-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="00fb3-151">RELATED LINKS</span></span>

[<span data-ttu-id="00fb3-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="00fb3-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="00fb3-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00fb3-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
