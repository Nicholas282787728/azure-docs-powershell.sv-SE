---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 5b41cedc02818db6c309e3c11bb1797fb6525d75
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926545"
---
# <span data-ttu-id="53717-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53717-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="53717-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53717-102">SYNOPSIS</span></span>
<span data-ttu-id="53717-103">Lägger till en adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="53717-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="53717-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53717-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53717-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53717-105">DESCRIPTION</span></span>
<span data-ttu-id="53717-106">Cmdleten **Add-AzApplicationGatewayBackendAddressPool** lägger till en backend-adresspool till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="53717-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="53717-107">En backend-adress kan anges med en IP-adress, ett fullkvalificerat domän namn (FQDN) eller IP-konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="53717-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="53717-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53717-108">EXAMPLES</span></span>

### <span data-ttu-id="53717-109">Exempel 1: lägga till en backend-adresspool med hjälp av en server för backend-servern</span><span class="sxs-lookup"><span data-stu-id="53717-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="53717-110">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda FQDN-namn.</span><span class="sxs-lookup"><span data-stu-id="53717-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="53717-111">Exempel 2: lägga till en backend-adresspool genom att använda IP-adresser för backend-servern</span><span class="sxs-lookup"><span data-stu-id="53717-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="53717-112">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="53717-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="53717-113">Exempel 3: Seta backend-adresspool genom att använda ID för backend-serverns IP-adress</span><span class="sxs-lookup"><span data-stu-id="53717-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="53717-114">Det första kommandot får ett nätverks gränssnitts objekt med namnet Nic01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar det i variabeln $Nic 01. Det andra kommandot får ett nätverks gränssnitts objekt med namnet Nic02 som tillhör resurs gruppen med namnet ResourceGroup02 och lagrar det i $Nic 02-variabeln. Det tredje kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01" och lagrar den i $AppGw variabel. Kommandot det sista använder IP-konfigurations-ID för backend från $Nic 01 och $Nic 02 för att lägga till backend-adresspoolen för Application Gateway som lagras i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="53717-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="53717-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53717-115">PARAMETERS</span></span>

### <span data-ttu-id="53717-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53717-116">-ApplicationGateway</span></span>
<span data-ttu-id="53717-117">Anger den Programgateway som denna cmdlet lägger till en backend-adresspool för.</span><span class="sxs-lookup"><span data-stu-id="53717-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="53717-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="53717-118">-BackendFqdns</span></span>
<span data-ttu-id="53717-119">Anger en lista över FQDN-namn för Server delar som denna cmdlet lägger till som backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="53717-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53717-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="53717-120">-BackendIPAddresses</span></span>
<span data-ttu-id="53717-121">Anger en lista över backend-IP-adresser som denna cmdlet lägger till som backend-server.</span><span class="sxs-lookup"><span data-stu-id="53717-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53717-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53717-122">-DefaultProfile</span></span>
<span data-ttu-id="53717-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53717-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53717-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="53717-124">-Name</span></span>
<span data-ttu-id="53717-125">Anger namnet på backend-serverpoolen som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="53717-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="53717-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53717-126">-Confirm</span></span>
<span data-ttu-id="53717-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53717-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53717-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53717-128">-WhatIf</span></span>
<span data-ttu-id="53717-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="53717-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53717-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="53717-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53717-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53717-131">CommonParameters</span></span>
<span data-ttu-id="53717-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53717-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53717-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53717-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53717-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53717-134">INPUTS</span></span>

### <span data-ttu-id="53717-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53717-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53717-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53717-136">OUTPUTS</span></span>

### <span data-ttu-id="53717-137">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53717-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="53717-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53717-138">NOTES</span></span>

## <span data-ttu-id="53717-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53717-139">RELATED LINKS</span></span>

[<span data-ttu-id="53717-140">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53717-140">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="53717-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53717-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="53717-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53717-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="53717-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53717-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="53717-144">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="53717-144">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


