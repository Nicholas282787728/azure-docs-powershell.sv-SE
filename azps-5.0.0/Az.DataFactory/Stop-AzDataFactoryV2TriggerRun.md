---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320788"
---
# <span data-ttu-id="ea0cf-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="ea0cf-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="ea0cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0cf-103">Stoppar en Utlös ande körning i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="ea0cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea0cf-104">SYNTAX</span></span>

### <span data-ttu-id="ea0cf-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ea0cf-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0cf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ea0cf-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea0cf-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ea0cf-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea0cf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea0cf-108">DESCRIPTION</span></span>
<span data-ttu-id="ea0cf-109">Cmdleten **Stop-AzDataFactoryV2TriggerRun** stoppar en Utlös ande körning i en data fabrik som anges med Utlösarens namn och utlösarens kör-ID.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="ea0cf-110">För närvarande endast för TumblingWindowTriggers i WaitingOnDependency-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="ea0cf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea0cf-111">EXAMPLES</span></span>

### <span data-ttu-id="ea0cf-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ea0cf-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="ea0cf-113">Det här kommandot stoppar trigger-körningen med ID ' 08586002468005888497807248799CU16 ' i fabriken WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="ea0cf-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea0cf-114">PARAMETERS</span></span>

### <span data-ttu-id="ea0cf-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ea0cf-115">-DataFactory</span></span>
<span data-ttu-id="ea0cf-116">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-116">The data factory object.</span></span>

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

### <span data-ttu-id="ea0cf-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ea0cf-117">-DataFactoryName</span></span>
<span data-ttu-id="ea0cf-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-118">The data factory name.</span></span>

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

### <span data-ttu-id="ea0cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0cf-119">-DefaultProfile</span></span>
<span data-ttu-id="ea0cf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea0cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea0cf-121">-InputObject</span></span>
<span data-ttu-id="ea0cf-122">Information om trigger-körningen.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0cf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea0cf-123">-PassThru</span></span>
<span data-ttu-id="ea0cf-124">Om det anges att cmdleten Skriv in true i Case-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="ea0cf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea0cf-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea0cf-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-126">The resource group name.</span></span>

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

### <span data-ttu-id="ea0cf-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ea0cf-127">-TriggerName</span></span>
<span data-ttu-id="ea0cf-128">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0cf-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="ea0cf-129">-TriggerRunId</span></span>
<span data-ttu-id="ea0cf-130">Kör-ID för utlösaren.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0cf-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea0cf-131">-Confirm</span></span>
<span data-ttu-id="ea0cf-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0cf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0cf-133">-WhatIf</span></span>
<span data-ttu-id="ea0cf-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea0cf-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0cf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0cf-136">CommonParameters</span></span>
<span data-ttu-id="ea0cf-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea0cf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0cf-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea0cf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0cf-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea0cf-139">INPUTS</span></span>

### <span data-ttu-id="ea0cf-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="ea0cf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="ea0cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea0cf-141">System.String</span></span>

### <span data-ttu-id="ea0cf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ea0cf-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ea0cf-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea0cf-143">OUTPUTS</span></span>

### <span data-ttu-id="ea0cf-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea0cf-144">System.Boolean</span></span>

## <span data-ttu-id="ea0cf-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea0cf-145">NOTES</span></span>

## <span data-ttu-id="ea0cf-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea0cf-146">RELATED LINKS</span></span>