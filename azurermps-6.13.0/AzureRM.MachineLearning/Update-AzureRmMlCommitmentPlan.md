---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/update-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 38228cd8f7618d3dfeec1836621d2eeffc5ecb4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577947"
---
# <span data-ttu-id="52388-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="52388-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="52388-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52388-102">SYNOPSIS</span></span>
<span data-ttu-id="52388-103">Uppdaterar egenskaper för en befintlig åtagande Plans resurs.</span><span class="sxs-lookup"><span data-stu-id="52388-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52388-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52388-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52388-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52388-105">DESCRIPTION</span></span>
<span data-ttu-id="52388-106">Uppdaterar en befintlig resurs för åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="52388-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="52388-107">Observera att de flesta egenskaperna för åtagande planen är oföränderliga och inte kan ändras.</span><span class="sxs-lookup"><span data-stu-id="52388-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="52388-108">Egenskaper som kan ändras är bland annat SKU (för att du ska kunna migrera ett åtagande från en SKU till en annan) och taggar.</span><span class="sxs-lookup"><span data-stu-id="52388-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="52388-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52388-109">EXAMPLES</span></span>

### <span data-ttu-id="52388-110">Exempel 1: uppdatera en åtagande plan</span><span class="sxs-lookup"><span data-stu-id="52388-110">Example 1: Update a commitment plan</span></span>
```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="52388-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52388-111">PARAMETERS</span></span>

### <span data-ttu-id="52388-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52388-112">-DefaultProfile</span></span>
<span data-ttu-id="52388-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="52388-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52388-114">-Force</span><span class="sxs-lookup"><span data-stu-id="52388-114">-Force</span></span>
<span data-ttu-id="52388-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="52388-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="52388-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="52388-116">-Name</span></span>
<span data-ttu-id="52388-117">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="52388-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="52388-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52388-118">-ResourceGroupName</span></span>
<span data-ttu-id="52388-119">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="52388-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="52388-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="52388-120">-SkuCapacity</span></span>
<span data-ttu-id="52388-121">Kapaciteten för SKU: n som ska användas vid uppdatering av abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="52388-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52388-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="52388-122">-SkuName</span></span>
<span data-ttu-id="52388-123">Namnet på den SKU som ska användas vid uppdatering av abonnemanget Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="52388-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="52388-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="52388-124">-SkuTier</span></span>
<span data-ttu-id="52388-125">Nivån på den SKU som ska användas vid uppdatering av abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="52388-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="52388-126">-Tagg</span><span class="sxs-lookup"><span data-stu-id="52388-126">-Tag</span></span>
<span data-ttu-id="52388-127">Taggar för resursen för åtagandet.</span><span class="sxs-lookup"><span data-stu-id="52388-127">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52388-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52388-128">-Confirm</span></span>
<span data-ttu-id="52388-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52388-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52388-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52388-130">-WhatIf</span></span>
<span data-ttu-id="52388-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52388-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52388-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52388-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52388-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52388-133">CommonParameters</span></span>
<span data-ttu-id="52388-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52388-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52388-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52388-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52388-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52388-136">INPUTS</span></span>

### <span data-ttu-id="52388-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="52388-137">None</span></span>

## <span data-ttu-id="52388-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52388-138">OUTPUTS</span></span>

### <span data-ttu-id="52388-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="52388-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="52388-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52388-140">NOTES</span></span>
<span data-ttu-id="52388-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="52388-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="52388-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52388-142">RELATED LINKS</span></span>