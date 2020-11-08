---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271588"
---
# <span data-ttu-id="d11dd-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="d11dd-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="d11dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d11dd-102">SYNOPSIS</span></span>
<span data-ttu-id="d11dd-103">Hämtar alla tillgängliga regel uppsättningar för webb programs brand väggar.</span><span class="sxs-lookup"><span data-stu-id="d11dd-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d11dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d11dd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d11dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d11dd-105">DESCRIPTION</span></span>
<span data-ttu-id="d11dd-106">Cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** hämtar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="d11dd-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d11dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d11dd-107">EXAMPLES</span></span>

### <span data-ttu-id="d11dd-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d11dd-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="d11dd-109">Det här kommandot returnerar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="d11dd-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="d11dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d11dd-110">PARAMETERS</span></span>

### <span data-ttu-id="d11dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11dd-111">-DefaultProfile</span></span>
<span data-ttu-id="d11dd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d11dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d11dd-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11dd-113">CommonParameters</span></span>
<span data-ttu-id="d11dd-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11dd-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11dd-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d11dd-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11dd-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d11dd-116">INPUTS</span></span>

### <span data-ttu-id="d11dd-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="d11dd-117">None</span></span>

## <span data-ttu-id="d11dd-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d11dd-118">OUTPUTS</span></span>

### <span data-ttu-id="d11dd-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="d11dd-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="d11dd-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d11dd-120">NOTES</span></span>
<span data-ttu-id="d11dd-121">**List-AzApplicationGatewayAvailableWafRuleSets** är ett alias för cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="d11dd-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="d11dd-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d11dd-122">RELATED LINKS</span></span>
