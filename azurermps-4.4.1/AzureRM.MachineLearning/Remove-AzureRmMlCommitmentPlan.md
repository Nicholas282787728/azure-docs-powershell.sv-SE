---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 31678552a43951406d18c49ee80ffaa7897fd1d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758389"
---
# <span data-ttu-id="65ef4-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="65ef4-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="65ef4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="65ef4-103">Tar bort en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="65ef4-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65ef4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65ef4-104">SYNTAX</span></span>

### <span data-ttu-id="65ef4-105">Ta bort en Azure ML-plan för åtaganden enligt namn och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="65ef4-105">Remove an Azure ML commitment plan specified by name and resource group.</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ef4-106">Ta bort en Azure ML-plan för åtaganden angivet som ett objekt.</span><span class="sxs-lookup"><span data-stu-id="65ef4-106">Remove an Azure ML commitment plan specified as an object.</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ef4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65ef4-107">DESCRIPTION</span></span>
<span data-ttu-id="65ef4-108">Tar bort en Azure Machine Learning-plan.</span><span class="sxs-lookup"><span data-stu-id="65ef4-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="65ef4-109">Observera att det finns åtaganden som inte kan tas bort.</span><span class="sxs-lookup"><span data-stu-id="65ef4-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="65ef4-110">Åtagande associationer kan bara tas bort av mål resursen.</span><span class="sxs-lookup"><span data-stu-id="65ef4-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="65ef4-111">Om du till exempel tar bort en Azure Machine Learning-webbtjänst raderas åtagandet som associerar webb tjänsten med en åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="65ef4-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="65ef4-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65ef4-112">EXAMPLES</span></span>

### <span data-ttu-id="65ef4-113">--------------------------Exempel 1: ta bort en åtagande plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="65ef4-113">--------------------------  Example 1: Delete a commitment plan  --------------------------</span></span>
<span data-ttu-id="65ef4-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="65ef4-114">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="65ef4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65ef4-115">PARAMETERS</span></span>

### <span data-ttu-id="65ef4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="65ef4-116">-Force</span></span>
<span data-ttu-id="65ef4-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="65ef4-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="65ef4-118">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="65ef4-118">-MlCommitmentPlan</span></span>
<span data-ttu-id="65ef4-119">Objektet utbildnings webb tjänst objekt.</span><span class="sxs-lookup"><span data-stu-id="65ef4-119">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: Remove an Azure ML commitment plan specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ef4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="65ef4-120">-Name</span></span>
<span data-ttu-id="65ef4-121">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="65ef4-121">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ef4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ef4-122">-ResourceGroupName</span></span>
<span data-ttu-id="65ef4-123">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="65ef4-123">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML commitment plan specified by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ef4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65ef4-124">-Confirm</span></span>
<span data-ttu-id="65ef4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65ef4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ef4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ef4-126">-WhatIf</span></span>
<span data-ttu-id="65ef4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="65ef4-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65ef4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="65ef4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ef4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ef4-129">-DefaultProfile</span></span>
<span data-ttu-id="65ef4-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="65ef4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65ef4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ef4-131">CommonParameters</span></span>
<span data-ttu-id="65ef4-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ef4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ef4-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65ef4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ef4-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65ef4-134">INPUTS</span></span>

### <span data-ttu-id="65ef4-135">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="65ef4-135">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="65ef4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65ef4-136">OUTPUTS</span></span>

### <span data-ttu-id="65ef4-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="65ef4-137">None</span></span>

## <span data-ttu-id="65ef4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65ef4-138">NOTES</span></span>
<span data-ttu-id="65ef4-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="65ef4-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="65ef4-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65ef4-140">RELATED LINKS</span></span>

