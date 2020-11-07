---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorMatchConditionObject.md
ms.openlocfilehash: ed711160bf761fe7b28f02a94d1ab4ffa6fdb59f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916717"
---
# <span data-ttu-id="1f41b-101">New-AzFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="1f41b-101">New-AzFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="1f41b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f41b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f41b-103">Skapa MatchCondition-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="1f41b-103">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="1f41b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f41b-104">SYNTAX</span></span>

```
New-AzFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable> -OperatorProperty <PSOperatorProperty>
 [-MatchValue <String[]>] [-Selector <String>] [-NegateCondition <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f41b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f41b-105">DESCRIPTION</span></span>
<span data-ttu-id="1f41b-106">Skapa MatchCondition-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="1f41b-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="1f41b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f41b-107">EXAMPLES</span></span>

### <span data-ttu-id="1f41b-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1f41b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "User-Agent" -MatchValue "Windows"


MatchVariable OperatorProperty MatchValue Selector   NegateCondition
------------- ---------------- ---------- --------   ---------------
RequestHeader         Contains {Windows}  User-Agent           False
```

<span data-ttu-id="1f41b-109">Skapa ett MatchCondition-objekt</span><span class="sxs-lookup"><span data-stu-id="1f41b-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="1f41b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f41b-110">PARAMETERS</span></span>

### <span data-ttu-id="1f41b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f41b-111">-DefaultProfile</span></span>
<span data-ttu-id="1f41b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1f41b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f41b-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="1f41b-113">-MatchValue</span></span>
<span data-ttu-id="1f41b-114">Match värde.</span><span class="sxs-lookup"><span data-stu-id="1f41b-114">Match value.</span></span>

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

### <span data-ttu-id="1f41b-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="1f41b-115">-MatchVariable</span></span>
<span data-ttu-id="1f41b-116">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="1f41b-116">Match Variable.</span></span>
<span data-ttu-id="1f41b-117">Möjliga värden inkluderar: "RemoteAddr", "RequestMethod", "QueryString", "PostArgs", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="1f41b-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMatchVariable
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeader, RequestBody

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f41b-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="1f41b-118">-NegateCondition</span></span>
<span data-ttu-id="1f41b-119">Beskriver om det här är negerade villkor eller om det inte är standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="1f41b-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="1f41b-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="1f41b-120">-OperatorProperty</span></span>
<span data-ttu-id="1f41b-121">Beskriver vilken operator som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="1f41b-121">Describes operator to be matched.</span></span>
<span data-ttu-id="1f41b-122">Möjliga värden är: "any", "IPMatch", "mindreän", "Equal", "contains", "", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "börjarmed", "Slutarmed" "</span><span class="sxs-lookup"><span data-stu-id="1f41b-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSOperatorProperty
Parameter Sets: (All)
Aliases:
Accepted values: Any, IPMatch, GeoMatch, Equal, Contains, LessThan, GreaterThan, LessThanOrEqual, GreaterThanOrEqual, BeginsWith, EndsWith

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f41b-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="1f41b-123">-Selector</span></span>
<span data-ttu-id="1f41b-124">Namn på väljaren i RequestHeader eller RequestBody som ska matchas</span><span class="sxs-lookup"><span data-stu-id="1f41b-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="1f41b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f41b-125">CommonParameters</span></span>
<span data-ttu-id="1f41b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f41b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f41b-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f41b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f41b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f41b-128">INPUTS</span></span>

### <span data-ttu-id="1f41b-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="1f41b-129">None</span></span>

## <span data-ttu-id="1f41b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f41b-130">OUTPUTS</span></span>

### <span data-ttu-id="1f41b-131">Microsoft. Azure. commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="1f41b-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="1f41b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f41b-132">NOTES</span></span>

## <span data-ttu-id="1f41b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f41b-133">RELATED LINKS</span></span>

[<span data-ttu-id="1f41b-134">New-AzFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="1f41b-134">New-AzFrontDoorCustomRuleObject</span></span>](./New-AzFrontDoorCustomRuleObject.md)
