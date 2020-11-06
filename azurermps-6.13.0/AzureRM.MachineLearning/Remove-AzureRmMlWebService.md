---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577944"
---
# <span data-ttu-id="e60b4-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="e60b4-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="e60b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e60b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e60b4-103">Tar bort en webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="e60b4-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e60b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e60b4-104">SYNTAX</span></span>

### <span data-ttu-id="e60b4-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e60b4-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e60b4-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="e60b4-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e60b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e60b4-107">DESCRIPTION</span></span>
<span data-ttu-id="e60b4-108">Tar bort en Azure Machine Learning-webbtjänst som refereras av resurs grupp och-namn.</span><span class="sxs-lookup"><span data-stu-id="e60b4-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="e60b4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e60b4-109">EXAMPLES</span></span>

### <span data-ttu-id="e60b4-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e60b4-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="e60b4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e60b4-111">PARAMETERS</span></span>

### <span data-ttu-id="e60b4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60b4-112">-DefaultProfile</span></span>
<span data-ttu-id="e60b4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e60b4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e60b4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e60b4-114">-Force</span></span>
<span data-ttu-id="e60b4-115">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e60b4-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e60b4-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="e60b4-116">-MlWebService</span></span>
<span data-ttu-id="e60b4-117">Webb tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e60b4-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="e60b4-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e60b4-118">-Name</span></span>
<span data-ttu-id="e60b4-119">Namnet på webb tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="e60b4-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="e60b4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e60b4-120">-ResourceGroupName</span></span>
<span data-ttu-id="e60b4-121">Webb tjänstens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e60b4-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="e60b4-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e60b4-122">-Confirm</span></span>
<span data-ttu-id="e60b4-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e60b4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e60b4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e60b4-124">-WhatIf</span></span>
<span data-ttu-id="e60b4-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e60b4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e60b4-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e60b4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e60b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60b4-127">CommonParameters</span></span>
<span data-ttu-id="e60b4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60b4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60b4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60b4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e60b4-130">INPUTS</span></span>

### <span data-ttu-id="e60b4-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="e60b4-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="e60b4-132">Parametrar: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e60b4-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="e60b4-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e60b4-133">OUTPUTS</span></span>

### <span data-ttu-id="e60b4-134">System. Void</span><span class="sxs-lookup"><span data-stu-id="e60b4-134">System.Void</span></span>

## <span data-ttu-id="e60b4-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e60b4-135">NOTES</span></span>
<span data-ttu-id="e60b4-136">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="e60b4-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e60b4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e60b4-137">RELATED LINKS</span></span>
