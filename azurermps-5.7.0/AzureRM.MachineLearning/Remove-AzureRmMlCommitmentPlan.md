---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 6c02b076de3d3f63685938a84e4a437e22c1e16f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586063"
---
# <span data-ttu-id="6f694-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6f694-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="6f694-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f694-102">SYNOPSIS</span></span>
<span data-ttu-id="6f694-103">Tar bort en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="6f694-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f694-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f694-104">SYNTAX</span></span>

### <span data-ttu-id="6f694-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f694-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f694-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="6f694-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f694-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f694-107">DESCRIPTION</span></span>
<span data-ttu-id="6f694-108">Tar bort en Azure Machine Learning-plan.</span><span class="sxs-lookup"><span data-stu-id="6f694-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="6f694-109">Observera att det finns åtaganden som inte kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="6f694-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="6f694-110">Åtagande associationer kan bara tas bort av mål resursen.</span><span class="sxs-lookup"><span data-stu-id="6f694-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="6f694-111">Om du till exempel tar bort en Azure Machine Learning-webbtjänst raderas åtagandet som associerar webb tjänsten med en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="6f694-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="6f694-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f694-112">EXAMPLES</span></span>

### <span data-ttu-id="6f694-113">--------------------------Exempel 1: ta bort en åtagande plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="6f694-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="6f694-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f694-114">PARAMETERS</span></span>

### <span data-ttu-id="6f694-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f694-115">-DefaultProfile</span></span>
<span data-ttu-id="6f694-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6f694-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6f694-117">-Force</span></span>
<span data-ttu-id="6f694-118">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6f694-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6f694-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="6f694-120">Objektet utbildnings webb tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="6f694-120">The machine learning web service object.</span></span>

```yaml
Type: CommitmentPlan
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f694-121">-Name</span></span>
<span data-ttu-id="6f694-122">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="6f694-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f694-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f694-124">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="6f694-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f694-125">-Confirm</span></span>
<span data-ttu-id="6f694-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f694-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f694-127">-WhatIf</span></span>
<span data-ttu-id="6f694-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f694-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f694-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f694-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f694-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f694-130">CommonParameters</span></span>
<span data-ttu-id="6f694-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f694-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f694-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f694-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f694-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f694-133">INPUTS</span></span>

### <span data-ttu-id="6f694-134">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="6f694-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="6f694-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f694-135">OUTPUTS</span></span>

### <span data-ttu-id="6f694-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="6f694-136">None</span></span>

## <span data-ttu-id="6f694-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f694-137">NOTES</span></span>
<span data-ttu-id="6f694-138">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="6f694-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6f694-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f694-139">RELATED LINKS</span></span>

