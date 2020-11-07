---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 6f6421659f47d2a6d119d5acd8e614765f356298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757378"
---
# <span data-ttu-id="e88da-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e88da-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="e88da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e88da-102">SYNOPSIS</span></span>
<span data-ttu-id="e88da-103">Hämtar information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e88da-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e88da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e88da-104">SYNTAX</span></span>

### <span data-ttu-id="e88da-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e88da-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e88da-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e88da-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e88da-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e88da-107">DESCRIPTION</span></span>
<span data-ttu-id="e88da-108">Cmdleten **Get-AzureRmDataFactoryDataset** hämtar information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e88da-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="e88da-109">Om du anger namnet på en data uppsättning får denna cmdlet information om den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e88da-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="e88da-110">Om du inte anger ett namn får den här cmdleten information om alla data uppsättningarna i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e88da-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="e88da-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e88da-111">EXAMPLES</span></span>

### <span data-ttu-id="e88da-112">Exempel 1: få information om alla data mängder</span><span class="sxs-lookup"><span data-stu-id="e88da-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="e88da-113">Det här kommandot får information om alla data mängder i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e88da-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e88da-114">Exempel 2: Hämta information om en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="e88da-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="e88da-115">Med det här kommandot får du information om den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e88da-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e88da-116">Exempel 3: Hämta platsen för en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="e88da-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="e88da-117">Det här kommandot hämtar information för den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa **platsen** som är kopplad till den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e88da-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="e88da-118">Du kan också tilldela utdata från cmdleten **Get-AzureRmDataFactoryDataset** till en variabel och sedan använda punkt notation för att visa egenskapen plats som är kopplad till det DataSet-objekt som lagras i variabeln.</span><span class="sxs-lookup"><span data-stu-id="e88da-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="e88da-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e88da-119">PARAMETERS</span></span>

### <span data-ttu-id="e88da-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e88da-120">-DataFactory</span></span>
<span data-ttu-id="e88da-121">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e88da-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e88da-122">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e88da-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88da-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e88da-123">-DataFactoryName</span></span>
<span data-ttu-id="e88da-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e88da-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e88da-125">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e88da-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e88da-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88da-126">-DefaultProfile</span></span>
<span data-ttu-id="e88da-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e88da-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e88da-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e88da-128">-Name</span></span>
<span data-ttu-id="e88da-129">Anger namnet på den dataset som innehåller information om den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e88da-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e88da-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88da-130">-ResourceGroupName</span></span>
<span data-ttu-id="e88da-131">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e88da-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e88da-132">Denna cmdlet hämtar data mängder som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e88da-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e88da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88da-133">CommonParameters</span></span>
<span data-ttu-id="e88da-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88da-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88da-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e88da-136">INPUTS</span></span>

### <span data-ttu-id="e88da-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e88da-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="e88da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e88da-138">System.String</span></span>

## <span data-ttu-id="e88da-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e88da-139">OUTPUTS</span></span>

### <span data-ttu-id="e88da-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e88da-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="e88da-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e88da-141">NOTES</span></span>
* <span data-ttu-id="e88da-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="e88da-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e88da-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e88da-143">RELATED LINKS</span></span>

[<span data-ttu-id="e88da-144">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e88da-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="e88da-145">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e88da-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


