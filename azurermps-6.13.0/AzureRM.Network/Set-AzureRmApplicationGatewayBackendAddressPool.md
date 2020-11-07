---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d62afff67d1b5e7722b107b70810ac82e5b151d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756373"
---
# <span data-ttu-id="361cc-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="361cc-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="361cc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="361cc-102">SYNOPSIS</span></span>
<span data-ttu-id="361cc-103">Uppdaterar en server för backend-adresspoolen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="361cc-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="361cc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="361cc-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="361cc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="361cc-105">DESCRIPTION</span></span>
<span data-ttu-id="361cc-106">Cmdleten **set-AzureRmApplicationGatewayBackendAddressPool** uppdaterar en backend-adresspool för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="361cc-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="361cc-107">Backend-adresser kan anges som IP-adresser, FQDN (Fully Qualified Domain Names) eller IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="361cc-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="361cc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="361cc-108">EXAMPLES</span></span>

### <span data-ttu-id="361cc-109">Exempel 1: Ange en backend-adresspool med hjälp av FQDN</span><span class="sxs-lookup"><span data-stu-id="361cc-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="361cc-110">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="361cc-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="361cc-111">Det andra kommandot uppdaterar backend-adresspoolen för programgatewayen i $AppGw genom att använda FQDN-namn.</span><span class="sxs-lookup"><span data-stu-id="361cc-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="361cc-112">Exempel 2: Ange en backend-adresspool genom att använda IP-adresser för backend-servern</span><span class="sxs-lookup"><span data-stu-id="361cc-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="361cc-113">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="361cc-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="361cc-114">Det andra kommandot uppdaterar backend-adresspoolen för programgatewayen i $AppGw genom att använda IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="361cc-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="361cc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="361cc-115">PARAMETERS</span></span>

### <span data-ttu-id="361cc-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="361cc-116">-ApplicationGateway</span></span>
<span data-ttu-id="361cc-117">Anger den Programgateway som denna cmdlet kopplar till backend-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="361cc-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="361cc-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="361cc-118">-BackendFqdns</span></span>
<span data-ttu-id="361cc-119">Anger en lista över backend-IP-adresser som ska användas som backend-server.</span><span class="sxs-lookup"><span data-stu-id="361cc-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="361cc-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="361cc-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="361cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361cc-121">-DefaultProfile</span></span>
<span data-ttu-id="361cc-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="361cc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="361cc-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="361cc-123">-Name</span></span>
<span data-ttu-id="361cc-124">Anger namnet på backend-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="361cc-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="361cc-125">Denna backend-adresspool måste finnas i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="361cc-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="361cc-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="361cc-126">-Confirm</span></span>
<span data-ttu-id="361cc-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="361cc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="361cc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="361cc-128">-WhatIf</span></span>
<span data-ttu-id="361cc-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="361cc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="361cc-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="361cc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="361cc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361cc-131">CommonParameters</span></span>
<span data-ttu-id="361cc-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361cc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361cc-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="361cc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361cc-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="361cc-134">INPUTS</span></span>

### <span data-ttu-id="361cc-135">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="361cc-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="361cc-136">Parametrar: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="361cc-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="361cc-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="361cc-137">OUTPUTS</span></span>

### <span data-ttu-id="361cc-138">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="361cc-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="361cc-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="361cc-139">NOTES</span></span>

## <span data-ttu-id="361cc-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="361cc-140">RELATED LINKS</span></span>

[<span data-ttu-id="361cc-141">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="361cc-141">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="361cc-142">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="361cc-142">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="361cc-143">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="361cc-143">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="361cc-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="361cc-144">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


