---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 400862dbb27eb38d3189c08f741bb595a8e939b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320795"
---
# <span data-ttu-id="3b5f2-101">Stop-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="3b5f2-101">Stop-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="3b5f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b5f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5f2-103">Stoppar en pipeline-körning i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-103">Stops a pipeline run in a data factory.</span></span>

## <span data-ttu-id="3b5f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b5f2-104">SYNTAX</span></span>

### <span data-ttu-id="3b5f2-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3b5f2-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3b5f2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b5f2-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5f2-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3b5f2-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b5f2-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b5f2-108">DESCRIPTION</span></span>
<span data-ttu-id="3b5f2-109">Cmdleten **Stop-AzDataFactoryV2PipelineRun** stoppar en pipeline-körning som är angiven med ID för pipeline-körningen.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-109">The **Stop-AzDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pipeline run ID.</span></span>

## <span data-ttu-id="3b5f2-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b5f2-110">EXAMPLES</span></span>

### <span data-ttu-id="3b5f2-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3b5f2-111">Example 1</span></span>
```
PS C:\> Stop-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="3b5f2-112">Det här kommandot stoppar pipeline-körningen med ID-b9730a13-AA12-4926-a8b3-8e3a974ab0bd i fabriken WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="3b5f2-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b5f2-113">PARAMETERS</span></span>

### <span data-ttu-id="3b5f2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3b5f2-114">-DataFactory</span></span>
<span data-ttu-id="3b5f2-115">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-115">The data factory object.</span></span>

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

### <span data-ttu-id="3b5f2-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3b5f2-116">-DataFactoryName</span></span>
<span data-ttu-id="3b5f2-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-117">The data factory name.</span></span>

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

### <span data-ttu-id="3b5f2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5f2-118">-DefaultProfile</span></span>
<span data-ttu-id="3b5f2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b5f2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b5f2-120">-InputObject</span></span>
<span data-ttu-id="3b5f2-121">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-121">The Run ID of the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5f2-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b5f2-122">-PassThru</span></span>
<span data-ttu-id="3b5f2-123">Om det anges att cmdleten Skriv in true i Case-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-123">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="3b5f2-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="3b5f2-124">-PipelineRunId</span></span>
<span data-ttu-id="3b5f2-125">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-125">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="3b5f2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5f2-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b5f2-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-127">The resource group name.</span></span>

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

### <span data-ttu-id="3b5f2-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b5f2-128">-Confirm</span></span>
<span data-ttu-id="3b5f2-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b5f2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5f2-130">-WhatIf</span></span>
<span data-ttu-id="3b5f2-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b5f2-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b5f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5f2-133">CommonParameters</span></span>
<span data-ttu-id="3b5f2-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b5f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5f2-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5f2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5f2-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b5f2-136">INPUTS</span></span>

### <span data-ttu-id="3b5f2-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="3b5f2-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

### <span data-ttu-id="3b5f2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3b5f2-138">System.String</span></span>

### <span data-ttu-id="3b5f2-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3b5f2-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3b5f2-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b5f2-140">OUTPUTS</span></span>

### <span data-ttu-id="3b5f2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b5f2-141">System.Boolean</span></span>

## <span data-ttu-id="3b5f2-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b5f2-142">NOTES</span></span>

## <span data-ttu-id="3b5f2-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b5f2-143">RELATED LINKS</span></span>
