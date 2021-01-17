---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400179"
---
# <span data-ttu-id="60f10-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="60f10-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="60f10-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="60f10-102">SYNOPSIS</span></span>
<span data-ttu-id="60f10-103">Hämtar den sammanfattande informationen för en eller flera åtagande associationer.</span><span class="sxs-lookup"><span data-stu-id="60f10-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="60f10-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="60f10-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60f10-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="60f10-105">DESCRIPTION</span></span>
<span data-ttu-id="60f10-106">Hämtar information om åtagande associationer.</span><span class="sxs-lookup"><span data-stu-id="60f10-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="60f10-107">Beroende på vilka parametrar som skickas returnerar cmdleten en specifik åtagande Association eller en samling åtagande organisationer för den angivna åtagande planen.</span><span class="sxs-lookup"><span data-stu-id="60f10-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="60f10-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="60f10-108">EXAMPLES</span></span>

### <span data-ttu-id="60f10-109">Exempel 1: skaffa en specifik åtagande Association</span><span class="sxs-lookup"><span data-stu-id="60f10-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="60f10-110">Exempel 2: få alla åtagande associationer för den angivna åtagande planen</span><span class="sxs-lookup"><span data-stu-id="60f10-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="60f10-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="60f10-111">PARAMETERS</span></span>

### <span data-ttu-id="60f10-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="60f10-112">-CommitmentPlanName</span></span>
<span data-ttu-id="60f10-113">Namnet på den plan för Azure ML-åtagande som har en eller flera åtagande associationer.</span><span class="sxs-lookup"><span data-stu-id="60f10-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="60f10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f10-114">-DefaultProfile</span></span>
<span data-ttu-id="60f10-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="60f10-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60f10-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="60f10-116">-Name</span></span>
<span data-ttu-id="60f10-117">Namnet på Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="60f10-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="60f10-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60f10-118">-ResourceGroupName</span></span>
<span data-ttu-id="60f10-119">Namnet på resurs gruppen för en Azure ML-associering.</span><span class="sxs-lookup"><span data-stu-id="60f10-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="60f10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f10-120">CommonParameters</span></span>
<span data-ttu-id="60f10-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60f10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f10-122">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60f10-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f10-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="60f10-123">INPUTS</span></span>

### <span data-ttu-id="60f10-124">Ingen</span><span class="sxs-lookup"><span data-stu-id="60f10-124">None</span></span>

## <span data-ttu-id="60f10-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="60f10-125">OUTPUTS</span></span>

### <span data-ttu-id="60f10-126">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="60f10-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="60f10-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="60f10-127">NOTES</span></span>
<span data-ttu-id="60f10-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="60f10-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="60f10-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="60f10-129">RELATED LINKS</span></span>
