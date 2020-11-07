---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: f977344f2beabe8352a7417130063c3e9d4d3e1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758418"
---
# <span data-ttu-id="cfd7d-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="cfd7d-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="cfd7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cfd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd7d-103">Länkar ett data lager eller en moln tjänst till data fabrik.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfd7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cfd7d-104">SYNTAX</span></span>

### <span data-ttu-id="cfd7d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="cfd7d-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cfd7d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd7d-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="cfd7d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cfd7d-107">DESCRIPTION</span></span>
<span data-ttu-id="cfd7d-108">Set-AzureRmDataFactoryV2LinkedService cmdlet länkar ett data lager eller en moln tjänst till Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="cfd7d-109">Om du anger ett namn för en länkad tjänst som redan finns uppmanas du att bekräfta den här cmdleten innan den länkade tjänsten byts ut.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="cfd7d-110">Om du anger parametern Force ersätter cmdlet den befintliga länkade tjänsten utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="cfd7d-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="cfd7d-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="cfd7d-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cfd7d-112">EXAMPLES</span></span>

### <span data-ttu-id="cfd7d-113">Exempel 1: skapa en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="cfd7d-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

```

<span data-ttu-id="cfd7d-114">Det här kommandot skapar en länkad tjänst som heter LinkedServiceCuratedWikiData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="cfd7d-115">Den här länkade tjänsten länkar en Azure Blob-lagringsplats som angetts i filen till data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="cfd7d-116">Kommandot skickar resultatet till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cfd7d-117">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="cfd7d-118">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="cfd7d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cfd7d-119">PARAMETERS</span></span>

### <span data-ttu-id="cfd7d-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cfd7d-120">-Confirm</span></span>
<span data-ttu-id="cfd7d-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfd7d-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cfd7d-122">-DataFactoryName</span></span>
<span data-ttu-id="cfd7d-123">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cfd7d-124">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfd7d-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="cfd7d-125">-DefinitionFile</span></span>
<span data-ttu-id="cfd7d-126">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-126">The JSON file path.</span></span>

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

### <span data-ttu-id="cfd7d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="cfd7d-127">-Force</span></span>
<span data-ttu-id="cfd7d-128">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cfd7d-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="cfd7d-129">-Name</span></span>
<span data-ttu-id="cfd7d-130">Anger namnet på den länkade tjänst som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd7d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfd7d-131">-ResourceGroupName</span></span>
<span data-ttu-id="cfd7d-132">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cfd7d-133">Denna cmdlet skapar en länkad tjänst för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfd7d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd7d-134">-ResourceId</span></span>
<span data-ttu-id="cfd7d-135">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cfd7d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfd7d-136">-WhatIf</span></span>
<span data-ttu-id="cfd7d-137">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cfd7d-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="cfd7d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cfd7d-138">INPUTS</span></span>

### <span data-ttu-id="cfd7d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cfd7d-139">System.String</span></span>


## <span data-ttu-id="cfd7d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cfd7d-140">OUTPUTS</span></span>

### <span data-ttu-id="cfd7d-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="cfd7d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="cfd7d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cfd7d-142">NOTES</span></span>
<span data-ttu-id="cfd7d-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="cfd7d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cfd7d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cfd7d-144">RELATED LINKS</span></span>
[<span data-ttu-id="cfd7d-145">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="cfd7d-145">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="cfd7d-146">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="cfd7d-146">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
