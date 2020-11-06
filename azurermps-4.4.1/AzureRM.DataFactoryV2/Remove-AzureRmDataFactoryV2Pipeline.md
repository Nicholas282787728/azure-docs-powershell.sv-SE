---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586567"
---
# <span data-ttu-id="37137-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="37137-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="37137-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37137-102">SYNOPSIS</span></span>
<span data-ttu-id="37137-103">Tar bort en rörledning från data fabriken.</span><span class="sxs-lookup"><span data-stu-id="37137-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37137-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37137-104">SYNTAX</span></span>

### <span data-ttu-id="37137-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="37137-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="37137-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="37137-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="37137-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="37137-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="37137-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37137-108">DESCRIPTION</span></span>
<span data-ttu-id="37137-109">Remove-AzureRmDataFactoryV2Pipeline cmdlet tar bort en pipeline från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="37137-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="37137-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37137-110">EXAMPLES</span></span>

### <span data-ttu-id="37137-111">Exempel 1: ta bort en rörledning</span><span class="sxs-lookup"><span data-stu-id="37137-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="37137-112">Denna cmdlet tar bort pipelinen med namnet DPWikisample från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="37137-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="37137-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="37137-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="37137-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37137-114">PARAMETERS</span></span>

### <span data-ttu-id="37137-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="37137-115">-Confirm</span></span>
<span data-ttu-id="37137-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37137-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37137-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="37137-117">-DataFactoryName</span></span>
<span data-ttu-id="37137-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="37137-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="37137-119">Denna cmdlet tar bort en pipeline från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="37137-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37137-120">-Force</span><span class="sxs-lookup"><span data-stu-id="37137-120">-Force</span></span>
<span data-ttu-id="37137-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="37137-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="37137-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="37137-122">-Name</span></span>
<span data-ttu-id="37137-123">Anger namnet på den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="37137-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37137-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37137-124">-InputObject</span></span>
<span data-ttu-id="37137-125">Anger ett pipeline-objekt.</span><span class="sxs-lookup"><span data-stu-id="37137-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="37137-126">Denna cmdlet tar bort pipeline som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="37137-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37137-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37137-127">-ResourceGroupName</span></span>
<span data-ttu-id="37137-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="37137-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="37137-129">Denna cmdlet tar bort en pipeline från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="37137-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37137-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37137-130">-ResourceId</span></span>
<span data-ttu-id="37137-131">Azure Resource ID för den pipeline som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="37137-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37137-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37137-132">-WhatIf</span></span>
<span data-ttu-id="37137-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="37137-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="37137-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37137-134">INPUTS</span></span>

### <span data-ttu-id="37137-135">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="37137-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="37137-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37137-136">System.String</span></span>


## <span data-ttu-id="37137-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37137-137">OUTPUTS</span></span>

### <span data-ttu-id="37137-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="37137-138">System.Object</span></span>

## <span data-ttu-id="37137-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37137-139">NOTES</span></span>
<span data-ttu-id="37137-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="37137-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="37137-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37137-141">RELATED LINKS</span></span>
[<span data-ttu-id="37137-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="37137-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="37137-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="37137-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="37137-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="37137-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

