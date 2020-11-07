---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
ms.openlocfilehash: c450d2f6fd3d9a9b0368a667573aadadbd218d8f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930186"
---
# <span data-ttu-id="52231-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52231-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="52231-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52231-102">SYNOPSIS</span></span>
<span data-ttu-id="52231-103">Skapar en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="52231-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52231-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52231-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52231-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52231-105">DESCRIPTION</span></span>
<span data-ttu-id="52231-106">Den lokala Nätverksgatewayen är det objekt som representerar din privata VPN-enhet.</span><span class="sxs-lookup"><span data-stu-id="52231-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="52231-107">Cmdleten **New-AzureRmLocalNetworkGateway** skapar objektet som representerar din lokala-gateway baserat på gatewayens namn, resurs gruppens namn, plats och IP-adress, samt adressprefixet för det lokala nätverket som ansluter till Azure.</span><span class="sxs-lookup"><span data-stu-id="52231-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="52231-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52231-108">EXAMPLES</span></span>

### <span data-ttu-id="52231-109">1: skapa en lokal nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="52231-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="52231-110">Skapar objektet för den lokala Nätverksgatewayen med namnet "myLocalGW" i resurs gruppen "myRG" i plats "West" med IP-adressen "23.99.221.164" och adressprefixet "10.5.51.0/24" på-lokala.</span><span class="sxs-lookup"><span data-stu-id="52231-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="52231-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52231-111">PARAMETERS</span></span>

### <span data-ttu-id="52231-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="52231-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52231-113">-AsJob</span></span>
<span data-ttu-id="52231-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="52231-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52231-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="52231-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="52231-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52231-117">-DefaultProfile</span></span>
<span data-ttu-id="52231-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52231-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52231-119">-Force</span><span class="sxs-lookup"><span data-stu-id="52231-119">-Force</span></span>
<span data-ttu-id="52231-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="52231-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="52231-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="52231-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="52231-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="52231-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="52231-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52231-125">-ResourceGroupName</span></span>
<span data-ttu-id="52231-126">Anger den resurs grupp som den lokala nät portens Gateway tillhör.</span><span class="sxs-lookup"><span data-stu-id="52231-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-127">-Tagg</span><span class="sxs-lookup"><span data-stu-id="52231-127">-Tag</span></span>
<span data-ttu-id="52231-128">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="52231-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="52231-129">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="52231-129">For example:</span></span>

<span data-ttu-id="52231-130">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="52231-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52231-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52231-131">-Confirm</span></span>
<span data-ttu-id="52231-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52231-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52231-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52231-133">-WhatIf</span></span>
<span data-ttu-id="52231-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52231-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52231-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52231-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52231-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52231-136">CommonParameters</span></span>
<span data-ttu-id="52231-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52231-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52231-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52231-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52231-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52231-139">INPUTS</span></span>

## <span data-ttu-id="52231-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52231-140">OUTPUTS</span></span>

### <span data-ttu-id="52231-141">Microsoft. Azure. commands. Networks. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52231-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="52231-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52231-142">NOTES</span></span>

## <span data-ttu-id="52231-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52231-143">RELATED LINKS</span></span>

[<span data-ttu-id="52231-144">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52231-144">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="52231-145">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52231-145">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="52231-146">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="52231-146">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
