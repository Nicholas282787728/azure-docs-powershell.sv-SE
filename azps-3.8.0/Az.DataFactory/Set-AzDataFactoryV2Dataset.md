---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2Dataset.md
ms.openlocfilehash: c02ce9b0ba62f7baf4879946bd0ab04efdd5c9e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927734"
---
# <span data-ttu-id="3dfbc-101">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3dfbc-101">Set-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="3dfbc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dfbc-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfbc-103">Skapar en data uppsättning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="3dfbc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dfbc-104">SYNTAX</span></span>

### <span data-ttu-id="3dfbc-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3dfbc-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dfbc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3dfbc-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dfbc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dfbc-107">DESCRIPTION</span></span>
<span data-ttu-id="3dfbc-108">Set-AzDataFactoryV2Dataset-cmdleten skapar en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-108">The Set-AzDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="3dfbc-109">Om du anger ett namn för en data mängd som redan finns uppmanas du att bekräfta denna cmdlet innan den ersätter DataSet.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="3dfbc-110">Om du anger parametern Force ersätter cmdleten det befintliga dataset utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="3dfbc-111">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="3dfbc-112">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-112">-- Create linked services.</span></span>
<span data-ttu-id="3dfbc-113">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-113">-- Create datasets.</span></span>
<span data-ttu-id="3dfbc-114">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-114">-- Create a pipeline.</span></span>
<span data-ttu-id="3dfbc-115">Om det redan finns en data uppsättning med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga data uppsättningen med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-115">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="3dfbc-116">Om du bekräftar att den befintliga data mängden skrivs över ersätts även data uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-116">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="3dfbc-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dfbc-117">EXAMPLES</span></span>

### <span data-ttu-id="3dfbc-118">Exempel 1: skapa en data mängd</span><span class="sxs-lookup"><span data-stu-id="3dfbc-118">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="3dfbc-119">Det här kommandot skapar en data mängd som heter DA_WikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-119">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="3dfbc-120">Kommandot baserar data uppsättningen på informationen i filen DAWikipediaClickEvents.js.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-120">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="3dfbc-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dfbc-121">PARAMETERS</span></span>

### <span data-ttu-id="3dfbc-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3dfbc-122">-DataFactoryName</span></span>
<span data-ttu-id="3dfbc-123">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3dfbc-124">Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-124">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3dfbc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfbc-125">-DefaultProfile</span></span>
<span data-ttu-id="3dfbc-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dfbc-127">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3dfbc-127">-DefinitionFile</span></span>
<span data-ttu-id="3dfbc-128">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-128">The JSON file path.</span></span>

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

### <span data-ttu-id="3dfbc-129">-Force</span><span class="sxs-lookup"><span data-stu-id="3dfbc-129">-Force</span></span>
<span data-ttu-id="3dfbc-130">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-130">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3dfbc-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="3dfbc-131">-Name</span></span>
<span data-ttu-id="3dfbc-132">Anger namnet på den data uppsättning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-132">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="3dfbc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dfbc-133">-ResourceGroupName</span></span>
<span data-ttu-id="3dfbc-134">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3dfbc-135">Denna cmdlet skapar en data mängd i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-135">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3dfbc-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dfbc-136">-ResourceId</span></span>
<span data-ttu-id="3dfbc-137">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3dfbc-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3dfbc-138">-Confirm</span></span>
<span data-ttu-id="3dfbc-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfbc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfbc-140">-WhatIf</span></span>
<span data-ttu-id="3dfbc-141">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-141">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3dfbc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfbc-142">CommonParameters</span></span>
<span data-ttu-id="3dfbc-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfbc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfbc-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfbc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfbc-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dfbc-145">INPUTS</span></span>

### <span data-ttu-id="3dfbc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3dfbc-146">System.String</span></span>

## <span data-ttu-id="3dfbc-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dfbc-147">OUTPUTS</span></span>

### <span data-ttu-id="3dfbc-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3dfbc-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="3dfbc-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dfbc-149">NOTES</span></span>
<span data-ttu-id="3dfbc-150">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="3dfbc-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3dfbc-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dfbc-151">RELATED LINKS</span></span>

[<span data-ttu-id="3dfbc-152">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3dfbc-152">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="3dfbc-153">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="3dfbc-153">Remove-AzDataFactoryV2Dataset</span></span>]()
