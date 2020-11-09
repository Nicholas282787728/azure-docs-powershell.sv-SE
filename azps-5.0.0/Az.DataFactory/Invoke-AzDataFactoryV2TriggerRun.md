---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320972"
---
# <span data-ttu-id="20cee-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="20cee-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="20cee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20cee-102">SYNOPSIS</span></span>
 <span data-ttu-id="20cee-103">Anropar en annan instans av en trigger-körning.</span><span class="sxs-lookup"><span data-stu-id="20cee-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="20cee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20cee-104">SYNTAX</span></span>

### <span data-ttu-id="20cee-105">ByFactoryNameByParameterFile (standard)</span><span class="sxs-lookup"><span data-stu-id="20cee-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20cee-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="20cee-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20cee-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="20cee-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20cee-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="20cee-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20cee-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20cee-109">DESCRIPTION</span></span>
<span data-ttu-id="20cee-110">Med kommandot **Invoke-AzDataFactoryV2TriggerRun** startas en instans av en trigger med ett nytt Utlös ande kör-ID.</span><span class="sxs-lookup"><span data-stu-id="20cee-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="20cee-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20cee-111">EXAMPLES</span></span>

### <span data-ttu-id="20cee-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20cee-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="20cee-113">Startar en annan instans av en Utlös ande kör-ID, och behåller samma windowStartTime och windowEndTime som den ursprungliga utlösaren.</span><span class="sxs-lookup"><span data-stu-id="20cee-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="20cee-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20cee-114">PARAMETERS</span></span>

### <span data-ttu-id="20cee-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="20cee-115">-DataFactory</span></span>
<span data-ttu-id="20cee-116">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="20cee-116">The data factory object.</span></span>

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

### <span data-ttu-id="20cee-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="20cee-117">-DataFactoryName</span></span>
<span data-ttu-id="20cee-118">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="20cee-118">The data factory name.</span></span>

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

### <span data-ttu-id="20cee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20cee-119">-DefaultProfile</span></span>
<span data-ttu-id="20cee-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20cee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20cee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20cee-121">-InputObject</span></span>
<span data-ttu-id="20cee-122">Information om trigger-körningen.</span><span class="sxs-lookup"><span data-stu-id="20cee-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="20cee-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20cee-123">-PassThru</span></span>
<span data-ttu-id="20cee-124">Om det anges att cmdleten Skriv in true i Case-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="20cee-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="20cee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20cee-125">-ResourceGroupName</span></span>
<span data-ttu-id="20cee-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="20cee-126">The resource group name.</span></span>

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

### <span data-ttu-id="20cee-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="20cee-127">-TriggerName</span></span>
<span data-ttu-id="20cee-128">Utlösarens namn.</span><span class="sxs-lookup"><span data-stu-id="20cee-128">The trigger name.</span></span>

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

### <span data-ttu-id="20cee-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="20cee-129">-TriggerRunId</span></span>
<span data-ttu-id="20cee-130">Kör-ID för utlösaren.</span><span class="sxs-lookup"><span data-stu-id="20cee-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="20cee-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20cee-131">-Confirm</span></span>
<span data-ttu-id="20cee-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20cee-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20cee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20cee-133">-WhatIf</span></span>
<span data-ttu-id="20cee-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20cee-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20cee-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20cee-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20cee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cee-136">CommonParameters</span></span>
<span data-ttu-id="20cee-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20cee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cee-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20cee-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cee-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20cee-139">INPUTS</span></span>

### <span data-ttu-id="20cee-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="20cee-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="20cee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="20cee-141">System.String</span></span>

### <span data-ttu-id="20cee-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="20cee-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="20cee-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20cee-143">OUTPUTS</span></span>

### <span data-ttu-id="20cee-144">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="20cee-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="20cee-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20cee-145">NOTES</span></span>

## <span data-ttu-id="20cee-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20cee-146">RELATED LINKS</span></span>
