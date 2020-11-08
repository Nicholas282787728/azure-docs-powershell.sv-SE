---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengineruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineRuleObject.md
ms.openlocfilehash: c02fa092532f70567405f314dc8943e4e2ce51f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270640"
---
# <span data-ttu-id="ec658-101">New-AzFrontDoorRulesEngineRuleObject</span><span class="sxs-lookup"><span data-stu-id="ec658-101">New-AzFrontDoorRulesEngineRuleObject</span></span>

## <span data-ttu-id="ec658-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ec658-102">SYNOPSIS</span></span>
<span data-ttu-id="ec658-103">Skapa ett PSRulesEngineRule-objekt för att skapa regel motorn.</span><span class="sxs-lookup"><span data-stu-id="ec658-103">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

## <span data-ttu-id="ec658-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ec658-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineRuleObject -Name <String> -Priority <Int32> -Action <PSRulesEngineAction>
 [-MatchProcessingBehavior <PSMatchProcessingBehavior>] [-MatchCondition <PSRulesEngineMatchCondition[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec658-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ec658-105">DESCRIPTION</span></span>
<span data-ttu-id="ec658-106">Skapa ett PSRulesEngineRule-objekt för att skapa regel motorn.</span><span class="sxs-lookup"><span data-stu-id="ec658-106">Create a PSRulesEngineRule object for Rules Engine creation.</span></span>

<span data-ttu-id="ec658-107">Använd cmdlet "New-AzFrontDoorRulesEngineActionObject" för att skapa PSRulesEngineAction-objekt som ska överföras till parametern "-Action".</span><span class="sxs-lookup"><span data-stu-id="ec658-107">Use cmdlet "New-AzFrontDoorRulesEngineActionObject" to create PSRulesEngineAction object to pass into the "-Action" parameter.</span></span>
<span data-ttu-id="ec658-108">Använd cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" för att skapa PSRulesEngineMatchCondition-objekt som ska överföras till parametern "-MatchCondition".</span><span class="sxs-lookup"><span data-stu-id="ec658-108">Use cmdlet "New-AzFrontDoorRulesEngineMatchConditionObject" to create PSRulesEngineMatchCondition object to pass into the "-MatchCondition" parameter.</span></span>

## <span data-ttu-id="ec658-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ec658-109">EXAMPLES</span></span>

### <span data-ttu-id="ec658-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ec658-110">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority 0 -Action $rulesEngineAction -MatchProcessingBehavior Stop -MatchCondition $rulesEngineMatchCondition

Name                    : rules1
Priority                : 0
MatchProcessingBehavior : Stop
MatchCondition          : {Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition}
Action                  : Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction


PS C:\> $rulesEngineRule1.Action

RequestHeaderActions           ResponseHeaderActions RouteConfigurationOverride
--------------------           --------------------- --------------------------
{headeraction1, headeraction2} {}                    Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfigurati�

PS C:\> $rulesEngineRule1.MatchCondition[0]

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transforms               : {Lowercase, Uppercase}
```

<span data-ttu-id="ec658-111">Skapa nytt PSRulesEngineRule-objekt och visa hur du kan se under fält.</span><span class="sxs-lookup"><span data-stu-id="ec658-111">Create new PSRulesEngineRule object and demonstrate how to see the subfields.</span></span>

### <span data-ttu-id="ec658-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="ec658-112">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
New-AzFrontDoorRulesEngineRuleObject : Cannot validate argument on parameter 'Priority'. The -1 argument is less than the minimum allowed range of 0. Supply an argument that is greater than or equal to 0 and then try the command again.
At line:1 char:81
+ ... ule1 = New-AzFrontDoorRulesEngineRuleObject -Name rules1 -Priority -1
+                                                                        ~~
+ CategoryInfo          : InvalidData: (:) [New-AzFrontDoorRulesEngineRuleObject], ParameterBindingValidationException
+ FullyQualifiedErrorId : ParameterArgumentValidationError,Microsoft.Azure.Commands.FrontDoor.Cmdlets.NewFrontDoorRulesEngineRuleObject
```

<span data-ttu-id="ec658-113">Utdata förväntas när ett ogiltigt prioritets värde överförs.</span><span class="sxs-lookup"><span data-stu-id="ec658-113">Expect output when passing in invalid priority value.</span></span>

## <span data-ttu-id="ec658-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ec658-114">PARAMETERS</span></span>

### <span data-ttu-id="ec658-115">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="ec658-115">-Action</span></span>
<span data-ttu-id="ec658-116">Åtgärder att utföra i begäran och svar om alla matchnings villkor uppfylls.</span><span class="sxs-lookup"><span data-stu-id="ec658-116">Actions to perform on the request and response if all of the match conditions are met.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineAction
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec658-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec658-117">-DefaultProfile</span></span>
<span data-ttu-id="ec658-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ec658-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec658-119">-MatchCondition</span><span class="sxs-lookup"><span data-stu-id="ec658-119">-MatchCondition</span></span>
<span data-ttu-id="ec658-120">En lista över matchnings villkor som måste uppfyllas för att åtgärderna i regeln ska fungera.</span><span class="sxs-lookup"><span data-stu-id="ec658-120">A list of match conditions that must meet in order for the actions of this rule to run.</span></span> <span data-ttu-id="ec658-121">Åtgärderna kommer alltid att köras.</span><span class="sxs-lookup"><span data-stu-id="ec658-121">Having no match conditions means the actions will always run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec658-122">-MatchProcessingBehavior</span><span class="sxs-lookup"><span data-stu-id="ec658-122">-MatchProcessingBehavior</span></span>
<span data-ttu-id="ec658-123">Om den här regeln är en matchning bör regel motorn fortsätta köra de återstående reglerna eller stoppa.</span><span class="sxs-lookup"><span data-stu-id="ec658-123">If this rule is a match should the rules engine continue running the remaining rules or stop.</span></span>
<span data-ttu-id="ec658-124">Möjliga värden är Fortsätt och stoppa.</span><span class="sxs-lookup"><span data-stu-id="ec658-124">Possible values are Continue and Stop.</span></span>
<span data-ttu-id="ec658-125">Om det inte finns någon kan du fortsätta.</span><span class="sxs-lookup"><span data-stu-id="ec658-125">If not present, defaults to Continue.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchProcessingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: Continue, Stop

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec658-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="ec658-126">-Name</span></span>
<span data-ttu-id="ec658-127">Ett namn som refererar till den här specifika regeln.</span><span class="sxs-lookup"><span data-stu-id="ec658-127">A name to refer to this specific rule.</span></span>

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

### <span data-ttu-id="ec658-128">-Prioritet</span><span class="sxs-lookup"><span data-stu-id="ec658-128">-Priority</span></span>
<span data-ttu-id="ec658-129">En prioritet som tilldelats den här regeln.</span><span class="sxs-lookup"><span data-stu-id="ec658-129">A priority assigned to this rule.</span></span>
<span data-ttu-id="ec658-130">Får inte vara negativt.</span><span class="sxs-lookup"><span data-stu-id="ec658-130">Cannot be negative.</span></span>

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

### <span data-ttu-id="ec658-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec658-131">CommonParameters</span></span>
<span data-ttu-id="ec658-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec658-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec658-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec658-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec658-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ec658-134">INPUTS</span></span>

### <span data-ttu-id="ec658-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="ec658-135">None</span></span>

## <span data-ttu-id="ec658-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ec658-136">OUTPUTS</span></span>

### <span data-ttu-id="ec658-137">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngineRule</span><span class="sxs-lookup"><span data-stu-id="ec658-137">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule</span></span>

## <span data-ttu-id="ec658-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ec658-138">NOTES</span></span>

## <span data-ttu-id="ec658-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ec658-139">RELATED LINKS</span></span>
