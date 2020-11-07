---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758055"
---
# <span data-ttu-id="cfe11-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="cfe11-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="cfe11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfe11-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe11-103">Hämtar information om användnings historik för en viss åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="cfe11-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfe11-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfe11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfe11-105">DESCRIPTION</span></span>
<span data-ttu-id="cfe11-106">Hämtar information om användnings historik för en viss åtagande plan, inklusive resurser som används och resurser som finns kvar i planen.</span><span class="sxs-lookup"><span data-stu-id="cfe11-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="cfe11-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfe11-107">EXAMPLES</span></span>

### <span data-ttu-id="cfe11-108">--------------------------Exempel 1: Hämta användnings historik för en specifik åtagandes plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="cfe11-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="cfe11-109">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="cfe11-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="cfe11-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfe11-110">PARAMETERS</span></span>

### <span data-ttu-id="cfe11-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfe11-111">-Name</span></span>
<span data-ttu-id="cfe11-112">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="cfe11-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="cfe11-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe11-113">-ResourceGroupName</span></span>
<span data-ttu-id="cfe11-114">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="cfe11-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="cfe11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe11-115">-DefaultProfile</span></span>
<span data-ttu-id="cfe11-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe11-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe11-117">CommonParameters</span></span>
<span data-ttu-id="cfe11-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe11-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe11-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe11-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe11-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfe11-120">INPUTS</span></span>

## <span data-ttu-id="cfe11-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfe11-121">OUTPUTS</span></span>

### <span data-ttu-id="cfe11-122">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="cfe11-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="cfe11-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfe11-123">NOTES</span></span>
<span data-ttu-id="cfe11-124">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="cfe11-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="cfe11-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfe11-125">RELATED LINKS</span></span>

