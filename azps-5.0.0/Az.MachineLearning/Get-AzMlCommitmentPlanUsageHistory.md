---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 5b628ffa1392b4ebfed5b5643539f0a9fa541cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273342"
---
# <span data-ttu-id="aedad-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="aedad-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="aedad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aedad-102">SYNOPSIS</span></span>
<span data-ttu-id="aedad-103">Hämtar information om användnings historik för en viss åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="aedad-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="aedad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aedad-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aedad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aedad-105">DESCRIPTION</span></span>
<span data-ttu-id="aedad-106">Hämtar information om användnings historik för en viss åtagande plan, inklusive resurser som används och resurser som finns kvar i planen.</span><span class="sxs-lookup"><span data-stu-id="aedad-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="aedad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aedad-107">EXAMPLES</span></span>

### <span data-ttu-id="aedad-108">Exempel 1: Hämta användnings historik för en viss åtagande plan</span><span class="sxs-lookup"><span data-stu-id="aedad-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="aedad-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aedad-109">PARAMETERS</span></span>

### <span data-ttu-id="aedad-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aedad-110">-DefaultProfile</span></span>
<span data-ttu-id="aedad-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aedad-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aedad-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="aedad-112">-Name</span></span>
<span data-ttu-id="aedad-113">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="aedad-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="aedad-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aedad-114">-ResourceGroupName</span></span>
<span data-ttu-id="aedad-115">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="aedad-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="aedad-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aedad-116">CommonParameters</span></span>
<span data-ttu-id="aedad-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aedad-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aedad-118">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aedad-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aedad-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aedad-119">INPUTS</span></span>

### <span data-ttu-id="aedad-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="aedad-120">None</span></span>

## <span data-ttu-id="aedad-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aedad-121">OUTPUTS</span></span>

### <span data-ttu-id="aedad-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="aedad-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="aedad-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aedad-123">NOTES</span></span>
<span data-ttu-id="aedad-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="aedad-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="aedad-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aedad-125">RELATED LINKS</span></span>
