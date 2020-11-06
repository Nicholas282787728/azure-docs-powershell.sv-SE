---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 01c2849c69cfbdd785fae092aeed63117a07b1ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574988"
---
# <span data-ttu-id="5a222-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="5a222-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="5a222-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a222-102">SYNOPSIS</span></span>
<span data-ttu-id="5a222-103">Hämtar information om data mängder i data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5a222-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a222-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a222-104">SYNTAX</span></span>

### <span data-ttu-id="5a222-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="5a222-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a222-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5a222-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a222-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a222-107">DESCRIPTION</span></span>
<span data-ttu-id="5a222-108">Get-AzureRmDataFactoryV2Dataset cmdlet får information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5a222-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="5a222-109">Om du anger namnet på en data uppsättning får denna cmdlet information om den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="5a222-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="5a222-110">Om du inte anger ett namn får den här cmdleten information om alla data uppsättningarna i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5a222-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="5a222-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a222-111">EXAMPLES</span></span>

### <span data-ttu-id="5a222-112">Exempel 1: få information om alla data mängder</span><span class="sxs-lookup"><span data-stu-id="5a222-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="5a222-113">Det här kommandot får information om alla data mängder i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5a222-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="5a222-114">Exempel 2: Hämta information om en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="5a222-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="5a222-115">Med det här kommandot får du information om den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="5a222-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="5a222-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a222-116">PARAMETERS</span></span>

### <span data-ttu-id="5a222-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5a222-117">-DataFactory</span></span>
<span data-ttu-id="5a222-118">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="5a222-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="5a222-119">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5a222-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a222-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5a222-120">-DataFactoryName</span></span>
<span data-ttu-id="5a222-121">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="5a222-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5a222-122">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5a222-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a222-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a222-123">-Name</span></span>
<span data-ttu-id="5a222-124">Anger namnet på den data uppsättning som du vill hämta information om.</span><span class="sxs-lookup"><span data-stu-id="5a222-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a222-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a222-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a222-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="5a222-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5a222-127">Denna cmdlet hämtar data mängder som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="5a222-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a222-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a222-128">-DefaultProfile</span></span>
<span data-ttu-id="5a222-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a222-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a222-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a222-130">CommonParameters</span></span>
<span data-ttu-id="5a222-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a222-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a222-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a222-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a222-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a222-133">INPUTS</span></span>

### <span data-ttu-id="5a222-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5a222-134">System.String</span></span>
<span data-ttu-id="5a222-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5a222-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5a222-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a222-136">OUTPUTS</span></span>

### <span data-ttu-id="5a222-137">System. Collections. Generic. list ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5a222-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="5a222-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="5a222-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="5a222-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a222-139">NOTES</span></span>
<span data-ttu-id="5a222-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="5a222-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5a222-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a222-141">RELATED LINKS</span></span>

[<span data-ttu-id="5a222-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="5a222-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="5a222-143">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="5a222-143">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
