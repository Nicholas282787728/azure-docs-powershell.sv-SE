---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/move-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 25a77e0e34e741273618ab4c434168b796595737
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577948"
---
# <span data-ttu-id="83857-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="83857-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="83857-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83857-102">SYNOPSIS</span></span>
<span data-ttu-id="83857-103">Flyttar en åtagande associering från en åtagande plan till ett annat.</span><span class="sxs-lookup"><span data-stu-id="83857-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83857-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83857-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83857-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83857-105">DESCRIPTION</span></span>
<span data-ttu-id="83857-106">Flyttar en åtagande Associations resurs från en överordnad åtagande plan till en annan åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="83857-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="83857-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83857-107">EXAMPLES</span></span>

### <span data-ttu-id="83857-108">Exempel 1: flytta en åtagande Association</span><span class="sxs-lookup"><span data-stu-id="83857-108">Example 1: Move a commitment association</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="83857-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83857-109">PARAMETERS</span></span>

### <span data-ttu-id="83857-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="83857-110">-CommitmentPlanName</span></span>
<span data-ttu-id="83857-111">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="83857-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="83857-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83857-112">-DefaultProfile</span></span>
<span data-ttu-id="83857-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="83857-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83857-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="83857-114">-DestinationPlanId</span></span>
<span data-ttu-id="83857-115">Azure-resurs-ID för mål gruppen Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="83857-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="83857-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="83857-116">-Name</span></span>
<span data-ttu-id="83857-117">Namnet på Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="83857-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="83857-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83857-118">-ResourceGroupName</span></span>
<span data-ttu-id="83857-119">Namnet på resurs gruppen för en Azure ML-associering.</span><span class="sxs-lookup"><span data-stu-id="83857-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="83857-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="83857-120">-Confirm</span></span>
<span data-ttu-id="83857-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="83857-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83857-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83857-122">-WhatIf</span></span>
<span data-ttu-id="83857-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="83857-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83857-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="83857-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83857-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83857-125">CommonParameters</span></span>
<span data-ttu-id="83857-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83857-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83857-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83857-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83857-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83857-128">INPUTS</span></span>

### <span data-ttu-id="83857-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="83857-129">None</span></span>

## <span data-ttu-id="83857-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83857-130">OUTPUTS</span></span>

### <span data-ttu-id="83857-131">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="83857-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="83857-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83857-132">NOTES</span></span>
<span data-ttu-id="83857-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="83857-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="83857-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83857-134">RELATED LINKS</span></span>
