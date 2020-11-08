---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090124"
---
# <span data-ttu-id="f2670-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="f2670-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="f2670-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2670-102">SYNOPSIS</span></span>
<span data-ttu-id="f2670-103">Ta bort en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f2670-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f2670-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2670-104">SYNTAX</span></span>

### <span data-ttu-id="f2670-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="f2670-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2670-106">Fäst</span><span class="sxs-lookup"><span data-stu-id="f2670-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2670-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2670-107">DESCRIPTION</span></span>
<span data-ttu-id="f2670-108">Remove-AzConsumptionBudget-cmdleten tar bort en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f2670-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="f2670-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2670-109">EXAMPLES</span></span>

### <span data-ttu-id="f2670-110">Exempel 1: ta bort en budget med ett budget namn på prenumerations nivå</span><span class="sxs-lookup"><span data-stu-id="f2670-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="f2670-111">Exempel 2: ta bort en budget med ett budget namn på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="f2670-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="f2670-112">Exempel 3: ta bort en budget genom överföring på abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="f2670-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="f2670-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2670-113">PARAMETERS</span></span>

### <span data-ttu-id="f2670-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2670-114">-DefaultProfile</span></span>
<span data-ttu-id="f2670-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2670-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2670-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2670-116">-InputObject</span></span>
<span data-ttu-id="f2670-117">Budget objekt.</span><span class="sxs-lookup"><span data-stu-id="f2670-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2670-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2670-118">-Name</span></span>
<span data-ttu-id="f2670-119">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="f2670-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2670-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2670-120">-PassThru</span></span>
<span data-ttu-id="f2670-121">Cmdleten returnerar sant om en budget har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="f2670-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="f2670-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2670-122">-ResourceGroupName</span></span>
<span data-ttu-id="f2670-123">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="f2670-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2670-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2670-124">-Confirm</span></span>
<span data-ttu-id="f2670-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2670-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2670-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2670-126">-WhatIf</span></span>
<span data-ttu-id="f2670-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2670-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2670-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2670-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2670-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2670-129">CommonParameters</span></span>
<span data-ttu-id="f2670-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2670-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2670-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2670-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2670-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2670-132">INPUTS</span></span>

### <span data-ttu-id="f2670-133">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="f2670-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="f2670-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2670-134">OUTPUTS</span></span>

### <span data-ttu-id="f2670-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2670-135">System.Boolean</span></span>

## <span data-ttu-id="f2670-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2670-136">NOTES</span></span>

## <span data-ttu-id="f2670-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2670-137">RELATED LINKS</span></span>