---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.CostManagement/new-AzCostManagementQueryFilterObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementQueryFilterObject.md
ms.openlocfilehash: e7b5c605af531bd1c1251a1c615da9498059d43d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526372"
---
# <span data-ttu-id="abd71-101">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="abd71-101">New-AzCostManagementQueryFilterObject</span></span>

## <span data-ttu-id="abd71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="abd71-102">SYNOPSIS</span></span>
<span data-ttu-id="abd71-103">Skapa ett objekt i minnet för QueryFilter</span><span class="sxs-lookup"><span data-stu-id="abd71-103">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="abd71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="abd71-104">SYNTAX</span></span>

```
New-AzCostManagementQueryFilterObject [-And <IQueryFilter[]>] [-Dimensions <IQueryComparisonExpression>]
 [-Not <IQueryFilter>] [-Or <IQueryFilter[]>] [-Tag <IQueryComparisonExpression>] [<CommonParameters>]
```

## <span data-ttu-id="abd71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="abd71-105">DESCRIPTION</span></span>
<span data-ttu-id="abd71-106">Skapa ett objekt i minnet för QueryFilter</span><span class="sxs-lookup"><span data-stu-id="abd71-106">Create a in-memory object for QueryFilter</span></span>

## <span data-ttu-id="abd71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="abd71-107">EXAMPLES</span></span>

### <span data-ttu-id="abd71-108">Exempel 1: skapa ett filter objekt av fråga för export av kostnads hantering</span><span class="sxs-lookup"><span data-stu-id="abd71-108">Example 1: Create a filter object of query for cost management export</span></span>
```powershell
PS C:\> $orDimension = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceLocation' -Operator In -Value @('East US', 'West Europe')
PS C:\> $orTag = New-AzCostManagementQueryComparisonExpressionObject -Name 'Environment' -Operator In -Value @('UAT', 'Prod')
PS C:\> New-AzCostManagementQueryFilterObject -or @((New-AzCostManagementQueryFilterObject -Dimension $orDimension), (New-AzCostManagementQueryFilterObject -Tag $orTag))

And       :
Dimension : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
Not       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter
Or        : {Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter, Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryFilter}
Tag       : Microsoft.Azure.PowerShell.Cmdlets.Cost.Models.Api20200601.QueryComparisonExpression
```

<span data-ttu-id="abd71-109">Det här kommandot skapar ett filter objekt av fråga för export av kostnads hantering.</span><span class="sxs-lookup"><span data-stu-id="abd71-109">this command creates a filter object of query for cost management export.</span></span>

## <span data-ttu-id="abd71-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="abd71-110">PARAMETERS</span></span>

### <span data-ttu-id="abd71-111">-Och</span><span class="sxs-lookup"><span data-stu-id="abd71-111">-And</span></span>
<span data-ttu-id="abd71-112">Det logiska uttrycket "och".</span><span class="sxs-lookup"><span data-stu-id="abd71-112">The logical "AND" expression.</span></span>
<span data-ttu-id="abd71-113">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-113">Must have at least 2 items.</span></span>
<span data-ttu-id="abd71-114">För att konstruera kan du läsa avsnittet anteckningar och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="abd71-114">To construct, see NOTES section for AND properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd71-115">-Dimensioner</span><span class="sxs-lookup"><span data-stu-id="abd71-115">-Dimensions</span></span>
<span data-ttu-id="abd71-116">Har jämförelse uttryck för en dimension.</span><span class="sxs-lookup"><span data-stu-id="abd71-116">Has comparison expression for a dimensions.</span></span>
<span data-ttu-id="abd71-117">Om du vill skapa läser du avsnittet anteckningar för egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="abd71-117">To construct, see NOTES section for DIMENSIONS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd71-118">-Inte</span><span class="sxs-lookup"><span data-stu-id="abd71-118">-Not</span></span>
<span data-ttu-id="abd71-119">Det logiska uttrycket "inte".</span><span class="sxs-lookup"><span data-stu-id="abd71-119">The logical "NOT" expression.</span></span>
<span data-ttu-id="abd71-120">För att konstruera kan du läsa avsnittet anteckningar och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="abd71-120">To construct, see NOTES section for NOT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd71-121">-Eller</span><span class="sxs-lookup"><span data-stu-id="abd71-121">-Or</span></span>
<span data-ttu-id="abd71-122">Det logiska uttrycket "eller".</span><span class="sxs-lookup"><span data-stu-id="abd71-122">The logical "OR" expression.</span></span>
<span data-ttu-id="abd71-123">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-123">Must have at least 2 items.</span></span>
<span data-ttu-id="abd71-124">För att konstruera, se avsnittet anteckningar för eller egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="abd71-124">To construct, see NOTES section for OR properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd71-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="abd71-125">-Tag</span></span>
<span data-ttu-id="abd71-126">Har jämförelse uttryck för en tagg.</span><span class="sxs-lookup"><span data-stu-id="abd71-126">Has comparison expression for a tag.</span></span>
<span data-ttu-id="abd71-127">För att konstruera kan du läsa avsnittet anteckningar för TAGGEGENSKAPER och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="abd71-127">To construct, see NOTES section for TAG properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryComparisonExpression
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd71-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd71-128">CommonParameters</span></span>
<span data-ttu-id="abd71-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd71-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd71-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abd71-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd71-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="abd71-131">INPUTS</span></span>

## <span data-ttu-id="abd71-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="abd71-132">OUTPUTS</span></span>

