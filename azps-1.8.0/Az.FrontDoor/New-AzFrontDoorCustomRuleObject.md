---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorCustomRuleObject.md
ms.openlocfilehash: 19f8215f8feaa1765da871f0fa38cc0120d842ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916750"
---
# <span data-ttu-id="b2b75-101">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="b2b75-101">New-AzFrontDoorCustomRuleObject</span></span>

## <span data-ttu-id="b2b75-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2b75-102">SYNOPSIS</span></span>
<span data-ttu-id="b2b75-103">Skapa CustomRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="b2b75-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b2b75-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2b75-104">SYNTAX</span></span>

```
New-AzFrontDoorCustomRuleObject -Name <String> -RuleType <PSCustomRuleType>
 -MatchCondition <PSMatchCondition[]> -Action <PSAction> -Priority <Int32>
 [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2b75-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2b75-105">DESCRIPTION</span></span>
<span data-ttu-id="b2b75-106">Skapa CustomRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="b2b75-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b2b75-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2b75-107">EXAMPLES</span></span>

### <span data-ttu-id="b2b75-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b2b75-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="b2b75-109">Skapa ett CustomRule-objekt</span><span class="sxs-lookup"><span data-stu-id="b2b75-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="b2b75-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2b75-110">PARAMETERS</span></span>

### <span data-ttu-id="b2b75-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="b2b75-111">-Action</span></span>
<span data-ttu-id="b2b75-112">Typ av åtgärder.</span><span class="sxs-lookup"><span data-stu-id="b2b75-112">Type of Actions.</span></span>
<span data-ttu-id="b2b75-113">Möjliga värden inkluderar: "Tillåt", "blockera", "log"</span><span class="sxs-lookup"><span data-stu-id="b2b75-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAction
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Block, Log, Redirect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b75-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2b75-114">-DefaultProfile</span></span>
<span data-ttu-id="b2b75-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b2b75-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2b75-116">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="b2b75-116">-MatchCondition</span></span>
<span data-ttu-id="b2b75-117">Lista över matchnings villkor.</span><span class="sxs-lookup"><span data-stu-id="b2b75-117">List of match conditions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b75-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2b75-118">-Name</span></span>
<span data-ttu-id="b2b75-119">Namn på regeln</span><span class="sxs-lookup"><span data-stu-id="b2b75-119">Name of the rule</span></span>

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

### <span data-ttu-id="b2b75-120">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="b2b75-120">-Priority</span></span>
<span data-ttu-id="b2b75-121">Beskriver prioriteten för regeln.</span><span class="sxs-lookup"><span data-stu-id="b2b75-121">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="b2b75-122">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="b2b75-122">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="b2b75-123">Hastighets gräns.</span><span class="sxs-lookup"><span data-stu-id="b2b75-123">Rate limit duration.</span></span> <span data-ttu-id="b2b75-124">Standard-1 minut</span><span class="sxs-lookup"><span data-stu-id="b2b75-124">Default - 1 minute</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b75-125">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="b2b75-125">-RateLimitThreshold</span></span>
<span data-ttu-id="b2b75-126">Frekvens gräns thresold</span><span class="sxs-lookup"><span data-stu-id="b2b75-126">Rate limit thresold</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b75-127">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b2b75-127">-RuleType</span></span>
<span data-ttu-id="b2b75-128">Typ av regel.</span><span class="sxs-lookup"><span data-stu-id="b2b75-128">Type of the rule.</span></span>
<span data-ttu-id="b2b75-129">Möjliga värden är: ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="b2b75-129">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRuleType
Parameter Sets: (All)
Aliases:
Accepted values: RateLimitRule, MatchRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2b75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2b75-130">CommonParameters</span></span>
<span data-ttu-id="b2b75-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2b75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2b75-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2b75-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2b75-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2b75-133">INPUTS</span></span>

### <span data-ttu-id="b2b75-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2b75-134">None</span></span>

## <span data-ttu-id="b2b75-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2b75-135">OUTPUTS</span></span>

### <span data-ttu-id="b2b75-136">Microsoft. Azure. commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="b2b75-136">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="b2b75-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2b75-137">NOTES</span></span>

## <span data-ttu-id="b2b75-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2b75-138">RELATED LINKS</span></span>

<span data-ttu-id="b2b75-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="b2b75-139">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)</span></span>
