---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091079"
---
# <span data-ttu-id="37b5a-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="37b5a-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="37b5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="37b5a-103">Hämtar de tillgängliga FQDN-taggarna för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="37b5a-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="37b5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37b5a-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37b5a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="37b5a-106">Cmdleten **Get-AzFirewallFqdnTag** hämtar listan över FQDN-taggar som kan användas för Azure Firewall Application-regler</span><span class="sxs-lookup"><span data-stu-id="37b5a-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="37b5a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="37b5a-108">1: Hämta alla tillgängliga FQDN-Taggar</span><span class="sxs-lookup"><span data-stu-id="37b5a-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="37b5a-109">I det här exemplet hämtas alla tillgängliga FQDN-taggar.</span><span class="sxs-lookup"><span data-stu-id="37b5a-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="37b5a-110">2: Använd den första tillgängliga FQDN-taggen i en program regel</span><span class="sxs-lookup"><span data-stu-id="37b5a-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="37b5a-111">I det här exemplet skapas en regel för brand Väggs program med den första tillgängliga FQDN-taggen</span><span class="sxs-lookup"><span data-stu-id="37b5a-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="37b5a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="37b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="37b5a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37b5a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b5a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b5a-115">CommonParameters</span></span>
<span data-ttu-id="37b5a-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b5a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b5a-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37b5a-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b5a-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37b5a-118">INPUTS</span></span>

### <span data-ttu-id="37b5a-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="37b5a-119">None</span></span>

## <span data-ttu-id="37b5a-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37b5a-120">OUTPUTS</span></span>

### <span data-ttu-id="37b5a-121">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="37b5a-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="37b5a-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. cmdletar. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="37b5a-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="37b5a-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37b5a-123">NOTES</span></span>

## <span data-ttu-id="37b5a-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37b5a-124">RELATED LINKS</span></span>

[<span data-ttu-id="37b5a-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="37b5a-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="37b5a-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="37b5a-126">New-AzFirewall</span></span>](./New-AzFirewall.md)