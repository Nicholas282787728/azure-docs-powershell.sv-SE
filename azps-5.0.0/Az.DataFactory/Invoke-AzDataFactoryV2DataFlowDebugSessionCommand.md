---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2dataflowdebugsessioncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md
ms.openlocfilehash: 4009835b2efe8346ff873bde59870954c73ab5d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320984"
---
# <span data-ttu-id="999d4-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="999d4-101">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>

## <span data-ttu-id="999d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="999d4-102">SYNOPSIS</span></span>
<span data-ttu-id="999d4-103">Kör fel söknings åtgärd i data flödets debug-session.</span><span class="sxs-lookup"><span data-stu-id="999d4-103">Invoke debug action in data flow debug session.</span></span>

## <span data-ttu-id="999d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="999d4-104">SYNTAX</span></span>

### <span data-ttu-id="999d4-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="999d4-105">ByFactoryName (Default)</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="999d4-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="999d4-106">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="999d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="999d4-107">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2DataFlowDebugSessionCommand [-SessionId] <String> [-Command] <String>
 [-StreamName] <String> [[-RowLimits] <Int32>] [[-Expression] <String>]
 [[-Columns] <System.Collections.Generic.List`1[System.String]>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="999d4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="999d4-108">DESCRIPTION</span></span>
<span data-ttu-id="999d4-109">Med det här kommandot körs för hands versionen av data för förhands granskning/förhands granskning för olika strömmar med data flöden i felsökningssessionen.</span><span class="sxs-lookup"><span data-stu-id="999d4-109">This command executes data preview/stats preview/expression preview for different stream of data flow in debug session.</span></span>
<span data-ttu-id="999d4-110">PowerShell-Kommandotolken för arbets flödet för data flödes sökning ska vara:</span><span class="sxs-lookup"><span data-stu-id="999d4-110">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="999d4-111">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="999d4-111">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="999d4-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="999d4-112">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="999d4-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (upprepa det här steget för olika kommandon/mål eller upprepa steg 2-3 för att ändra paket filen)</span><span class="sxs-lookup"><span data-stu-id="999d4-113">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="999d4-114">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="999d4-114">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="999d4-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="999d4-115">EXAMPLES</span></span>

### <span data-ttu-id="999d4-116">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="999d4-116">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $result = Invoke-AzDataFactoryV2DataFlowDebugSessionCommand -ResourceGroupName adf -DataFactoryName WiKiADF -Command executePreviewQuery -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d -StreamName source1 -RowLimits 100 -AsJob
PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Running       True            localhost            Invoke-AzDataFactoryV2...


(After 2 minutes)

PS C:\WINDOWS\system32> $result

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
3      Long Running... AzureLongRun... Completed     True            localhost            Invoke-AzDataFactoryV2...

PS C:\WINDOWS\system32> $output = ConvertFrom-Json($result.Output.Data)
PS C:\WINDOWS\system32> $output.output

    {
      "schema": "output(ResourceAgencyNum as string, PublicName as string)" ,
      "data": [["4445679354", "Syrian Refugee Information", 1], ["44456793", "Syrian Refugee Information", 1]]
    }


```

<span data-ttu-id="999d4-117">I det här exemplet anropas kommandot för förhands granskning för debug-session "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" i Data Factory "WiKiADF" och konverterar sedan JSON-utdata till läsbar sträng.</span><span class="sxs-lookup"><span data-stu-id="999d4-117">This example invokes data preview command for debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WiKiADF" and then convert the JSON output into readable string.</span></span>

## <span data-ttu-id="999d4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="999d4-118">PARAMETERS</span></span>

### <span data-ttu-id="999d4-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="999d4-119">-AsJob</span></span>
<span data-ttu-id="999d4-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="999d4-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="999d4-121">-Kolumner</span><span class="sxs-lookup"><span data-stu-id="999d4-121">-Columns</span></span>
<span data-ttu-id="999d4-122">Kolumn listan för förhands granskning av statistik för data flöde.</span><span class="sxs-lookup"><span data-stu-id="999d4-122">The columns list for data flow statistics preview.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999d4-123">-Kommando</span><span class="sxs-lookup"><span data-stu-id="999d4-123">-Command</span></span>
<span data-ttu-id="999d4-124">Kommandot debug för data flöde.</span><span class="sxs-lookup"><span data-stu-id="999d4-124">The data flow debug command.</span></span> <span data-ttu-id="999d4-125">Alternativen är executePreviewQuery, executeStatisticsQuery och executeExpressionQuery</span><span class="sxs-lookup"><span data-stu-id="999d4-125">Optionals are executePreviewQuery, executeStatisticsQuery and executeExpressionQuery</span></span>

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

### <span data-ttu-id="999d4-126">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="999d4-126">-DataFactory</span></span>
<span data-ttu-id="999d4-127">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="999d4-127">The data factory object.</span></span>

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

### <span data-ttu-id="999d4-128">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="999d4-128">-DataFactoryName</span></span>
<span data-ttu-id="999d4-129">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="999d4-129">The data factory name.</span></span>

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

### <span data-ttu-id="999d4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999d4-130">-DefaultProfile</span></span>
<span data-ttu-id="999d4-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="999d4-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="999d4-132">-Uttryck</span><span class="sxs-lookup"><span data-stu-id="999d4-132">-Expression</span></span>
<span data-ttu-id="999d4-133">Uttrycket för förhands granskning av data flödes uttryck.</span><span class="sxs-lookup"><span data-stu-id="999d4-133">The expression for data flow expression preview.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999d4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="999d4-134">-ResourceGroupName</span></span>
<span data-ttu-id="999d4-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="999d4-135">The resource group name.</span></span>

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

### <span data-ttu-id="999d4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="999d4-136">-ResourceId</span></span>
<span data-ttu-id="999d4-137">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="999d4-137">The Azure resource ID.</span></span>

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

### <span data-ttu-id="999d4-138">-RowLimits</span><span class="sxs-lookup"><span data-stu-id="999d4-138">-RowLimits</span></span>
<span data-ttu-id="999d4-139">Rad gränsen för förhands granskning av data flöde.</span><span class="sxs-lookup"><span data-stu-id="999d4-139">The row limit for data flow data preview.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999d4-140">-SessionId</span><span class="sxs-lookup"><span data-stu-id="999d4-140">-SessionId</span></span>
<span data-ttu-id="999d4-141">ID för debug-session med data flöde.</span><span class="sxs-lookup"><span data-stu-id="999d4-141">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999d4-142">-StreamName</span><span class="sxs-lookup"><span data-stu-id="999d4-142">-StreamName</span></span>
<span data-ttu-id="999d4-143">Strömmens namn för data flödet för fel sökning.</span><span class="sxs-lookup"><span data-stu-id="999d4-143">The stream name of data flow for debugging.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999d4-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="999d4-144">-Confirm</span></span>
<span data-ttu-id="999d4-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="999d4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="999d4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="999d4-146">-WhatIf</span></span>
<span data-ttu-id="999d4-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="999d4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="999d4-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="999d4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="999d4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999d4-149">CommonParameters</span></span>
<span data-ttu-id="999d4-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="999d4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999d4-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="999d4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999d4-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="999d4-152">INPUTS</span></span>

### <span data-ttu-id="999d4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="999d4-153">System.String</span></span>

### <span data-ttu-id="999d4-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="999d4-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="999d4-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="999d4-155">OUTPUTS</span></span>

### <span data-ttu-id="999d4-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span><span class="sxs-lookup"><span data-stu-id="999d4-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionCommandResult</span></span>

## <span data-ttu-id="999d4-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="999d4-157">NOTES</span></span>
<span data-ttu-id="999d4-158">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, factoriesKeywords: Azure, azurerm, arm, resurs, hantering, chef, data, fabriker</span><span class="sxs-lookup"><span data-stu-id="999d4-158">Keywords: azure, azurerm, arm, resource, management, manager, data, factoriesKeywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="999d4-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="999d4-159">RELATED LINKS</span></span>

[<span data-ttu-id="999d4-160">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="999d4-160">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="999d4-161">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="999d4-161">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="999d4-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="999d4-162">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="999d4-163">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="999d4-163">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
