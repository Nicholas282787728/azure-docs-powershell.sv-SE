---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 4254a243894893e58c1c59ea19a8953ddcc8f101
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574705"
---
# <span data-ttu-id="e6f40-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e6f40-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="e6f40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6f40-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f40-103">Skapar en data uppsättning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e6f40-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6f40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6f40-104">SYNTAX</span></span>

### <span data-ttu-id="e6f40-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e6f40-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6f40-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f40-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f40-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6f40-107">DESCRIPTION</span></span>
<span data-ttu-id="e6f40-108">Set-AzureRmDataFactoryV2Dataset-cmdleten skapar en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e6f40-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="e6f40-109">Om du anger ett namn för en data mängd som redan finns uppmanas du att bekräfta denna cmdlet innan den ersätter DataSet.</span><span class="sxs-lookup"><span data-stu-id="e6f40-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="e6f40-110">Om du anger parametern Force ersätter cmdleten det befintliga dataset utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e6f40-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="e6f40-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="e6f40-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="e6f40-112">Om det redan finns en data uppsättning med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga data uppsättningen med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="e6f40-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="e6f40-113">Om du bekräftar att den befintliga data mängden skrivs över ersätts även data uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="e6f40-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="e6f40-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6f40-114">EXAMPLES</span></span>

### <span data-ttu-id="e6f40-115">Exempel 1: skapa en data mängd</span><span class="sxs-lookup"><span data-stu-id="e6f40-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="e6f40-116">Det här kommandot skapar en data mängd som heter DA_WikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e6f40-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="e6f40-117">Kommandot baserar data uppsättningen på informationen i filen DAWikipediaClickEvents.js.</span><span class="sxs-lookup"><span data-stu-id="e6f40-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="e6f40-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6f40-118">PARAMETERS</span></span>

### <span data-ttu-id="e6f40-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6f40-119">-Confirm</span></span>
<span data-ttu-id="e6f40-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6f40-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f40-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e6f40-121">-DataFactoryName</span></span>
<span data-ttu-id="e6f40-122">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e6f40-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e6f40-123">Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e6f40-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6f40-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="e6f40-124">-DefinitionFile</span></span>
<span data-ttu-id="e6f40-125">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="e6f40-125">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f40-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e6f40-126">-Force</span></span>
<span data-ttu-id="e6f40-127">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e6f40-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e6f40-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6f40-128">-Name</span></span>
<span data-ttu-id="e6f40-129">Anger namnet på den data uppsättning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e6f40-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f40-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f40-130">-ResourceGroupName</span></span>
<span data-ttu-id="e6f40-131">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e6f40-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e6f40-132">Denna cmdlet skapar en data mängd i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e6f40-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e6f40-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f40-133">-ResourceId</span></span>
<span data-ttu-id="e6f40-134">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="e6f40-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e6f40-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f40-135">-WhatIf</span></span>
<span data-ttu-id="e6f40-136">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6f40-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e6f40-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f40-137">-DefaultProfile</span></span>
<span data-ttu-id="e6f40-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f40-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f40-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f40-139">CommonParameters</span></span>
<span data-ttu-id="e6f40-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f40-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f40-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f40-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f40-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6f40-142">INPUTS</span></span>

### <span data-ttu-id="e6f40-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f40-143">System.String</span></span>

## <span data-ttu-id="e6f40-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6f40-144">OUTPUTS</span></span>

### <span data-ttu-id="e6f40-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="e6f40-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="e6f40-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6f40-146">NOTES</span></span>
<span data-ttu-id="e6f40-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="e6f40-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e6f40-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6f40-148">RELATED LINKS</span></span>

[<span data-ttu-id="e6f40-149">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e6f40-149">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="e6f40-150">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="e6f40-150">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
