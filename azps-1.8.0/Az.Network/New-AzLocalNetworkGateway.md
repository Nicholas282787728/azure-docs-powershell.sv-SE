---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 9f622a6796cd63aeb6a4de760b21fd487d210af2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748041"
---
# <span data-ttu-id="10a27-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10a27-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="10a27-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10a27-102">SYNOPSIS</span></span>
<span data-ttu-id="10a27-103">Skapar en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="10a27-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="10a27-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10a27-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10a27-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10a27-105">DESCRIPTION</span></span>
<span data-ttu-id="10a27-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="10a27-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="10a27-107">Cmdleten **New-AzLocalNetworkGateway** skapar objektet som representerar din lokala-gateway baserat på gatewayens namn, resurs gruppens namn, plats och IP-adress, samt adressprefixet för det lokala nätverket som ansluter till Azure.</span><span class="sxs-lookup"><span data-stu-id="10a27-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="10a27-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10a27-108">EXAMPLES</span></span>

### <span data-ttu-id="10a27-109">1: skapa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="10a27-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="10a27-110">Skapar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG" i plats "West" med IP-adressen "23.99.221.164" och adressprefixet "10.5.51.0/24" på-lokala.</span><span class="sxs-lookup"><span data-stu-id="10a27-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="10a27-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10a27-111">PARAMETERS</span></span>

### <span data-ttu-id="10a27-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="10a27-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="10a27-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10a27-113">-AsJob</span></span>
<span data-ttu-id="10a27-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="10a27-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10a27-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="10a27-115">-Asn</span></span>
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

### <span data-ttu-id="10a27-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="10a27-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="10a27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a27-117">-DefaultProfile</span></span>
<span data-ttu-id="10a27-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10a27-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10a27-119">-Force</span><span class="sxs-lookup"><span data-stu-id="10a27-119">-Force</span></span>
<span data-ttu-id="10a27-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="10a27-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10a27-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="10a27-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="10a27-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="10a27-122">-Location</span></span>
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

### <span data-ttu-id="10a27-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="10a27-123">-Name</span></span>
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

### <span data-ttu-id="10a27-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="10a27-124">-PeerWeight</span></span>
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

### <span data-ttu-id="10a27-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10a27-125">-ResourceGroupName</span></span>
<span data-ttu-id="10a27-126">Anger den resurs grupp som den lokala nät portens Gateway tillhör.</span><span class="sxs-lookup"><span data-stu-id="10a27-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="10a27-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="10a27-127">-Tag</span></span>
<span data-ttu-id="10a27-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="10a27-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="10a27-129">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="10a27-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="10a27-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10a27-130">-Confirm</span></span>
<span data-ttu-id="10a27-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10a27-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a27-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a27-132">-WhatIf</span></span>
<span data-ttu-id="10a27-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10a27-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a27-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10a27-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a27-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a27-135">CommonParameters</span></span>
<span data-ttu-id="10a27-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a27-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a27-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a27-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a27-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10a27-138">INPUTS</span></span>

### <span data-ttu-id="10a27-139">System. String</span><span class="sxs-lookup"><span data-stu-id="10a27-139">System.String</span></span>

### <span data-ttu-id="10a27-140">System. string []</span><span class="sxs-lookup"><span data-stu-id="10a27-140">System.String[]</span></span>

### <span data-ttu-id="10a27-141">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="10a27-141">System.UInt32</span></span>

### <span data-ttu-id="10a27-142">System. Int32</span><span class="sxs-lookup"><span data-stu-id="10a27-142">System.Int32</span></span>

### <span data-ttu-id="10a27-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="10a27-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="10a27-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10a27-144">OUTPUTS</span></span>

### <span data-ttu-id="10a27-145">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10a27-145">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="10a27-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10a27-146">NOTES</span></span>

## <span data-ttu-id="10a27-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10a27-147">RELATED LINKS</span></span>

[<span data-ttu-id="10a27-148">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10a27-148">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="10a27-149">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10a27-149">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="10a27-150">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="10a27-150">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
