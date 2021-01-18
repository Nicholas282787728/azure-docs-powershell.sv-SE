---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryComparisonExpressionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryComparisonExpressionObject.md
ms.openlocfilehash: 5163f4747b926118bcd166304815b27bb1c1f629
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524278"
---
# <span data-ttu-id="0638e-101">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="0638e-101">New-AzCostManagementQueryComparisonExpressionObject</span></span>

## <span data-ttu-id="0638e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0638e-102">SYNOPSIS</span></span>
<span data-ttu-id="0638e-103">Skapa ett objekt i minnet för QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="0638e-103">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="0638e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0638e-104">SYNTAX</span></span>

```
New-AzCostManagementQueryComparisonExpressionObject -Name <String> -Operator <OperatorType> -Value <String[]>
 [<CommonParameters>]
```

## <span data-ttu-id="0638e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0638e-105">DESCRIPTION</span></span>
<span data-ttu-id="0638e-106">Skapa ett objekt i minnet för QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="0638e-106">Create a in-memory object for QueryComparisonExpression</span></span>

## <span data-ttu-id="0638e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0638e-107">EXAMPLES</span></span>

### <span data-ttu-id="0638e-108">Exempel 1: skapa ett jämförelse uttryck för fråga för export av kostnads hantering</span><span class="sxs-lookup"><span data-stu-id="0638e-108">Example 1: Create a comparison expression object of query for cost management export</span></span>
```powershell
PS C:\> New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')

Name             Operator Value
----             -------- -----
ResourceLocation In       {East US, West Europe}
```

<span data-ttu-id="0638e-109">Det här kommandot skapar ett jämförelse uttryck för fråga för export av kostnads hantering.</span><span class="sxs-lookup"><span data-stu-id="0638e-109">This command creates a comparison expression object of query for cost management export.</span></span>

## <span data-ttu-id="0638e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0638e-110">PARAMETERS</span></span>

### <span data-ttu-id="0638e-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="0638e-111">-Name</span></span>
<span data-ttu-id="0638e-112">Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="0638e-112">The name of the column to use in comparison.</span></span>

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

### <span data-ttu-id="0638e-113">-Operatör</span><span class="sxs-lookup"><span data-stu-id="0638e-113">-Operator</span></span>
<span data-ttu-id="0638e-114">Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="0638e-114">The operator to use for comparison.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.OperatorType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0638e-115">-Värde</span><span class="sxs-lookup"><span data-stu-id="0638e-115">-Value</span></span>
<span data-ttu-id="0638e-116">Matris med värden som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="0638e-116">Array of values to use for comparison.</span></span>

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

### <span data-ttu-id="0638e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0638e-117">CommonParameters</span></span>
<span data-ttu-id="0638e-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0638e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0638e-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0638e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0638e-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0638e-120">INPUTS</span></span>

## <span data-ttu-id="0638e-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0638e-121">OUTPUTS</span></span>

### <span data-ttu-id="0638e-122">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. QueryComparisonExpression</span><span class="sxs-lookup"><span data-stu-id="0638e-122">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryComparisonExpression</span></span>

## <span data-ttu-id="0638e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0638e-123">NOTES</span></span>

<span data-ttu-id="0638e-124">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0638e-124">ALIASES</span></span>

## <span data-ttu-id="0638e-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0638e-125">RELATED LINKS</span></span>

