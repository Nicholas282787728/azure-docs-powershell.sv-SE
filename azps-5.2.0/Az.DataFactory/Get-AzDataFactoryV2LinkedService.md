---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: ac3a45f9e150d65829a222e75e7072c6a2bdcd1e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393552"
---
# <span data-ttu-id="e72ed-101">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e72ed-101">Get-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="e72ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e72ed-102">SYNOPSIS</span></span>
<span data-ttu-id="e72ed-103">Hämtar information om de länkade tjänsterna i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e72ed-103">Gets information about linked services in Data Factory.</span></span>

## <span data-ttu-id="e72ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e72ed-104">SYNTAX</span></span>

### <span data-ttu-id="e72ed-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="e72ed-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e72ed-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="e72ed-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e72ed-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e72ed-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2LinkedService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e72ed-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e72ed-108">DESCRIPTION</span></span>
<span data-ttu-id="e72ed-109">I Get-AzDataFactoryV2LinkedService cmdlet får du information om länkade tjänster i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="e72ed-109">The Get-AzDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="e72ed-110">Om du anger namnet på en länkad tjänst får denna cmdlet information om den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e72ed-110">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="e72ed-111">Om du inte anger ett namn hämtas den här cmdleten information om alla länkade tjänster i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e72ed-111">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="e72ed-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e72ed-112">EXAMPLES</span></span>

### <span data-ttu-id="e72ed-113">Exempel 1: få information om alla länkade tjänster</span><span class="sxs-lookup"><span data-stu-id="e72ed-113">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="e72ed-114">Det här kommandot får information om alla länkade tjänster i data fabriken med namnet WikiADF och skickar sedan de länkade tjänsterna till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e72ed-114">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e72ed-115">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="e72ed-115">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="e72ed-116">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="e72ed-116">For more information, type Get-Help Format-List.</span></span>
<span data-ttu-id="e72ed-117">Du kan använda något av följande sätt:</span><span class="sxs-lookup"><span data-stu-id="e72ed-117">You can use either one of the following ways:</span></span>

### <span data-ttu-id="e72ed-118">Exempel 2: Hämta information om en specifik länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="e72ed-118">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="e72ed-119">Med det här kommandot får du information om den länkade tjänsten som heter LinkedServiceCuratedWikiData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="e72ed-119">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="e72ed-120">Exempel 3: Hämta information om en specifik länkad tjänst genom att ange parametern DataFactory</span><span class="sxs-lookup"><span data-stu-id="e72ed-120">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="e72ed-121">Det första kommandot använder cmdleten Get-AzDataFactoryV2 för att hämta data fabriken med namnet ContosoFactory och lagrar den sedan i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="e72ed-121">The first command uses the Get-AzDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="e72ed-122">Det andra kommandot får information om den länkade tjänsten för data fabriken som lagras i $DataFactory och skickar sedan informationen till Format-Table-cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="e72ed-122">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e72ed-123">I Format-Table cmdlet formateras utdata som en data uppsättning med de angivna egenskaperna som data mängds kolumner.</span><span class="sxs-lookup"><span data-stu-id="e72ed-123">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="e72ed-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e72ed-124">PARAMETERS</span></span>

### <span data-ttu-id="e72ed-125">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="e72ed-125">-DataFactory</span></span>
<span data-ttu-id="e72ed-126">Anger ett PSDataFactory-objekt.</span><span class="sxs-lookup"><span data-stu-id="e72ed-126">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="e72ed-127">Denna cmdlet tar emot länkade tjänster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e72ed-127">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e72ed-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e72ed-128">-DataFactoryName</span></span>
<span data-ttu-id="e72ed-129">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="e72ed-129">Specifies the name of a data factory.</span></span>
<span data-ttu-id="e72ed-130">Denna cmdlet tar emot länkade tjänster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e72ed-130">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="e72ed-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72ed-131">-DefaultProfile</span></span>
<span data-ttu-id="e72ed-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e72ed-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e72ed-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="e72ed-133">-Name</span></span>
<span data-ttu-id="e72ed-134">Anger namnet på den länkade tjänsten som ska få information om.</span><span class="sxs-lookup"><span data-stu-id="e72ed-134">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e72ed-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e72ed-135">-ResourceGroupName</span></span>
<span data-ttu-id="e72ed-136">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="e72ed-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e72ed-137">Denna cmdlet tar emot länkade tjänster som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e72ed-137">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e72ed-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e72ed-138">-ResourceId</span></span>
<span data-ttu-id="e72ed-139">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="e72ed-139">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e72ed-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72ed-140">CommonParameters</span></span>
<span data-ttu-id="e72ed-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72ed-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72ed-142">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72ed-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72ed-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e72ed-143">INPUTS</span></span>

### <span data-ttu-id="e72ed-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e72ed-144">System.String</span></span>

### <span data-ttu-id="e72ed-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e72ed-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e72ed-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e72ed-146">OUTPUTS</span></span>

### <span data-ttu-id="e72ed-147">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="e72ed-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="e72ed-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e72ed-148">NOTES</span></span>
<span data-ttu-id="e72ed-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="e72ed-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e72ed-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e72ed-150">RELATED LINKS</span></span>

[<span data-ttu-id="e72ed-151">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e72ed-151">Set-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="e72ed-152">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="e72ed-152">Remove-AzDataFactoryV2LinkedService</span></span>]()
