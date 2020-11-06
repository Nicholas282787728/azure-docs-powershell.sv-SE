---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 7ddbc2809c58172eea2cd98ce048e0e49fbb14f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576577"
---
# <span data-ttu-id="ef6a6-101">Stop-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="ef6a6-101">Stop-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="ef6a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef6a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6a6-103">Stoppar en pieline-körning i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-103">Stops a pieline run in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef6a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef6a6-104">SYNTAX</span></span>

### <span data-ttu-id="ef6a6-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ef6a6-105">ByFactoryName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6a6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ef6a6-106">ByInputObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-InputObject] <PSPipelineRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6a6-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ef6a6-107">ByFactoryObject</span></span>
```
Stop-AzureRmDataFactoryV2PipelineRun [-PipelineRunId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef6a6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef6a6-108">DESCRIPTION</span></span>
<span data-ttu-id="ef6a6-109">Cmdleten **Stop-AzureRmDataFactoryV2PipelineRun** stoppar en pipeline-körning i en data fabrik som anges med pieline kör-ID.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-109">The **Stop-AzureRmDataFactoryV2PipelineRun** cmdlet stops a pipeline run in a data factory specified with the pieline run ID.</span></span>

## <span data-ttu-id="ef6a6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef6a6-110">EXAMPLES</span></span>

### <span data-ttu-id="ef6a6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ef6a6-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId b9730a13-aa12-4926-a8b3-8e3a974ab0bd

Confirm
Are you sure you want to stop pipeline run 'b9730a13-aa12-4926-a8b3-8e3a974ab0bd' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

true
```

<span data-ttu-id="ef6a6-112">Det här kommandot stoppar pipeline-körningen med ID-b9730a13-AA12-4926-a8b3-8e3a974ab0bd i fabriken WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-112">This command stops the pipeline run with id b9730a13-aa12-4926-a8b3-8e3a974ab0bd in the factory WikiADF.</span></span>

## <span data-ttu-id="ef6a6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef6a6-113">PARAMETERS</span></span>

### <span data-ttu-id="ef6a6-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ef6a6-114">-DataFactory</span></span>
<span data-ttu-id="ef6a6-115">Data fabriks objekt.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-115">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ef6a6-116">-DataFactoryName</span></span>
<span data-ttu-id="ef6a6-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-117">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6a6-118">-DefaultProfile</span></span>
<span data-ttu-id="ef6a6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef6a6-120">-InputObject</span></span>
<span data-ttu-id="ef6a6-121">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-121">The Run ID of the pipeline.</span></span>

```yaml
Type: PSPipelineRun
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef6a6-122">-PassThru</span></span>
<span data-ttu-id="ef6a6-123">Om det anges att cmdleten Skriv in true i Case-åtgärden lyckas.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-123">If specified the cmdlet write true in case operation succeeds.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-124">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="ef6a6-124">-PipelineRunId</span></span>
<span data-ttu-id="ef6a6-125">Kör-ID för pipeline.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-125">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef6a6-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef6a6-128">-Confirm</span></span>
<span data-ttu-id="ef6a6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6a6-130">-WhatIf</span></span>
<span data-ttu-id="ef6a6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef6a6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6a6-133">CommonParameters</span></span>
<span data-ttu-id="ef6a6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef6a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6a6-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef6a6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6a6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef6a6-136">INPUTS</span></span>

### <span data-ttu-id="ef6a6-137">Microsoft. Azure. commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="ef6a6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>
<span data-ttu-id="ef6a6-138">System. String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ef6a6-138">System.String Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ef6a6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef6a6-139">OUTPUTS</span></span>

### <span data-ttu-id="ef6a6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef6a6-140">System.Boolean</span></span>

## <span data-ttu-id="ef6a6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef6a6-141">NOTES</span></span>

## <span data-ttu-id="ef6a6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef6a6-142">RELATED LINKS</span></span>

