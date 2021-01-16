---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: d44cf2faa4c7f50fcf1085fe528f638ba2e182df
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421939"
---
# <span data-ttu-id="dbdc5-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dbdc5-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dbdc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbdc5-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdc5-103">Skapar en backend-adresspool för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="dbdc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbdc5-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbdc5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbdc5-105">DESCRIPTION</span></span>
<span data-ttu-id="dbdc5-106">Cmdleten **New-AzApplicationGatewayBackendAddressPool** skapar en backend-adresspool för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="dbdc5-107">En backend-adress kan anges som en IP-adress, ett fullkvalificerat domän namn (FQDN) eller ett IP-konfigurations-ID.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="dbdc5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbdc5-108">EXAMPLES</span></span>

### <span data-ttu-id="dbdc5-109">Exempel 1: skapa en backend-adresspool genom att använda FQDN-namnet på en backend-server</span><span class="sxs-lookup"><span data-stu-id="dbdc5-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="dbdc5-110">Det här kommandot skapar en backend-adresspool med namnet Pool01 med hjälp av FQDN-namnen på backend-servrar och lagrar dem i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="dbdc5-111">Exempel 2: skapa en backend-adresspool med hjälp av IP-adressen för en backend-server</span><span class="sxs-lookup"><span data-stu-id="dbdc5-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="dbdc5-112">Det här kommandot skapar en backend-adresspool med namnet Pool02 med hjälp av IP-adresserna för backend-servrar och lagrar dem i $Pool variabel.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="dbdc5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbdc5-113">PARAMETERS</span></span>

### <span data-ttu-id="dbdc5-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="dbdc5-114">-BackendFqdns</span></span>
<span data-ttu-id="dbdc5-115">Anger en lista över FQDN-namn för backend som denna cmdlet associerar med backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="dbdc5-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="dbdc5-116">-BackendIPAddresses</span></span>
<span data-ttu-id="dbdc5-117">Anger en lista över backend-IP-adresser som denna cmdlet associerar med backend-serverpoolen.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="dbdc5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdc5-118">-DefaultProfile</span></span>
<span data-ttu-id="dbdc5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbdc5-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbdc5-120">-Name</span></span>
<span data-ttu-id="dbdc5-121">Anger namnet på backend-serverpoolen som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dbdc5-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbdc5-122">-Confirm</span></span>
<span data-ttu-id="dbdc5-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdc5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdc5-124">-WhatIf</span></span>
<span data-ttu-id="dbdc5-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdc5-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdc5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdc5-127">CommonParameters</span></span>
<span data-ttu-id="dbdc5-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdc5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdc5-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbdc5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdc5-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbdc5-130">INPUTS</span></span>

### <span data-ttu-id="dbdc5-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="dbdc5-131">None</span></span>

## <span data-ttu-id="dbdc5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbdc5-132">OUTPUTS</span></span>

### <span data-ttu-id="dbdc5-133">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dbdc5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dbdc5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbdc5-134">NOTES</span></span>

## <span data-ttu-id="dbdc5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbdc5-135">RELATED LINKS</span></span>

[<span data-ttu-id="dbdc5-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dbdc5-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dbdc5-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dbdc5-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dbdc5-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dbdc5-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dbdc5-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dbdc5-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


