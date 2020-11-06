---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 405ec877f139865082d21eb2c05ace17f1100e2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573458"
---
# <span data-ttu-id="51bf8-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="51bf8-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="51bf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="51bf8-103">Skapar en data uppsättning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="51bf8-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51bf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51bf8-104">SYNTAX</span></span>

### <span data-ttu-id="51bf8-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="51bf8-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51bf8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51bf8-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51bf8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51bf8-107">DESCRIPTION</span></span>
<span data-ttu-id="51bf8-108">Set-AzureRmDataFactoryV2Dataset-cmdleten skapar en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="51bf8-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="51bf8-109">Om du anger ett namn för en data mängd som redan finns uppmanas du att bekräfta denna cmdlet innan den ersätter DataSet.</span><span class="sxs-lookup"><span data-stu-id="51bf8-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="51bf8-110">Om du anger parametern Force ersätter cmdleten det befintliga dataset utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="51bf8-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="51bf8-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="51bf8-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="51bf8-112">Om det redan finns en data uppsättning med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga data uppsättningen med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="51bf8-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="51bf8-113">Om du bekräftar att den befintliga data mängden skrivs över ersätts även data uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="51bf8-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="51bf8-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51bf8-114">EXAMPLES</span></span>

### <span data-ttu-id="51bf8-115">Exempel 1: skapa en data mängd</span><span class="sxs-lookup"><span data-stu-id="51bf8-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="51bf8-116">Det här kommandot skapar en data mängd som heter DA_WikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="51bf8-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="51bf8-117">Kommandot baserar data uppsättningen på informationen i filen DAWikipediaClickEvents.js.</span><span class="sxs-lookup"><span data-stu-id="51bf8-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="51bf8-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51bf8-118">PARAMETERS</span></span>

### <span data-ttu-id="51bf8-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="51bf8-119">-DataFactoryName</span></span>
<span data-ttu-id="51bf8-120">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="51bf8-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="51bf8-121">Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51bf8-121">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="51bf8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51bf8-122">-DefaultProfile</span></span>
<span data-ttu-id="51bf8-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51bf8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51bf8-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="51bf8-124">-DefinitionFile</span></span>
<span data-ttu-id="51bf8-125">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="51bf8-125">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51bf8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="51bf8-126">-Force</span></span>
<span data-ttu-id="51bf8-127">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="51bf8-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="51bf8-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="51bf8-128">-Name</span></span>
<span data-ttu-id="51bf8-129">Anger namnet på den data uppsättning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="51bf8-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51bf8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51bf8-130">-ResourceGroupName</span></span>
<span data-ttu-id="51bf8-131">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="51bf8-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="51bf8-132">Denna cmdlet skapar en data mängd i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="51bf8-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="51bf8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51bf8-133">-ResourceId</span></span>
<span data-ttu-id="51bf8-134">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="51bf8-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="51bf8-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51bf8-135">-Confirm</span></span>
<span data-ttu-id="51bf8-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51bf8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51bf8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51bf8-137">-WhatIf</span></span>
<span data-ttu-id="51bf8-138">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51bf8-138">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="51bf8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51bf8-139">CommonParameters</span></span>
<span data-ttu-id="51bf8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51bf8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51bf8-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51bf8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51bf8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51bf8-142">INPUTS</span></span>

### <span data-ttu-id="51bf8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="51bf8-143">System.String</span></span>

## <span data-ttu-id="51bf8-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51bf8-144">OUTPUTS</span></span>

### <span data-ttu-id="51bf8-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="51bf8-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="51bf8-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51bf8-146">NOTES</span></span>
<span data-ttu-id="51bf8-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="51bf8-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="51bf8-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51bf8-148">RELATED LINKS</span></span>

[<span data-ttu-id="51bf8-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="51bf8-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="51bf8-150">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="51bf8-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
