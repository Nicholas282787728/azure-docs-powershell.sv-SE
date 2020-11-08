---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 0b66c75c3230754656b14e15eda66a4fb2912c4d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915910"
---
# <span data-ttu-id="be7cf-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="be7cf-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="be7cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="be7cf-103">Hämtar den sammanfattande informationen för ett eller flera utfästelser.</span><span class="sxs-lookup"><span data-stu-id="be7cf-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="be7cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be7cf-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be7cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be7cf-105">DESCRIPTION</span></span>
<span data-ttu-id="be7cf-106">Hämtar information om åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="be7cf-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="be7cf-107">Beroende på vilken paramenters som skickas returnerar cmdleten ett specifikt åtagande, en samling av åtagande planer för en viss resurs grupp inom det aktuella abonnemanget, eller en samling av åtagande planer inom det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="be7cf-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="be7cf-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be7cf-108">EXAMPLES</span></span>

### <span data-ttu-id="be7cf-109">Exempel 1: skaffa en särskild åtagande plan</span><span class="sxs-lookup"><span data-stu-id="be7cf-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="be7cf-110">Exempel 2: Hämta alla åtagande Plans resurser i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="be7cf-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="be7cf-111">Exempel 3: samla alla utfästelser i det aktuella abonnemanget och resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="be7cf-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="be7cf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be7cf-112">PARAMETERS</span></span>

### <span data-ttu-id="be7cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7cf-113">-DefaultProfile</span></span>
<span data-ttu-id="be7cf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="be7cf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be7cf-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="be7cf-115">-Name</span></span>
<span data-ttu-id="be7cf-116">Namnet på åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="be7cf-116">The name of the commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="be7cf-118">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="be7cf-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be7cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7cf-119">CommonParameters</span></span>
<span data-ttu-id="be7cf-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be7cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7cf-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be7cf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7cf-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be7cf-122">INPUTS</span></span>

### <span data-ttu-id="be7cf-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="be7cf-123">None</span></span>

## <span data-ttu-id="be7cf-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be7cf-124">OUTPUTS</span></span>

### <span data-ttu-id="be7cf-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="be7cf-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="be7cf-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be7cf-126">NOTES</span></span>
<span data-ttu-id="be7cf-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="be7cf-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="be7cf-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be7cf-128">RELATED LINKS</span></span>