### <span data-ttu-id="abd71-133">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. QueryFilter</span><span class="sxs-lookup"><span data-stu-id="abd71-133">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.QueryFilter</span></span>

## <span data-ttu-id="abd71-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="abd71-134">NOTES</span></span>

<span data-ttu-id="abd71-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="abd71-135">ALIASES</span></span>

<span data-ttu-id="abd71-136">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="abd71-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="abd71-137">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="abd71-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="abd71-138">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="abd71-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="abd71-139">OCH <IQueryFilter [] >: det logiska uttrycket "AND".</span><span class="sxs-lookup"><span data-stu-id="abd71-139">AND <IQueryFilter[]>: The logical "AND" expression.</span></span> <span data-ttu-id="abd71-140">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-140">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-141">`[And <IQueryFilter[]>]`: Det logiska uttrycket "och".</span><span class="sxs-lookup"><span data-stu-id="abd71-141">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="abd71-142">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-142">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-143">`[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension</span><span class="sxs-lookup"><span data-stu-id="abd71-143">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="abd71-144">`Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-144">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="abd71-145">`Operator <OperatorType>`: Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-145">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="abd71-146">`Value <String[]>`: Matris med värden som ska användas för jämförelse</span><span class="sxs-lookup"><span data-stu-id="abd71-146">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="abd71-147">`[Not <IQueryFilter>]`: Det logiska uttrycket "inte".</span><span class="sxs-lookup"><span data-stu-id="abd71-147">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="abd71-148">`[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller".</span><span class="sxs-lookup"><span data-stu-id="abd71-148">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="abd71-149">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-149">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-150">`[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg</span><span class="sxs-lookup"><span data-stu-id="abd71-150">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="abd71-151">MÅTT <IQueryComparisonExpression> : har jämförelse uttryck för en dimension.</span><span class="sxs-lookup"><span data-stu-id="abd71-151">DIMENSIONS <IQueryComparisonExpression>: Has comparison expression for a dimensions.</span></span>
  - <span data-ttu-id="abd71-152">`Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-152">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="abd71-153">`Operator <OperatorType>`: Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-153">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="abd71-154">`Value <String[]>`: Matris med värden som ska användas för jämförelse</span><span class="sxs-lookup"><span data-stu-id="abd71-154">`Value <String[]>`: Array of values to use for comparison</span></span>

<span data-ttu-id="abd71-155">INTE <IQueryFilter> : det logiska uttrycket "inte".</span><span class="sxs-lookup"><span data-stu-id="abd71-155">NOT <IQueryFilter>: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="abd71-156">`[And <IQueryFilter[]>]`: Det logiska uttrycket "och".</span><span class="sxs-lookup"><span data-stu-id="abd71-156">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="abd71-157">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-157">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-158">`[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension</span><span class="sxs-lookup"><span data-stu-id="abd71-158">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="abd71-159">`Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-159">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="abd71-160">`Operator <OperatorType>`: Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-160">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="abd71-161">`Value <String[]>`: Matris med värden som ska användas för jämförelse</span><span class="sxs-lookup"><span data-stu-id="abd71-161">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="abd71-162">`[Not <IQueryFilter>]`: Det logiska uttrycket "inte".</span><span class="sxs-lookup"><span data-stu-id="abd71-162">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="abd71-163">`[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller".</span><span class="sxs-lookup"><span data-stu-id="abd71-163">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="abd71-164">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-164">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-165">`[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg</span><span class="sxs-lookup"><span data-stu-id="abd71-165">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="abd71-166">ELLER <IQueryFilter [] >: det logiska uttrycket "eller".</span><span class="sxs-lookup"><span data-stu-id="abd71-166">OR <IQueryFilter[]>: The logical "OR" expression.</span></span> <span data-ttu-id="abd71-167">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-167">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-168">`[And <IQueryFilter[]>]`: Det logiska uttrycket "och".</span><span class="sxs-lookup"><span data-stu-id="abd71-168">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="abd71-169">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-169">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-170">`[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension</span><span class="sxs-lookup"><span data-stu-id="abd71-170">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="abd71-171">`Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-171">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="abd71-172">`Operator <OperatorType>`: Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-172">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="abd71-173">`Value <String[]>`: Matris med värden som ska användas för jämförelse</span><span class="sxs-lookup"><span data-stu-id="abd71-173">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="abd71-174">`[Not <IQueryFilter>]`: Det logiska uttrycket "inte".</span><span class="sxs-lookup"><span data-stu-id="abd71-174">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="abd71-175">`[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller".</span><span class="sxs-lookup"><span data-stu-id="abd71-175">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="abd71-176">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="abd71-176">Must have at least 2 items.</span></span>
  - <span data-ttu-id="abd71-177">`[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg</span><span class="sxs-lookup"><span data-stu-id="abd71-177">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="abd71-178">TAGG <IQueryComparisonExpression> : har jämförelse uttryck för en tagg.</span><span class="sxs-lookup"><span data-stu-id="abd71-178">TAG <IQueryComparisonExpression>: Has comparison expression for a tag.</span></span>
  - <span data-ttu-id="abd71-179">`Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-179">`Name <String>`: The name of the column to use in comparison.</span></span>
  - <span data-ttu-id="abd71-180">`Operator <OperatorType>`: Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="abd71-180">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
  - <span data-ttu-id="abd71-181">`Value <String[]>`: Matris med värden som ska användas för jämförelse</span><span class="sxs-lookup"><span data-stu-id="abd71-181">`Value <String[]>`: Array of values to use for comparison</span></span>

## <span data-ttu-id="abd71-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="abd71-182">RELATED LINKS</span></span>

