---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: faf5d80b231b93124279f3c9bb6a347f89d988d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755251"
---
# <span data-ttu-id="d9299-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d9299-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="d9299-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9299-102">SYNOPSIS</span></span>
<span data-ttu-id="d9299-103">Tar bort en data uppsättning från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d9299-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9299-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9299-104">SYNTAX</span></span>

### <span data-ttu-id="d9299-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="d9299-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9299-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9299-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9299-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9299-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9299-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9299-108">DESCRIPTION</span></span>
<span data-ttu-id="d9299-109">Remove-AzureRmDataFactoryV2Dataset cmdlet tar bort en data uppsättning från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d9299-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="d9299-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9299-110">EXAMPLES</span></span>

### <span data-ttu-id="d9299-111">Exempel 1: ta bort en data uppsättning</span><span class="sxs-lookup"><span data-stu-id="d9299-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="d9299-112">Det här kommandot tar bort den dataset som heter DAWikiAggregatedData från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d9299-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="d9299-113">Kommandot returnerar ett värde med $True.</span><span class="sxs-lookup"><span data-stu-id="d9299-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="d9299-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9299-114">PARAMETERS</span></span>

### <span data-ttu-id="d9299-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d9299-115">-DataFactoryName</span></span>
<span data-ttu-id="d9299-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d9299-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d9299-117">Denna cmdlet tar bort en data uppsättning från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d9299-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9299-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9299-118">-DefaultProfile</span></span>
<span data-ttu-id="d9299-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9299-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9299-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d9299-120">-Force</span></span>
<span data-ttu-id="d9299-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d9299-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d9299-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9299-122">-InputObject</span></span>
<span data-ttu-id="d9299-123">Anger ett DataSet-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d9299-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="d9299-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9299-124">-Name</span></span>
<span data-ttu-id="d9299-125">Anger namnet på den dataset som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d9299-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="d9299-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9299-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9299-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d9299-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d9299-128">Denna cmdlet tar bort en data uppsättning från gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d9299-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d9299-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9299-129">-ResourceId</span></span>
<span data-ttu-id="d9299-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="d9299-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d9299-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9299-131">-Confirm</span></span>
<span data-ttu-id="d9299-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9299-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9299-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9299-133">-WhatIf</span></span>
<span data-ttu-id="d9299-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9299-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d9299-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9299-135">CommonParameters</span></span>
<span data-ttu-id="d9299-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9299-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9299-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9299-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9299-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9299-138">INPUTS</span></span>

### <span data-ttu-id="d9299-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="d9299-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="d9299-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d9299-140">System.String</span></span>

## <span data-ttu-id="d9299-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9299-141">OUTPUTS</span></span>

### <span data-ttu-id="d9299-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="d9299-142">System.Object</span></span>

## <span data-ttu-id="d9299-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9299-143">NOTES</span></span>
<span data-ttu-id="d9299-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="d9299-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d9299-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9299-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9299-146">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d9299-146">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="d9299-147">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="d9299-147">Set-AzureRmDataFactoryV2Dataset</span></span>]()
