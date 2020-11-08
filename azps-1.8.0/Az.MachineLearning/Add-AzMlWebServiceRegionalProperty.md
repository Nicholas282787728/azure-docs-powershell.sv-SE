---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: 877ef93dbecf3510887a24cb0b5dfe65948658f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915921"
---
# <span data-ttu-id="2e656-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="2e656-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="2e656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e656-102">SYNOPSIS</span></span>
<span data-ttu-id="2e656-103">Skapar egenskaper för webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2e656-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="2e656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e656-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e656-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e656-105">DESCRIPTION</span></span>
<span data-ttu-id="2e656-106">Skapar nationella egenskaper för Azure Machine Learning för en befintlig webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="2e656-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="2e656-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e656-107">EXAMPLES</span></span>

### <span data-ttu-id="2e656-108">Exempel 1: lägga till nya nationella egenskaper för västra centrala USA</span><span class="sxs-lookup"><span data-stu-id="2e656-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="2e656-109">I det här exemplet kommando skapas en regional egenskap för en webb tjänst i regionen "Västra Central USA".</span><span class="sxs-lookup"><span data-stu-id="2e656-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="2e656-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e656-110">PARAMETERS</span></span>

### <span data-ttu-id="2e656-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e656-111">-DefaultProfile</span></span>
<span data-ttu-id="2e656-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2e656-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e656-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2e656-113">-Force</span></span>
<span data-ttu-id="2e656-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2e656-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e656-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e656-115">-Name</span></span>
<span data-ttu-id="2e656-116">Namnet på webb tjänsten.</span><span class="sxs-lookup"><span data-stu-id="2e656-116">The name for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e656-117">-Region</span><span class="sxs-lookup"><span data-stu-id="2e656-117">-Region</span></span>
<span data-ttu-id="2e656-118">Den region där du vill skapa webb tjänstens egenskaper.</span><span class="sxs-lookup"><span data-stu-id="2e656-118">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="2e656-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e656-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e656-120">Resurs gruppen som webb tjänsten tillhör.</span><span class="sxs-lookup"><span data-stu-id="2e656-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e656-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e656-121">-Confirm</span></span>
<span data-ttu-id="2e656-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e656-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e656-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e656-123">-WhatIf</span></span>
<span data-ttu-id="2e656-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e656-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e656-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e656-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e656-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e656-126">CommonParameters</span></span>
<span data-ttu-id="2e656-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e656-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e656-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e656-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e656-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e656-129">INPUTS</span></span>

### <span data-ttu-id="2e656-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2e656-130">System.String</span></span>

## <span data-ttu-id="2e656-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e656-131">OUTPUTS</span></span>

### <span data-ttu-id="2e656-132">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="2e656-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2e656-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e656-133">NOTES</span></span>
<span data-ttu-id="2e656-134">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="2e656-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2e656-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e656-135">RELATED LINKS</span></span>