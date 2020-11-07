---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: fd9d9c1b7956c16ab981b5426e9453de4d730dd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924286"
---
# <span data-ttu-id="f0c89-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0c89-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f0c89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0c89-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c89-103">Uppdaterar en server för backend-adresspoolen för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="f0c89-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="f0c89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0c89-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0c89-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0c89-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c89-106">Cmdleten **set-AzApplicationGatewayBackendAddressPool** uppdaterar en backend-adresspool för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f0c89-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="f0c89-107">Backend-adresser kan anges som IP-adresser, FQDN (Fully Qualified Domain Names) eller IP-konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="f0c89-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="f0c89-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0c89-108">EXAMPLES</span></span>

### <span data-ttu-id="f0c89-109">Exempel 1: Ange en backend-adresspool med hjälp av FQDN</span><span class="sxs-lookup"><span data-stu-id="f0c89-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="f0c89-110">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="f0c89-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f0c89-111">Det andra kommandot uppdaterar backend-adresspoolen för programgatewayen i $AppGw genom att använda FQDN-namn.</span><span class="sxs-lookup"><span data-stu-id="f0c89-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="f0c89-112">Exempel 2: Ange en backend-adresspool genom att använda IP-adresser för backend-servern</span><span class="sxs-lookup"><span data-stu-id="f0c89-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f0c89-113">Det första kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen som heter ResourceGroup01 och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="f0c89-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f0c89-114">Det andra kommandot uppdaterar backend-adresspoolen för programgatewayen i $AppGw genom att använda IP-adresser.</span><span class="sxs-lookup"><span data-stu-id="f0c89-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="f0c89-115">Exempel 3: Ange en backend-adresspool genom att använda ID för backend-serverns IP-adress</span><span class="sxs-lookup"><span data-stu-id="f0c89-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="f0c89-116">Det första kommandot får ett nätverks gränssnitts objekt med namnet Nic01 som tillhör resurs gruppen med namnet ResourceGroup01 och lagrar det i variabeln $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="f0c89-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="f0c89-117">Det andra kommandot får ett nätverks gränssnitts objekt med namnet Nic02 som tillhör resurs gruppen med namnet ResourceGroup02 och lagrar det i $Nic 02-variabeln.</span><span class="sxs-lookup"><span data-stu-id="f0c89-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="f0c89-118">Det tredje kommandot får den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01" och lagrar den i $AppGw variabel.</span><span class="sxs-lookup"><span data-stu-id="f0c89-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f0c89-119">Kommandot Använd använder IP-konfigurations-ID för backend från $Nic 01 och $Nic 02 för att uppdatera backend-adresspoolen för programgatewayen i $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f0c89-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="f0c89-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0c89-120">PARAMETERS</span></span>

### <span data-ttu-id="f0c89-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0c89-121">-ApplicationGateway</span></span>
<span data-ttu-id="f0c89-122">Anger den Programgateway som denna cmdlet kopplar till backend-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="f0c89-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c89-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f0c89-123">-BackendFqdns</span></span>
<span data-ttu-id="f0c89-124">Anger en lista över backend-IP-adresser som ska användas som backend-server.</span><span class="sxs-lookup"><span data-stu-id="f0c89-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="f0c89-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f0c89-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="f0c89-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c89-126">-DefaultProfile</span></span>
<span data-ttu-id="f0c89-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c89-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0c89-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0c89-128">-Name</span></span>
<span data-ttu-id="f0c89-129">Anger namnet på backend-adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="f0c89-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="f0c89-130">Denna backend-adresspool måste finnas i programgatewayen.</span><span class="sxs-lookup"><span data-stu-id="f0c89-130">This back-end address pool must exist in the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0c89-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f0c89-131">-Confirm</span></span>
<span data-ttu-id="f0c89-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f0c89-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c89-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c89-133">-WhatIf</span></span>
<span data-ttu-id="f0c89-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f0c89-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c89-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f0c89-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c89-136">CommonParameters</span></span>
<span data-ttu-id="f0c89-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c89-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0c89-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c89-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0c89-139">INPUTS</span></span>

### <span data-ttu-id="f0c89-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f0c89-140">System.String</span></span>

## <span data-ttu-id="f0c89-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0c89-141">OUTPUTS</span></span>

### <span data-ttu-id="f0c89-142">Microsoft. Azure. commands. Networks. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f0c89-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f0c89-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0c89-143">NOTES</span></span>

## <span data-ttu-id="f0c89-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0c89-144">RELATED LINKS</span></span>

[<span data-ttu-id="f0c89-145">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0c89-145">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0c89-146">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0c89-146">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0c89-147">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0c89-147">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f0c89-148">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f0c89-148">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


