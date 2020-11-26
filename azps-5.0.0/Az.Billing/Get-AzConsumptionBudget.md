---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271652"
---
# <span data-ttu-id="d1bb4-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="d1bb4-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="d1bb4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="d1bb4-103">Få en lista med budgetar i ett abonnemang eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d1bb4-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d1bb4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1bb4-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="d1bb4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="d1bb4-106">Get-AzConsumptionBudget-cmdleten får en lista med budgetar i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d1bb4-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d1bb4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="d1bb4-108">Exempel 1: Hämta en lista med budgetar på abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="d1bb4-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="d1bb4-109">Exempel 2: Hämta en lista med budgetar på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="d1bb4-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="d1bb4-110">Exempel 3: få en budget med budget namnet på abonnemangs nivån</span><span class="sxs-lookup"><span data-stu-id="d1bb4-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="d1bb4-111">Exempel 4: få en budget med budget namnet på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="d1bb4-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="d1bb4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1bb4-112">PARAMETERS</span></span>

### <span data-ttu-id="d1bb4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1bb4-113">-DefaultProfile</span></span>
<span data-ttu-id="d1bb4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1bb4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1bb4-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1bb4-115">-Name</span></span>
<span data-ttu-id="d1bb4-116">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="d1bb4-116">Name of a budget.</span></span>

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

### <span data-ttu-id="d1bb4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1bb4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1bb4-118">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="d1bb4-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="d1bb4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1bb4-119">CommonParameters</span></span>
<span data-ttu-id="d1bb4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1bb4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1bb4-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1bb4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1bb4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1bb4-122">INPUTS</span></span>

### <span data-ttu-id="d1bb4-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="d1bb4-123">None</span></span>

## <span data-ttu-id="d1bb4-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1bb4-124">OUTPUTS</span></span>

### <span data-ttu-id="d1bb4-125">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="d1bb4-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="d1bb4-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1bb4-126">NOTES</span></span>

## <span data-ttu-id="d1bb4-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1bb4-127">RELATED LINKS</span></span>