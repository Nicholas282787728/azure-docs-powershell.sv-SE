---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748290"
---
# <span data-ttu-id="d76a0-101">Get-AzFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="d76a0-101">Get-AzFirewallFqdnTag</span></span>

## <span data-ttu-id="d76a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d76a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d76a0-103">Hämtar de tillgängliga FQDN-taggarna för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="d76a0-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

## <span data-ttu-id="d76a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d76a0-104">SYNTAX</span></span>

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d76a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d76a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d76a0-106">Cmdleten **Get-AzFirewallFqdnTag** hämtar listan över FQDN-taggar som kan användas för Azure Firewall Application-regler</span><span class="sxs-lookup"><span data-stu-id="d76a0-106">The **Get-AzFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="d76a0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d76a0-107">EXAMPLES</span></span>

### <span data-ttu-id="d76a0-108">1: Hämta alla tillgängliga FQDN-Taggar</span><span class="sxs-lookup"><span data-stu-id="d76a0-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzFirewallFqdnTag
```

<span data-ttu-id="d76a0-109">I det här exemplet hämtas alla tillgängliga FQDN-taggar.</span><span class="sxs-lookup"><span data-stu-id="d76a0-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="d76a0-110">2: Använd den första tillgängliga FQDN-taggen i en program regel</span><span class="sxs-lookup"><span data-stu-id="d76a0-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="d76a0-111">I det här exemplet skapas en regel för brand Väggs program med den första tillgängliga FQDN-taggen</span><span class="sxs-lookup"><span data-stu-id="d76a0-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="d76a0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d76a0-112">PARAMETERS</span></span>

### <span data-ttu-id="d76a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76a0-113">-DefaultProfile</span></span>
<span data-ttu-id="d76a0-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d76a0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d76a0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76a0-115">CommonParameters</span></span>
<span data-ttu-id="d76a0-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76a0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76a0-117">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d76a0-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76a0-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d76a0-118">INPUTS</span></span>

### <span data-ttu-id="d76a0-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="d76a0-119">None</span></span>

## <span data-ttu-id="d76a0-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d76a0-120">OUTPUTS</span></span>

### <span data-ttu-id="d76a0-121">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="d76a0-121">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

### <span data-ttu-id="d76a0-122">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. commands. Network. Models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. cmdletar. Network, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d76a0-122">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d76a0-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d76a0-123">NOTES</span></span>

## <span data-ttu-id="d76a0-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d76a0-124">RELATED LINKS</span></span>

[<span data-ttu-id="d76a0-125">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d76a0-125">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="d76a0-126">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="d76a0-126">New-AzFirewall</span></span>](./New-AzFirewall.md)
