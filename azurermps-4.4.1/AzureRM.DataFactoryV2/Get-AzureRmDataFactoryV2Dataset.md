---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585687"
---
# <span data-ttu-id="66b24-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="66b24-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="66b24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66b24-102">SYNOPSIS</span></span>
<span data-ttu-id="66b24-103">Hämtar information om data mängder i data fabrik.</span><span class="sxs-lookup"><span data-stu-id="66b24-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66b24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66b24-104">SYNTAX</span></span>

### <span data-ttu-id="66b24-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="66b24-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="66b24-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="66b24-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="66b24-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66b24-107">DESCRIPTION</span></span>
<span data-ttu-id="66b24-108">Get-AzureRmDataFactoryV2Dataset cmdlet får information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="66b24-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="66b24-109">Om du anger namnet på en data uppsättning får denna cmdlet information om den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="66b24-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="66b24-110">Om du inte anger ett namn får den här cmdleten information om alla data uppsättningarna i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="66b24-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="66b24-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66b24-111">EXAMPLES</span></span>

### <span data-ttu-id="66b24-112">Exempel 1: få information om alla data mängder</span><span class="sxs-lookup"><span data-stu-id="66b24-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="66b24-113">Det här kommandot får information om alla data mängder i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="66b24-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="66b24-114">Exempel 2: Hämta information om en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="66b24-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="66b24-115">Med det här kommandot får du information om den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="66b24-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="66b24-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66b24-116">PARAMETERS</span></span>

### <span data-ttu-id="66b24-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="66b24-117">-DataFactory</span></span>
<span data-ttu-id="66b24-118">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="66b24-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="66b24-119">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="66b24-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66b24-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="66b24-120">-DataFactoryName</span></span>
<span data-ttu-id="66b24-121">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="66b24-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="66b24-122">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="66b24-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="66b24-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="66b24-123">-Name</span></span>
<span data-ttu-id="66b24-124">Anger namnet på den data uppsättning som du vill hämta information om.</span><span class="sxs-lookup"><span data-stu-id="66b24-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b24-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b24-125">-ResourceGroupName</span></span>
<span data-ttu-id="66b24-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="66b24-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="66b24-127">Denna cmdlet hämtar data mängder som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="66b24-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="66b24-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66b24-128">INPUTS</span></span>

### <span data-ttu-id="66b24-129">System. String</span><span class="sxs-lookup"><span data-stu-id="66b24-129">System.String</span></span>
<span data-ttu-id="66b24-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="66b24-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="66b24-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66b24-131">OUTPUTS</span></span>

### <span data-ttu-id="66b24-132">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="66b24-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="66b24-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="66b24-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="66b24-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66b24-134">NOTES</span></span>
<span data-ttu-id="66b24-135">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="66b24-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="66b24-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66b24-136">RELATED LINKS</span></span>
[<span data-ttu-id="66b24-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="66b24-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="66b24-138">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="66b24-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
