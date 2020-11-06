---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582748"
---
# <span data-ttu-id="2edce-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="2edce-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="2edce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2edce-102">SYNOPSIS</span></span>
<span data-ttu-id="2edce-103">Ta bort en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2edce-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2edce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2edce-104">SYNTAX</span></span>

### <span data-ttu-id="2edce-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="2edce-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2edce-106">Fäst</span><span class="sxs-lookup"><span data-stu-id="2edce-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2edce-107">DESCRIPTION</span></span>
<span data-ttu-id="2edce-108">Remove-AzureRmConsumptionBudget-cmdleten tar bort en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="2edce-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="2edce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2edce-109">EXAMPLES</span></span>

### <span data-ttu-id="2edce-110">Exempel 1: ta bort en budget med ett budget namn på prenumerations nivå</span><span class="sxs-lookup"><span data-stu-id="2edce-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="2edce-111">Exempel 2: ta bort en budget med ett budget namn på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="2edce-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="2edce-112">Exempel 3: ta bort en budget genom överföring på abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="2edce-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="2edce-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2edce-113">PARAMETERS</span></span>

### <span data-ttu-id="2edce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edce-114">-DefaultProfile</span></span>
<span data-ttu-id="2edce-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2edce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2edce-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2edce-116">-InputObject</span></span>
<span data-ttu-id="2edce-117">Budget objekt.</span><span class="sxs-lookup"><span data-stu-id="2edce-117">Budget object.</span></span>

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

### <span data-ttu-id="2edce-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2edce-118">-Name</span></span>
<span data-ttu-id="2edce-119">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="2edce-119">Name of a budget.</span></span>

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

### <span data-ttu-id="2edce-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2edce-120">-PassThru</span></span>
<span data-ttu-id="2edce-121">Cmdleten returnerar sant om en budget har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="2edce-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="2edce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edce-122">-ResourceGroupName</span></span>
<span data-ttu-id="2edce-123">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="2edce-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="2edce-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2edce-124">-Confirm</span></span>
<span data-ttu-id="2edce-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2edce-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edce-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edce-126">-WhatIf</span></span>
<span data-ttu-id="2edce-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2edce-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2edce-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2edce-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edce-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edce-129">CommonParameters</span></span>
<span data-ttu-id="2edce-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2edce-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edce-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2edce-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edce-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2edce-132">INPUTS</span></span>

### <span data-ttu-id="2edce-133">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="2edce-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="2edce-134">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2edce-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2edce-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2edce-135">OUTPUTS</span></span>

### <span data-ttu-id="2edce-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2edce-136">System.Boolean</span></span>

## <span data-ttu-id="2edce-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2edce-137">NOTES</span></span>

## <span data-ttu-id="2edce-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2edce-138">RELATED LINKS</span></span>
