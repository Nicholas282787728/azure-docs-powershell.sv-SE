---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 1c022d8ae97ac9f1e51bbabaff15a9dec61f5d87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915858"
---
# <span data-ttu-id="75ee0-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="75ee0-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="75ee0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="75ee0-103">Tar bort en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="75ee0-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="75ee0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75ee0-104">SYNTAX</span></span>

### <span data-ttu-id="75ee0-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75ee0-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75ee0-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="75ee0-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ee0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="75ee0-108">Tar bort en Azure Machine Learning-plan.</span><span class="sxs-lookup"><span data-stu-id="75ee0-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="75ee0-109">Observera att det finns åtaganden som inte kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="75ee0-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="75ee0-110">Åtagande associationer kan bara tas bort av mål resursen.</span><span class="sxs-lookup"><span data-stu-id="75ee0-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="75ee0-111">Om du till exempel tar bort en Azure Machine Learning-webbtjänst raderas åtagandet som associerar webb tjänsten med en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="75ee0-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="75ee0-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75ee0-112">EXAMPLES</span></span>

### <span data-ttu-id="75ee0-113">Exempel 1: ta bort en åtagande plan</span><span class="sxs-lookup"><span data-stu-id="75ee0-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="75ee0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75ee0-114">PARAMETERS</span></span>

### <span data-ttu-id="75ee0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ee0-115">-DefaultProfile</span></span>
<span data-ttu-id="75ee0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="75ee0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75ee0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="75ee0-117">-Force</span></span>
<span data-ttu-id="75ee0-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="75ee0-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="75ee0-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="75ee0-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="75ee0-120">Objektet utbildnings webb tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="75ee0-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75ee0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="75ee0-121">-Name</span></span>
<span data-ttu-id="75ee0-122">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="75ee0-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ee0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ee0-123">-ResourceGroupName</span></span>
<span data-ttu-id="75ee0-124">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="75ee0-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ee0-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75ee0-125">-Confirm</span></span>
<span data-ttu-id="75ee0-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75ee0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75ee0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ee0-127">-WhatIf</span></span>
<span data-ttu-id="75ee0-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75ee0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75ee0-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75ee0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75ee0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ee0-130">CommonParameters</span></span>
<span data-ttu-id="75ee0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75ee0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ee0-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ee0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ee0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75ee0-133">INPUTS</span></span>

### <span data-ttu-id="75ee0-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="75ee0-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="75ee0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75ee0-135">OUTPUTS</span></span>

### <span data-ttu-id="75ee0-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="75ee0-136">System.Void</span></span>

## <span data-ttu-id="75ee0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75ee0-137">NOTES</span></span>
<span data-ttu-id="75ee0-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="75ee0-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="75ee0-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75ee0-139">RELATED LINKS</span></span>
