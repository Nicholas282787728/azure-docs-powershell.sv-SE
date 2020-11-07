---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafMatchConditionObject.md
ms.openlocfilehash: f192eb4bf88201f30f8648cba6468fb406401f43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744134"
---
# <span data-ttu-id="13963-101">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="13963-101">New-AzFrontDoorWafMatchConditionObject</span></span>

## <span data-ttu-id="13963-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13963-102">SYNOPSIS</span></span>
<span data-ttu-id="13963-103">Skapa MatchCondition-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="13963-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="13963-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13963-104">SYNTAX</span></span>

```
New-AzFrontDoorWafMatchConditionObject -MatchVariable <String> -OperatorProperty <String>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>] [-Transform <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13963-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13963-105">DESCRIPTION</span></span>
<span data-ttu-id="13963-106">Skapa MatchCondition-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="13963-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="13963-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13963-107">EXAMPLES</span></span>

### <span data-ttu-id="13963-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13963-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {Windows}  User-Agent           False
```

### <span data-ttu-id="13963-109">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13963-109">Example 2</span></span>
```powershell
PS C:\> New-AzFrontDoorWafMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "WINDOWS" -Transform Uppercase


MatchVariable OperatorProperty MatchValue Selector   NegateCondition Transform
------------- ---------------- ---------- --------   --------------- ---------
RequestHeader Contains         {WINDOWS}  User-Agent           False {Uppercase}
```

<span data-ttu-id="13963-110">Skapa ett MatchCondition-objekt</span><span class="sxs-lookup"><span data-stu-id="13963-110">Create a MatchCondition object</span></span>

## <span data-ttu-id="13963-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13963-111">PARAMETERS</span></span>

### <span data-ttu-id="13963-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13963-112">-DefaultProfile</span></span>
<span data-ttu-id="13963-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13963-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13963-114">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="13963-114">-MatchValue</span></span>
<span data-ttu-id="13963-115">Match värde.</span><span class="sxs-lookup"><span data-stu-id="13963-115">Match value.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13963-116">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="13963-116">-MatchVariable</span></span>
<span data-ttu-id="13963-117">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="13963-117">Match Variable.</span></span>
<span data-ttu-id="13963-118">Möjliga värden inkluderar: "RemoteAddr", "RequestMethod", "QueryString", "PostArgs", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="13963-118">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="13963-119">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="13963-119">-NegateCondition</span></span>
<span data-ttu-id="13963-120">Beskriver om det här är negerade villkor eller om det inte är standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="13963-120">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="13963-121">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="13963-121">-OperatorProperty</span></span>
<span data-ttu-id="13963-122">Beskriver vilken operator som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="13963-122">Describes operator to be matched.</span></span>
<span data-ttu-id="13963-123">Möjliga värden är: "any", "IPMatch", "mindreän", "Equal", "", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "börjarmed", "Slutarmed", "RegEx"</span><span class="sxs-lookup"><span data-stu-id="13963-123">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith', 'RegEx'</span></span>

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

### <span data-ttu-id="13963-124">-Selector</span><span class="sxs-lookup"><span data-stu-id="13963-124">-Selector</span></span>
<span data-ttu-id="13963-125">Namn på väljaren i RequestHeader eller RequestBody som ska matchas</span><span class="sxs-lookup"><span data-stu-id="13963-125">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="13963-126">-Omvandla</span><span class="sxs-lookup"><span data-stu-id="13963-126">-Transform</span></span>
<span data-ttu-id="13963-127">Transformeringar som ska användas.</span><span class="sxs-lookup"><span data-stu-id="13963-127">Transforms to apply.</span></span> <span data-ttu-id="13963-128">Möjliga värden är: gemener, versaler, "trim", "UrlDecode", "UrlEncode", "RemoveNulls".</span><span class="sxs-lookup"><span data-stu-id="13963-128">Possible values include: 'Lowercase', 'Uppercase', 'Trim', 'UrlDecode', 'UrlEncode', 'RemoveNulls'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13963-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13963-129">CommonParameters</span></span>
<span data-ttu-id="13963-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13963-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13963-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13963-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13963-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13963-132">INPUTS</span></span>

### <span data-ttu-id="13963-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="13963-133">None</span></span>

## <span data-ttu-id="13963-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13963-134">OUTPUTS</span></span>

### <span data-ttu-id="13963-135">Microsoft. Azure. commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="13963-135">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="13963-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13963-136">NOTES</span></span>

## <span data-ttu-id="13963-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13963-137">RELATED LINKS</span></span>

[<span data-ttu-id="13963-138">New-AzFrontDoorWafCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="13963-138">New-AzFrontDoorWafCustomRuleObject</span></span>](./New-AzFrontDoorWafCustomRuleObject.md)
