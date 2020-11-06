---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d14baa5382d5d9ffeeac8efd863a17cbad279865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582647"
---
# <span data-ttu-id="ab894-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab894-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="ab894-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab894-102">SYNOPSIS</span></span>
<span data-ttu-id="ab894-103">Tar bort en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="ab894-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab894-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab894-104">SYNTAX</span></span>

### <span data-ttu-id="ab894-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab894-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab894-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="ab894-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab894-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab894-107">DESCRIPTION</span></span>
<span data-ttu-id="ab894-108">Tar bort en Azure Machine Learning-plan.</span><span class="sxs-lookup"><span data-stu-id="ab894-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="ab894-109">Observera att det finns åtaganden som inte kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="ab894-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="ab894-110">Åtagande associationer kan bara tas bort av mål resursen.</span><span class="sxs-lookup"><span data-stu-id="ab894-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="ab894-111">Om du till exempel tar bort en Azure Machine Learning-webbtjänst raderas åtagandet som associerar webb tjänsten med en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="ab894-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="ab894-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab894-112">EXAMPLES</span></span>

### <span data-ttu-id="ab894-113">Exempel 1: ta bort en åtagande plan</span><span class="sxs-lookup"><span data-stu-id="ab894-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="ab894-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab894-114">PARAMETERS</span></span>

### <span data-ttu-id="ab894-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab894-115">-DefaultProfile</span></span>
<span data-ttu-id="ab894-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ab894-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab894-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ab894-117">-Force</span></span>
<span data-ttu-id="ab894-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ab894-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab894-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab894-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="ab894-120">Objektet utbildnings webb tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="ab894-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="ab894-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ab894-121">-Name</span></span>
<span data-ttu-id="ab894-122">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="ab894-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab894-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab894-123">-ResourceGroupName</span></span>
<span data-ttu-id="ab894-124">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="ab894-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="ab894-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ab894-125">-Confirm</span></span>
<span data-ttu-id="ab894-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ab894-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab894-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab894-127">-WhatIf</span></span>
<span data-ttu-id="ab894-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ab894-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab894-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ab894-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab894-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab894-130">CommonParameters</span></span>
<span data-ttu-id="ab894-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab894-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab894-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab894-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab894-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab894-133">INPUTS</span></span>

### <span data-ttu-id="ab894-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ab894-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="ab894-135">Parametrar: MlCommitmentPlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab894-135">Parameters: MlCommitmentPlan (ByValue)</span></span>

## <span data-ttu-id="ab894-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab894-136">OUTPUTS</span></span>

### <span data-ttu-id="ab894-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="ab894-137">System.Void</span></span>

## <span data-ttu-id="ab894-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab894-138">NOTES</span></span>
<span data-ttu-id="ab894-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="ab894-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ab894-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab894-140">RELATED LINKS</span></span>
