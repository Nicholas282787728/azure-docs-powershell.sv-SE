---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesenginematchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngineMatchConditionObject.md
ms.openlocfilehash: 991d3233dd484025e699bba455b7d43e86f586e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100989"
---
# <span data-ttu-id="7ba16-101">New-AzFrontDoorRulesEngineMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7ba16-101">New-AzFrontDoorRulesEngineMatchConditionObject</span></span>

## <span data-ttu-id="7ba16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ba16-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba16-103">Skapa ett PSRulesEngineMatchCondition-objekt för att skapa en regel för regel motor.</span><span class="sxs-lookup"><span data-stu-id="7ba16-103">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="7ba16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ba16-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable <PSRulesEngineMatchVariable>
 -MatchValue <String[]> [-Selector <String>] [-Operator <PSRulesEngineOperator>] [-NegateCondition <Boolean>]
 [-Transform <PSTransform[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ba16-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ba16-105">DESCRIPTION</span></span>
<span data-ttu-id="7ba16-106">Skapa ett PSRulesEngineMatchCondition-objekt för att skapa en regel för regel motor.</span><span class="sxs-lookup"><span data-stu-id="7ba16-106">Create a PSRulesEngineMatchCondition object for creating a rules engine rule.</span></span>

## <span data-ttu-id="7ba16-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ba16-107">EXAMPLES</span></span>

### <span data-ttu-id="7ba16-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ba16-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngineMatchConditionObject -MatchVariable RequestHeader -Operator Equal -MatchValue allowoverride -Transform "LowerCase", "UpperCase"-Selector Rules-Engine-Route-Forward -NegateCondition $false

RulesEngineMatchVariable : RequestHeader
RulesEngineMatchValue    : {allowoverride}
Selector                 : Rules-Engine-Route-Forward
RulesEngineOperator      : Equal
NegateCondition          : False
Transform                : {Lowercase, Uppercase}
```

<span data-ttu-id="7ba16-109">Greate ett nytt PSRulesEngineMatchCondition-objekt.</span><span class="sxs-lookup"><span data-stu-id="7ba16-109">Greate a new PSRulesEngineMatchCondition object.</span></span>

## <span data-ttu-id="7ba16-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ba16-110">PARAMETERS</span></span>

### <span data-ttu-id="7ba16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba16-111">-DefaultProfile</span></span>
<span data-ttu-id="7ba16-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ba16-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba16-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="7ba16-113">-MatchValue</span></span>
<span data-ttu-id="7ba16-114">Matcha värden för att passa.</span><span class="sxs-lookup"><span data-stu-id="7ba16-114">Match values to match against.</span></span>
<span data-ttu-id="7ba16-115">Operatorn gäller för varje värde i här med eller semantik.</span><span class="sxs-lookup"><span data-stu-id="7ba16-115">The operator will apply to each value in here with OR semantics.</span></span>
<span data-ttu-id="7ba16-116">Om någon av dem matchar variabeln med den givna operatorn anses matchnings villkoret vara en träff.</span><span class="sxs-lookup"><span data-stu-id="7ba16-116">If any of them match the variable with the given operator this match condition is considered a match.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba16-117">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="7ba16-117">-MatchVariable</span></span>
<span data-ttu-id="7ba16-118">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="7ba16-118">Match Variable.</span></span>
<span data-ttu-id="7ba16-119">Möjliga värden är IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span><span class="sxs-lookup"><span data-stu-id="7ba16-119">Possible values are IsMobile, RemoteAddr, RequestMethod, QueryString, PostArg, RequestUri, RequestPath, RequestFileName, RequestfilenameExtension, RequestHeader, RequestBody, RequestScheme</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: IsMobile, RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestPath, RequestFilename, RequestFilenameExtension, RequestHeader, RequestBody, RequestScheme

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba16-120">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="7ba16-120">-NegateCondition</span></span>
<span data-ttu-id="7ba16-121">Beskriver om det här är negationer eller inte</span><span class="sxs-lookup"><span data-stu-id="7ba16-121">Describes if this is negate condition or not</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba16-122">-Operatör</span><span class="sxs-lookup"><span data-stu-id="7ba16-122">-Operator</span></span>
<span data-ttu-id="7ba16-123">Beskriver vilken operator som ska användas för matchnings villkoret.</span><span class="sxs-lookup"><span data-stu-id="7ba16-123">Describes operator to apply to the match condition.</span></span>
<span data-ttu-id="7ba16-124">Möjliga värden är alla, IPMatch, mindreän, lika med, innehåller,, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, börjarmed, Slutarmed.</span><span class="sxs-lookup"><span data-stu-id="7ba16-124">Possible values are Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineOperator
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba16-125">-Selector</span><span class="sxs-lookup"><span data-stu-id="7ba16-125">-Selector</span></span>
<span data-ttu-id="7ba16-126">Namn på väljaren i RequestHeader eller RequestBody som ska matchas</span><span class="sxs-lookup"><span data-stu-id="7ba16-126">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="7ba16-127">-Omvandla</span><span class="sxs-lookup"><span data-stu-id="7ba16-127">-Transform</span></span>
<span data-ttu-id="7ba16-128">Lista över vilka transformeringar som ska tillämpas innan du matchar.</span><span class="sxs-lookup"><span data-stu-id="7ba16-128">List of what transforms are applied before matching.</span></span> <span data-ttu-id="7ba16-129">Möjliga enskilda värden för transformering är gemener, versaler, trim, UrlDecode, UrlEncode, RemoveNulls.</span><span class="sxs-lookup"><span data-stu-id="7ba16-129">Possible individual transform values are Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSTransform[]
Parameter Sets: (All)
Aliases:
Accepted values: Lowercase, Uppercase, Trim, UrlDecode, UrlEncode, RemoveNulls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ba16-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba16-130">CommonParameters</span></span>
<span data-ttu-id="7ba16-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ba16-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba16-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ba16-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba16-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ba16-133">INPUTS</span></span>

### <span data-ttu-id="7ba16-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="7ba16-134">None</span></span>

## <span data-ttu-id="7ba16-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ba16-135">OUTPUTS</span></span>

### <span data-ttu-id="7ba16-136">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngineMatchCondition</span><span class="sxs-lookup"><span data-stu-id="7ba16-136">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineMatchCondition</span></span>

## <span data-ttu-id="7ba16-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ba16-137">NOTES</span></span>

## <span data-ttu-id="7ba16-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ba16-138">RELATED LINKS</span></span>