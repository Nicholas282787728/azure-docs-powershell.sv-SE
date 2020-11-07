---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757848"
---
# <span data-ttu-id="d6c58-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="d6c58-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="d6c58-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6c58-102">SYNOPSIS</span></span>
<span data-ttu-id="d6c58-103">Hämtar de tillgängliga FQDN-taggarna för Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="d6c58-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6c58-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6c58-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6c58-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6c58-105">DESCRIPTION</span></span>
<span data-ttu-id="d6c58-106">Cmdleten **Get-AzureRmFirewallFqdnTag** hämtar listan över FQDN-taggar som kan användas för Azure Firewall Application-regler</span><span class="sxs-lookup"><span data-stu-id="d6c58-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="d6c58-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6c58-107">EXAMPLES</span></span>

### <span data-ttu-id="d6c58-108">1: Hämta alla tillgängliga FQDN-Taggar</span><span class="sxs-lookup"><span data-stu-id="d6c58-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="d6c58-109">I det här exemplet hämtas alla tillgängliga FQDN-taggar.</span><span class="sxs-lookup"><span data-stu-id="d6c58-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="d6c58-110">2: Använd den första tillgängliga FQDN-taggen i en program regel</span><span class="sxs-lookup"><span data-stu-id="d6c58-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="d6c58-111">I det här exemplet skapas en regel för brand Väggs program med den första tillgängliga FQDN-taggen</span><span class="sxs-lookup"><span data-stu-id="d6c58-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="d6c58-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6c58-112">PARAMETERS</span></span>

### <span data-ttu-id="d6c58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6c58-113">-DefaultProfile</span></span>
<span data-ttu-id="d6c58-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6c58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6c58-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6c58-115">CommonParameters</span></span>
<span data-ttu-id="d6c58-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6c58-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6c58-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6c58-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6c58-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6c58-118">INPUTS</span></span>

### <span data-ttu-id="d6c58-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="d6c58-119">None</span></span>
<span data-ttu-id="d6c58-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="d6c58-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6c58-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6c58-121">OUTPUTS</span></span>

### <span data-ttu-id="d6c58-122">Microsoft. Azure. commands. Networks. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="d6c58-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="d6c58-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6c58-123">NOTES</span></span>

## <span data-ttu-id="d6c58-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6c58-124">RELATED LINKS</span></span>

[<span data-ttu-id="d6c58-125">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="d6c58-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="d6c58-126">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="d6c58-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
