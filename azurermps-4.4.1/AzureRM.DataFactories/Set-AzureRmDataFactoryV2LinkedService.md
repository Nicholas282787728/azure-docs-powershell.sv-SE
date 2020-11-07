---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: 5e0ee389a5d2d126cfbccc2a91b1644d81a5fedf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758104"
---
# <span data-ttu-id="53145-101">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="53145-101">Set-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="53145-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="53145-102">SYNOPSIS</span></span>
<span data-ttu-id="53145-103">Länkar ett data lager eller en moln tjänst till data fabrik.</span><span class="sxs-lookup"><span data-stu-id="53145-103">Links a data store or a cloud service to Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53145-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="53145-104">SYNTAX</span></span>

### <span data-ttu-id="53145-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="53145-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53145-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="53145-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53145-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="53145-107">DESCRIPTION</span></span>
<span data-ttu-id="53145-108">Set-AzureRmDataFactoryV2LinkedService cmdlet länkar ett data lager eller en moln tjänst till Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="53145-108">The Set-AzureRmDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="53145-109">Om du anger ett namn för en länkad tjänst som redan finns uppmanas du att bekräfta den här cmdleten innan den länkade tjänsten byts ut.</span><span class="sxs-lookup"><span data-stu-id="53145-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="53145-110">Om du anger parametern Force ersätter cmdlet den befintliga länkade tjänsten utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="53145-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="53145-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="53145-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="53145-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="53145-112">EXAMPLES</span></span>

### <span data-ttu-id="53145-113">Exempel 1: skapa en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="53145-113">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="53145-114">Det här kommandot skapar en länkad tjänst som heter LinkedServiceCuratedWikiData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="53145-114">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="53145-115">Den här länkade tjänsten länkar en Azure Blob-lagringsplats som angetts i filen till data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="53145-115">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="53145-116">Kommandot skickar resultatet till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="53145-116">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53145-117">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="53145-117">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="53145-118">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="53145-118">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="53145-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="53145-119">PARAMETERS</span></span>

### <span data-ttu-id="53145-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="53145-120">-Confirm</span></span>
<span data-ttu-id="53145-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53145-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53145-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="53145-122">-DataFactoryName</span></span>
<span data-ttu-id="53145-123">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="53145-123">Specifies the name of a data factory.</span></span>
<span data-ttu-id="53145-124">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53145-124">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="53145-125">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="53145-125">-DefinitionFile</span></span>
<span data-ttu-id="53145-126">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="53145-126">The JSON file path.</span></span>

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

### <span data-ttu-id="53145-127">-Force</span><span class="sxs-lookup"><span data-stu-id="53145-127">-Force</span></span>
<span data-ttu-id="53145-128">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="53145-128">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="53145-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="53145-129">-Name</span></span>
<span data-ttu-id="53145-130">Anger namnet på den länkade tjänst som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="53145-130">Specifies the name of the linked service to create.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53145-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53145-131">-ResourceGroupName</span></span>
<span data-ttu-id="53145-132">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="53145-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="53145-133">Denna cmdlet skapar en länkad tjänst för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="53145-133">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53145-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53145-134">-ResourceId</span></span>
<span data-ttu-id="53145-135">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="53145-135">The Azure resource ID.</span></span>

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

### <span data-ttu-id="53145-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53145-136">-WhatIf</span></span>
<span data-ttu-id="53145-137">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="53145-137">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="53145-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53145-138">-DefaultProfile</span></span>
<span data-ttu-id="53145-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="53145-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53145-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53145-140">CommonParameters</span></span>
<span data-ttu-id="53145-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53145-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53145-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53145-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53145-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="53145-143">INPUTS</span></span>

### <span data-ttu-id="53145-144">System. String</span><span class="sxs-lookup"><span data-stu-id="53145-144">System.String</span></span>

## <span data-ttu-id="53145-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="53145-145">OUTPUTS</span></span>

### <span data-ttu-id="53145-146">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="53145-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="53145-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="53145-147">NOTES</span></span>
<span data-ttu-id="53145-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="53145-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="53145-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="53145-149">RELATED LINKS</span></span>

[<span data-ttu-id="53145-150">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="53145-150">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="53145-151">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="53145-151">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
