---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583331"
---
# <span data-ttu-id="a2adf-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a2adf-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="a2adf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2adf-102">SYNOPSIS</span></span>
<span data-ttu-id="a2adf-103">Tar bort en data uppsättning från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a2adf-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2adf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2adf-104">SYNTAX</span></span>

### <span data-ttu-id="a2adf-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="a2adf-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2adf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2adf-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a2adf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2adf-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a2adf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2adf-108">DESCRIPTION</span></span>
<span data-ttu-id="a2adf-109">Remove-AzureRmDataFactoryV2Dataset cmdlet tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a2adf-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="a2adf-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2adf-110">EXAMPLES</span></span>

### <span data-ttu-id="a2adf-111">Exempel 1: ta bort en data uppsättning</span><span class="sxs-lookup"><span data-stu-id="a2adf-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="a2adf-112">Det här kommandot tar bort den dataset som heter DAWikiAggregatedData från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a2adf-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="a2adf-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="a2adf-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="a2adf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2adf-114">PARAMETERS</span></span>

### <span data-ttu-id="a2adf-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2adf-115">-Confirm</span></span>
<span data-ttu-id="a2adf-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2adf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2adf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a2adf-117">-DataFactoryName</span></span>
<span data-ttu-id="a2adf-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a2adf-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a2adf-119">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a2adf-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2adf-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2adf-120">-InputObject</span></span>
<span data-ttu-id="a2adf-121">Anger ett DataSet-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a2adf-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2adf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a2adf-122">-Force</span></span>
<span data-ttu-id="a2adf-123">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a2adf-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a2adf-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a2adf-124">-Name</span></span>
<span data-ttu-id="a2adf-125">Anger namnet på den dataset som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a2adf-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2adf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2adf-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2adf-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="a2adf-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a2adf-128">Denna cmdlet tar bort en data uppsättning från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a2adf-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2adf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2adf-129">-ResourceId</span></span>
<span data-ttu-id="a2adf-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="a2adf-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a2adf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2adf-131">-WhatIf</span></span>
<span data-ttu-id="a2adf-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2adf-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="a2adf-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2adf-133">INPUTS</span></span>

### <span data-ttu-id="a2adf-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="a2adf-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="a2adf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a2adf-135">System.String</span></span>


## <span data-ttu-id="a2adf-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2adf-136">OUTPUTS</span></span>

### <span data-ttu-id="a2adf-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="a2adf-137">System.Object</span></span>

## <span data-ttu-id="a2adf-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2adf-138">NOTES</span></span>
<span data-ttu-id="a2adf-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="a2adf-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a2adf-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2adf-140">RELATED LINKS</span></span>
[<span data-ttu-id="a2adf-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a2adf-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="a2adf-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="a2adf-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
