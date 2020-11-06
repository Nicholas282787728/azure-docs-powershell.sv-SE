---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584319"
---
# <span data-ttu-id="94032-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="94032-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="94032-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94032-102">SYNOPSIS</span></span>
<span data-ttu-id="94032-103">Hämtar den sammanfattande informationen för en eller flera åtagande associationer.</span><span class="sxs-lookup"><span data-stu-id="94032-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94032-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94032-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94032-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94032-105">DESCRIPTION</span></span>
<span data-ttu-id="94032-106">Hämtar information om åtagande associationer.</span><span class="sxs-lookup"><span data-stu-id="94032-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="94032-107">Beroende på vilken paramenters som skickas returnerar cmdleten en specifik åtagande Association eller en samling åtagande organisationer för den angivna åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="94032-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="94032-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94032-108">EXAMPLES</span></span>

### <span data-ttu-id="94032-109">--------------------------Exempel 1: skaffa en specifik åtagande Association--------------------------</span><span class="sxs-lookup"><span data-stu-id="94032-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="94032-110">--------------------------Exempel 2: skaffa alla åtagande associationer för den angivna åtagande planen--------------------------</span><span class="sxs-lookup"><span data-stu-id="94032-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="94032-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94032-111">PARAMETERS</span></span>

### <span data-ttu-id="94032-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="94032-112">-CommitmentPlanName</span></span>
<span data-ttu-id="94032-113">Namnet på den plan för Azure ML-åtagande som har en eller flera åtagande associationer.</span><span class="sxs-lookup"><span data-stu-id="94032-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="94032-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94032-114">-DefaultProfile</span></span>
<span data-ttu-id="94032-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="94032-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94032-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="94032-116">-Name</span></span>
<span data-ttu-id="94032-117">Namnet på Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="94032-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94032-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94032-118">-ResourceGroupName</span></span>
<span data-ttu-id="94032-119">Namnet på resurs gruppen för en Azure ML-associering.</span><span class="sxs-lookup"><span data-stu-id="94032-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="94032-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94032-120">CommonParameters</span></span>
<span data-ttu-id="94032-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94032-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94032-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94032-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94032-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94032-123">INPUTS</span></span>

### <span data-ttu-id="94032-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="94032-124">None</span></span>
<span data-ttu-id="94032-125">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="94032-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="94032-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94032-126">OUTPUTS</span></span>

### <span data-ttu-id="94032-127">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="94032-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="94032-128">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="94032-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="94032-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94032-129">NOTES</span></span>
<span data-ttu-id="94032-130">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="94032-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="94032-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94032-131">RELATED LINKS</span></span>

