---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/new-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/New-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 1c3c7d0dce441ecc6048e9ab98d56bf79b90020e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758221"
---
# <span data-ttu-id="623a0-101">New-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="623a0-101">New-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="623a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="623a0-102">SYNOPSIS</span></span>
<span data-ttu-id="623a0-103">Skapar en ny åtagande plan.</span><span class="sxs-lookup"><span data-stu-id="623a0-103">Creates a new commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="623a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="623a0-104">SYNTAX</span></span>

```
New-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="623a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="623a0-105">DESCRIPTION</span></span>
<span data-ttu-id="623a0-106">Skapar en plan för en Azure Machine-utbildningskurs i en befintlig resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="623a0-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="623a0-107">Om det finns en åtagande plan med samma namn i resurs gruppen, fungerar samtalet som en uppdatering och den befintliga åtagande planen skrivs över.</span><span class="sxs-lookup"><span data-stu-id="623a0-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="623a0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="623a0-108">EXAMPLES</span></span>

### <span data-ttu-id="623a0-109">--------------------------Exempel 1: skapa en ny åtagande plan--------------------------</span><span class="sxs-lookup"><span data-stu-id="623a0-109">--------------------------  Example 1: Create a new commitment plan  --------------------------</span></span>
```
New-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="623a0-110">Skapar en ny Azure Machine-plan för studie åtagande med namnet "MyCommitmentPlanName" i gruppen "MyResourceGroup" och i södra Central amerikanska region.</span><span class="sxs-lookup"><span data-stu-id="623a0-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="623a0-111">I det här exemplet används SKU-DevTest/standard, vilket innebär att resurserna som tillhandahålls av åtagande planen kommer att definied genom att begränsa DevTest/standarden.</span><span class="sxs-lookup"><span data-stu-id="623a0-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be definied by the limits of DevTest/Standard.</span></span> <span data-ttu-id="623a0-112">SkuCapacity i det här exemplet är 1, vilket innebär att kostnaden för abonnemanget är DevTest, och att resurserna i planen innehåller är 1x-vilka DevTest erbjuder.</span><span class="sxs-lookup"><span data-stu-id="623a0-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="623a0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="623a0-113">PARAMETERS</span></span>

### <span data-ttu-id="623a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623a0-114">-DefaultProfile</span></span>
<span data-ttu-id="623a0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="623a0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="623a0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="623a0-116">-Force</span></span>
<span data-ttu-id="623a0-117">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="623a0-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623a0-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="623a0-118">-Location</span></span>
<span data-ttu-id="623a0-119">Platsen för abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="623a0-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="623a0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="623a0-120">-Name</span></span>
<span data-ttu-id="623a0-121">Namnet på abonnemanget för Azure ML-åtagandet.</span><span class="sxs-lookup"><span data-stu-id="623a0-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="623a0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623a0-122">-ResourceGroupName</span></span>
<span data-ttu-id="623a0-123">Namnet på resurs gruppen för abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="623a0-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="623a0-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="623a0-124">-SkuCapacity</span></span>
<span data-ttu-id="623a0-125">Kapaciteten för SKU: n som ska användas vid etablering av abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="623a0-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623a0-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="623a0-126">-SkuName</span></span>
<span data-ttu-id="623a0-127">Namnet på den SKU som ska användas vid etablering av abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="623a0-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="623a0-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="623a0-128">-SkuTier</span></span>
<span data-ttu-id="623a0-129">Nivån på den SKU som ska användas vid etablering av abonnemanget för Azure ML-åtagande.</span><span class="sxs-lookup"><span data-stu-id="623a0-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="623a0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="623a0-130">-Confirm</span></span>
<span data-ttu-id="623a0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="623a0-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623a0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="623a0-132">-WhatIf</span></span>
<span data-ttu-id="623a0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="623a0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="623a0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="623a0-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="623a0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623a0-135">CommonParameters</span></span>
<span data-ttu-id="623a0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623a0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623a0-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="623a0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623a0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="623a0-138">INPUTS</span></span>

### <span data-ttu-id="623a0-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="623a0-139">None</span></span>
<span data-ttu-id="623a0-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="623a0-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="623a0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="623a0-141">OUTPUTS</span></span>

### <span data-ttu-id="623a0-142">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="623a0-142">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="623a0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="623a0-143">NOTES</span></span>
<span data-ttu-id="623a0-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="623a0-144">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="623a0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="623a0-145">RELATED LINKS</span></span>

