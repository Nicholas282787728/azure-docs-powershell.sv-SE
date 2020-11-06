---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b2f881b57639a83227c2f590ffd260b78509a54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584323"
---
# <span data-ttu-id="c685e-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="c685e-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="c685e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c685e-102">SYNOPSIS</span></span>
<span data-ttu-id="c685e-103">Skapar egenskaper för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c685e-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c685e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c685e-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c685e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c685e-105">DESCRIPTION</span></span>
<span data-ttu-id="c685e-106">Skapar nationella egenskaper för Azure Machine Learning för en befintlig webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="c685e-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="c685e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c685e-107">EXAMPLES</span></span>

### <span data-ttu-id="c685e-108">--------------------------Exempel 1: lägga till nya nationella egenskaper för västra centrala USA--------------------------</span><span class="sxs-lookup"><span data-stu-id="c685e-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="c685e-109">I det här exemplet kommando skapas en regional egenskap för en webb tjänst i regionen "Västra Central USA".</span><span class="sxs-lookup"><span data-stu-id="c685e-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="c685e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c685e-110">PARAMETERS</span></span>

### <span data-ttu-id="c685e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c685e-111">-DefaultProfile</span></span>
<span data-ttu-id="c685e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c685e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c685e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c685e-113">-Force</span></span>
<span data-ttu-id="c685e-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c685e-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c685e-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c685e-115">-Name</span></span>
<span data-ttu-id="c685e-116">Namnet på webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c685e-116">The name for the web service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c685e-117">-Region</span><span class="sxs-lookup"><span data-stu-id="c685e-117">-Region</span></span>
<span data-ttu-id="c685e-118">Den region där du vill skapa webb tjänstens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="c685e-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="c685e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c685e-119">-ResourceGroupName</span></span>
<span data-ttu-id="c685e-120">Resurs gruppen som webb tjänsten tillhör.</span><span class="sxs-lookup"><span data-stu-id="c685e-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c685e-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c685e-121">-Confirm</span></span>
<span data-ttu-id="c685e-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c685e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c685e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c685e-123">-WhatIf</span></span>
<span data-ttu-id="c685e-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c685e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c685e-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c685e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c685e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c685e-126">CommonParameters</span></span>
<span data-ttu-id="c685e-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c685e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c685e-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c685e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c685e-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c685e-129">INPUTS</span></span>

### <span data-ttu-id="c685e-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="c685e-130">None</span></span>
<span data-ttu-id="c685e-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="c685e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c685e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c685e-132">OUTPUTS</span></span>

### <span data-ttu-id="c685e-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="c685e-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="c685e-134">En sammanfattning av Azure Machine Learning web service.</span><span class="sxs-lookup"><span data-stu-id="c685e-134">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="c685e-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c685e-135">NOTES</span></span>
<span data-ttu-id="c685e-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="c685e-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c685e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c685e-137">RELATED LINKS</span></span>

