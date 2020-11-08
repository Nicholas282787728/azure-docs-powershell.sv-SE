---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: df04d3f3dd19c62c37ffbb82cbd57e50c3d73c15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092634"
---
# <span data-ttu-id="d311d-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="d311d-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="d311d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d311d-102">SYNOPSIS</span></span>
<span data-ttu-id="d311d-103">Skapar en leverans regel.</span><span class="sxs-lookup"><span data-stu-id="d311d-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="d311d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d311d-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d311d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d311d-105">DESCRIPTION</span></span>
<span data-ttu-id="d311d-106">Cmdleten **New-AzCdnDeliveryRule** skapar en leverans regel för generering av CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="d311d-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="d311d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d311d-107">EXAMPLES</span></span>

### <span data-ttu-id="d311d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d311d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="d311d-109">Skapa en enkel regel.</span><span class="sxs-lookup"><span data-stu-id="d311d-109">Create a simple rule.</span></span>

## <span data-ttu-id="d311d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d311d-110">PARAMETERS</span></span>

### <span data-ttu-id="d311d-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="d311d-111">-Action</span></span>
<span data-ttu-id="d311d-112">En lista med åtgärder som utförs när alla villkor för en regel uppfylls.</span><span class="sxs-lookup"><span data-stu-id="d311d-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d311d-113">-Villkor</span><span class="sxs-lookup"><span data-stu-id="d311d-113">-Condition</span></span>
<span data-ttu-id="d311d-114">En lista med villkor som måste matchas för att åtgärderna ska utföras.</span><span class="sxs-lookup"><span data-stu-id="d311d-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d311d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d311d-115">-DefaultProfile</span></span>
<span data-ttu-id="d311d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d311d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d311d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d311d-117">-Name</span></span>
<span data-ttu-id="d311d-118">Namn på regeln</span><span class="sxs-lookup"><span data-stu-id="d311d-118">Name of the rule</span></span>

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

### <span data-ttu-id="d311d-119">-Beställ</span><span class="sxs-lookup"><span data-stu-id="d311d-119">-Order</span></span>
<span data-ttu-id="d311d-120">Ordning för regeln</span><span class="sxs-lookup"><span data-stu-id="d311d-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d311d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d311d-121">CommonParameters</span></span>
<span data-ttu-id="d311d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d311d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d311d-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d311d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d311d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d311d-124">INPUTS</span></span>

### <span data-ttu-id="d311d-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="d311d-125">None</span></span>

## <span data-ttu-id="d311d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d311d-126">OUTPUTS</span></span>

### <span data-ttu-id="d311d-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="d311d-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="d311d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d311d-128">NOTES</span></span>

## <span data-ttu-id="d311d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d311d-129">RELATED LINKS</span></span>
