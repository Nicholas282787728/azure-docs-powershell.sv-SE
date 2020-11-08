---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259393"
---
# <span data-ttu-id="40bd8-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="40bd8-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="40bd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="40bd8-103">Tar bort en webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="40bd8-103">Deletes a web service.</span></span>

## <span data-ttu-id="40bd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40bd8-104">SYNTAX</span></span>

### <span data-ttu-id="40bd8-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40bd8-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40bd8-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="40bd8-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40bd8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40bd8-107">DESCRIPTION</span></span>
<span data-ttu-id="40bd8-108">Tar bort en Azure Machine Learning-webbtjänst som refereras av resurs grupp och-namn.</span><span class="sxs-lookup"><span data-stu-id="40bd8-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="40bd8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40bd8-109">EXAMPLES</span></span>

### <span data-ttu-id="40bd8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="40bd8-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="40bd8-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40bd8-111">PARAMETERS</span></span>

### <span data-ttu-id="40bd8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bd8-112">-DefaultProfile</span></span>
<span data-ttu-id="40bd8-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="40bd8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40bd8-114">-Force</span><span class="sxs-lookup"><span data-stu-id="40bd8-114">-Force</span></span>
<span data-ttu-id="40bd8-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="40bd8-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="40bd8-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="40bd8-116">-MlWebService</span></span>
<span data-ttu-id="40bd8-117">Webb tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="40bd8-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40bd8-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="40bd8-118">-Name</span></span>
<span data-ttu-id="40bd8-119">Namnet på webb tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="40bd8-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40bd8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bd8-120">-ResourceGroupName</span></span>
<span data-ttu-id="40bd8-121">Webb tjänstens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="40bd8-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40bd8-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40bd8-122">-Confirm</span></span>
<span data-ttu-id="40bd8-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40bd8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bd8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bd8-124">-WhatIf</span></span>
<span data-ttu-id="40bd8-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40bd8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bd8-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40bd8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bd8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bd8-127">CommonParameters</span></span>
<span data-ttu-id="40bd8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bd8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bd8-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40bd8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bd8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40bd8-130">INPUTS</span></span>

### <span data-ttu-id="40bd8-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="40bd8-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="40bd8-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40bd8-132">OUTPUTS</span></span>

### <span data-ttu-id="40bd8-133">System. Void</span><span class="sxs-lookup"><span data-stu-id="40bd8-133">System.Void</span></span>

## <span data-ttu-id="40bd8-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40bd8-134">NOTES</span></span>
<span data-ttu-id="40bd8-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="40bd8-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="40bd8-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40bd8-136">RELATED LINKS</span></span>
