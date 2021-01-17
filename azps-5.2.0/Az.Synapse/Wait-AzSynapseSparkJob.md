---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/wait-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Wait-AzSynapseSparkJob.md
ms.openlocfilehash: c7137e9fda6c947755c8bd2e0091dd33347027fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418024"
---
# <span data-ttu-id="4a06f-101">Wait-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4a06f-101">Wait-AzSynapseSparkJob</span></span>

## <span data-ttu-id="4a06f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a06f-102">SYNOPSIS</span></span>
<span data-ttu-id="4a06f-103">Väntar på att ett Synapse-jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="4a06f-103">Waits for a Synapse Analytics Spark job to complete.</span></span>

## <span data-ttu-id="4a06f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a06f-104">SYNTAX</span></span>

### <span data-ttu-id="4a06f-105">WaitSparkJobByIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4a06f-105">WaitSparkJobByIdParameterSet (Default)</span></span>
```
Wait-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32>
 [-WaitIntervalInSeconds <Int32>] [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a06f-106">WaitSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a06f-106">WaitSparkJobByIdFromParentObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a06f-107">WaitSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a06f-107">WaitSparkJobByIdFromInputObjectParameterSet</span></span>
```
Wait-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-WaitIntervalInSeconds <Int32>]
 [-TimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a06f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a06f-108">DESCRIPTION</span></span>
<span data-ttu-id="4a06f-109">Cmdleten **wait-AzSynapseSparkJob** väntar på att ett Azure Synapse-analys jobb ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="4a06f-109">The **Wait-AzSynapseSparkJob** cmdlet waits for an Azure Synapse Analytics job to complete.</span></span>

## <span data-ttu-id="4a06f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a06f-110">EXAMPLES</span></span>

### <span data-ttu-id="4a06f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a06f-111">Example 1</span></span>
```powershell
PS C:\> Wait-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="4a06f-112">Det här kommandot väntar på jobbet med det ID som ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="4a06f-112">This command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="4a06f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a06f-113">PARAMETERS</span></span>

### <span data-ttu-id="4a06f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a06f-114">-DefaultProfile</span></span>
<span data-ttu-id="4a06f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a06f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a06f-116">-LivyId</span><span class="sxs-lookup"><span data-stu-id="4a06f-116">-LivyId</span></span>
<span data-ttu-id="4a06f-117">Identifierare för Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="4a06f-117">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdParameterSet, WaitSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-118">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="4a06f-118">-SparkJobObject</span></span>
<span data-ttu-id="4a06f-119">Ingångs objekt för Spark-jobb, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a06f-119">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: WaitSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-120">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="4a06f-120">-SparkPoolName</span></span>
<span data-ttu-id="4a06f-121">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="4a06f-121">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-122">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="4a06f-122">-SparkPoolObject</span></span>
<span data-ttu-id="4a06f-123">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="4a06f-123">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: WaitSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-124">-TimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="4a06f-124">-TimeoutInSeconds</span></span>
<span data-ttu-id="4a06f-125">Den maximala vänte tiden innan felet uppstår. Standardvärdet är att aldrig tids gräns.</span><span class="sxs-lookup"><span data-stu-id="4a06f-125">The maximum amount of time to wait before erroring out. Default value is to never timeout.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-126">-WaitIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4a06f-126">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="4a06f-127">Avsöknings intervall mellan kontroller för jobb status, i sekunder.</span><span class="sxs-lookup"><span data-stu-id="4a06f-127">The polling interval between checks for the job status, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4a06f-128">-WorkspaceName</span></span>
<span data-ttu-id="4a06f-129">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="4a06f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: WaitSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a06f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a06f-130">CommonParameters</span></span>
<span data-ttu-id="4a06f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a06f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a06f-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a06f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a06f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a06f-133">INPUTS</span></span>

### <span data-ttu-id="4a06f-134">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="4a06f-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="4a06f-135">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="4a06f-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="4a06f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a06f-136">OUTPUTS</span></span>

### <span data-ttu-id="4a06f-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a06f-137">System.Boolean</span></span>

## <span data-ttu-id="4a06f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a06f-138">NOTES</span></span>

## <span data-ttu-id="4a06f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a06f-139">RELATED LINKS</span></span>
