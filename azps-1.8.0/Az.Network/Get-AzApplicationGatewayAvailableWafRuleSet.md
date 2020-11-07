---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: e550d00d1d952fb372db81ec87a35c701d6dedde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748392"
---
# <span data-ttu-id="ebf4c-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="ebf4c-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="ebf4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ebf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf4c-103">Hämtar alla tillgängliga regel uppsättningar för webb programs brand väggar.</span><span class="sxs-lookup"><span data-stu-id="ebf4c-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ebf4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ebf4c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebf4c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ebf4c-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf4c-106">Cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** hämtar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="ebf4c-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ebf4c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ebf4c-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf4c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ebf4c-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="ebf4c-109">Det här kommandot returnerar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="ebf4c-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="ebf4c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ebf4c-110">PARAMETERS</span></span>

### <span data-ttu-id="ebf4c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf4c-111">-DefaultProfile</span></span>
<span data-ttu-id="ebf4c-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf4c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebf4c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf4c-113">CommonParameters</span></span>
<span data-ttu-id="ebf4c-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf4c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf4c-115">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebf4c-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf4c-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ebf4c-116">INPUTS</span></span>

### <span data-ttu-id="ebf4c-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="ebf4c-117">None</span></span>

## <span data-ttu-id="ebf4c-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ebf4c-118">OUTPUTS</span></span>

### <span data-ttu-id="ebf4c-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="ebf4c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="ebf4c-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ebf4c-120">NOTES</span></span>
<span data-ttu-id="ebf4c-121">**List-AzApplicationGatewayAvailableWafRuleSets** är ett alias för cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="ebf4c-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="ebf4c-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ebf4c-122">RELATED LINKS</span></span>
