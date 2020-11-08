---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263469"
---
# <span data-ttu-id="39261-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="39261-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="39261-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39261-102">SYNOPSIS</span></span>
<span data-ttu-id="39261-103">Avbryter ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="39261-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="39261-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39261-104">SYNTAX</span></span>

### <span data-ttu-id="39261-105">StopSparkJobByIdParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="39261-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39261-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39261-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39261-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39261-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39261-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39261-108">DESCRIPTION</span></span>
<span data-ttu-id="39261-109">Cmdleten **Stop-AzSynapseSparkJob** avbryter ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="39261-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="39261-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39261-110">EXAMPLES</span></span>

### <span data-ttu-id="39261-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="39261-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="39261-112">Det här kommandot avbryter ett Synapse Analytics Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="39261-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="39261-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="39261-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="39261-114">Det här kommandot avbryter ett Synapse Analytics Spark-jobb genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="39261-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="39261-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="39261-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="39261-116">Det här kommandot avbryter ett Synapse Analytics Spark-jobb genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="39261-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="39261-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39261-117">PARAMETERS</span></span>

### <span data-ttu-id="39261-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39261-118">-DefaultProfile</span></span>
<span data-ttu-id="39261-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39261-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39261-120">-Force</span><span class="sxs-lookup"><span data-stu-id="39261-120">-Force</span></span>
<span data-ttu-id="39261-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="39261-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="39261-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="39261-122">-LivyId</span></span>
<span data-ttu-id="39261-123">Identifierare för Spark-jobb.</span><span class="sxs-lookup"><span data-stu-id="39261-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39261-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39261-124">-PassThru</span></span>
<span data-ttu-id="39261-125">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="39261-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="39261-126">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="39261-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="39261-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="39261-127">-SparkJobObject</span></span>
<span data-ttu-id="39261-128">Ingångs objekt för Spark-jobb, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="39261-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39261-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="39261-129">-SparkPoolName</span></span>
<span data-ttu-id="39261-130">Namn på Synapse Spark-pool.</span><span class="sxs-lookup"><span data-stu-id="39261-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39261-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="39261-131">-SparkPoolObject</span></span>
<span data-ttu-id="39261-132">Indata från Spark-pool, vanligt vis passerar genom pipeline.</span><span class="sxs-lookup"><span data-stu-id="39261-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39261-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39261-133">-WorkspaceName</span></span>
<span data-ttu-id="39261-134">Namn på Synapse-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="39261-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39261-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39261-135">-Confirm</span></span>
<span data-ttu-id="39261-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39261-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39261-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39261-137">-WhatIf</span></span>
<span data-ttu-id="39261-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39261-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39261-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39261-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39261-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39261-140">CommonParameters</span></span>
<span data-ttu-id="39261-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39261-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39261-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39261-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39261-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39261-143">INPUTS</span></span>

### <span data-ttu-id="39261-144">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="39261-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="39261-145">Microsoft. Azure. commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="39261-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="39261-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39261-146">OUTPUTS</span></span>

### <span data-ttu-id="39261-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39261-147">System.Boolean</span></span>

## <span data-ttu-id="39261-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39261-148">NOTES</span></span>

## <span data-ttu-id="39261-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39261-149">RELATED LINKS</span></span>
