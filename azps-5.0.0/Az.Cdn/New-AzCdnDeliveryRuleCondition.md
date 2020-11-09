---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322252"
---
# <span data-ttu-id="69c79-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="69c79-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="69c79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="69c79-102">SYNOPSIS</span></span>
<span data-ttu-id="69c79-103">Skapar ett villkor för leverans regel.</span><span class="sxs-lookup"><span data-stu-id="69c79-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="69c79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="69c79-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69c79-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="69c79-105">DESCRIPTION</span></span>
<span data-ttu-id="69c79-106">Cmdleten **New-AzCdnDeliveryRule** skapar en leverans regel för generering av CDN-slutpunkt.</span><span class="sxs-lookup"><span data-stu-id="69c79-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="69c79-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="69c79-107">EXAMPLES</span></span>

### <span data-ttu-id="69c79-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="69c79-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="69c79-109">Skapa ett enkelt villkor.</span><span class="sxs-lookup"><span data-stu-id="69c79-109">Create a simple condition.</span></span>

## <span data-ttu-id="69c79-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="69c79-110">PARAMETERS</span></span>

### <span data-ttu-id="69c79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c79-111">-DefaultProfile</span></span>
<span data-ttu-id="69c79-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="69c79-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c79-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="69c79-113">-MatchValue</span></span>
<span data-ttu-id="69c79-114">Lista med möjliga matchnings värden.</span><span class="sxs-lookup"><span data-stu-id="69c79-114">List of possible match values.</span></span>

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

### <span data-ttu-id="69c79-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="69c79-115">-MatchVariable</span></span>
<span data-ttu-id="69c79-116">Matcha variabel för villkoret.</span><span class="sxs-lookup"><span data-stu-id="69c79-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="69c79-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="69c79-117">-NegateCondition</span></span>
<span data-ttu-id="69c79-118">Här beskrivs hur det här villkoret ska negeras.</span><span class="sxs-lookup"><span data-stu-id="69c79-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69c79-119">-Operatör</span><span class="sxs-lookup"><span data-stu-id="69c79-119">-Operator</span></span>
<span data-ttu-id="69c79-120">Beskriver vilken operator som ska matchas</span><span class="sxs-lookup"><span data-stu-id="69c79-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="69c79-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="69c79-121">-Selector</span></span>
<span data-ttu-id="69c79-122">Namn på väljaren som ska matchas</span><span class="sxs-lookup"><span data-stu-id="69c79-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="69c79-123">-Omvandla</span><span class="sxs-lookup"><span data-stu-id="69c79-123">-Transform</span></span>
<span data-ttu-id="69c79-124">Omvandla för att tillämpas före matchning.</span><span class="sxs-lookup"><span data-stu-id="69c79-124">Transform to apply before matching.</span></span>
<span data-ttu-id="69c79-125">Möjliga värden är gemener och versaler</span><span class="sxs-lookup"><span data-stu-id="69c79-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="69c79-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c79-126">CommonParameters</span></span>
<span data-ttu-id="69c79-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c79-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c79-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69c79-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c79-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="69c79-129">INPUTS</span></span>

### <span data-ttu-id="69c79-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="69c79-130">None</span></span>

## <span data-ttu-id="69c79-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="69c79-131">OUTPUTS</span></span>

### <span data-ttu-id="69c79-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="69c79-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="69c79-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="69c79-133">NOTES</span></span>

## <span data-ttu-id="69c79-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="69c79-134">RELATED LINKS</span></span>
