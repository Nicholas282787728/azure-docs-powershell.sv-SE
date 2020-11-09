---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 38af817205f8d80615fa94799eee5a7a54f05e78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320959"
---
# <span data-ttu-id="7a087-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="7a087-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="7a087-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a087-102">SYNOPSIS</span></span>
<span data-ttu-id="7a087-103">Skapar en data uppsättning i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="7a087-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="7a087-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a087-104">SYNTAX</span></span>

### <span data-ttu-id="7a087-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="7a087-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a087-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7a087-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a087-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a087-107">DESCRIPTION</span></span>
<span data-ttu-id="7a087-108">Cmdleten **New-AzDataFactoryDataset** skapar en data uppsättning i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7a087-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="7a087-109">Om du anger ett namn för en data mängd som redan finns uppmanas du att bekräfta denna cmdlet innan den ersätter DataSet.</span><span class="sxs-lookup"><span data-stu-id="7a087-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="7a087-110">Om du anger parametern *Force* ersätter cmdleten det befintliga dataset utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7a087-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="7a087-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="7a087-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="7a087-112">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="7a087-112">Create a data factory.</span></span> 
- <span data-ttu-id="7a087-113">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="7a087-113">Create linked services.</span></span> 
- <span data-ttu-id="7a087-114">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="7a087-114">Create datasets.</span></span> 
- <span data-ttu-id="7a087-115">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="7a087-115">Create a pipeline.</span></span>
<span data-ttu-id="7a087-116">Om det redan finns en data uppsättning med samma namn i data fabriken uppmanas du att bekräfta om du vill skriva över den befintliga data uppsättningen med den nya data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="7a087-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="7a087-117">Om du bekräftar att den befintliga data mängden skrivs över ersätts även data uppsättnings definitionen.</span><span class="sxs-lookup"><span data-stu-id="7a087-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="7a087-118">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a087-118">EXAMPLES</span></span>

### <span data-ttu-id="7a087-119">Exempel 1: skapa en data mängd</span><span class="sxs-lookup"><span data-stu-id="7a087-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="7a087-120">Det här kommandot skapar en data mängd som heter DA_WikipediaClickEvents i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7a087-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="7a087-121">Kommandot baserar data uppsättningen på informationen i filen DAWikipediaClickEvents.js.</span><span class="sxs-lookup"><span data-stu-id="7a087-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="7a087-122">Exempel 2: Visa tillgänglighet för en ny data uppsättning</span><span class="sxs-lookup"><span data-stu-id="7a087-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="7a087-123">Det första kommandot skapar en data mängd som heter DA_WikipediaClickEvents, som i ett föregående exempel, och tilldelar sedan denna dataset till $Dataset variabel.</span><span class="sxs-lookup"><span data-stu-id="7a087-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="7a087-124">I det andra kommandot används standard punkt notation för att visa information om egenskapen Availability för data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="7a087-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="7a087-125">Exempel 3: Visa plats för en ny data uppsättning</span><span class="sxs-lookup"><span data-stu-id="7a087-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="7a087-126">Det första kommandot skapar en data mängd som heter DA_WikipediaClickEvents, som i ett föregående exempel, och tilldelar sedan denna dataset till $Dataset variabel.</span><span class="sxs-lookup"><span data-stu-id="7a087-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="7a087-127">Det andra kommandot visar information om egenskapen location för data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="7a087-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="7a087-128">Exempel 4: Visa verifierings uttryck för en ny data uppsättning</span><span class="sxs-lookup"><span data-stu-id="7a087-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="7a087-129">Det första kommandot skapar en data mängd som heter DA_WikipediaClickEvents, som i ett föregående exempel, och tilldelar sedan denna dataset till $Dataset variabel.</span><span class="sxs-lookup"><span data-stu-id="7a087-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="7a087-130">Det andra kommandot hämtar information om verifierings reglerna för data uppsättningen och skickar sedan vidare dem till Format-List cmdlet genom att använda pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="7a087-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7a087-131">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="7a087-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="7a087-132">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="7a087-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="7a087-133">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a087-133">PARAMETERS</span></span>

### <span data-ttu-id="7a087-134">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7a087-134">-DataFactory</span></span>
<span data-ttu-id="7a087-135">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="7a087-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7a087-136">Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7a087-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a087-137">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7a087-137">-DataFactoryName</span></span>
<span data-ttu-id="7a087-138">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="7a087-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7a087-139">Den här cmdleten skapar en data mängd i data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7a087-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a087-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a087-140">-DefaultProfile</span></span>
<span data-ttu-id="7a087-141">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7a087-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a087-142">-Fil</span><span class="sxs-lookup"><span data-stu-id="7a087-142">-File</span></span>
<span data-ttu-id="7a087-143">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av data mängden.</span><span class="sxs-lookup"><span data-stu-id="7a087-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a087-144">-Force</span><span class="sxs-lookup"><span data-stu-id="7a087-144">-Force</span></span>
<span data-ttu-id="7a087-145">Anger att denna cmdlet ersätter en befintlig data uppsättning utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7a087-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="7a087-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="7a087-146">-Name</span></span>
<span data-ttu-id="7a087-147">Anger namnet på den data uppsättning som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7a087-147">Specifies the name of the dataset to create.</span></span>

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

### <span data-ttu-id="7a087-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a087-148">-ResourceGroupName</span></span>
<span data-ttu-id="7a087-149">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="7a087-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7a087-150">Denna cmdlet skapar en data mängd i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="7a087-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7a087-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a087-151">-Confirm</span></span>
<span data-ttu-id="7a087-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a087-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a087-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a087-153">-WhatIf</span></span>
<span data-ttu-id="7a087-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a087-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a087-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a087-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a087-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a087-156">CommonParameters</span></span>
<span data-ttu-id="7a087-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a087-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a087-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a087-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a087-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a087-159">INPUTS</span></span>

### <span data-ttu-id="7a087-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7a087-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="7a087-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7a087-161">System.String</span></span>

## <span data-ttu-id="7a087-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a087-162">OUTPUTS</span></span>

### <span data-ttu-id="7a087-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="7a087-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="7a087-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a087-164">NOTES</span></span>
* <span data-ttu-id="7a087-165">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="7a087-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7a087-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a087-166">RELATED LINKS</span></span>

[<span data-ttu-id="7a087-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="7a087-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="7a087-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="7a087-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


