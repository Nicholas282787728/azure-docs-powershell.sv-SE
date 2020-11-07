---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585472"
---
# <span data-ttu-id="bbb1d-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="bbb1d-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="bbb1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bbb1d-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb1d-103">Flyttar en åtagande associering från en åtagande plan till ett annat.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbb1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bbb1d-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbb1d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bbb1d-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb1d-106">Flyttar en åtagande Associations resurs från en överordnad åtagande plan till en annan åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="bbb1d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bbb1d-107">EXAMPLES</span></span>

### <span data-ttu-id="bbb1d-108">--------------------------Exempel 1: flytta en åtagande Associations--------------------------</span><span class="sxs-lookup"><span data-stu-id="bbb1d-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="bbb1d-109">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="bbb1d-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="bbb1d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bbb1d-110">PARAMETERS</span></span>

### <span data-ttu-id="bbb1d-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="bbb1d-111">-CommitmentPlanName</span></span>
<span data-ttu-id="bbb1d-112">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bbb1d-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="bbb1d-113">-DestinationPlanId</span></span>
<span data-ttu-id="bbb1d-114">Azure-resurs-ID för mål gruppen Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="bbb1d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="bbb1d-115">-Name</span></span>
<span data-ttu-id="bbb1d-116">Namnet på Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="bbb1d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb1d-117">-ResourceGroupName</span></span>
<span data-ttu-id="bbb1d-118">Namnet på resurs gruppen för en Azure ML-associering.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="bbb1d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bbb1d-119">-Confirm</span></span>
<span data-ttu-id="bbb1d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb1d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb1d-121">-WhatIf</span></span>
<span data-ttu-id="bbb1d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbb1d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb1d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb1d-124">-DefaultProfile</span></span>
<span data-ttu-id="bbb1d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbb1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb1d-126">CommonParameters</span></span>
<span data-ttu-id="bbb1d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbb1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb1d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbb1d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb1d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bbb1d-129">INPUTS</span></span>

## <span data-ttu-id="bbb1d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bbb1d-130">OUTPUTS</span></span>

### <span data-ttu-id="bbb1d-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="bbb1d-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="bbb1d-132">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="bbb1d-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="bbb1d-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bbb1d-133">NOTES</span></span>
<span data-ttu-id="bbb1d-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="bbb1d-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bbb1d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bbb1d-135">RELATED LINKS</span></span>
