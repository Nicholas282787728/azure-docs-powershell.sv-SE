---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755946"
---
# <span data-ttu-id="57653-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="57653-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="57653-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57653-102">SYNOPSIS</span></span>
<span data-ttu-id="57653-103">Hämtar den sammanfattande informationen för ett eller flera utfästelser.</span><span class="sxs-lookup"><span data-stu-id="57653-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57653-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57653-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57653-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57653-105">DESCRIPTION</span></span>
<span data-ttu-id="57653-106">Hämtar information om åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="57653-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="57653-107">Beroende på vilken paramenters som skickas returnerar cmdleten ett specifikt åtagande, en samling av åtagande planer för en viss resurs grupp inom det aktuella abonnemanget, eller en samling av åtagande planer inom det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="57653-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="57653-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57653-108">EXAMPLES</span></span>

### <span data-ttu-id="57653-109">Exempel 1: skaffa en särskild åtagande plan</span><span class="sxs-lookup"><span data-stu-id="57653-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="57653-110">Exempel 2: Hämta alla åtagande Plans resurser i aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="57653-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="57653-111">Exempel 3: samla alla utfästelser i det aktuella abonnemanget och resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="57653-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="57653-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57653-112">PARAMETERS</span></span>

### <span data-ttu-id="57653-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57653-113">-DefaultProfile</span></span>
<span data-ttu-id="57653-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="57653-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57653-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="57653-115">-Name</span></span>
<span data-ttu-id="57653-116">Namnet på åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="57653-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="57653-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57653-117">-ResourceGroupName</span></span>
<span data-ttu-id="57653-118">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="57653-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="57653-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57653-119">CommonParameters</span></span>
<span data-ttu-id="57653-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57653-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57653-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57653-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57653-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57653-122">INPUTS</span></span>

### <span data-ttu-id="57653-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="57653-123">None</span></span>

## <span data-ttu-id="57653-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57653-124">OUTPUTS</span></span>

### <span data-ttu-id="57653-125">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="57653-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="57653-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57653-126">NOTES</span></span>
<span data-ttu-id="57653-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="57653-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="57653-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57653-128">RELATED LINKS</span></span>
