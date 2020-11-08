---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091308"
---
# <span data-ttu-id="694cd-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="694cd-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="694cd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="694cd-102">SYNOPSIS</span></span>
<span data-ttu-id="694cd-103">Hämtar alla tillgängliga regel uppsättningar för webb programs brand väggar.</span><span class="sxs-lookup"><span data-stu-id="694cd-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="694cd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="694cd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="694cd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="694cd-105">DESCRIPTION</span></span>
<span data-ttu-id="694cd-106">Cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** hämtar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="694cd-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="694cd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="694cd-107">EXAMPLES</span></span>

### <span data-ttu-id="694cd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="694cd-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="694cd-109">Det här kommandot returnerar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="694cd-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="694cd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="694cd-110">PARAMETERS</span></span>

### <span data-ttu-id="694cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694cd-111">-DefaultProfile</span></span>
<span data-ttu-id="694cd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="694cd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694cd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694cd-113">CommonParameters</span></span>
<span data-ttu-id="694cd-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="694cd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694cd-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="694cd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694cd-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="694cd-116">INPUTS</span></span>

### <span data-ttu-id="694cd-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="694cd-117">None</span></span>

## <span data-ttu-id="694cd-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="694cd-118">OUTPUTS</span></span>

### <span data-ttu-id="694cd-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="694cd-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="694cd-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="694cd-120">NOTES</span></span>
<span data-ttu-id="694cd-121">**List-AzApplicationGatewayAvailableWafRuleSets** är ett alias för cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="694cd-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="694cd-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="694cd-122">RELATED LINKS</span></span>