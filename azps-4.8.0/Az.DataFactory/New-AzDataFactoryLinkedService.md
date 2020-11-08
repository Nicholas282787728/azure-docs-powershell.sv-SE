---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 8CD2BE3E-2FA1-4EAB-BC01-B1E1E3203FF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryLinkedService.md
ms.openlocfilehash: 09b766ec77b9f915a03bf6f5b20bd53941b66fc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260044"
---
# <span data-ttu-id="1b5fa-101">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1b5fa-101">New-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="1b5fa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5fa-103">Länkar ett data lager eller en moln tjänst till en Azure-datafabrik.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-103">Links a data store or a cloud service to an Azure Data Factory.</span></span>

## <span data-ttu-id="1b5fa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b5fa-104">SYNTAX</span></span>

### <span data-ttu-id="1b5fa-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="1b5fa-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryLinkedService [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b5fa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b5fa-106">ByFactoryObject</span></span>
```
New-AzDataFactoryLinkedService [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b5fa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b5fa-107">DESCRIPTION</span></span>
<span data-ttu-id="1b5fa-108">**New-AzDataFactoryLinkedService** cmdlet länkar ett data lager eller en moln tjänst till Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-108">The **New-AzDataFactoryLinkedService** cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="1b5fa-109">Om du anger ett namn för en länkad tjänst som redan finns uppmanas du att bekräfta den här cmdleten innan den länkade tjänsten byts ut.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="1b5fa-110">Om du anger parametern *Force* ersätter cmdlet den befintliga länkade tjänsten utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-110">If you specify the *Force* parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="1b5fa-111">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="1b5fa-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="1b5fa-112">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-112">Create a data factory.</span></span> 
- <span data-ttu-id="1b5fa-113">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-113">Create linked services.</span></span> 
- <span data-ttu-id="1b5fa-114">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-114">Create datasets.</span></span> 
- <span data-ttu-id="1b5fa-115">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-115">Create a pipeline.</span></span>

## <span data-ttu-id="1b5fa-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b5fa-116">EXAMPLES</span></span>

### <span data-ttu-id="1b5fa-117">Exempel 1: skapa en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="1b5fa-117">Example 1: Create a linked service</span></span>
```
PS C:\>New-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List
LinkedServiceName : LinkedServiceCuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.AzureStorageLinkedService
```

<span data-ttu-id="1b5fa-118">Det här kommandot skapar en länkad tjänst som heter LinkedServiceCuratedWikiData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-118">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="1b5fa-119">Den här länkade tjänsten länkar en Azure Blob-lagringsplats som angetts i filen till data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-119">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="1b5fa-120">Kommandot skickar resultatet till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-120">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1b5fa-121">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-121">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="1b5fa-122">Om du vill ha mer information skriver du `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="1b5fa-122">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="1b5fa-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b5fa-123">PARAMETERS</span></span>

### <span data-ttu-id="1b5fa-124">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b5fa-124">-DataFactory</span></span>
<span data-ttu-id="1b5fa-125">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-125">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="1b5fa-126">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-126">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b5fa-127">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1b5fa-127">-DataFactoryName</span></span>
<span data-ttu-id="1b5fa-128">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1b5fa-129">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-129">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b5fa-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5fa-130">-DefaultProfile</span></span>
<span data-ttu-id="1b5fa-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1b5fa-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b5fa-132">-Fil</span><span class="sxs-lookup"><span data-stu-id="1b5fa-132">-File</span></span>
<span data-ttu-id="1b5fa-133">Anger den fullständiga sökvägen till den JavaScript-fil som innehåller en beskrivning av den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-133">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the linked service.</span></span>

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

### <span data-ttu-id="1b5fa-134">-Force</span><span class="sxs-lookup"><span data-stu-id="1b5fa-134">-Force</span></span>
<span data-ttu-id="1b5fa-135">Anger att denna cmdlet ersätter en befintlig länkad tjänst utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-135">Indicates that this cmdlet replaces an existing linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="1b5fa-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b5fa-136">-Name</span></span>
<span data-ttu-id="1b5fa-137">Anger namnet på den länkade tjänst som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-137">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="1b5fa-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b5fa-138">-ResourceGroupName</span></span>
<span data-ttu-id="1b5fa-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b5fa-140">Denna cmdlet skapar en länkad tjänst för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-140">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b5fa-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b5fa-141">-Confirm</span></span>
<span data-ttu-id="1b5fa-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b5fa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b5fa-143">-WhatIf</span></span>
<span data-ttu-id="1b5fa-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b5fa-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b5fa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5fa-146">CommonParameters</span></span>
<span data-ttu-id="1b5fa-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b5fa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5fa-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b5fa-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5fa-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b5fa-149">INPUTS</span></span>

### <span data-ttu-id="1b5fa-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b5fa-150">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="1b5fa-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1b5fa-151">System.String</span></span>

## <span data-ttu-id="1b5fa-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b5fa-152">OUTPUTS</span></span>

### <span data-ttu-id="1b5fa-153">Microsoft. Azure. commands. DataFactories. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="1b5fa-153">Microsoft.Azure.Commands.DataFactories.Models.PSLinkedService</span></span>

## <span data-ttu-id="1b5fa-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b5fa-154">NOTES</span></span>
* <span data-ttu-id="1b5fa-155">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="1b5fa-155">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b5fa-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b5fa-156">RELATED LINKS</span></span>

[<span data-ttu-id="1b5fa-157">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1b5fa-157">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="1b5fa-158">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="1b5fa-158">Remove-AzDataFactoryLinkedService</span></span>](./Remove-AzDataFactoryLinkedService.md)


