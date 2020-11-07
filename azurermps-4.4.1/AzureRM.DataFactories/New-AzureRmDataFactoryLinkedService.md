---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 9ae1dfe79361e926325b82199469eaf9a9f5d92b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577660"
---
# <span data-ttu-id="8be5b-101">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8be5b-101">New-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="8be5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8be5b-102">SYNOPSIS</span></span>
<span data-ttu-id="8be5b-103">Länkar ett data lager eller en moln tjänst till en Azure-datafabrik.</span><span class="sxs-lookup"><span data-stu-id="8be5b-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8be5b-104">SYNTAX</span></span>

### <span data-ttu-id="8be5b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8be5b-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8be5b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8be5b-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be5b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8be5b-107">DESCRIPTION</span></span>
<span data-ttu-id="8be5b-108">**New-AzureRmDataFactoryLinkedService** cmdlet länkar ett data lager eller en moln tjänst till Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8be5b-108">The **New-AzureRmDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="8be5b-109">Om du anger ett namn för en länkad tjänst som redan finns uppmanas du att bekräfta den här cmdleten innan den länkade tjänsten byts ut.</span><span class="sxs-lookup"><span data-stu-id="8be5b-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="8be5b-110">Om du anger parametern *Force* ersätter cmdlet den befintliga länkade tjänsten utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8be5b-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>

<span data-ttu-id="8be5b-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="8be5b-111">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="8be5b-112">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8be5b-112">Create a data factory.</span></span> 
- <span data-ttu-id="8be5b-113">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="8be5b-113">Create linked services.</span></span> 
- <span data-ttu-id="8be5b-114">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="8be5b-114">Create datasets.</span></span> 
- <span data-ttu-id="8be5b-115">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="8be5b-115">Create a pipeline.</span></span>

## <span data-ttu-id="8be5b-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8be5b-116">EXAMPLES</span></span>

### <span data-ttu-id="8be5b-117">Exempel 1: skapa en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="8be5b-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="8be5b-118">Det här kommandot skapar en länkad tjänst som heter LinkedServiceCuratedWikiData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8be5b-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="8be5b-119">Den här länkade tjänsten länkar en Azure Blob-lagringsplats som angetts i filen till data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8be5b-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="8be5b-120">Kommandot skickar resultatet till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="8be5b-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8be5b-121">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="8be5b-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="8be5b-122">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="8be5b-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="8be5b-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8be5b-123">PARAMETERS</span></span>

### <span data-ttu-id="8be5b-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8be5b-124">-DataFactory</span></span>
<span data-ttu-id="8be5b-125">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8be5b-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8be5b-126">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8be5b-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be5b-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8be5b-127">-DataFactoryName</span></span>
<span data-ttu-id="8be5b-128">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8be5b-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8be5b-129">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8be5b-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be5b-130">-Fil</span><span class="sxs-lookup"><span data-stu-id="8be5b-130">-File</span></span>
<span data-ttu-id="8be5b-131">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8be5b-131">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="8be5b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8be5b-132">-Force</span></span>
<span data-ttu-id="8be5b-133">Anger att denna cmdlet ersätter en befintlig länkad tjänst utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8be5b-133">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8be5b-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="8be5b-134">-Name</span></span>
<span data-ttu-id="8be5b-135">Anger namnet på den länkade tjänst som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="8be5b-135">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="8be5b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be5b-136">-ResourceGroupName</span></span>
<span data-ttu-id="8be5b-137">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="8be5b-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8be5b-138">Denna cmdlet skapar en länkad tjänst för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8be5b-138">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be5b-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8be5b-139">-Confirm</span></span>
<span data-ttu-id="8be5b-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8be5b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be5b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be5b-141">-WhatIf</span></span>
<span data-ttu-id="8be5b-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8be5b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be5b-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8be5b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be5b-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be5b-144">-DefaultProfile</span></span>
<span data-ttu-id="8be5b-145">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8be5b-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be5b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be5b-146">CommonParameters</span></span>
<span data-ttu-id="8be5b-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be5b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be5b-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be5b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be5b-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8be5b-149">INPUTS</span></span>

## <span data-ttu-id="8be5b-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8be5b-150">OUTPUTS</span></span>

### <span data-ttu-id="8be5b-151">Microsoft. WindowsAzure. commands. Utilities. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="8be5b-151">Microsoft.WindowsAzure.Commands.Utilities.PSLinkedService</span></span>

## <span data-ttu-id="8be5b-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8be5b-152">NOTES</span></span>
* <span data-ttu-id="8be5b-153">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="8be5b-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8be5b-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8be5b-154">RELATED LINKS</span></span>

[<span data-ttu-id="8be5b-155">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8be5b-155">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="8be5b-156">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8be5b-156">Remove-AzureRmDataFactoryLinkedService</span></span>](./Remove-AzureRmDataFactoryLinkedService.md)

