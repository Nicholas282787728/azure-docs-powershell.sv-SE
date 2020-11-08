---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicythreatintelwhitelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyThreatIntelWhitelist.md
ms.openlocfilehash: b0c7924ec4e18fff159caa95f035ca2289eaf5b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261846"
---
# <span data-ttu-id="2de20-101">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2de20-101">New-AzFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="2de20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2de20-102">SYNOPSIS</span></span>
<span data-ttu-id="2de20-103">Skapa en ny Threat Intelligence-Lägg för Azure Firewall policy</span><span class="sxs-lookup"><span data-stu-id="2de20-103">Create a new threat intelligence whitelist for Azure Firewall Policy</span></span>

## <span data-ttu-id="2de20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2de20-104">SYNTAX</span></span>

```
New-AzFirewallPolicyThreatIntelWhitelist [-FQDN <String[]>] [-IpAddress <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2de20-105">DESCRIPTION</span></span>
<span data-ttu-id="2de20-106">**New-AzFirewallPolicyThreatIntelWhitelist-** cmdleten skapar ett hot Intel Lägg-objekt som du kan använda när du skapar eller ställer in en Azure Firewall-princip.</span><span class="sxs-lookup"><span data-stu-id="2de20-106">The **New-AzFirewallPolicyThreatIntelWhitelist** cmdlet creates a threat intel whitelist object, which can be used when creating or setting an Azure Firewall Policy.</span></span>

## <span data-ttu-id="2de20-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2de20-107">EXAMPLES</span></span>

### <span data-ttu-id="2de20-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2de20-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
```

<span data-ttu-id="2de20-109">I det här exemplet skapas ett hot Intel Lägg som innehåller en FQDN-Lägg med en post och en IP-adress Lägg med två poster</span><span class="sxs-lookup"><span data-stu-id="2de20-109">This example creates a threat intel whitelist containing a FQDN whitelist of one entry and an Ip address whitelist of two entries</span></span>

## <span data-ttu-id="2de20-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2de20-110">PARAMETERS</span></span>

### <span data-ttu-id="2de20-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de20-111">-DefaultProfile</span></span>
<span data-ttu-id="2de20-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2de20-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de20-113">-FQDN</span><span class="sxs-lookup"><span data-stu-id="2de20-113">-FQDN</span></span>
<span data-ttu-id="2de20-114">FQDN-namn för hotet Intel Lägg</span><span class="sxs-lookup"><span data-stu-id="2de20-114">The FQDNs of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de20-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2de20-115">-IpAddress</span></span>
<span data-ttu-id="2de20-116">IP-adresserna för hotet Intel Lägg</span><span class="sxs-lookup"><span data-stu-id="2de20-116">The IP Addresses of the Threat Intel Whitelist</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de20-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de20-117">CommonParameters</span></span>
<span data-ttu-id="2de20-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de20-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de20-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2de20-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de20-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2de20-120">INPUTS</span></span>

### <span data-ttu-id="2de20-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="2de20-121">None</span></span>

## <span data-ttu-id="2de20-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2de20-122">OUTPUTS</span></span>

### <span data-ttu-id="2de20-123">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="2de20-123">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyThreatIntelWhitelist</span></span>

## <span data-ttu-id="2de20-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2de20-124">NOTES</span></span>

## <span data-ttu-id="2de20-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2de20-125">RELATED LINKS</span></span>
