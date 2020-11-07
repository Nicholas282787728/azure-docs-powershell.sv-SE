---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: DFA41A2B-7C8A-42CB-B0B6-5E6FF853EFEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 7503d775b7241bbb1be6196db153e41587c0e736
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758113"
---
# <span data-ttu-id="b1a91-101">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a91-101">Get-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="b1a91-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1a91-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a91-103">Hämtar information om de länkade tjänsterna i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1a91-103">Gets information about linked services in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a91-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1a91-104">SYNTAX</span></span>

### <span data-ttu-id="b1a91-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b1a91-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a91-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b1a91-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a91-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1a91-107">DESCRIPTION</span></span>
<span data-ttu-id="b1a91-108">Cmdleten **Get-AzureRmDataFactoryLinkedService** hämtar information om länkade tjänster i Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b1a91-108">The **Get-AzureRmDataFactoryLinkedService** cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="b1a91-109">Om du anger namnet på en länkad tjänst får denna cmdlet information om den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b1a91-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="b1a91-110">Om du inte anger ett namn hämtas den här cmdleten information om alla länkade tjänster i data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b1a91-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="b1a91-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1a91-111">EXAMPLES</span></span>

### <span data-ttu-id="b1a91-112">Exempel 1: få information om alla länkade tjänster</span><span class="sxs-lookup"><span data-stu-id="b1a91-112">Example 1: Get information about all linked services</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List
```

<span data-ttu-id="b1a91-113">Det här kommandot får information om alla länkade tjänster i data fabriken med namnet WikiADF och skickar sedan de länkade tjänsterna till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b1a91-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1a91-114">Denna cmdlet formaterar resultaten.</span><span class="sxs-lookup"><span data-stu-id="b1a91-114">That cmdlet formats the results.</span></span>
<span data-ttu-id="b1a91-115">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="b1a91-115">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="b1a91-116">Exempel 2: Hämta information om en specifik länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="b1a91-116">Example 2: Get information about a specific linked service</span></span>
```
PS C:\>Get-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "HDILinkedService"
LinkedServiceName   ResourceGroupName     DataFactoryName              Properties
-----------------   -----------------     ---------------              ----------
HDILinkedService    ADF                   WikiADF                      Microsoft.DataFactories.HDInsightBYOCAsset
```

<span data-ttu-id="b1a91-117">Med det här kommandot får du information om den länkade tjänsten som heter HDILinkedService i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b1a91-117">This command gets information about the linked service named HDILinkedService in the data factory named WikiADF.</span></span>

### <span data-ttu-id="b1a91-118">Exempel 3: Hämta information om en specifik länkad tjänst genom att ange parametern DataFactory</span><span class="sxs-lookup"><span data-stu-id="b1a91-118">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "ContosoFactory"
PS C:\> Get-AzureRmDataFactoryLinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="b1a91-119">Det första kommandot använder cmdleten Get-AzureRmDataFactory för att hämta data fabriken med namnet ContosoFactory och lagrar den sedan i $DataFactory variabel.</span><span class="sxs-lookup"><span data-stu-id="b1a91-119">The first command uses the Get-AzureRmDataFactory cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="b1a91-120">Det andra kommandot får information om den länkade tjänsten för data fabriken som lagras i $DataFactory och skickar sedan informationen till Format-Table-cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="b1a91-120">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b1a91-121">**Format-tabell** formaterar utdata som en data uppsättning med de angivna egenskaperna som data mängds kolumner.</span><span class="sxs-lookup"><span data-stu-id="b1a91-121">**Format-Table** formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="b1a91-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1a91-122">PARAMETERS</span></span>

### <span data-ttu-id="b1a91-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b1a91-123">-DataFactory</span></span>
<span data-ttu-id="b1a91-124">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b1a91-124">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b1a91-125">Denna cmdlet tar emot länkade tjänster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b1a91-125">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1a91-126">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b1a91-126">-DataFactoryName</span></span>
<span data-ttu-id="b1a91-127">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b1a91-127">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b1a91-128">Denna cmdlet tar emot länkade tjänster som tillhör data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b1a91-128">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1a91-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1a91-129">-Name</span></span>
<span data-ttu-id="b1a91-130">Anger namnet på den länkade tjänsten som ska få information om.</span><span class="sxs-lookup"><span data-stu-id="b1a91-130">Specifies the name of the linked service about which to get information.</span></span>

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

### <span data-ttu-id="b1a91-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a91-131">-ResourceGroupName</span></span>
<span data-ttu-id="b1a91-132">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="b1a91-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b1a91-133">Denna cmdlet tar emot länkade tjänster som tillhör gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b1a91-133">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1a91-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a91-134">-DefaultProfile</span></span>
<span data-ttu-id="b1a91-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1a91-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a91-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a91-136">CommonParameters</span></span>
<span data-ttu-id="b1a91-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a91-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a91-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a91-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a91-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1a91-139">INPUTS</span></span>

## <span data-ttu-id="b1a91-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1a91-140">OUTPUTS</span></span>

### <span data-ttu-id="b1a91-141">System. Collections. Generic. list ' 1 [[Microsoft. WindowsAzure. commands. Utilities. PSLinkedService, Microsoft. WindowsAzure. commands. Utilities, version = 0.8.2.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. kommandon. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a91-141">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="b1a91-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1a91-142">NOTES</span></span>
* <span data-ttu-id="b1a91-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b1a91-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b1a91-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1a91-144">RELATED LINKS</span></span>

[<span data-ttu-id="b1a91-145">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a91-145">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="b1a91-146">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b1a91-146">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)


