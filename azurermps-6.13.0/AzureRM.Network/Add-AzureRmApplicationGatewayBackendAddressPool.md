---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 29e127d974b6c7ef0bdf0272c16c036f69e53428
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757063"
---
# <span data-ttu-id="ef29b-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef29b-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="ef29b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef29b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef29b-103">Lägger till en adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ef29b-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef29b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef29b-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef29b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef29b-105">DESCRIPTION</span></span>
<span data-ttu-id="ef29b-106">Cmdleten **Add-AzureRmApplicationGatewayBackendAddressPool** lägger till en backend-adresspool till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="ef29b-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="ef29b-107">En backend-adress kan anges med en IP-adress, ett fullkvalificerat domän namn (FQDN) eller IP-konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="ef29b-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="ef29b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef29b-108">EXAMPLES</span></span>

### <span data-ttu-id="ef29b-109">Exempel 1: lägga till en backend-adresspool med hjälp av en server för backend-servern</span><span class="sxs-lookup"><span data-stu-id="ef29b-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="ef29b-110">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda FQDN-namn.</span><span class="sxs-lookup"><span data-stu-id="ef29b-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="ef29b-111">Exempel 2: lägga till en backend-adresspool genom att använda IP-adresser för backend-servern</span><span class="sxs-lookup"><span data-stu-id="ef29b-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="ef29b-112">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="ef29b-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="ef29b-113">Exempel 3: Seta backend-adresspool genom att använda ID för backend-serverns IP-adress</span><span class="sxs-lookup"><span data-stu-id="ef29b-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="ef29b-114">Det första kommandot får ett nätverks gränssnitts objekt med namnet Nic01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar det i variabeln $Nic 01. Det andra kommandot får ett nätverks gränssnitts objekt med namnet Nic02 som tillhör resurs gruppen med namnet ResourceGroup02 och lagrar det i $Nic 02-variabeln. Det tredje kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01" och lagrar den i $AppGw variabel. Kommandot det sista använder IP-konfigurations-ID för backend från $Nic 01 och $Nic 02 för att lägga till backend-adresspoolen för Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ef29b-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="ef29b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef29b-115">PARAMETERS</span></span>

### <span data-ttu-id="ef29b-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef29b-116">-ApplicationGateway</span></span>
<span data-ttu-id="ef29b-117">Anger den Programgateway som denna cmdlet lägger till en backend-adresspool för.</span><span class="sxs-lookup"><span data-stu-id="ef29b-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef29b-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="ef29b-118">-BackendFqdns</span></span>
<span data-ttu-id="ef29b-119">Anger en lista över FQDN-namn för Server delar som denna cmdlet lägger till som backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="ef29b-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef29b-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="ef29b-120">-BackendIPAddresses</span></span>
<span data-ttu-id="ef29b-121">Anger en lista över backend-IP-adresser som denna cmdlet lägger till som backend-server.</span><span class="sxs-lookup"><span data-stu-id="ef29b-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef29b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef29b-122">-DefaultProfile</span></span>
<span data-ttu-id="ef29b-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef29b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef29b-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef29b-124">-Name</span></span>
<span data-ttu-id="ef29b-125">Anger namnet på backend-serverpoolen som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="ef29b-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="ef29b-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef29b-126">-Confirm</span></span>
<span data-ttu-id="ef29b-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef29b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef29b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef29b-128">-WhatIf</span></span>
<span data-ttu-id="ef29b-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef29b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef29b-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef29b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef29b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef29b-131">CommonParameters</span></span>
<span data-ttu-id="ef29b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef29b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef29b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef29b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef29b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef29b-134">INPUTS</span></span>

### <span data-ttu-id="ef29b-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef29b-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="ef29b-136">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef29b-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="ef29b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef29b-137">OUTPUTS</span></span>

### <span data-ttu-id="ef29b-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef29b-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef29b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef29b-139">NOTES</span></span>

## <span data-ttu-id="ef29b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef29b-140">RELATED LINKS</span></span>

[<span data-ttu-id="ef29b-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef29b-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef29b-142">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef29b-142">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef29b-143">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef29b-143">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef29b-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef29b-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="ef29b-145">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ef29b-145">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


