---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 98b34b4926dc4edc15d30308b2d6bfee33336f0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744687"
---
# <span data-ttu-id="962f6-101">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="962f6-101">Start-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="962f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="962f6-102">SYNOPSIS</span></span>
<span data-ttu-id="962f6-103">Startar en data flödes debug-session i Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="962f6-103">Starts a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="962f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="962f6-104">SYNTAX</span></span>

### <span data-ttu-id="962f6-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="962f6-105">ByFactoryName (Default)</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="962f6-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="962f6-106">ByFactoryObject</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="962f6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="962f6-107">ByResourceId</span></span>
```
Start-AzDataFactoryV2DataFlowDebugSession [[-IntegrationRuntimeFile] <String>] [-AsJob] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="962f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="962f6-108">DESCRIPTION</span></span>
<span data-ttu-id="962f6-109">Det här långa kommandot startar en data flödes-debug-session för de kommande debug-kommandona.</span><span class="sxs-lookup"><span data-stu-id="962f6-109">This long running command starts a data flow debug session for the upcoming debug commands.</span></span> <span data-ttu-id="962f6-110">Det här kommandot kan kopplas till en definition för integrations körning för att konfigurera storleken/typen för ett kluster med debug-sessioner.</span><span class="sxs-lookup"><span data-stu-id="962f6-110">This command can attach with an integration runtime definition to configure the size/type of debug session cluster.</span></span>
<span data-ttu-id="962f6-111">PowerShell-Kommandotolken för arbets flödet för data flödes sökning ska vara:</span><span class="sxs-lookup"><span data-stu-id="962f6-111">The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="962f6-112">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="962f6-112">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="962f6-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="962f6-113">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="962f6-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (upprepa det här steget för olika kommandon/mål eller upprepa steg 2-3 för att ändra paket filen)</span><span class="sxs-lookup"><span data-stu-id="962f6-114">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="962f6-115">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="962f6-115">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="962f6-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="962f6-116">EXAMPLES</span></span>

### <span data-ttu-id="962f6-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="962f6-117">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> $job = Start-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName jikma0601sea -AsJob
PS C:\WINDOWS\system32> $job 

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            Start-AzDataFactoryV2D...

(After 5 minutes)

PS C:\WINDOWS\system32> $job

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Completed     True            localhost            Start-AzDataFactoryV2D...


PS C:\WINDOWS\system32> $job.Output

SessionId                            Status
---------                            ------
550effe4-93a3-485c-8525-eaf25259efbd Succeeded

```

<span data-ttu-id="962f6-118">Startar en felsökningssession med flaggan AsJob.</span><span class="sxs-lookup"><span data-stu-id="962f6-118">Starts a debug session with AsJob flag.</span></span>

## <span data-ttu-id="962f6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="962f6-119">PARAMETERS</span></span>

### <span data-ttu-id="962f6-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="962f6-120">-AsJob</span></span>
<span data-ttu-id="962f6-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="962f6-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="962f6-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="962f6-122">-DataFactory</span></span>
<span data-ttu-id="962f6-123">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="962f6-123">The data factory object.</span></span>

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

### <span data-ttu-id="962f6-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="962f6-124">-DataFactoryName</span></span>
<span data-ttu-id="962f6-125">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="962f6-125">The data factory name.</span></span>

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

### <span data-ttu-id="962f6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962f6-126">-DefaultProfile</span></span>
<span data-ttu-id="962f6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="962f6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="962f6-128">-IntegrationRuntimeFile</span><span class="sxs-lookup"><span data-stu-id="962f6-128">-IntegrationRuntimeFile</span></span>
<span data-ttu-id="962f6-129">Sökvägen till JSON-filen.</span><span class="sxs-lookup"><span data-stu-id="962f6-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962f6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="962f6-130">-ResourceGroupName</span></span>
<span data-ttu-id="962f6-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="962f6-131">The resource group name.</span></span>

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

### <span data-ttu-id="962f6-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="962f6-132">-ResourceId</span></span>
<span data-ttu-id="962f6-133">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="962f6-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="962f6-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="962f6-134">-Confirm</span></span>
<span data-ttu-id="962f6-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="962f6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="962f6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="962f6-136">-WhatIf</span></span>
<span data-ttu-id="962f6-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="962f6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="962f6-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="962f6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="962f6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962f6-139">CommonParameters</span></span>
<span data-ttu-id="962f6-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962f6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962f6-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="962f6-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962f6-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="962f6-142">INPUTS</span></span>

### <span data-ttu-id="962f6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="962f6-143">System.String</span></span>

### <span data-ttu-id="962f6-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="962f6-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="962f6-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="962f6-145">OUTPUTS</span></span>

### <span data-ttu-id="962f6-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="962f6-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSession</span></span>

## <span data-ttu-id="962f6-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="962f6-147">NOTES</span></span>
<span data-ttu-id="962f6-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="962f6-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="962f6-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="962f6-149">RELATED LINKS</span></span>

[<span data-ttu-id="962f6-150">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="962f6-150">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="962f6-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="962f6-151">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="962f6-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="962f6-152">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="962f6-153">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="962f6-153">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)