---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580588"
---
# <span data-ttu-id="daaa3-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="daaa3-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="daaa3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="daaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="daaa3-103">Hämtar den sammanfattande informationen för ett eller flera utfästelser.</span><span class="sxs-lookup"><span data-stu-id="daaa3-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daaa3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="daaa3-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daaa3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="daaa3-105">DESCRIPTION</span></span>
<span data-ttu-id="daaa3-106">Hämtar information om åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="daaa3-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="daaa3-107">Beroende på vilken paramenters som skickas returnerar cmdleten ett specifikt åtagande, en samling av åtagande planer för en viss resurs grupp inom det aktuella abonnemanget, eller en samling av åtagande planer inom det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="daaa3-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="daaa3-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="daaa3-108">EXAMPLES</span></span>

### <span data-ttu-id="daaa3-109">--------------------------Exempel 1: skaffa en särskild åtagande plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="daaa3-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="daaa3-110">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="daaa3-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="daaa3-111">--------------------------Exempel 2: Hämta alla åtagande Plans resurser i aktuell prenumeration--------------------------</span><span class="sxs-lookup"><span data-stu-id="daaa3-111">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
<span data-ttu-id="daaa3-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="daaa3-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="daaa3-113">--------------------------Exempel 3: få alla åtagande planer i det aktuella abonnemanget och den angivna resurs gruppen--------------------------</span><span class="sxs-lookup"><span data-stu-id="daaa3-113">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="daaa3-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="daaa3-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="daaa3-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="daaa3-115">PARAMETERS</span></span>

### <span data-ttu-id="daaa3-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="daaa3-116">-Name</span></span>
<span data-ttu-id="daaa3-117">Namnet på åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="daaa3-117">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="daaa3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daaa3-118">-ResourceGroupName</span></span>
<span data-ttu-id="daaa3-119">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="daaa3-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="daaa3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daaa3-120">-DefaultProfile</span></span>
<span data-ttu-id="daaa3-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="daaa3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daaa3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daaa3-122">CommonParameters</span></span>
<span data-ttu-id="daaa3-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daaa3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daaa3-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daaa3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daaa3-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="daaa3-125">INPUTS</span></span>

## <span data-ttu-id="daaa3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="daaa3-126">OUTPUTS</span></span>

### <span data-ttu-id="daaa3-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="daaa3-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="daaa3-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="daaa3-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="daaa3-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="daaa3-129">NOTES</span></span>
<span data-ttu-id="daaa3-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="daaa3-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="daaa3-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="daaa3-131">RELATED LINKS</span></span>

