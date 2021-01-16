---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafcustomruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafCustomRuleObject.md
ms.openlocfilehash: 4612f1ef1dac22d87b6794e35f9541a39f6312ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406288"
---
# <span data-ttu-id="e9bd2-101">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="e9bd2-101">New-AzFrontDoorWafCustomRuleObject</span></span>

## <span data-ttu-id="e9bd2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bd2-103">Skapa CustomRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="e9bd2-103">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e9bd2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9bd2-104">SYNTAX</span></span>

```
New-AzFrontDoorWafCustomRuleObject -Name <String> -RuleType <String> -MatchCondition <PSMatchCondition[]>
 -Action <String> -Priority <Int32> [-RateLimitDurationInMinutes <Int32>] [-RateLimitThreshold <Int32>]
 [-EnabledState <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9bd2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="e9bd2-106">Skapa CustomRule-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="e9bd2-106">Create CustomRule Object for WAF policy creation</span></span>

## <span data-ttu-id="e9bd2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9bd2-107">EXAMPLES</span></span>

### <span data-ttu-id="e9bd2-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e9bd2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafCustomRuleObject -Name "Rule1" -RuleType MatchRule -MatchCondition $matchCondition1 -Action Block -Priority 2

Name   RuleType Action Priority RateLimitDurationInMinutes
----   -------- ------ -------- --------------------------
Rule1 MatchRule  Block        2                          1
```

<span data-ttu-id="e9bd2-109">Skapa ett CustomRule-objekt</span><span class="sxs-lookup"><span data-stu-id="e9bd2-109">Create a CustomRule Object</span></span>

## <span data-ttu-id="e9bd2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9bd2-110">PARAMETERS</span></span>

### <span data-ttu-id="e9bd2-111">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="e9bd2-111">-Action</span></span>
<span data-ttu-id="e9bd2-112">Typ av åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-112">Type of Actions.</span></span>
<span data-ttu-id="e9bd2-113">Möjliga värden inkluderar: "Tillåt", "blockera", "log"</span><span class="sxs-lookup"><span data-stu-id="e9bd2-113">Possible values include: 'Allow', 'Block', 'Log'</span></span>

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

### <span data-ttu-id="e9bd2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bd2-114">-DefaultProfile</span></span>
<span data-ttu-id="e9bd2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bd2-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e9bd2-116">-EnabledState</span></span>
<span data-ttu-id="e9bd2-117">Aktiverat läge.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-117">Enabled State.</span></span> <span data-ttu-id="e9bd2-118">Möjliga värden inkluderar: "Enabled", "Disabled".</span><span class="sxs-lookup"><span data-stu-id="e9bd2-118">Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="e9bd2-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="e9bd2-119">-MatchCondition</span></span>
<span data-ttu-id="e9bd2-120">Lista över matchnings villkor.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-120">List of match conditions.</span></span>

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

### <span data-ttu-id="e9bd2-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9bd2-121">-Name</span></span>
<span data-ttu-id="e9bd2-122">Namn på regeln</span><span class="sxs-lookup"><span data-stu-id="e9bd2-122">Name of the rule</span></span>

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

### <span data-ttu-id="e9bd2-123">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="e9bd2-123">-Priority</span></span>
<span data-ttu-id="e9bd2-124">Beskriver prioriteten för regeln.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-124">Describes priority of the rule.</span></span>

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

### <span data-ttu-id="e9bd2-125">-RateLimitDurationInMinutes</span><span class="sxs-lookup"><span data-stu-id="e9bd2-125">-RateLimitDurationInMinutes</span></span>
<span data-ttu-id="e9bd2-126">Hastighets gräns.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-126">Rate limit duration.</span></span> <span data-ttu-id="e9bd2-127">Standard-1 minut</span><span class="sxs-lookup"><span data-stu-id="e9bd2-127">Default - 1 minute</span></span>

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

### <span data-ttu-id="e9bd2-128">-RateLimitThreshold</span><span class="sxs-lookup"><span data-stu-id="e9bd2-128">-RateLimitThreshold</span></span>
<span data-ttu-id="e9bd2-129">Tröskelvärde för kvot gräns</span><span class="sxs-lookup"><span data-stu-id="e9bd2-129">Rate limit threshold</span></span>

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

### <span data-ttu-id="e9bd2-130">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e9bd2-130">-RuleType</span></span>
<span data-ttu-id="e9bd2-131">Typ av regel.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-131">Type of the rule.</span></span>
<span data-ttu-id="e9bd2-132">Möjliga värden är: ' MatchRule ', ' RateLimitRule '</span><span class="sxs-lookup"><span data-stu-id="e9bd2-132">Possible values include: 'MatchRule', 'RateLimitRule'</span></span>

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

### <span data-ttu-id="e9bd2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bd2-133">CommonParameters</span></span>
<span data-ttu-id="e9bd2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bd2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bd2-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9bd2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bd2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9bd2-136">INPUTS</span></span>

### <span data-ttu-id="e9bd2-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="e9bd2-137">None</span></span>

## <span data-ttu-id="e9bd2-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9bd2-138">OUTPUTS</span></span>

### <span data-ttu-id="e9bd2-139">Microsoft. Azure. commands. FrontDoor. Models. PSCustomRule</span><span class="sxs-lookup"><span data-stu-id="e9bd2-139">Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule</span></span>

## <span data-ttu-id="e9bd2-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9bd2-140">NOTES</span></span>

## <span data-ttu-id="e9bd2-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9bd2-141">RELATED LINKS</span></span>

<span data-ttu-id="e9bd2-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="e9bd2-142">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)</span></span>
