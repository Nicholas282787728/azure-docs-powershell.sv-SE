---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580584"
---
# <span data-ttu-id="6cfea-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="6cfea-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="6cfea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cfea-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfea-103">Tar bort en webb tjänst.</span><span class="sxs-lookup"><span data-stu-id="6cfea-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cfea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cfea-104">SYNTAX</span></span>

### <span data-ttu-id="6cfea-105">Ta bort en Azure ML-webbtjänst genom namn och resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6cfea-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cfea-106">Ta bort en Azure ML-webb tjänst som angetts som ett objekt.</span><span class="sxs-lookup"><span data-stu-id="6cfea-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cfea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cfea-107">DESCRIPTION</span></span>
<span data-ttu-id="6cfea-108">Tar bort en Azure Machine Learning-webbtjänst som refereras av resurs grupp och-namn.</span><span class="sxs-lookup"><span data-stu-id="6cfea-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="6cfea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cfea-109">EXAMPLES</span></span>

### <span data-ttu-id="6cfea-110">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6cfea-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="6cfea-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="6cfea-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="6cfea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cfea-112">PARAMETERS</span></span>

### <span data-ttu-id="6cfea-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6cfea-113">-Force</span></span>
<span data-ttu-id="6cfea-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6cfea-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6cfea-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="6cfea-115">-MlWebService</span></span>
<span data-ttu-id="6cfea-116">Webb tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6cfea-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfea-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cfea-117">-Name</span></span>
<span data-ttu-id="6cfea-118">Namnet på webb tjänsten som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="6cfea-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfea-119">-ResourceGroupName</span></span>
<span data-ttu-id="6cfea-120">Webb tjänstens resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6cfea-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cfea-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cfea-121">-Confirm</span></span>
<span data-ttu-id="6cfea-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cfea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cfea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cfea-123">-WhatIf</span></span>
<span data-ttu-id="6cfea-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cfea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cfea-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cfea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cfea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfea-126">-DefaultProfile</span></span>
<span data-ttu-id="6cfea-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cfea-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cfea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfea-128">CommonParameters</span></span>
<span data-ttu-id="6cfea-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfea-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cfea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfea-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cfea-131">INPUTS</span></span>

### <span data-ttu-id="6cfea-132">Webb tjänst</span><span class="sxs-lookup"><span data-stu-id="6cfea-132">WebService</span></span>
<span data-ttu-id="6cfea-133">Parametern ' MlWebService ' godkänner värdet för typen "WebService" från pipeline</span><span class="sxs-lookup"><span data-stu-id="6cfea-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="6cfea-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cfea-134">OUTPUTS</span></span>

### <span data-ttu-id="6cfea-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="6cfea-135">None</span></span>

## <span data-ttu-id="6cfea-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cfea-136">NOTES</span></span>
<span data-ttu-id="6cfea-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="6cfea-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6cfea-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cfea-138">RELATED LINKS</span></span>

