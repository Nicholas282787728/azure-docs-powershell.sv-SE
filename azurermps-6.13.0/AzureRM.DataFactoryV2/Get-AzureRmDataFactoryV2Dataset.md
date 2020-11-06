---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 2479336e2c646f82b6868ee2382af508d0404a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577070"
---
# <span data-ttu-id="b8efa-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b8efa-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="b8efa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8efa-102">SYNOPSIS</span></span>
<span data-ttu-id="b8efa-103">Hämtar information om data mängder i data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b8efa-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8efa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8efa-104">SYNTAX</span></span>

### <span data-ttu-id="b8efa-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8efa-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8efa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b8efa-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8efa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8efa-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8efa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8efa-108">DESCRIPTION</span></span>
<span data-ttu-id="b8efa-109">Get-AzureRmDataFactoryV2Dataset cmdlet får information om data mängder i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b8efa-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="b8efa-110">Om du anger namnet på en data uppsättning får denna cmdlet information om den data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b8efa-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="b8efa-111">Om du inte anger ett namn får den här cmdleten information om alla data uppsättningarna i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b8efa-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="b8efa-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8efa-112">EXAMPLES</span></span>

### <span data-ttu-id="b8efa-113">Exempel 1: få information om alla data mängder</span><span class="sxs-lookup"><span data-stu-id="b8efa-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="b8efa-114">Det här kommandot får information om alla data mängder i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b8efa-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b8efa-115">Exempel 2: Hämta information om en viss data uppsättning</span><span class="sxs-lookup"><span data-stu-id="b8efa-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="b8efa-116">Med det här kommandot får du information om den data uppsättning som heter DAWikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b8efa-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="b8efa-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8efa-117">PARAMETERS</span></span>

### <span data-ttu-id="b8efa-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b8efa-118">-DataFactory</span></span>
<span data-ttu-id="b8efa-119">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="b8efa-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="b8efa-120">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8efa-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8efa-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8efa-121">-DataFactoryName</span></span>
<span data-ttu-id="b8efa-122">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b8efa-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b8efa-123">Denna cmdlet hämtar data uppsättningar som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8efa-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8efa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8efa-124">-DefaultProfile</span></span>
<span data-ttu-id="b8efa-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8efa-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8efa-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8efa-126">-Name</span></span>
<span data-ttu-id="b8efa-127">Anger namnet på den data uppsättning som du vill hämta information om.</span><span class="sxs-lookup"><span data-stu-id="b8efa-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8efa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8efa-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8efa-129">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="b8efa-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b8efa-130">Denna cmdlet hämtar data mängder som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b8efa-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b8efa-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8efa-131">-ResourceId</span></span>
<span data-ttu-id="b8efa-132">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="b8efa-132">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8efa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8efa-133">CommonParameters</span></span>
<span data-ttu-id="b8efa-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8efa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8efa-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8efa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8efa-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8efa-136">INPUTS</span></span>

### <span data-ttu-id="b8efa-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b8efa-137">System.String</span></span>

### <span data-ttu-id="b8efa-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b8efa-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="b8efa-139">Parametrar: DataFactory (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b8efa-139">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="b8efa-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8efa-140">OUTPUTS</span></span>

### <span data-ttu-id="b8efa-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="b8efa-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="b8efa-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8efa-142">NOTES</span></span>
<span data-ttu-id="b8efa-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b8efa-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b8efa-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8efa-144">RELATED LINKS</span></span>

[<span data-ttu-id="b8efa-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b8efa-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="b8efa-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="b8efa-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
