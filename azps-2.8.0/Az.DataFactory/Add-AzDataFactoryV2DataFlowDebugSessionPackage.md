---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: fdf8d4fefef434e503c0fc21c3036577e56b56c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744820"
---
# <span data-ttu-id="b44e0-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b44e0-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="b44e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b44e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b44e0-103">Lägga till data flödes resurser och dess samband i specifika data flödes-felsökningssessionen.</span><span class="sxs-lookup"><span data-stu-id="b44e0-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="b44e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b44e0-104">SYNTAX</span></span>

### <span data-ttu-id="b44e0-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="b44e0-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b44e0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b44e0-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b44e0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b44e0-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b44e0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b44e0-108">DESCRIPTION</span></span>
<span data-ttu-id="b44e0-109">Det här kommandot kopplar data flödes resursen och dess beroenden till den specifika felsökningssessionen som PowerShell-Kommandotolken för arbets flödet för data flödes sökning ska vara:</span><span class="sxs-lookup"><span data-stu-id="b44e0-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="b44e0-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b44e0-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="b44e0-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b44e0-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="b44e0-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (upprepa det här steget för olika kommandon/mål eller upprepa steg 2-3 för att ändra paket filen)</span><span class="sxs-lookup"><span data-stu-id="b44e0-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="b44e0-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b44e0-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="b44e0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b44e0-114">EXAMPLES</span></span>

### <span data-ttu-id="b44e0-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b44e0-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="b44e0-116">Lägga till data flödes paket i debug-session "550effe4-93a3-485c-8525-eaf25259efbd" i "WikiADF" Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b44e0-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="b44e0-117">Pakcage-filen innehåller fel söknings resurs för data flöde, lista över fel söknings resurser för den länkade tjänsten, fel söknings inställning och sessions-ID.</span><span class="sxs-lookup"><span data-stu-id="b44e0-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="b44e0-118">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="b44e0-118">For instance:</span></span>

<span data-ttu-id="b44e0-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName = namn; AccountKey = Key; EndpointSuffix = Core. Windows. net "}}}]," debugSettings ": {" sourceSettings ": [{" sourceName ":" source1 "," rowLimit ": 1000}]}," sessionId ":" 4f988caf-e765-47d2-82cd-430334a6b135 "}</span><span class="sxs-lookup"><span data-stu-id="b44e0-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="b44e0-120">Parametern SessionID används för att ersätta den befintliga sessionId-egenskapen i paket filen.</span><span class="sxs-lookup"><span data-stu-id="b44e0-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="b44e0-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b44e0-121">PARAMETERS</span></span>

### <span data-ttu-id="b44e0-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b44e0-122">-DataFactory</span></span>
<span data-ttu-id="b44e0-123">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="b44e0-123">The data factory object.</span></span>

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

### <span data-ttu-id="b44e0-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b44e0-124">-DataFactoryName</span></span>
<span data-ttu-id="b44e0-125">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b44e0-125">The data factory name.</span></span>

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

### <span data-ttu-id="b44e0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44e0-126">-DefaultProfile</span></span>
<span data-ttu-id="b44e0-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b44e0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b44e0-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="b44e0-128">-PackageFile</span></span>
<span data-ttu-id="b44e0-129">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="b44e0-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b44e0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b44e0-130">-PassThru</span></span>
<span data-ttu-id="b44e0-131">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="b44e0-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="b44e0-132">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="b44e0-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="b44e0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b44e0-133">-ResourceGroupName</span></span>
<span data-ttu-id="b44e0-134">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b44e0-134">The resource group name.</span></span>

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

### <span data-ttu-id="b44e0-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b44e0-135">-ResourceId</span></span>
<span data-ttu-id="b44e0-136">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="b44e0-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b44e0-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b44e0-137">-Confirm</span></span>
<span data-ttu-id="b44e0-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b44e0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b44e0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b44e0-139">-WhatIf</span></span>
<span data-ttu-id="b44e0-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b44e0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b44e0-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b44e0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b44e0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44e0-142">CommonParameters</span></span>
<span data-ttu-id="b44e0-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b44e0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44e0-144">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b44e0-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44e0-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b44e0-145">INPUTS</span></span>

### <span data-ttu-id="b44e0-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b44e0-146">System.String</span></span>

### <span data-ttu-id="b44e0-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b44e0-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b44e0-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b44e0-148">OUTPUTS</span></span>

### <span data-ttu-id="b44e0-149">System. Void</span><span class="sxs-lookup"><span data-stu-id="b44e0-149">System.Void</span></span>

### <span data-ttu-id="b44e0-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b44e0-150">System.Boolean</span></span>

## <span data-ttu-id="b44e0-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b44e0-151">NOTES</span></span>
<span data-ttu-id="b44e0-152">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b44e0-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b44e0-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b44e0-153">RELATED LINKS</span></span>

[<span data-ttu-id="b44e0-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b44e0-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b44e0-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b44e0-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b44e0-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="b44e0-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="b44e0-157">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b44e0-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
