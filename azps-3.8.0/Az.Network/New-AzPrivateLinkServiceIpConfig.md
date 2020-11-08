---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: e1d7c2d78bf58240cc87e7a224be1632828984d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090983"
---
# <span data-ttu-id="a734c-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a734c-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="a734c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a734c-102">SYNOPSIS</span></span>
<span data-ttu-id="a734c-103">Skapa en IP-konfiguration för privata länk tjänster.</span><span class="sxs-lookup"><span data-stu-id="a734c-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="a734c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a734c-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a734c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a734c-105">DESCRIPTION</span></span>
<span data-ttu-id="a734c-106">Cmdleten **New-AzPrivateLinkServiceIpConfig** skapar en IP-konfiguration för privata länk tjänster.</span><span class="sxs-lookup"><span data-stu-id="a734c-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="a734c-107">Denna konfiguration används för käll-NAT-ing den inkommande trafiken från privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="a734c-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="a734c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a734c-108">EXAMPLES</span></span>

### <span data-ttu-id="a734c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a734c-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="a734c-110">I det här exemplet skapas en IP-konfiguration för privata länk tjänster i minnet.</span><span class="sxs-lookup"><span data-stu-id="a734c-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="a734c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a734c-111">PARAMETERS</span></span>

### <span data-ttu-id="a734c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a734c-112">-DefaultProfile</span></span>
<span data-ttu-id="a734c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a734c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a734c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a734c-114">-Name</span></span>
<span data-ttu-id="a734c-115">Namnet på IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a734c-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="a734c-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="a734c-116">-PrivateIpAddress</span></span>
<span data-ttu-id="a734c-117">Den privata IP-adressen för ipConfiguration om statisk tilldelning har angetts.</span><span class="sxs-lookup"><span data-stu-id="a734c-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734c-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="a734c-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="a734c-119">IP-version för IP-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="a734c-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734c-120">-Primär</span><span class="sxs-lookup"><span data-stu-id="a734c-120">-Primary</span></span>
<span data-ttu-id="a734c-121">Ange att aktuell IP-konfiguration är primär eller inte.</span><span class="sxs-lookup"><span data-stu-id="a734c-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="a734c-122">-Undernät</span><span class="sxs-lookup"><span data-stu-id="a734c-122">-Subnet</span></span>
<span data-ttu-id="a734c-123">Under</span><span class="sxs-lookup"><span data-stu-id="a734c-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a734c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a734c-124">CommonParameters</span></span>
<span data-ttu-id="a734c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a734c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a734c-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a734c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a734c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a734c-127">INPUTS</span></span>

### <span data-ttu-id="a734c-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="a734c-128">None</span></span>

## <span data-ttu-id="a734c-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a734c-129">OUTPUTS</span></span>

### <span data-ttu-id="a734c-130">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a734c-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="a734c-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a734c-131">NOTES</span></span>

## <span data-ttu-id="a734c-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a734c-132">RELATED LINKS</span></span>

[<span data-ttu-id="a734c-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a734c-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)