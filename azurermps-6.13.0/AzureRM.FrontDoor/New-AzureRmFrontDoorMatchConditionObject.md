---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormatchconditionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorMatchConditionObject.md
ms.openlocfilehash: 70ab8b592c550280f424f9c0a4bfced877942edc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756159"
---
# <span data-ttu-id="097be-101">New-AzureRmFrontDoorMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="097be-101">New-AzureRmFrontDoorMatchConditionObject</span></span>

## <span data-ttu-id="097be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="097be-102">SYNOPSIS</span></span>
<span data-ttu-id="097be-103">Skapa MatchCondition-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="097be-103">Create MatchCondition Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="097be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="097be-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorMatchConditionObject -MatchVariable <PSMatchVariable>
 -OperatorProperty <PSOperatorProperty> -MatchValue <String[]> [-Selector <String>]
 [-NegateCondition <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="097be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="097be-105">DESCRIPTION</span></span>
<span data-ttu-id="097be-106">Skapa MatchCondition-objekt för WAF-princip</span><span class="sxs-lookup"><span data-stu-id="097be-106">Create MatchCondition Object for WAF policy creation</span></span>

## <span data-ttu-id="097be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="097be-107">EXAMPLES</span></span>

### <span data-ttu-id="097be-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="097be-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorMatchConditionObject -MatchVariable RequestHeader -OperatorProperty Contains -Selector "UserAgent" -MatchValue "Windows"


MatchVariable    : RequestHeader
OperatorProperty : Contains
MatchValue       : {Windows}
Selector         : UserAgent
NegateCondition  : False
```

<span data-ttu-id="097be-109">Skapa ett MatchCondition-objekt</span><span class="sxs-lookup"><span data-stu-id="097be-109">Create a MatchCondition object</span></span>

## <span data-ttu-id="097be-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="097be-110">PARAMETERS</span></span>

### <span data-ttu-id="097be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097be-111">-DefaultProfile</span></span>
<span data-ttu-id="097be-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="097be-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="097be-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="097be-113">-MatchValue</span></span>
<span data-ttu-id="097be-114">Match värde.</span><span class="sxs-lookup"><span data-stu-id="097be-114">Match value.</span></span>

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

### <span data-ttu-id="097be-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="097be-115">-MatchVariable</span></span>
<span data-ttu-id="097be-116">Matcha variabel.</span><span class="sxs-lookup"><span data-stu-id="097be-116">Match Variable.</span></span>
<span data-ttu-id="097be-117">Möjliga värden inkluderar: "RemoteAddr", "RequestMethod", "QueryString", "PostArgs", "RequestUri", "RequestHeader", "RequestBody"</span><span class="sxs-lookup"><span data-stu-id="097be-117">Possible values include: 'RemoteAddr', 'RequestMethod', 'QueryString', 'PostArgs','RequestUri', 'RequestHeader', 'RequestBody'</span></span>

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

### <span data-ttu-id="097be-118">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="097be-118">-NegateCondition</span></span>
<span data-ttu-id="097be-119">Beskriver om det här är negerade villkor eller om det inte är standardvärdet är falskt</span><span class="sxs-lookup"><span data-stu-id="097be-119">Describes if this is negate condition or not Default value is false</span></span>

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

### <span data-ttu-id="097be-120">-OperatorProperty</span><span class="sxs-lookup"><span data-stu-id="097be-120">-OperatorProperty</span></span>
<span data-ttu-id="097be-121">Beskriver vilken operator som ska matchas.</span><span class="sxs-lookup"><span data-stu-id="097be-121">Describes operator to be matched.</span></span>
<span data-ttu-id="097be-122">Möjliga värden är: "any", "IPMatch", "mindreän", "Equal", "contains", "", "GreaterThan", "LessThanOrEqual", "GreaterThanOrEqual", "börjarmed", "Slutarmed" "</span><span class="sxs-lookup"><span data-stu-id="097be-122">Possible values include: 'Any', 'IPMatch', 'GeoMatch', 'Equal', 'Contains', 'LessThan', 'GreaterThan', 'LessThanOrEqual', 'GreaterThanOrEqual', 'BeginsWith', 'EndsWith''</span></span>

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

### <span data-ttu-id="097be-123">-Selector</span><span class="sxs-lookup"><span data-stu-id="097be-123">-Selector</span></span>
<span data-ttu-id="097be-124">Namn på väljaren i RequestHeader eller RequestBody som ska matchas</span><span class="sxs-lookup"><span data-stu-id="097be-124">Name of selector in RequestHeader or RequestBody to be matched</span></span>

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

### <span data-ttu-id="097be-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097be-125">CommonParameters</span></span>
<span data-ttu-id="097be-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="097be-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097be-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="097be-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097be-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="097be-128">INPUTS</span></span>

### <span data-ttu-id="097be-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="097be-129">None</span></span>

## <span data-ttu-id="097be-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="097be-130">OUTPUTS</span></span>

### <span data-ttu-id="097be-131">Microsoft. Azure. commands. FrontDoor. Models. PSMatchCondition</span><span class="sxs-lookup"><span data-stu-id="097be-131">Microsoft.Azure.Commands.FrontDoor.Models.PSMatchCondition</span></span>

## <span data-ttu-id="097be-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="097be-132">NOTES</span></span>

## <span data-ttu-id="097be-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="097be-133">RELATED LINKS</span></span>

[<span data-ttu-id="097be-134">New-AzureRmFrontDoorCustomRuleObject</span><span class="sxs-lookup"><span data-stu-id="097be-134">New-AzureRmFrontDoorCustomRuleObject</span></span>](./New-AzureRmFrontDoorCustomRuleObject.md)
