---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93758439"
---
# <span data-ttu-id="b2393-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="b2393-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="b2393-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2393-102">SYNOPSIS</span></span>
<span data-ttu-id="b2393-103">Hämtar information om användnings historik för en viss åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="b2393-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2393-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2393-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2393-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2393-105">DESCRIPTION</span></span>
<span data-ttu-id="b2393-106">Hämtar information om användnings historik för en viss åtagande plan, inklusive resurser som används och resurser som finns kvar i planen.</span><span class="sxs-lookup"><span data-stu-id="b2393-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="b2393-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2393-107">EXAMPLES</span></span>

### <span data-ttu-id="b2393-108">--------------------------Exempel 1: Hämta användnings historik för en specifik åtagandes plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="b2393-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="b2393-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2393-109">PARAMETERS</span></span>

### <span data-ttu-id="b2393-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2393-110">-DefaultProfile</span></span>
<span data-ttu-id="b2393-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b2393-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2393-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2393-112">-Name</span></span>
<span data-ttu-id="b2393-113">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="b2393-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b2393-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2393-114">-ResourceGroupName</span></span>
<span data-ttu-id="b2393-115">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="b2393-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="b2393-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2393-116">CommonParameters</span></span>
<span data-ttu-id="b2393-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2393-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2393-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2393-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2393-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2393-119">INPUTS</span></span>

### <span data-ttu-id="b2393-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="b2393-120">None</span></span>
<span data-ttu-id="b2393-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b2393-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2393-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2393-122">OUTPUTS</span></span>

### <span data-ttu-id="b2393-123">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="b2393-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="b2393-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2393-124">NOTES</span></span>
<span data-ttu-id="b2393-125">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="b2393-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b2393-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2393-126">RELATED LINKS</span></span>

