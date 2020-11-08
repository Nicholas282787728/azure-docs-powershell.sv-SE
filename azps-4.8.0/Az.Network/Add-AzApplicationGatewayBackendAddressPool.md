---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258844"
---
# <span data-ttu-id="81485-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81485-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="81485-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="81485-102">SYNOPSIS</span></span>
<span data-ttu-id="81485-103">Lägger till en adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="81485-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="81485-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="81485-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81485-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="81485-105">DESCRIPTION</span></span>
<span data-ttu-id="81485-106">Cmdleten **Add-AzApplicationGatewayBackendAddressPool** lägger till en backend-adresspool till en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="81485-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="81485-107">En backend-adress kan anges med en IP-adress, ett fullkvalificerat domän namn (FQDN) eller IP-konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="81485-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="81485-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="81485-108">EXAMPLES</span></span>

### <span data-ttu-id="81485-109">Exempel 1: lägga till en backend-adresspool med hjälp av en server för backend-servern</span><span class="sxs-lookup"><span data-stu-id="81485-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="81485-110">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda FQDN-namn.</span><span class="sxs-lookup"><span data-stu-id="81485-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="81485-111">Exempel 2: lägga till en backend-adresspool genom att använda IP-adresser för backend-servern</span><span class="sxs-lookup"><span data-stu-id="81485-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="81485-112">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel. Det andra kommandot lägger till backend-adresspoolen för den Programgateway som lagras i $AppGw genom att använda IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="81485-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="81485-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="81485-113">PARAMETERS</span></span>

### <span data-ttu-id="81485-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81485-114">-ApplicationGateway</span></span>
<span data-ttu-id="81485-115">Anger den Programgateway som denna cmdlet lägger till en backend-adresspool för.</span><span class="sxs-lookup"><span data-stu-id="81485-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="81485-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="81485-116">-BackendFqdns</span></span>
<span data-ttu-id="81485-117">Anger en lista över FQDN-namn för Server delar som denna cmdlet lägger till som backend-adresspool.</span><span class="sxs-lookup"><span data-stu-id="81485-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="81485-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="81485-118">-BackendIPAddresses</span></span>
<span data-ttu-id="81485-119">Anger en lista över backend-IP-adresser som denna cmdlet lägger till som backend-server.</span><span class="sxs-lookup"><span data-stu-id="81485-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="81485-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81485-120">-DefaultProfile</span></span>
<span data-ttu-id="81485-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="81485-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81485-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="81485-122">-Name</span></span>
<span data-ttu-id="81485-123">Anger namnet på backend-serverpoolen som denna cmdlet lägger till.</span><span class="sxs-lookup"><span data-stu-id="81485-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="81485-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="81485-124">-Confirm</span></span>
<span data-ttu-id="81485-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="81485-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81485-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81485-126">-WhatIf</span></span>
<span data-ttu-id="81485-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="81485-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81485-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="81485-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81485-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81485-129">CommonParameters</span></span>
<span data-ttu-id="81485-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81485-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81485-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81485-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81485-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="81485-132">INPUTS</span></span>

### <span data-ttu-id="81485-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81485-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81485-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="81485-134">OUTPUTS</span></span>

### <span data-ttu-id="81485-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="81485-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="81485-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="81485-136">NOTES</span></span>

## <span data-ttu-id="81485-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="81485-137">RELATED LINKS</span></span>

[<span data-ttu-id="81485-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81485-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81485-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81485-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81485-140">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81485-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81485-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81485-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81485-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="81485-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="81485-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="81485-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
