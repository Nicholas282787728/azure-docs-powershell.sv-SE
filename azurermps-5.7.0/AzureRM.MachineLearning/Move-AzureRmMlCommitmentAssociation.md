---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 2bd650e86a1a4b59694dc88dc915da0fd7713e5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586076"
---
# <span data-ttu-id="f65d8-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="f65d8-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="f65d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f65d8-102">SYNOPSIS</span></span>
<span data-ttu-id="f65d8-103">Flyttar en åtagande associering från en åtagande plan till ett annat.</span><span class="sxs-lookup"><span data-stu-id="f65d8-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f65d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f65d8-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f65d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f65d8-105">DESCRIPTION</span></span>
<span data-ttu-id="f65d8-106">Flyttar en åtagande Associations resurs från en överordnad åtagande plan till en annan åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="f65d8-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="f65d8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f65d8-107">EXAMPLES</span></span>

### <span data-ttu-id="f65d8-108">--------------------------Exempel 1: flytta en åtagande Associations--------------------------</span><span class="sxs-lookup"><span data-stu-id="f65d8-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="f65d8-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f65d8-109">PARAMETERS</span></span>

### <span data-ttu-id="f65d8-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="f65d8-110">-CommitmentPlanName</span></span>
<span data-ttu-id="f65d8-111">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="f65d8-111">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65d8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f65d8-112">-DefaultProfile</span></span>
<span data-ttu-id="f65d8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f65d8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f65d8-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="f65d8-114">-DestinationPlanId</span></span>
<span data-ttu-id="f65d8-115">Azure-resurs-ID för mål gruppen Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="f65d8-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65d8-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="f65d8-116">-Name</span></span>
<span data-ttu-id="f65d8-117">Namnet på Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="f65d8-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65d8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f65d8-118">-ResourceGroupName</span></span>
<span data-ttu-id="f65d8-119">Namnet på resurs gruppen för en Azure ML-associering.</span><span class="sxs-lookup"><span data-stu-id="f65d8-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f65d8-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f65d8-120">-Confirm</span></span>
<span data-ttu-id="f65d8-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f65d8-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f65d8-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f65d8-122">-WhatIf</span></span>
<span data-ttu-id="f65d8-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f65d8-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f65d8-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f65d8-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f65d8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f65d8-125">CommonParameters</span></span>
<span data-ttu-id="f65d8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f65d8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f65d8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f65d8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f65d8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f65d8-128">INPUTS</span></span>

### <span data-ttu-id="f65d8-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="f65d8-129">None</span></span>
<span data-ttu-id="f65d8-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f65d8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f65d8-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f65d8-131">OUTPUTS</span></span>

### <span data-ttu-id="f65d8-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f65d8-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="f65d8-133">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="f65d8-133">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="f65d8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f65d8-134">NOTES</span></span>
<span data-ttu-id="f65d8-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="f65d8-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f65d8-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f65d8-136">RELATED LINKS</span></span>

