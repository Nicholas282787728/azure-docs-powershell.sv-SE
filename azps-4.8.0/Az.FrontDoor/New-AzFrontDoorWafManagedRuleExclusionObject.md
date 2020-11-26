---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleexclusionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleExclusionObject.md
ms.openlocfilehash: 1f59a7366106c59f6dc5e5af3a32368594a00537
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262248"
---
# <span data-ttu-id="6137e-101">New-AzFrontDoorWafManagedRuleExclusionObject</span><span class="sxs-lookup"><span data-stu-id="6137e-101">New-AzFrontDoorWafManagedRuleExclusionObject</span></span>

## <span data-ttu-id="6137e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6137e-102">SYNOPSIS</span></span>
<span data-ttu-id="6137e-103">Skapa objekt med hanterad regel för WAF hanterade regel uppsättningar, grupper eller regler.</span><span class="sxs-lookup"><span data-stu-id="6137e-103">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="6137e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6137e-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleExclusionObject -Variable <String> -Operator <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6137e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6137e-105">DESCRIPTION</span></span>
<span data-ttu-id="6137e-106">Skapa objekt med hanterad regel för WAF hanterade regel uppsättningar, grupper eller regler.</span><span class="sxs-lookup"><span data-stu-id="6137e-106">Create managed rule exclusion object for WAF managed rule sets, groups, or rules.</span></span>

## <span data-ttu-id="6137e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6137e-107">EXAMPLES</span></span>

### <span data-ttu-id="6137e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6137e-108">Example 1</span></span>
```powershell
PS C:> New-AzFrontDoorWafManagedRuleExclusionObject -Variable QueryStringArgNames -Operator Equals -Selector "ParameterName"

MatchVariable       SelectorMatchOperator Selector
-------------       --------------------- --------
QueryStringArgNames Equals                ParameterName
```

## <span data-ttu-id="6137e-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6137e-109">PARAMETERS</span></span>

### <span data-ttu-id="6137e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6137e-110">-DefaultProfile</span></span>
<span data-ttu-id="6137e-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6137e-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6137e-112">-Operatör</span><span class="sxs-lookup"><span data-stu-id="6137e-112">-Operator</span></span>
<span data-ttu-id="6137e-113">Operator som ska användas vid markering av väljaren EqualsAny betyder ingen Selector (alla matchande variabler för den angivna typen)</span><span class="sxs-lookup"><span data-stu-id="6137e-113">Operator to use when matching the selector, EqualsAny means no selector (all match variables of the specified type)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6137e-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="6137e-114">-Selector</span></span>
<span data-ttu-id="6137e-115">Selector-mönster att matcha med operatorn (om operatorn inte är EqualsAny)</span><span class="sxs-lookup"><span data-stu-id="6137e-115">Selector pattern to match using the operator (if the operator is not EqualsAny)</span></span>

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

### <span data-ttu-id="6137e-116">-Variabel</span><span class="sxs-lookup"><span data-stu-id="6137e-116">-Variable</span></span>
<span data-ttu-id="6137e-117">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="6137e-117">Match variable.</span></span> <span data-ttu-id="6137e-118">Möjliga värden är RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span><span class="sxs-lookup"><span data-stu-id="6137e-118">Possible values are RequestHeaderNames, RequestCookieNames, QueryStringArgNames, RequestBodyPostArgNames.</span></span>
<span data-ttu-id="6137e-119">QueryStringArgNames är till exempel ett undantag av GET-parametrar som matchar väljaren med en given operator.</span><span class="sxs-lookup"><span data-stu-id="6137e-119">For example, QueryStringArgNames is an exclusion of GET parameters matching the selector with the given operator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6137e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6137e-120">CommonParameters</span></span>
<span data-ttu-id="6137e-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6137e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6137e-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6137e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6137e-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6137e-123">INPUTS</span></span>

### <span data-ttu-id="6137e-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="6137e-124">None</span></span>

## <span data-ttu-id="6137e-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6137e-125">OUTPUTS</span></span>

### <span data-ttu-id="6137e-126">Microsoft. Azure. commands. FrontDoor. Models. PSManagedRuleExclusion</span><span class="sxs-lookup"><span data-stu-id="6137e-126">Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion</span></span>

## <span data-ttu-id="6137e-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6137e-127">NOTES</span></span>

## <span data-ttu-id="6137e-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6137e-128">RELATED LINKS</span></span>

<span data-ttu-id="6137e-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md) 
 [New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="6137e-129">[New-AzFrontDoorWafManagedRuleOverrideObject](./New-AzFrontDoorWafManagedRuleOverrideObject.md)
[New-AzFrontDoorWafRuleGroupOverrideObject](./New-AzFrontDoorWafRuleGroupOverrideObject.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>