---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526282"
---
# <span data-ttu-id="bf443-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="bf443-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="bf443-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf443-102">SYNOPSIS</span></span>
 <span data-ttu-id="bf443-103">Anropar en annan instans av en trigger-körning.</span><span class="sxs-lookup"><span data-stu-id="bf443-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="bf443-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf443-104">SYNTAX</span></span>

### <span data-ttu-id="bf443-105">ByFactoryNameByParameterFile (standard)</span><span class="sxs-lookup"><span data-stu-id="bf443-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf443-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bf443-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf443-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="bf443-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf443-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bf443-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf443-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf443-109">DESCRIPTION</span></span>
<span data-ttu-id="bf443-110">Med kommandot **Invoke-AzDataFactoryV2TriggerRun** startas en instans av en trigger med ett nytt Utlös ande kör-ID.</span><span class="sxs-lookup"><span data-stu-id="bf443-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="bf443-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf443-111">EXAMPLES</span></span>

### <span data-ttu-id="bf443-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bf443-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="bf443-113">Startar en annan instans av en Utlös ande kör-ID, och behåller samma windowStartTime och windowEndTime som den ursprungliga utlösaren.</span><span class="sxs-lookup"><span data-stu-id="bf443-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="bf443-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf443-114">PARAMETERS</span></span>

### <span data-ttu-id="bf443-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf443-115">-DataFactory</span></span>
<span data-ttu-id="bf443-116">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="bf443-116">The data factory object.</span></span>

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

### <span data-ttu-id="bf443-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bf443-117">-DataFactoryName</span></span>
<span data-ttu-id="bf443-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="bf443-118">The data factory name.</span></span>

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

### <span data-ttu-id="bf443-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf443-119">-DefaultProfile</span></span>
<span data-ttu-id="bf443-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bf443-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf443-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf443-121">-InputObject</span></span>
<span data-ttu-id="bf443-122">Information om trigger-körningen.</span><span class="sxs-lookup"><span data-stu-id="bf443-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="bf443-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf443-123">-PassThru</span></span>
<span data-ttu-id="bf443-124">Om det anges att cmdleten Skriv in true i Case-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="bf443-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="bf443-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf443-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf443-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="bf443-126">The resource group name.</span></span>

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

### <span data-ttu-id="bf443-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="bf443-127">-TriggerName</span></span>
<span data-ttu-id="bf443-128">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="bf443-128">The trigger name.</span></span>

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

### <span data-ttu-id="bf443-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="bf443-129">-TriggerRunId</span></span>
<span data-ttu-id="bf443-130">Kör-ID för utlösaren.</span><span class="sxs-lookup"><span data-stu-id="bf443-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="bf443-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf443-131">-Confirm</span></span>
<span data-ttu-id="bf443-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf443-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf443-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf443-133">-WhatIf</span></span>
<span data-ttu-id="bf443-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf443-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf443-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf443-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf443-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf443-136">CommonParameters</span></span>
<span data-ttu-id="bf443-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf443-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf443-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf443-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf443-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf443-139">INPUTS</span></span>

### <span data-ttu-id="bf443-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="bf443-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="bf443-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf443-141">System.String</span></span>

### <span data-ttu-id="bf443-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bf443-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="bf443-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf443-143">OUTPUTS</span></span>

### <span data-ttu-id="bf443-144">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="bf443-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="bf443-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf443-145">NOTES</span></span>

## <span data-ttu-id="bf443-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf443-146">RELATED LINKS</span></span>
