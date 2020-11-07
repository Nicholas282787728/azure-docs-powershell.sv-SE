---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: c7ea999af626206b741e86457d92627e4db196a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918214"
---
# <span data-ttu-id="234c3-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="234c3-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="234c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="234c3-102">SYNOPSIS</span></span>
<span data-ttu-id="234c3-103">Skapa en IP-konfiguration för privata länk tjänster.</span><span class="sxs-lookup"><span data-stu-id="234c3-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="234c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="234c3-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="234c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="234c3-105">DESCRIPTION</span></span>
<span data-ttu-id="234c3-106">Cmdleten **New-AzPrivateLinkServiceIpConfig** skapar en IP-konfiguration för privata länk tjänster.</span><span class="sxs-lookup"><span data-stu-id="234c3-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="234c3-107">Denna konfiguration används för käll-NAT-ing den inkommande trafiken från privat slut punkt.</span><span class="sxs-lookup"><span data-stu-id="234c3-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="234c3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="234c3-108">EXAMPLES</span></span>

### <span data-ttu-id="234c3-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="234c3-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="234c3-110">I det här exemplet skapas en IP-konfiguration för privata länk tjänster i minnet.</span><span class="sxs-lookup"><span data-stu-id="234c3-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="234c3-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="234c3-111">PARAMETERS</span></span>

### <span data-ttu-id="234c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="234c3-112">-DefaultProfile</span></span>
<span data-ttu-id="234c3-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="234c3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="234c3-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="234c3-114">-Name</span></span>
<span data-ttu-id="234c3-115">Namnet på IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="234c3-115">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="234c3-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="234c3-116">-PrivateIpAddress</span></span>
<span data-ttu-id="234c3-117">Den privata IP-adressen för ipConfiguration om statisk tilldelning har angetts.</span><span class="sxs-lookup"><span data-stu-id="234c3-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

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

### <span data-ttu-id="234c3-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="234c3-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="234c3-119">IP-version för IP-konfigurationen</span><span class="sxs-lookup"><span data-stu-id="234c3-119">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="234c3-120">-Primär</span><span class="sxs-lookup"><span data-stu-id="234c3-120">-Primary</span></span>
<span data-ttu-id="234c3-121">Ange att aktuell IP-konfiguration är primär eller inte.</span><span class="sxs-lookup"><span data-stu-id="234c3-121">Indicate current ip configuration is primary or not.</span></span>

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

### <span data-ttu-id="234c3-122">-Undernät</span><span class="sxs-lookup"><span data-stu-id="234c3-122">-Subnet</span></span>
<span data-ttu-id="234c3-123">Under</span><span class="sxs-lookup"><span data-stu-id="234c3-123">Subnet</span></span>

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

### <span data-ttu-id="234c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="234c3-124">CommonParameters</span></span>
<span data-ttu-id="234c3-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="234c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="234c3-126">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="234c3-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="234c3-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="234c3-127">INPUTS</span></span>

### <span data-ttu-id="234c3-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="234c3-128">None</span></span>

## <span data-ttu-id="234c3-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="234c3-129">OUTPUTS</span></span>

### <span data-ttu-id="234c3-130">Microsoft. Azure. commands. Networks. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="234c3-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="234c3-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="234c3-131">NOTES</span></span>

## <span data-ttu-id="234c3-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="234c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="234c3-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="234c3-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)