---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585956"
---
# <span data-ttu-id="c45b8-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="c45b8-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="c45b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c45b8-102">SYNOPSIS</span></span>
<span data-ttu-id="c45b8-103">Hämtar information om användnings historik för en viss åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="c45b8-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c45b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c45b8-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c45b8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c45b8-105">DESCRIPTION</span></span>
<span data-ttu-id="c45b8-106">Hämtar information om användnings historik för en viss åtagande plan, inklusive resurser som används och resurser som finns kvar i planen.</span><span class="sxs-lookup"><span data-stu-id="c45b8-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="c45b8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c45b8-107">EXAMPLES</span></span>

### <span data-ttu-id="c45b8-108">Exempel 1: Hämta användnings historik för en viss åtagande plan</span><span class="sxs-lookup"><span data-stu-id="c45b8-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="c45b8-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c45b8-109">PARAMETERS</span></span>

### <span data-ttu-id="c45b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c45b8-110">-DefaultProfile</span></span>
<span data-ttu-id="c45b8-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c45b8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c45b8-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="c45b8-112">-Name</span></span>
<span data-ttu-id="c45b8-113">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="c45b8-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c45b8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c45b8-114">-ResourceGroupName</span></span>
<span data-ttu-id="c45b8-115">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="c45b8-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c45b8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c45b8-116">CommonParameters</span></span>
<span data-ttu-id="c45b8-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c45b8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c45b8-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c45b8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c45b8-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c45b8-119">INPUTS</span></span>

### <span data-ttu-id="c45b8-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="c45b8-120">None</span></span>

## <span data-ttu-id="c45b8-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c45b8-121">OUTPUTS</span></span>

### <span data-ttu-id="c45b8-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="c45b8-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="c45b8-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c45b8-123">NOTES</span></span>
<span data-ttu-id="c45b8-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="c45b8-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c45b8-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c45b8-125">RELATED LINKS</span></span>
