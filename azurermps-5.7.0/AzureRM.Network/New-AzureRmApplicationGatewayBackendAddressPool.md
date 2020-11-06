---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 7b92f090a4866dabeb064e828dbf3386e26fcb53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577140"
---
# <span data-ttu-id="3aeee-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3aeee-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="3aeee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3aeee-102">SYNOPSIS</span></span>
<span data-ttu-id="3aeee-103">Skapar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="3aeee-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3aeee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3aeee-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aeee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3aeee-105">DESCRIPTION</span></span>
<span data-ttu-id="3aeee-106">Cmdleten **New-AzureRmApplicationGatewayBackendAddressPool** skapar en backend-adresspool för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="3aeee-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="3aeee-107">En backend-adress kan anges som en IP-adress, ett fullkvalificerat domän namn (FQDN) eller ett IP-konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="3aeee-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="3aeee-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3aeee-108">EXAMPLES</span></span>

### <span data-ttu-id="3aeee-109">Exempel 1: skapa en backend-adresspool genom att använda FQDN-namnet på en backend-server</span><span class="sxs-lookup"><span data-stu-id="3aeee-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="3aeee-110">Det här kommandot skapar en backend-adresspool med namnet Pool01 med hjälp av FQDN-namnen på backend-servrar och lagrar dem i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="3aeee-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="3aeee-111">Exempel 2: skapa en backend-adresspool med hjälp av IP-adressen för en backend-server</span><span class="sxs-lookup"><span data-stu-id="3aeee-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="3aeee-112">Det här kommandot skapar en backend-adresspool med namnet Pool02 med hjälp av IP-adresserna för backend-servrar och lagrar dem i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="3aeee-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="3aeee-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3aeee-113">PARAMETERS</span></span>

### <span data-ttu-id="3aeee-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="3aeee-114">-BackendFqdns</span></span>
<span data-ttu-id="3aeee-115">Anger en lista över FQDN-namn för backend som denna cmdlet associerar med backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="3aeee-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="3aeee-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="3aeee-116">-BackendIPAddresses</span></span>
<span data-ttu-id="3aeee-117">Anger en lista över backend-IP-adresser som denna cmdlet associerar med backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="3aeee-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="3aeee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aeee-118">-DefaultProfile</span></span>
<span data-ttu-id="3aeee-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3aeee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3aeee-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="3aeee-120">-Name</span></span>
<span data-ttu-id="3aeee-121">Anger namnet på backend-serverpoolen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3aeee-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3aeee-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3aeee-122">-Confirm</span></span>
<span data-ttu-id="3aeee-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3aeee-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aeee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aeee-124">-WhatIf</span></span>
<span data-ttu-id="3aeee-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3aeee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aeee-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3aeee-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aeee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aeee-127">CommonParameters</span></span>
<span data-ttu-id="3aeee-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aeee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aeee-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aeee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aeee-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3aeee-130">INPUTS</span></span>

### <span data-ttu-id="3aeee-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3aeee-131">System.String</span></span>

## <span data-ttu-id="3aeee-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3aeee-132">OUTPUTS</span></span>

### <span data-ttu-id="3aeee-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3aeee-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="3aeee-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3aeee-134">NOTES</span></span>

## <span data-ttu-id="3aeee-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3aeee-135">RELATED LINKS</span></span>

[<span data-ttu-id="3aeee-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3aeee-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3aeee-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3aeee-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3aeee-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3aeee-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="3aeee-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3aeee-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


