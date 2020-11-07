---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableWafRuleSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: f8f8411a40ddbc4d0e2f0e4b508385717e0c4173
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922338"
---
# <span data-ttu-id="f83ff-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="f83ff-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="f83ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f83ff-102">SYNOPSIS</span></span>
<span data-ttu-id="f83ff-103">Hämtar alla tillgängliga regel uppsättningar för webb programs brand väggar.</span><span class="sxs-lookup"><span data-stu-id="f83ff-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="f83ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f83ff-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f83ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f83ff-105">DESCRIPTION</span></span>
<span data-ttu-id="f83ff-106">Cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** hämtar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="f83ff-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="f83ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f83ff-107">EXAMPLES</span></span>

### <span data-ttu-id="f83ff-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f83ff-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="f83ff-109">Det här kommandot returnerar alla tillgängliga regel uppsättningar för webb program brand väggar.</span><span class="sxs-lookup"><span data-stu-id="f83ff-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="f83ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f83ff-110">PARAMETERS</span></span>

### <span data-ttu-id="f83ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83ff-111">-DefaultProfile</span></span>
<span data-ttu-id="f83ff-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f83ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f83ff-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83ff-113">CommonParameters</span></span>
<span data-ttu-id="f83ff-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f83ff-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83ff-115">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83ff-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83ff-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f83ff-116">INPUTS</span></span>

### <span data-ttu-id="f83ff-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="f83ff-117">None</span></span>

## <span data-ttu-id="f83ff-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f83ff-118">OUTPUTS</span></span>

### <span data-ttu-id="f83ff-119">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="f83ff-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="f83ff-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f83ff-120">NOTES</span></span>
<span data-ttu-id="f83ff-121">**List-AzApplicationGatewayAvailableWafRuleSet** är ett alias för cmdleten **Get-AzApplicationGatewayAvailableWafRuleSet** .</span><span class="sxs-lookup"><span data-stu-id="f83ff-121">**List-AzApplicationGatewayAvailableWafRuleSet** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="f83ff-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f83ff-122">RELATED LINKS</span></span>

