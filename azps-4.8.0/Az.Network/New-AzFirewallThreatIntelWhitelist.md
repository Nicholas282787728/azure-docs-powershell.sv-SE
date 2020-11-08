---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallthreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallThreatIntelWhitelist.md
ms.openlocfilehash: 8f55ccc6049ffccc9e2d4b5083597aca101b10bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259305"
---
# <span data-ttu-id="46587-101">New-AzFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="46587-101">New-AzFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="46587-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46587-102">SYNOPSIS</span></span>
<span data-ttu-id="46587-103">Skapa en ny Threat Intelligence-Lägg för Azure-brandväggen</span><span class="sxs-lookup"><span data-stu-id="46587-103">Create a new threat intelligence whitelist for Azure Firewall</span></span>

## <span data-ttu-id="46587-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46587-104">SYNTAX</span></span>

```
New-AzFirewallThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46587-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46587-105">DESCRIPTION</span></span>
<span data-ttu-id="46587-106">**New-AzFirewallThreatIntelWhitelist-** cmdleten skapar ett hot Intel Lägg-objekt som kan användas när du skapar eller ställer in en Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="46587-106">The **New-AzFirewallThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall.</span></span>

## <span data-ttu-id="46587-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46587-107">EXAMPLES</span></span>

### <span data-ttu-id="46587-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46587-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallThreatIntelWhitelist -IpAddress @("2.2.2.2", "3.3.3.3") -FQDN @("bing.com", "yammer.com")
```

<span data-ttu-id="46587-109">I det här exemplet skapas ett hot Intel Lägg som innehåller en FQDN-Lägg med två poster och en IP-adress Lägg med två poster</span><span class="sxs-lookup"><span data-stu-id="46587-109">This example creates a threat intel whitelist containing a FQDN whitelist of two entries and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="46587-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46587-110">PARAMETERS</span></span>

### <span data-ttu-id="46587-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46587-111">-DefaultProfile</span></span>
<span data-ttu-id="46587-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46587-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46587-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="46587-113">-FQDN</span></span>
<span data-ttu-id="46587-114">FQDN-namn för hotet Intel Lägg</span><span class="sxs-lookup"><span data-stu-id="46587-114">The FQDNs of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="46587-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="46587-115">-IpAddress</span></span>
<span data-ttu-id="46587-116">IP-adresserna för hotet Intel Lägg</span><span class="sxs-lookup"><span data-stu-id="46587-116">The IP Addresses of the Threat Intel Whitelist</span></span>

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

### <span data-ttu-id="46587-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46587-117">CommonParameters</span></span>
<span data-ttu-id="46587-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46587-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46587-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46587-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46587-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46587-120">INPUTS</span></span>

### <span data-ttu-id="46587-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="46587-121">None</span></span>

## <span data-ttu-id="46587-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46587-122">OUTPUTS</span></span>

### <span data-ttu-id="46587-123">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="46587-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallThreatIntelWhitelist</span></span>

## <span data-ttu-id="46587-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46587-124">NOTES</span></span>

## <span data-ttu-id="46587-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46587-125">RELATED LINKS</span></span>

[<span data-ttu-id="46587-126">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46587-126">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="46587-127">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46587-127">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="46587-128">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="46587-128">Set-AzFirewall</span></span>](./Set-AzFirewall.md)