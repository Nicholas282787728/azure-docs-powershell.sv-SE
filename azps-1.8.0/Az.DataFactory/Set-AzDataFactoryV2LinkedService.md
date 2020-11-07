---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 2ff8e4a92c01c38b81ad5f1fded5661501b1c46c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754343"
---
# <span data-ttu-id="2f640-101">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2f640-101">Set-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="2f640-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f640-102">SYNOPSIS</span></span>
<span data-ttu-id="2f640-103">Länkar ett data lager eller en moln tjänst till data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2f640-103">Links a data store or a cloud service to Data Factory.</span></span>

## <span data-ttu-id="2f640-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f640-104">SYNTAX</span></span>

### <span data-ttu-id="2f640-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="2f640-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2LinkedService [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f640-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f640-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2LinkedService [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f640-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f640-107">DESCRIPTION</span></span>
<span data-ttu-id="2f640-108">Set-AzDataFactoryV2LinkedService cmdlet länkar ett data lager eller en moln tjänst till Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="2f640-108">The Set-AzDataFactoryV2LinkedService cmdlet links a data store or a cloud service to Azure Data Factory.</span></span>
<span data-ttu-id="2f640-109">Om du anger ett namn för en länkad tjänst som redan finns uppmanas du att bekräfta den här cmdleten innan den länkade tjänsten byts ut.</span><span class="sxs-lookup"><span data-stu-id="2f640-109">If you specify a name for a linked service that already exists, this cmdlet prompts you for confirmation before it replaces the linked service.</span></span>
<span data-ttu-id="2f640-110">Om du anger parametern Force ersätter cmdlet den befintliga länkade tjänsten utan att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2f640-110">If you specify the Force parameter, the cmdlet replaces the existing linked service without confirmation.</span></span>
<span data-ttu-id="2f640-111">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2f640-111">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="2f640-112">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="2f640-112">-- Create linked services.</span></span>
<span data-ttu-id="2f640-113">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="2f640-113">-- Create datasets.</span></span>
<span data-ttu-id="2f640-114">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="2f640-114">-- Create a pipeline.</span></span>

## <span data-ttu-id="2f640-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f640-115">EXAMPLES</span></span>

### <span data-ttu-id="2f640-116">Exempel 1: skapa en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="2f640-116">Example 1: Create a linked service</span></span>
```
PS C:\> Set-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData" -File "C:\\samples\\WikiSample\\LinkedServiceCuratedWikiData.json" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="2f640-117">Det här kommandot skapar en länkad tjänst som heter LinkedServiceCuratedWikiData i data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2f640-117">This command creates a linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>
<span data-ttu-id="2f640-118">Den här länkade tjänsten länkar en Azure Blob-lagringsplats som angetts i filen till data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2f640-118">This linked service links an Azure blob store specified in the file to the data factory named WikiADF.</span></span>
<span data-ttu-id="2f640-119">Kommandot skickar resultatet till Format-List cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="2f640-119">The command passes the result to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2f640-120">Som Windows PowerShell-cmdlet formaterar resultatet.</span><span class="sxs-lookup"><span data-stu-id="2f640-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="2f640-121">För mer information, skriv Get-Help format-lista.</span><span class="sxs-lookup"><span data-stu-id="2f640-121">For more information, type Get-Help Format-List.</span></span>

## <span data-ttu-id="2f640-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f640-122">PARAMETERS</span></span>

### <span data-ttu-id="2f640-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2f640-123">-DataFactoryName</span></span>
<span data-ttu-id="2f640-124">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2f640-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2f640-125">Denna cmdlet skapar en länkad tjänst för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2f640-125">This cmdlet creates a linked service for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f640-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f640-126">-DefaultProfile</span></span>
<span data-ttu-id="2f640-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f640-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f640-128">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="2f640-128">-DefinitionFile</span></span>
<span data-ttu-id="2f640-129">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="2f640-129">The JSON file path.</span></span>

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

### <span data-ttu-id="2f640-130">-Force</span><span class="sxs-lookup"><span data-stu-id="2f640-130">-Force</span></span>
<span data-ttu-id="2f640-131">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2f640-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2f640-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f640-132">-Name</span></span>
<span data-ttu-id="2f640-133">Anger namnet på den länkade tjänst som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="2f640-133">Specifies the name of the linked service to create.</span></span>

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

### <span data-ttu-id="2f640-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f640-134">-ResourceGroupName</span></span>
<span data-ttu-id="2f640-135">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="2f640-135">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2f640-136">Denna cmdlet skapar en länkad tjänst för gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="2f640-136">This cmdlet creates a linked service for the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f640-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f640-137">-ResourceId</span></span>
<span data-ttu-id="2f640-138">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="2f640-138">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2f640-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2f640-139">-Confirm</span></span>
<span data-ttu-id="2f640-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f640-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f640-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f640-141">-WhatIf</span></span>
<span data-ttu-id="2f640-142">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2f640-142">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2f640-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f640-143">CommonParameters</span></span>
<span data-ttu-id="2f640-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f640-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f640-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f640-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f640-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f640-146">INPUTS</span></span>

### <span data-ttu-id="2f640-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2f640-147">System.String</span></span>

## <span data-ttu-id="2f640-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f640-148">OUTPUTS</span></span>

### <span data-ttu-id="2f640-149">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="2f640-149">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

## <span data-ttu-id="2f640-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f640-150">NOTES</span></span>
<span data-ttu-id="2f640-151">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="2f640-151">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2f640-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f640-152">RELATED LINKS</span></span>

[<span data-ttu-id="2f640-153">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2f640-153">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="2f640-154">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="2f640-154">Remove-AzDataFactoryV2LinkedService</span></span>]()
