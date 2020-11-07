---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 976f00f62cfda991e7d1aff349a0b04807dbbe1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744709"
---
# <span data-ttu-id="62f2b-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="62f2b-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="62f2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="62f2b-103">Laddar ned loggfiler från Azure HDInsight-bearbetning.</span><span class="sxs-lookup"><span data-stu-id="62f2b-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="62f2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62f2b-104">SYNTAX</span></span>

### <span data-ttu-id="62f2b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="62f2b-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62f2b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="62f2b-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62f2b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62f2b-107">DESCRIPTION</span></span>
<span data-ttu-id="62f2b-108">Cmdleten **Save-AzDataFactoryLog-** filer som är associerade med Azure HDInsight-bearbetning av gris-eller registrerings projekt eller för anpassade aktiviteter till din lokala hård disk.</span><span class="sxs-lookup"><span data-stu-id="62f2b-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="62f2b-109">Du kör först Get-AzDataFactoryRun cmdlet för att få ett ID för en aktivitet som körs för en data sektor och sedan använda ID: t för att hämta loggfiler från den binära Large Object (BLOB) som är kopplad till HDInsight-klustret.</span><span class="sxs-lookup"><span data-stu-id="62f2b-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="62f2b-110">Om du inte anger parametern *DownloadLogs* returnerar cmdleten bara platsen för loggfilerna.</span><span class="sxs-lookup"><span data-stu-id="62f2b-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="62f2b-111">Om du anger *DownloadLogs* utan att ange en utdatakatalogen ( *utdataparameter* ) hämtas loggfilerna till mappen standard dokument.</span><span class="sxs-lookup"><span data-stu-id="62f2b-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="62f2b-112">Om du anger *DownloadLogs* tillsammans med en utdatafil ( *utdata* ) hämtas loggfilerna till den angivna mappen.</span><span class="sxs-lookup"><span data-stu-id="62f2b-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="62f2b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62f2b-113">EXAMPLES</span></span>

### <span data-ttu-id="62f2b-114">Exempel 1: spara loggfiler i en viss mapp</span><span class="sxs-lookup"><span data-stu-id="62f2b-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="62f2b-115">Det här kommandot sparar loggfiler för aktiviteten som körs med ID-numret för 841b77c9-d56c-48D1-99a3-8c16c3e77d39 där aktiviteten tillhör en pipeline i data fabriken med namnet LogProcessingFactory i resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="62f2b-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="62f2b-116">Loggfilerna sparas i mappen C:\Test.</span><span class="sxs-lookup"><span data-stu-id="62f2b-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="62f2b-117">Exempel 2: spara loggfiler i mappen standard dokument</span><span class="sxs-lookup"><span data-stu-id="62f2b-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="62f2b-118">Det här kommandot sparar loggfiler i mappen dokument (standard).</span><span class="sxs-lookup"><span data-stu-id="62f2b-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="62f2b-119">Exempel 3: Hämta sökvägen till loggfilerna</span><span class="sxs-lookup"><span data-stu-id="62f2b-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="62f2b-120">Det här kommandot returnerar platsen för loggfilerna.</span><span class="sxs-lookup"><span data-stu-id="62f2b-120">This command returns the location of log files.</span></span>
<span data-ttu-id="62f2b-121">Observera att *DownloadLogs* inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="62f2b-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="62f2b-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62f2b-122">PARAMETERS</span></span>

### <span data-ttu-id="62f2b-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="62f2b-123">-DataFactory</span></span>
<span data-ttu-id="62f2b-124">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="62f2b-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="62f2b-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="62f2b-125">-DataFactoryName</span></span>
<span data-ttu-id="62f2b-126">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="62f2b-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="62f2b-127">Denna cmdlet laddar ned loggfiler för data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="62f2b-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="62f2b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f2b-128">-DefaultProfile</span></span>
<span data-ttu-id="62f2b-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="62f2b-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62f2b-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="62f2b-130">-DownloadLogs</span></span>
<span data-ttu-id="62f2b-131">Anger att denna cmdlet laddar ned loggfilerna till din lokala dator.</span><span class="sxs-lookup"><span data-stu-id="62f2b-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="62f2b-132">Om mappen *utdatafil* inte anges sparas filer i mappen dokument under en undermapp.</span><span class="sxs-lookup"><span data-stu-id="62f2b-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="62f2b-133">-ID</span><span class="sxs-lookup"><span data-stu-id="62f2b-133">-Id</span></span>
<span data-ttu-id="62f2b-134">Anger ID för aktivitets körningen för data sektorn.</span><span class="sxs-lookup"><span data-stu-id="62f2b-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="62f2b-135">Använd Get-AzDataFactoryRun cmdlet för att hämta ett ID.</span><span class="sxs-lookup"><span data-stu-id="62f2b-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f2b-136">-Utdata</span><span class="sxs-lookup"><span data-stu-id="62f2b-136">-Output</span></span>
<span data-ttu-id="62f2b-137">Anger den mapp där de hämtade loggfilerna sparas.</span><span class="sxs-lookup"><span data-stu-id="62f2b-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f2b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f2b-138">-ResourceGroupName</span></span>
<span data-ttu-id="62f2b-139">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="62f2b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="62f2b-140">Denna cmdlet skapar en data fabrik som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="62f2b-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="62f2b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f2b-141">CommonParameters</span></span>
<span data-ttu-id="62f2b-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f2b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f2b-143">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f2b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f2b-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62f2b-144">INPUTS</span></span>

### <span data-ttu-id="62f2b-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="62f2b-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="62f2b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="62f2b-146">System.String</span></span>

## <span data-ttu-id="62f2b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62f2b-147">OUTPUTS</span></span>

### <span data-ttu-id="62f2b-148">Microsoft. Azure. commands. DataFactories. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="62f2b-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="62f2b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62f2b-149">NOTES</span></span>
* <span data-ttu-id="62f2b-150">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="62f2b-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="62f2b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62f2b-151">RELATED LINKS</span></span>

[<span data-ttu-id="62f2b-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="62f2b-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="62f2b-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="62f2b-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="62f2b-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="62f2b-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="62f2b-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="62f2b-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="62f2b-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="62f2b-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="62f2b-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="62f2b-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


