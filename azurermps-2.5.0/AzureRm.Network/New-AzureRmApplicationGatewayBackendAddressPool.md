---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: dcce5b85fc9d3e8046ecc90330da5f3d40b88e33
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929742"
---
# <span data-ttu-id="7d43f-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d43f-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7d43f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d43f-102">SYNOPSIS</span></span>
<span data-ttu-id="7d43f-103">Skapar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="7d43f-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d43f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d43f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d43f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d43f-105">DESCRIPTION</span></span>
<span data-ttu-id="7d43f-106">Cmdleten **New-AzureRmApplicationGatewayBackendAddressPool** skapar en backend-adresspool för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7d43f-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="7d43f-107">En backend-adress kan anges som en IP-adress, ett fullkvalificerat domän namn (FQDN) eller ett IP-konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="7d43f-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="7d43f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d43f-108">EXAMPLES</span></span>

### <span data-ttu-id="7d43f-109">Exempel 1: skapa en backend-adresspool genom att använda FQDN-namnet på en backend-server</span><span class="sxs-lookup"><span data-stu-id="7d43f-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="7d43f-110">Det här kommandot skapar en backend-adresspool med namnet Pool01 med hjälp av FQDN-namnen på backend-servrar och lagrar dem i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="7d43f-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="7d43f-111">Exempel 2: skapa en backend-adresspool med hjälp av IP-adressen för en backend-server</span><span class="sxs-lookup"><span data-stu-id="7d43f-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="7d43f-112">Det här kommandot skapar en backend-adresspool med namnet Pool02 med hjälp av IP-adresserna för backend-servrar och lagrar dem i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="7d43f-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="7d43f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d43f-113">PARAMETERS</span></span>

### <span data-ttu-id="7d43f-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="7d43f-114">-BackendFqdns</span></span>
<span data-ttu-id="7d43f-115">Anger en lista över FQDN-namn för backend som denna cmdlet associerar med backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="7d43f-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="7d43f-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="7d43f-116">-BackendIPAddresses</span></span>
<span data-ttu-id="7d43f-117">Anger en lista över backend-IP-adresser som denna cmdlet associerar med backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="7d43f-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="7d43f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d43f-118">-DefaultProfile</span></span>
<span data-ttu-id="7d43f-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d43f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d43f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d43f-120">-Name</span></span>
<span data-ttu-id="7d43f-121">Anger namnet på backend-serverpoolen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="7d43f-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7d43f-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d43f-122">-Confirm</span></span>
<span data-ttu-id="7d43f-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d43f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d43f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d43f-124">-WhatIf</span></span>
<span data-ttu-id="7d43f-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d43f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d43f-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d43f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d43f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d43f-127">CommonParameters</span></span>
<span data-ttu-id="7d43f-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d43f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d43f-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d43f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d43f-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d43f-130">INPUTS</span></span>

### <span data-ttu-id="7d43f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7d43f-131">System.String</span></span>

## <span data-ttu-id="7d43f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d43f-132">OUTPUTS</span></span>

### <span data-ttu-id="7d43f-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d43f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="7d43f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d43f-134">NOTES</span></span>

## <span data-ttu-id="7d43f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d43f-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d43f-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d43f-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7d43f-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d43f-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7d43f-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d43f-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="7d43f-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d43f-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


