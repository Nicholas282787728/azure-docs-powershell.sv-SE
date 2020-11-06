---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 0898b65c0a124b278d0878ac1749e955011e1dab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573648"
---
# <span data-ttu-id="e86c0-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e86c0-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="e86c0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e86c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e86c0-103">Hämtar information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e86c0-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e86c0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e86c0-104">SYNTAX</span></span>

### <span data-ttu-id="e86c0-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e86c0-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e86c0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e86c0-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e86c0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e86c0-107">DESCRIPTION</span></span>
<span data-ttu-id="e86c0-108">Cmdleten **Get-AzureRmDataFactoryDataset** hämtar information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e86c0-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="e86c0-109">Om du anger namnet på en data uppsättning får denna cmdlet information om den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e86c0-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="e86c0-110">Om du inte anger ett namn får den här cmdleten information om alla data uppsättningarna i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e86c0-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="e86c0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e86c0-111">EXAMPLES</span></span>

### <span data-ttu-id="e86c0-112">Exempel 1: få information om alla data mängder</span><span class="sxs-lookup"><span data-stu-id="e86c0-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="e86c0-113">Det här kommandot får information om alla data mängder i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e86c0-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e86c0-114">Exempel 2: Hämta information om en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="e86c0-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="e86c0-115">Med det här kommandot får du information om den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e86c0-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e86c0-116">Exempel 3: Hämta platsen för en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="e86c0-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="e86c0-117">Det här kommandot hämtar information för den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF och använder sedan standard punkt notation för att visa **platsen** som är kopplad till den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e86c0-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="e86c0-118">Du kan också tilldela utdata från cmdleten **Get-AzureRmDataFactoryDataset** till en variabel och sedan använda punkt notation för att visa egenskapen plats som är kopplad till det DataSet-objekt som lagras i variabeln.</span><span class="sxs-lookup"><span data-stu-id="e86c0-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="e86c0-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e86c0-119">PARAMETERS</span></span>

### <span data-ttu-id="e86c0-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e86c0-120">-DataFactory</span></span>
<span data-ttu-id="e86c0-121">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e86c0-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="e86c0-122">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e86c0-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e86c0-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e86c0-123">-DataFactoryName</span></span>
<span data-ttu-id="e86c0-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e86c0-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e86c0-125">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e86c0-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e86c0-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="e86c0-126">-Name</span></span>
<span data-ttu-id="e86c0-127">Anger namnet på den dataset som innehåller information om den här cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e86c0-127">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="e86c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e86c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="e86c0-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e86c0-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e86c0-130">Denna cmdlet hämtar data mängder som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e86c0-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e86c0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86c0-131">-DefaultProfile</span></span>
<span data-ttu-id="e86c0-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e86c0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e86c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86c0-133">CommonParameters</span></span>
<span data-ttu-id="e86c0-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e86c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86c0-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e86c0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86c0-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e86c0-136">INPUTS</span></span>

## <span data-ttu-id="e86c0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e86c0-137">OUTPUTS</span></span>

### <span data-ttu-id="e86c0-138">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft. WindowsAzure. commands. Utilities, version = 0.8.2.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e86c0-138">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataset, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataset</span></span>

## <span data-ttu-id="e86c0-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e86c0-139">NOTES</span></span>
* <span data-ttu-id="e86c0-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="e86c0-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e86c0-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e86c0-141">RELATED LINKS</span></span>

[<span data-ttu-id="e86c0-142">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e86c0-142">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="e86c0-143">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="e86c0-143">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


